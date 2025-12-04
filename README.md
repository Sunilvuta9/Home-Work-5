# Homeworkml5

**CS5710 – Machine Learning**
**Homework 5 – Transformers, Attention, and Ethics**

**Student:** Sunil Kumar Vuta
**Student ID:** 700772302

---

This README explains how I completed Homework 5, including both the short‑answer theory section and the coding tasks in Part B. I describe the steps I followed, the methods I used, and how to run the code.

---

# Part A — Short Answers 

For this section, I wrote all answers concisely (2–3 lines each) while clearly explaining the required concepts. Below is how I approached each group of questions.

---

## Positional Encoding

* Explained why transformers need positional encodings since they do not process tokens sequentially.
* Described properties of good encodings, such as uniqueness and smooth generalization.
* Clarified what it means for positional encodings to be unitary and norm‑preserving.

---

## Attention Mechanism

* Explained how attention scores are calculated using the dot product between queries and keys.
* Described how softmax converts alignment scores into normalized attention weights.
* Showed how the context vector is formed from weighted value vectors.

---

## Multi‑Head Attention

* Discussed how multiple heads help capture different linguistic or semantic patterns.
* Explained why splitting Q, K, and V improves representation learning.
* Clarified why concatenation and a final linear projection are required.

---

## Ethical Foundations

* Summarized the difference between ethics, laws, and personal emotions.
* Described two classical ethical theories and how they approach AI decisions.
* Explained why no single ethical framework works in all real‑world contexts.

---

## AI Harms

* Defined allocational and representational harms with real‑world examples.
* Explained why representational harm is harder to measure due to cultural context.

---

## Dataset Bias

* Listed major causes of bias during data collection and annotation.
* Described which communities are under‑represented in large datasets.
* Explained how training can amplify even small existing imbalances.

---

## Safety, Security, and Privacy

* Defined data poisoning and how it manipulates models.
* Discussed ethical concerns of model memorization.
* Explained the risks of model stealing for privacy and intellectual property.

All short answers are included in the submitted PDF.

---

# Part B — Coding 

## Q1. Scaled Dot‑Product Attention (NumPy)

I implemented the scaled dot‑product attention mechanism step by step:

1. Computed similarity scores using the matrix product of queries and keys.
2. Scaled the scores by the square root of the key dimension.
3. Applied a stable softmax to obtain attention weights.
4. Multiplied the attention weights with the values to produce the context vector.

I verified dimensions for random matrices. The function returns both the attention weights and the context vector.

**To run:** Use `HW5.py` or `HW5.ipynb`.

---

## Q2. Simple Transformer Encoder Block (PyTorch)

I built a simplified Transformer encoder block using PyTorch.

### Steps I followed

1. Used `nn.MultiheadAttention` with `batch_first=True` to process tensors shaped (batch, sequence length, embedding size).
2. Implemented a feed‑forward network consisting of two Linear layers with a ReLU activation.
3. Added residual connections and layer normalization after attention and feed‑forward sublayers.
4. Tested using:

   * Batch size: 32
   * Sequence length: 10 tokens
   * Embedding size: 128

The output shape correctly matched **32 × 10 × 128**.

**To run:** Code is included in both `.py` and `.ipynb` files.

---

# Repository Structure

* `HW5.py` — Python implementation (Part B)
* `HW5.ipynb` — Notebook version with outputs
* `PDF file` — Contains Part A answers
* `README` — This file

---

# How to Reproduce My Work

### 1. Install dependencies

(NumPy, PyTorch, etc.)

### 2. Run the files

* Run `HW5.py` in a terminal.
* Open `HW5.ipynb` in Jupyter Notebook.

### 3. Review the PDF

All theory answers from Part A are included.

---

# Final Notes

This README summarizes how I completed both the theoretical and coding tasks for Homework 5. All work follows the transformer architecture taught in class, and all answers are concise and aligned with course expectations.

If you want me to insert your GitHub link, add screenshots, or adjust formatting, just let me know!
