# 🧠 Fine-Tuning Pythia-410M with LoRA for Financial QA from 10-K Filings

This project demonstrates how to fine-tune the [EleutherAI/pythia-410m](https://huggingface.co/EleutherAI/pythia-410m) model using [PEFT (LoRA)](https://github.com/huggingface/peft) for a domain-specific question-answering task based on financial risk factors extracted from SEC 10-K filings.

> 🚀 Goal: Create a specialized model that can answer financial risk-related questions better than the base model, using a small instruction-tuned dataset and parameter-efficient fine-tuning techniques.

---

---

## 📊 Dataset

We use the [`virattt/financial-qa-10K`](https://huggingface.co/datasets/virattt/financial-qa-10K) dataset from Hugging Face. This contains instruction-style question-answer pairs extracted from public 10-K filings, focused on risk disclosures.

Each example follows an **Alpaca-style format**:

Colab Notebook : https://colab.research.google.com/drive/1VEGf0q8qgzbtvoebEdm970aViIUAWs4p#scrollTo=q9DD3NIvS28J
```txt
### Instruction:
What are Tesla's main risk factors mentioned in their 10-K filing?

### Response:
Tesla's main risk factors include...
