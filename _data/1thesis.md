---
name: Symbolic Music Generation using Recurrent Neural Networks
tools: [Deep Learning, Music generation, LSTM, Attention mechanism, master thesis]
image: https://github.com/cristianmtr/master_thesis_symbolic_music_generation/blob/master/thesis_examples.png?raw=true
description: The project aims to investigate symbolic music generation using LSTMs. Experiments in dataset encoding, dataset stylistic homogeneity, attention mechanism, and bidirectionality.
---

# Symbolic Music Generation using Recurrent Neural Networks

Master thesis project at M. Sc. IT & Cognition, University of Copenhagen.

June, 2019.

Abstract:

```
The current work aims to address the task of symbolic music generation with recurrent neural networks.
I provide an overview of the state of the art techniques in the ﬁeld, with a discussion of how these
techniques have been employed on this speciﬁc task. I then conduct experiments on how diﬀerent factors
aﬀect learning. I test for dataset properties (stylistic homogeneity, encoding format) and sequential
mechanisms (attention mechanism, bidirectionality). In evaluating the models I employ an objective
methodology that compares the generated samples with the training sets on multiple musical domain
statistics. I also measure the degree of plagiarism in each of the generated sets, as compared with
the training samples. I provide a discussion on how and why the mechanisms impact symbolic music
generation. I then perform a subjective analysis of the quality of the samples generated. Finally, I conduct
a user study comparing the generated sets with the training sets. The most important conclusions are: the
attention mechanism commonly employed in machine translation does improve learning in symbolic music
generation in this experiment; dataset homogeneity has a prominent impact on learning; bidirectional
LSTMs do oﬀer an improvement; the model trained on the pianoroll format has a slightly more varied
rhythmic vocabulary than the melody counterpart.
```

Paper available [here](https://github.com/cristianmtr/master_thesis_symbolic_music_generation/blob/master/CristianMitroi_thesis2019.pdf)

## Details

In my master thesis I set to investigate two main hypotheses areas:

1. how does the dataset of music used to train the model affect its learning capabilities?
   
   Sub-questions:
   1. distribution of styles and genres within a dataset 
   2. dataset encoding format

2. how do mechanism for sequential, temporal learning affect the model?

    Sub-questions:
    1. how does the attention mechanism affect learning?
    2. how does the bidirectional wrapper for the LSTM affect learning?

### Evaluation


### Architecture

The architecture is based on RNNs with LSTM cells.

The problem we are solving is a supervised, sequential learning problem, with a many-to-one model (as per Karpathy’s classiﬁcation in [his blog post](http://karpathy.github.io/2015/05/21/rnn-effectiveness/)).

See below figure for architecture of system:

![architecture](https://github.com/cristianmtr/master_thesis_symbolic_music_generation/blob/master/arch.PNG?raw=true)


