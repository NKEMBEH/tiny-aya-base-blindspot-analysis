# Tiny Aya Base (3.35B) Blind Spot Analysis

## Overview

This repository presents a systematic evaluation of **CohereLabs/tiny-aya-base (3.35B)**, a multilingual pretrained language model. The objective is to identify and categorize model blind spots across reasoning, constraint adherence, factual reliability, and hallucination behavior.

The curated blind spot dataset is publicly available on Hugging Face:

👉 https://huggingface.co/datasets/NKEMBEH-B/tiny-aya-base-blindspots

---

## Evaluation Objectives

The model was evaluated for weaknesses in:

- Arithmetic reasoning
- Multi-step logical reasoning
- Strict constraint following (e.g., exact word count, JSON-only output)
- Ambiguity handling
- Region-specific factual knowledge
- Logical consistency
- Scientific citation hallucination

---

## Methodology

The model was loaded in Google Colab using Hugging Face Transformers. Carefully designed prompts were used to probe systematic failure modes.

Each evaluation entry includes:
- `input`
- `expected_output`
- `model_output`
- `blind_spot_category`
- `notes`

---

## Key Findings

The model demonstrates:

- Arithmetic instability and multi-step reasoning errors
- Failure to obey strict output formatting constraints
- Overconfident hallucination of scientific citations
- Fragility in local and region-specific knowledge
- Logical inconsistency when handling contradictory premises

---

## Suggested Improvements

To mitigate these blind spots, the model would benefit from:

1. Verified math and logical reasoning datasets
2. Constraint-following training with automatic validators
3. Curated factual QA datasets (especially for lower-resource regions)
4. Uncertainty calibration training to discourage hallucination

---

## Author

Nkembeh Benjamin Mezindah  
Douala, Cameroon
