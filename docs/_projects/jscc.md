---
layout: page
title: "Joint Source Channel Coding using Attention-Based Variational Autoencoder"
description: "Enhancements to VQ-VAE for image transmission and transformers for textual message delivery over corrupted communication channels"
date: 2024-04-01
permalink: /projects/JSCC/
usemathjax: true
---
### Useful Links
[Link to the repository](https://gitfront.io/r/fmdowey/SwcPPL47Y4c7/JSCC/)

<a href="{{ site.baseurl }}/reports/CPSC550_project_report-3-3_Redacted.pdf" target="_blank">View the report</a> 

### Project Overview
In this paper, we present two examples of data-driven solutions to the problem
of joint source channel coding (JSCC). The first example uses images as messages, and the second uses textual
data. We consider two types of channels: binary erasure channel (BEC) and additive white
Gaussian noise (AWGN). We propose a novel adjustment to the current vector quantized variational autoencoder (VQ-VAE) that utilizes attention to make codeword assignments and showcases its performance over a
method presented using soft assignments. The second example enhances the results
of a recent paper by using the transformer model as proposed by Vaswani with
cross-entropy loss function. Comparisons are made to standard source/channel
coding techniques such as Huffman/Turbo coding demonstrating the efficacy of
our proposed model.

Incorporating an attention-based protocol lets the model learn which codewords are potentially
more beneficial and also allows for gradient computation in automatic differentiation, which is
"skipped" in VQ-VAEs. We also did a soft assignment of nearest codewords by keeping the method of calculating distances between the messages and the encodings. However, we removed the arg min and replaced it with a
negated softmax. We believe this is a novel application to VQ-VAEs.

### Results
#### Image Date
Experiments were conducted on the CelebA dataset. Refer to the report for a complete analysis. 

<img src="{{site.baseurl}}/images/jscc_reconstruction.jpg" alt="VQ-VAE results" title="Samples collected from the trained models" width="600" height="300">

(a) VQ-VAE soft assignments trained with no noise. (b) VQ-VAE attentive assignments
trained with no noise. Row 1: original images, row 2: reconstructed images from VQ-VAE, row 3:
reconstructed images from VQ-VAE with AWGN $\sigma^{(a)}$ = 0.01, $\sigma^{(b)}$ = 0.1, $\mu$ = 0.

#### Text Data
TODO
