# Multi Source Diffusion Models

 * **Paper:** Multi-Source Diffusion Models for Simultaneous Audio Generation and Separation \((arxiv)[todo]\)
 * **Authors:** Irene Tallini\*, Giorgio Mariani\*, Emilian Postolache\*, Michele Mancusi\*, Luca Cosmo, Emanuele Rodolà
 * **Abstract:**  In this work we define a diffusion-based generative model capable of both music synthesis and source separation by learning the score of the joint probability density of sources sharing a context. Alongside the classic total inference tasks (i.e. generating a mixture, separating the sources), we also introduce and experiment on the partial inference task of *source imputation*, where we generate a subset of the sources given the others (e.g., play a bass track that goes well with the drums). Iteratively performing hint-based separation with randomly imputed sources, starting with the estimates of a total separation run, is equivalent to Gibbs sampling and improves separation results.
 Additionally, we introduce a novel inference method  for the separation task. We train our model on *Slakh2100*, a standard dataset for musical source separation, provide qualitative results in the generation settings and showcase competitive quantitative results in the separation setting.
 Our method is the first example of a single model that can handle both generation and separation tasks, and it represents a step toward general audio models.

Below are some examples of the tasks we can perform with our approach.

## Generation
[sample-1](/media/generation-1.mp3)
[sample-2](/media/generation-2.mp3)
[sample-3](/media/generation-3.mp3)
[sample-4](/media/generation-4.mp3)

## Imputation (partial generation)

## Separation

