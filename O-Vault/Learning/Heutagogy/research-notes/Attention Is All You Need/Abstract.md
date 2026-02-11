> The *attention* mechanism of the transformer is simple a clever application **matrix operations** and **weighted sums**.

**Matrix Operation Examples:**
- **Matrix–vector multiplication**
- **Matrix–matrix multiplication**
- **Matrix addition / subtraction**
- **Matrix transpose**
- **Matrix–matrix multiplication**

The "Attention Is All You Need" is the foundational paper where the Transformer architecture was first introduced. The **Attention mechanism** in an AI mode is simply a way for the model to "focus" on different parts of the input when producing each part of the output.

> "We propose a new simple network architecture, the Transformer, based solely on attention mechanisms, dispensing with recurrence and convolutions entirely."

--- start-multi-column: ID_ddks
```column-settings
Number of Columns: 2
Largest Column: standard
```

**What they're saying**:
- Previous models: RNNs/CNNs + attention (as a helper)
- **Transformer**: ONLY attention, no RNNs or CNNs at all

--- column-break ---

**Why is this radical?**
Remember how RNNs process sequences one element at a time?
- Word 1 → process → Word 2 → process → Word 3 → process...
- This is **sequential** - you MUST finish processing Word 1 before you can start Word 2

--- end-multi-column

