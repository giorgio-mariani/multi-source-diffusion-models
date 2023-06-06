# Multi Source Diffusion Models

 * **Paper:** ***Multi-Source Diffusion Models for Simultaneous Audio Generation and Separation*** \([arXiv.org](https://arxiv.org/abs/2302.02257)\)  <br/><br/>
 * **Authors:** *Giorgio Mariani\*, Irene Tallini\*, Emilian Postolache\*, Michele Mancusi\*, Luca Cosmo, Emanuele Rodolà*  <br/><br/>
 * **Abstract:** In this work, we define a diffusion-based generative model capable of both music synthesis and source separation by learning the score of the joint probability density of sources sharing a context. Alongside the classic total inference tasks (i.e. generating a mixture, separating the sources), we also introduce and experiment on the partial inference task of source imputation, where we generate a subset of the sources given the others (e.g., play a piano track that goes well with the drums). Additionally, we introduce a novel inference method for the separation task. We train our model on Slakh2100, a standard dataset for musical source separation, provide qualitative results in the generation settings, and showcase competitive quantitative results in the separation setting. Our method is the first example of a single model that can handle both generation and separation tasks, thus representing a step toward general audio models.
Below are some examples of the tasks we can perform with our approach.

## Generation
Here we ask the neural model to randomly generate some new music:

| Sample #1    | Sample #2    |
| :----------: | :----------: |
|<audio controls><source src="media/generation/1/mix.mp3"></audio> | <audio controls><source src="media/generation/2/mix.mp3"></audio> |

| Sample #3    | Sample #4    |
| :----------: | :----------: |
| <audio controls><source src="media/generation/3/mix.mp3"></audio>| <audio controls><source src="media/generation/4/mix.mp3"></audio>|

| Sample #5    | Sample #6    |
| :----------: | :----------: |
| <audio controls><source src="media/generation/5/mix.mp3"></audio> |   <audio controls><source src="media/generation/6/mix.mp3"></audio>|

| Sample #7    | Sample #8    |
| :----------: | :----------: |
|<audio controls><source src="media/generation/7/mix.mp3"></audio> | <audio controls><source src="media/generation/8/mix.mp3"></audio> |

| Sample #9    | Sample #10    |
| :----------: | :----------: |
| <audio controls><source src="media/generation/9/mix.mp3"></audio>| <audio controls><source src="media/generation/10/mix.mp3"></audio>|

<br/><br/>

## Source Imputation (a.k.a. Partial Generation)
Given a source stem as input (e.g. drums), the neural model generates accompanying instruments:

| Original Source #1 | Generated accompaniment #1 |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/inpainting/1/fixed.mp3" type="audio/mpeg"> </audio> |   <audio controls preload="none"><source src="media/inpainting/1/mix.mp3" type="audio/mpeg"> </audio>|

| Original Source #2 | Generated accompaniment #2 |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/inpainting/2/fixed.mp3" type="audio/mpeg"> </audio> |   <audio controls preload="none"><source src="media/inpainting/2/mix.mp3" type="audio/mpeg"> </audio>|

| Original Source #3 | Generated accompaniment #3 |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/inpainting/3/fixed.mp3" type="audio/mpeg"> </audio> |   <audio controls preload="none"><source src="media/inpainting/3/mix.mp3" type="audio/mpeg"> </audio>|

| Original Source #4 | Generated accompaniment #4 |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/inpainting/4/fixed.mp3" type="audio/mpeg"> </audio> |   <audio controls preload="none"><source src="media/inpainting/4/mix.mp3" type="audio/mpeg"> </audio>|

| Original Source #5 | Generated accompaniment #5 |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/inpainting/5/fixed.mp3" type="audio/mpeg"> </audio> |   <audio controls preload="none"><source src="media/inpainting/5/mix.mp3" type="audio/mpeg"> </audio>|

| Original Source #6 | Generated accompaniment #6 |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/inpainting/6/fixed.mp3" type="audio/mpeg"> </audio> |   <audio controls preload="none"><source src="media/inpainting/6/mix.mp3" type="audio/mpeg"> </audio>|

| Original Source #7 | Generated accompaniment #7 |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/inpainting/7/fixed.mp3" type="audio/mpeg"> </audio> |   <audio controls preload="none"><source src="media/inpainting/7/mix.mp3" type="audio/mpeg"> </audio>|

| Original Source #8 | Generated accompaniment #8 |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/inpainting/8/fixed.mp3" type="audio/mpeg"> </audio> |   <audio controls preload="none"><source src="media/inpainting/8/mix.mp3" type="audio/mpeg"> </audio>|

<br/><br/>

## Source Separation
Finally, it is possible to use our model to extract single sources from an input mixture:

**Input Mixture 1**
<audio controls preload="none"><source src="media/separation/1/mix.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>

| Separated Bass | Separated Drums |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/1/sep1.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/1/sep2.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |

|Separated Guitar| Separated Piano|
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/1/sep3.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/1/sep4.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>|

<br/><br/>

**Input Mixture 2**
<audio controls preload="none"><source src="media/separation/2/mix.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>

| Separated Bass | Separated Drums |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/2/sep1.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/2/sep2.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |

|Separated Guitar| Separated Piano|
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/2/sep3.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/2/sep4.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>|

<br/><br/>

**Input Mixture 3**
<audio controls preload="none"><source src="media/separation/3/mix.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>

| Separated Bass | Separated Drums |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/3/sep1.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/3/sep2.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |

|Separated Guitar| Separated Piano|
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/3/sep3.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/3/sep4.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>|

<br/><br/>

**Input Mixture 4**
<audio controls preload="none"><source src="media/separation/4/mix.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>

| Separated Bass | Separated Drums |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/4/sep1.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/4/sep2.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |

|Separated Guitar| Separated Piano|
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/4/sep3.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/4/sep4.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>|

<br/><br/>

**Input Mixture 5**
<audio controls preload="none"><source src="media/separation/5/mix.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>

| Separated Bass | Separated Drums |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/5/sep1.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/5/sep2.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |

|Separated Guitar| Separated Piano|
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/5/sep3.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/5/sep4.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>|

<br/><br/>

**Input Mixture 6**
<audio controls preload="none"><source src="media/separation/6/mix.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>

| Separated Bass | Separated Drums |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/6/sep1.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/6/sep2.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |

|Separated Guitar| Separated Piano|
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/6/sep3.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/6/sep4.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>|

<br/><br/>

**Input Mixture 7**
<audio controls preload="none"><source src="media/separation/7/mix.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>

| Separated Bass | Separated Drums |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/7/sep1.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/7/sep2.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |

|Separated Guitar| Separated Piano|
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/7/sep3.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/7/sep4.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>|

<br/><br/>

**Input Mixture 8**
<audio controls preload="none"><source src="media/separation/8/mix.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>

| Separated Bass | Separated Drums |
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/8/sep1.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/8/sep2.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |

|Separated Guitar| Separated Piano|
| :----------: | :----------: |
|<audio controls preload="none"><source src="media/separation/8/sep3.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio> |    <audio controls preload="none"><source src="media/separation/8/sep4.mp3" type="audio/mpeg"> Your browser does not support the audio element.</audio>|
