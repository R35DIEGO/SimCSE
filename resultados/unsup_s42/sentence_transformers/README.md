---
language: en
library_name: sentence-transformers
tags: [simcse, sentence-similarity]
---
# U2T02 SimCSE
Author: Diego Jesus Loria Campos; add remaining team members before publishing.

Training: provided SNLI train-only 100k subset; 165529 unique sentences / 33351 entailment pairs; 9488 pairs have contradictions. No STS-B training.

Recipe: `{"seed": 42, "batch_size": 64, "temperature": 0.05, "epochs": 1, "dropout": 0.1, "eval_steps": 250, "name": "unsup_s42", "mode": "unsup", "lr": 3e-05, "same_mask": false, "hard_negatives": false}`. Max length: 64; best checkpoint selected using STS-B dev.

Test results: `{"spearman": 69.84138558926836, "alignment": 0.2273658961057663, "uniformity": -2.3765439987182617}`. Spearman ×100; normalized cosine, no regressor. Alignment: score >=0.8 pairs, alpha=2; uniformity: t=2, 20000 sampled pairs.

Limitations: English only, short sentences, limited NLI data, domain bias, no claim of medical or factual reliability. Semantic similarity is not factual entailment.
