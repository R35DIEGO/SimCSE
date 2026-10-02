# SimCSE Sentence Embeddings

Implementation of **U2T02: SimCSE, train your own sentence embedding model**.

This project implements unsupervised and supervised SimCSE using `bert-base-uncased`, trained on the provided SNLI subset and evaluated on STS-B.

The notebook includes training, evaluation, dropout and hard-negative ablations, and model export.

## Hugging Face Model

### [Unsupervised SimCSE](https://huggingface.co/Perry-DLC/upy-u2t02-simcse)

Encodes English sentences into vectors for semantic similarity and retrieval. The published model was reloaded from Hugging Face and verified against the original test results.

## Code

[SimCSE notebook](U2T02_SimCSE_.ipynb)

Open the notebook in Google Colab with a GPU and follow its execution instructions.

The full methodology, results, analysis and team information are included in the accompanying report.
