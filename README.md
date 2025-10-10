# Through the Lenses: A Circuit Odyssey

A mechanistic interpretability study exploring how different "lenses" decode transformer intermediate activations, with a focus on hallucination analysis in large language models.

Read the detailed blog here: [Through the Lenses – A Circuit Odyssey](https://docs.google.com/document/d/1lqqle-WUVm4EEkRZMeCC-BaaJ8Kmvngm_GEQigYzGMY/)


## Overview

This repository accompanies our research blog post investigating circuit analysis techniques for understanding hallucinations in LLMs. We explore three different approaches for interpreting intermediate layer activations:

- **Logit Lens**: Direct projection using the unembedding matrix
- **Tuned Lens**: Layer-specific affine transformations learned to match final layer distributions
- **Normed Lens**: Our novel approach using normalized unembedding vectors


## Key Findings

- Logit Lens frequently surfaces rare, high-norm tokens in intermediate layers
- Tuned Lens doesn't fully resolve interpretation issues
- **Normed Lens** provides more consistent interpretability across layers by using cosine similarity instead of raw dot products


## Repository Contents

- `tuned-lens-training_script.ipynb`: Training script for Tuned Lens (supports TransformerLens and Gemma-2 models)
- `lens-expt.ipynb`:
Jupyter notebook to reproduce all graphs and data in the blog.


## Model

All experiments conducted on **Gemma-2-2B-IT** using TransformerLens.

## Citation

If you find this work useful, please cite our blog post:

```
Pakshal Nagda & Smitali Bhandari (2025). Through the Lenses: A Circuit Odyssey.
Project Viveka, AI Club, Centre for Innovation, IIT Madras.
```


## Authors

**Pakshal Nagda** and **Smitali Bhandari**

Project Viveka
AI Club, Centre for Innovation
IIT Madras
