> **Tiny (train in minutes on a CPU or free Colab GPU) — best for getting your code working**

## [**Tiny Shakespeare**](https://hf.co/datasets/karpathy/tiny_shakespeare) (1MB): 
40k lines of Shakespeare. This is _the_ classic starter dataset for exactly your use case. Andrej Karpathy used it in his famous "Unreasonable Effectiveness of Recurrent Neural Networks" blog post (which you should read — it's the perfect companion to what you're doing). It's character-level friendly, so you can skip tokenizer complexity entirely and focus on the architecture comparison. Both your LSTM and Transformer will learn to generate pseudo-Shakespeare, making qualitative comparison fun and easy. Start here.





---
# Obtain& Split
You split your data into separate chunks so you can tell whether your model is actually _learning patterns_ or just _memorizing the answers_.

**Training set** — This is what the model actually learns from. During training, the model sees this data over and over, adjusts its internal parameters (weights) to get better at predicting the next character, and gradually improves. Think of it like the practice problems in a textbook.

**Validation set** — This is data the model _never trains on_, but you check its performance on periodically _during_ training. After every few hundred training steps, you ask "how well does the model predict text it's never seen before?" If training loss goes down but validation loss stops improving (or goes up), your model is **overfitting** — it's memorizing the training text rather than learning general patterns of English/Shakespeare. The validation set is like a practice exam you use to gauge your understanding while studying.

**Test set** — Data the model never sees until you're completely done training and tuning. This is your final, unbiased evaluation. You only use it once at the very end. It's the actual final exam.

If you only had a training set, you'd have no idea whether the model generalizes. If you used your test set to make decisions during training (like "should I train for more epochs?"), you'd indirectly optimize for it, and it would no longer be an unbiased measure. The validation set exists so you have something to make those decisions against _without contaminating your final evaluation_.

Usually just by splitting the original data. Common approaches to obtain:
- **Random split** — shuffle the data and carve off percentages, like 80% train / 10% validation / 10% test. This is the most common.
- **Pre-split** — the dataset author already did it for you (which is the case with the Trelis/tiny-shakespeare dataset you loaded — it came with train and test already separated).
- **Chronological split** — for time-series or sequential data, you sometimes use earlier data for training and later data for testing, so you're evaluating on "the future."

In your case, the dataset gave you train (472 rows) and test (49 rows). You could carve a validation set out of the training 
data, or just use the test set as your validation set for this project since you're comparing architectures rather than doing rigorous final evaluation. For a learning exercise, two splits is fine.

```Python
from datasets import load_dataset
ds = load_dataset("Trelis/tiny-shakespeare", trust_remote_code=True)

train = ds["train"].to_pandas()
test = ds["test"].to_pandas()
```

## **The core problem:** 
Neural networks only understand numbers, not text. They do math — [[matrix multiplications]], [[additions]], [[activations]]. So before any model can process language, you need a way to convert characters (or words) into numbers and back again. That's what all of this code below is doing.

```Python
chars = sorted(set(train_text))
vocab_size = len(chars)
print(f"Vocab size: {vocab_size}")
print(''.join(chars))

stoi = {ch: i for i, ch in enumerate(chars)}
itos = {i: ch for i, ch in enumerate(chars)}

encode = lambda s: [stoi[c] for c in s]
decode = lambda l: ''.join([itos[i] for i in l])

# Quick test
print(encode("hello"))
print(decode(encode("hello")))
```
**Character mappings** (`stoi` **and** `itos`) are just lookup tables:
- `stoi` (string-to-integer): `'a' → 0, 'b' → 1, 'c' → 2, ...` — converts each character to a unique number
- `itos` (integer-to-string): `0 → 'a', 1 → 'b', 2 → 'c', ...` — converts back 
`encode` uses `stoi` to turn a string into a list of numbers. `decode` uses `itos` to turn numbers back into text. That's it — nothing fancy.

## **Why this matters for the model:** 
The entire training loop looks like this:
1. **Encode** the text into numbers → `"hello" → [7, 4, 11, 11, 14]`
2. **Feed those numbers into the model** ([[LSTM]] or [[Transformer]]) — the model sees a sequence of integers and tries to predict what integer comes next
3. **Model outputs a probability distribution** over the whole vocabulary — for each position it says "I think the next character is 'a' with 5% chance, 'b' with 2% chance, 'e' with 30% chance..." etc.
4. **Decode** the model's predicted numbers back into text for us to read
---
## **Character-level vs. token-level:** 
What we're doing here is _character-level_ — every single character (including spaces and punctuation) gets its own number. This gives us a tiny vocabulary (~65 characters for Shakespeare). Real models like GPT use _token-level_ encoding where common words or word-pieces get a single number (`"the" → 1532`), giving vocabularies of 50k–100k. The concepts are identical, just at different granularity. We're using character-level because it's simpler and the dataset is small.

## **Embeddings:** 
The model doesn't actually work with raw integer IDs either. The first layer of both the LSTM and Transformer is an _embedding layer_, which converts each integer into a dense vector (a list of, say, 64 or 128 numbers). So `7` becomes `[0.23, -0.41, 0.87, ...]`. These vectors are what the network actually does its computations on — and they're _learned_ during training, so the model figures out its own internal representation of each character. But that's the next step.

---
## Character Mapping
```Python
chars = sorted(set(train_text))
vocab_size = len(chars)
print(f"Vocab size: {vocab_size}")
print(''.join(chars))

stoi = {ch: i for i, ch in enumerate(chars)}
itos = {i: ch for i, ch in enumerate(chars)}

encode = lambda s: [stoi[c] for c in s]
decode = lambda l: ''.join([itos[i] for i in l])

# Quick test
print(encode("hello"))
print(decode(encode("hello")))
```
---
# Torching
```Python
# Convert text to tensors of integers 
train_data = torch.tensor(encode(train_text), dtype=torch.long) val_data = torch.tensor(encode(val_text), dtype=torch.long)
```

```Python
# context length: how many characters the model sees at once
block_size = 128   

# how many sequences to process in parallel
batch_size = 32    

device = "cuda" if torch.cuda.is_available() else "cpu"
print(f"Using device: {device}")

def get_batch(split):
    data = train_data if split == "train" else val_data
    # Pick random starting positions
    ix = torch.randint(len(data) - block_size, (batch_size,))
    # Input: chunk of text
    x = torch.stack([data[i:i+block_size] for i in ix])
    # Target: same chunk shifted by one character
    y = torch.stack([data[i+1:i+block_size+1] for i in ix])
    return x.to(device), y.to(device)
```

