# CatGPT

<p align="center">
  <img src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" width="300" alt="Cat coding">
</p>

<h3 align="center">A tiny GPT that is trying very hard to become a cat.</h3>

<p align="center">
  <i>A fun from-scratch language model project for learning how GPTs actually work.</i>
</p>

---

## About

**CatGPT** is a small GPT-style language model built from scratch using PyTorch.

The idea is simple:

```text
Build a tiny GPT
       ↓
Teach it language
       ↓
Teach it cat behavior
       ↓
Hope for the best
```

This is primarily a **learning and experimentation project**, not an attempt to build a production LLM.

---

## The Goal

I want CatGPT to eventually respond like this:

<p align="center">
  <img src="https://media.giphy.com/media/ICOgUNjpvO0PC/giphy.gif" width="220" alt="Funny cat">
</p>

```text
Human: Are you hungry?
CatGPT: Obviously.

Human: I just fed you.
CatGPT: That was a long time ago.

Human: Why are you sitting on my laptop?
CatGPT: Because you were using it.

Human: Who is the boss?
CatGPT: Me.
```

---

## Architecture

```text
                 Training Data
                      |
                      v
                  Tokenizer
                      |
                      v
                   Tokens
                      |
                      v
                Embeddings
                      |
                      v
        +-------------------------+
        |    Transformer Block    |
        |                         |
        |  Causal Self-Attention  |
        |           ↓             |
        |     Feed Forward        |
        +-------------------------+
                      |
                  ... Blocks
                      |
                      v
                LM Head
                      |
                      v
              Next Token
```

CatGPT learns through **next-token prediction**.

Given:

```text
Human: Why are you sitting on my
```

it tries to predict:

```text
laptop
```

Then it predicts the next token, and so on.

---

## What I'm Learning

This project is mainly about understanding:

* Tokenization
* Embeddings
* Positional encoding
* Self-attention
* Causal masking
* Transformer blocks
* Next-token prediction
* Cross-entropy loss
* Backpropagation
* AdamW
* GPU training
* Mixed precision
* Text generation
* Sampling
* Dataset quality

---

## Tech Stack

| Technology              | Purpose              |
| ----------------------- | -------------------- |
| Python                  | Development          |
| PyTorch                 | Model & training     |
| Hugging Face Tokenizers | BPE tokenizer        |
| Google Colab            | Training environment |
| NVIDIA T4               | GPU                  |

---

## Dataset

CatGPT combines:

**General conversation data**

Used to teach basic conversational language.

**Curated cat personality data**

Used to teach behaviors such as:

```text
Food
Sleep
Boxes
Keyboard stealing
Zoomies
Chaos
Ignoring humans
```

The personality dataset is intentionally curated instead of simply using a huge amount of noisy generated text.

---

## A Useful Failure

One early experiment taught the model from a noisy cat-personality dataset.

The result?

```text
Human: Are you hungry?

CatGPT:
This is such a fascinating topic!
There's so much depth to explore!
Nya~
```

The model wasn't broken.

It was **learning exactly what we gave it**.

That experiment became an important lesson:

> Data quality matters.


---

## Current Status

**Version:** CatGPT V1 — In Development

**Training:** Google Colab + NVIDIA T4

**Model:** Small decoder-only Transformer

**Goal:** Learn by building, not just using.

---

## Run It

The project is currently developed in Google Colab.

```bash
git clone <your-repository>
```

Open the notebook and enable:

```text
Runtime → Change runtime type → T4 GPU
```

Then run the notebook from top to bottom.

---

## Why CatGPT?

Because building a serious LLM is a little ambitious.

Building a tiny one that gets angry when you touch its keyboard?

Much more reasonable.

<p align="center">
  <img src="https://media.giphy.com/media/mlvseq9yvZhba/giphy.gif" width="250" alt="Cat looking at computer">
</p>

---

## Philosophy

```text
Build.
Break.
Understand.
Fix.
Repeat.
```

If the final model becomes intelligent:

Great.

If it becomes a very convincing idiot cat:

Also great.

---

<p align="center">
  <b>CatGPT — because every Transformer deserves a little chaos.</b>
</p>
