# deep_ml_project_19
link for colab Notebook [here](https://colab.research.google.com/drive/1AuAllaSfyH2CeOOIhTfAYsHlt0NH88xH)

## Abstract

In the context of this project we intend to implement a deep convolutional neural network architecture proposed by[1], propose variances derived from the latter architecture and study the influence of each hyperparemeter on the performance of the network. As a bonus we intend to embed our best model into a pc application that translates a sequence of sign language characters into text. This appears to be of a great utility considering that this may present the first step towards a real time translator on smartphones that we intend to implement beyond the scope of this project.


## Motivation

Language translation is one of the core AI tasks. AI systems have reached a competitive performance in the translation between various spoken and written languages.
An important form of language, which is well spread but yet not sufficiently treated, is the sign language. More than 460 million people [5] around the world use sign language to communicate with one another or to translate from/to other languages. <br>
Automating the task of translating from or to sign language appears then to be a perfect application for Deep Learning solutions. In fact many research institutions and companies have tried to offer deep learning based solutions but as far as we know, no publicly available official paper implementations have been published.<br>

In this project we therefore try then to implement a proposed solution by "Vivek and Dianna" from the "State University of New York at Buffalo" from their paper "Using Deep Convolutional Neural Networks for Gesture Recognition in American Sign Language". 
We found this paper especially interesting, since it does not rely on transfer learning as many other approaches like from Jalal et al. [3].
Since an official implementation has not been published, we consider implementing the proposed architecture and reproducing the results to familiarize our selves with deep learning frameworks. We then intend to propose other variants of the architecture and study their influence on the network's performance.<br>

This proposal is then description of what we intend to do during this project and contains:
1. description of the used Data Set
2. details about the baseline architecture 
3. the set hyperparameters variation that we intend to study

## Dataset

The data set used in this project will be the "MUHandImagesASL", made publicly available by the Massey University[2]. The dataset is based on American Sign Language hand gestures and is also used in a variety of other papers, e.g. by Garcia et al. [4]. The particularity of this dataset lies on covering large variety of hands, dialects and illumination conditions.<br>

The dataset contains 2425 images of 5 individuals, divided in 5 separated folders, one for each volunteer.


## Reference Paper
### Method
For the task of classifying sign Language, Convolutional Neural Networks (CNNs) are used.  CNNs have been extremely 
successful in image recognition and classification problems, and have been successfully implemented for human gesture 
recognition in recent years [1].
### Architecture
The implemented architecture consists of a CNN with multiple convolutional and dense layers followed by a max-pool layer
and a dropout layer and two groups of fully connected layer, followed by a drop-out layer and one final output layer 
![cnn](https://gitlab.com/ramzi_ourari/deep_ml_project_19/uploads/a2ccd912c7c6cc0d241385ac2070d392/cnn.PNG)
### Proposed variations:
We will make use of random-search hyper-parameter optimization to determine the best parameters for this architecture and 
benchmark the results with the published accuracy values.
The set of parameters we will cover in this search are: Number of layers, Density of layers, Drop-out rate, Learning rate of the optimizer and the regularization term.

Besides, we will compare different optimizers and different loss-functions.  Finally, we will compare the effect of using batch-normalization in comparison to setting a dropout-rate

## References
[1] :Using Deep Convolutional Networks for Gesture Recognition in American Sign Language,
Vivek Bheda and N.Dianna Radpour, State University of New York at Buffalo.<br>
[2] :A. L. C. Barczak, N. H. Reyes, M. Abastillas, A. Piccio, and T. Susnjak, A new 2d static hand
gesture colour image dataset for asl gestures, Research Letters in the Information and Mathematical Sciences 15 (2011), 12–20.<br>
[3] :M. A. Jalal, R. Chen, R. K. Moore and L. Mihaylova, "American Sign Language Posture Understanding with Deep Neural Networks," 2018 21st International Conference on Information Fusion (FUSION), Cambridge, 2018, pp. 573-579.<br>
[4] :Garcia, B., & Viesca, S. A. (2016). Real-time american sign language recognition with convolutional neural networks. Convolutional Neural Networks for Visual Recognition, 2.<br>
[5] :https://www.who.int/news-room/fact-sheets/detail/deafness-and-hearing-loss
