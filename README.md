# ArabicDistilBERT: Knowledge Distillation of BERT for Arabic

**Published at:**
- [ICLR 2023 — Tiny Papers track](https://openreview.net/forum?id=-bMH1Sk8SSF)
- NeurIPS 2023 — Spotlight Talk, North Africans in ML Workshop
- Deep Learning Indaba

**20,000+ HuggingFace downloads.**

---

## Overview

Arabic NLP has lagged behind English in the availability of efficient, deployable models. Large Arabic BERT models achieve strong performance but are too computationally expensive for many real-world deployments, particularly in low-resource environments.

This project applies knowledge distillation to produce a smaller Arabic BERT model that retains most of the teacher's performance at a fraction of the cost.

## Results

| Model | Parameters | Relative performance |
|---|---|---|
| BERT-large-arabic (teacher) | ~340M | 100% |
| ArabicDistilBERT (student) | ~102M | **92.4%** |

**70% fewer parameters. 92.4% of BERT's Arabic QA performance.**

## Method

- Teacher model: `asafaya/bert-large-arabic`
- Standard knowledge distillation with a modified Hugging Face Transformers library adapted for Arabic tokenisation and the distillation pipeline
- Training data: Arabic text corpus, binarised and tokenised for the distillation procedure

## Installation

```bash
python3 -m venv env && source env/bin/activate
unzip transformers.zip && cd transformers && pip install .
pip install -r transformers/examples/research_projects/distillation/requirements.txt
```

## Citation

```
@inproceedings{elidrisi2023arabicDistilBERT,
  title     = {Knowledge Distillation of BERT on Arabic},
  author    = {Abrar Elidrisi},
  booktitle = {ICLR 2023 Tiny Papers},
  year      = {2023},
  url       = {https://openreview.net/forum?id=-bMH1Sk8SSF}
}
```

## Contact

[abrar.elidrisi@gmail.com](mailto:abrar.elidrisi@gmail.com) —
[abrarelidrisi.github.io](https://abrarelidrisi.github.io) —
[Google Scholar](https://scholar.google.com/citations?user=dPvL6okAAAAJ&hl=en)
