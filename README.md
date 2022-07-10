# Federated-Learning
Demonstration of unintentional leakage of private data in federated learning environment using Generative Adversarial Network (GAN). This repository was part of my term project submission, Data Analytics course (CLL 788), IIT Delhi.


## Overview
The project was directly inspired from following research papers which have tried to point out privacy issues in federated learning environment. It could be noted that this directly contradict with their supposed advantage over centralized learning environment
[Paper 1](https://arxiv.org/pdf/1702.07464.pdf) [Paper 2](https://www.researchgate.net/publication/336947655_Poisoning_Attack_in_Federated_Learning_using_Generative_Adversarial_Nets)

## Paper review

> The following statements are according to my personal understanding of the topic. It is possible that these statements could be counter argued.

- Although the proposed method seems to be working, it is bound to number of constraints. First of all the paper assumes that the label being reproduced is unique to an individual which may or may not be the case in real world scenario.
- If the target label is not unique than the reproduced data can be considered as statistical average of the data belonging to multiple indiviudal, which again might not be enough to reveal some sensitive information.
- Tuning GAN is generally tougher than other deep learning architecture. In collaborative environmen where some percentage of weight is taken (Paper 1) or weight averaging is done (Paper 2) to derive parameters for central model, proper tuning becomes even more difficult to extract information within limited number of rounds. In our case I did some pretraining for faster convergence as suggested by [Jaskiee](https://github.com/Jaskiee/GAN-Attack-against-Federated-Deep-Learning)
- The authors (Paper 1) asserts that the collaborative setup is fundamentally broken, which I believe is bit harsh given the number of conditional dependencies of attack setup.

