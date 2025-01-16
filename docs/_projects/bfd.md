---
layout: page
title: "Bit Flipping Decoding, A Reinforcement Learning Approach"
description: "TODO"
date: 2024-12-06
permalink: /projects/bdf/
usemathjax: true
---
### Useful Links
[Link to the repository](https://github.com/FlynnDowey/RL_decoding)

<a href="{{ site.baseurl }}/reports/Error_Correction_Codes___Project_Report-4-2_Redacted.pdf" target="_blank">View the report</a> 

### Project Overview
This project report delves into the innovative application
of Reinforcement Learning (RL) techniques for decoding
error-correcting codes, with a focus on binary linear codes and a
bit-flipping (BF) decoding strategy. Utilizing the SARSA and Qlearning
algorithms within a Markov Decision Process (MDP)
framework, the study extends the conventional approach to
decoding by iteratively making BF decisions based on individual
bits, thereby transforming the decoding process into a series of
RL problems. The exploration includes a comprehensive background
on channel coding, detailing the transition of received
signals over an additive white Gaussian noise channel to a binary
symmetric channel, and explicates the BF decoding algorithm as
well as the foundational elements of Markov Decision Processes.
A paramount challenge addressed in this work is the prohibitive
memory complexity associated with tabular RL algorithms. To
mitigate this, a solution involving the integration of a lowcomplexity,
parameterized approximator for the Q-function is
discussed, utilizing a Neural Network (NN). This approach not
only offers a scalable alternative to tabular methods but also
leverages the advantages of machine learning to enhance decoding
performance. Empirical results from simulations illustrate
the efficacy of the tabular SARSA decoder, which surpasses both
traditional and BF decoders in terms of Bit Error Rate (BER),
with higher computational efficiency. While the parameterized
SARSA decoder does not outperform its tabular counterpart,
it nonetheless presents a viable option for decoding large codes,
where tabular methods are impractical. The comparison between
SARSA and Q-learning highlights the situational advantages of
each, suggesting avenues for future research to optimize decoder
performance across different channel models and coding schemes.
This investigation underscores the potential of RL techniques in
the realm of error correction coding, particularly in optimizing
decoding strategies for binary linear codes.