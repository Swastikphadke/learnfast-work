# N-gram Language Model

## Next-Word Prediction using Alice's Adventures in Wonderland

**Corpus:** Alice's Adventures in Wonderland — Lewis Carroll  
**Source:** Project Gutenberg, eBook #11

## Overview

A statistical language model that learns word-transition patterns and predicts the next word using N-grams.

## Implementation

- N-gram count construction
- Maximum Likelihood Estimation (MLE)
- Bigram and trigram text generation
- Add-k smoothing
- Held-out perplexity evaluation
- Comparison of model configurations

## Experimental Results

Perplexity comparison after correcting unknown-word handling:

| k | Bigram | Trigram |
|---|---:|---:|
| 0.01 | 81.31 | 224.27 |
| 0.1 | 92.93 | 319.64 |
| 0.5 | 147.72 | 513.00 |
| 1.0 | 196.51 | 631.58 |

### Findings

- The bigram model achieved lower perplexity for all tested smoothing values.
- Smaller smoothing values performed better on this corpus.
- Trigram contexts were sparser and performed worse with the available training data.
- A larger corpus may provide more examples of trigram contexts.

## Best Tested Configuration

**Bigram with k = 0.01**, achieving a perplexity of 81.31.

## Files

- `ngram_language_model.ipynb` — Complete implementation and experiments.
- `alice.txt` — Source corpus downloaded from Project Gutenberg.

## Technologies

- Python
- Jupyter Notebook
- Regular Expressions
- Collections (`Counter`, `defaultdict`)
- Mathematical functions (`math`)
