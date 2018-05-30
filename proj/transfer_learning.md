---
layout: proj_transferlearning
title: "space.ml :: Transfer Learning"
slogan: "Using transfer learning to detect galaxy mergers"
projname: "transfer_learning"
paperbutton: "MNRAS 2018"
paperlink: https://arxiv.org/abs/1805.10289
---


**Abstract:**

We investigate the use of deep convolutional neural networks (deep CNNs) for automatic visual detection of galaxy mergers. Moreover, we investigate the use of transfer learning in conjunction with CNNs, by retraining networks first trained on pictures of everyday objects. We test the hypothesis that transfer learning is useful for improving classification performance for small training sets. This would make transfer learning useful for finding rare objects in astronomical imaging datasets.
We find that these deep learning methods perform significantly better than current state-of-the-art merger detection methods based on nonparametric systems like CAS and GM<sub>20</sub>. Our method is end-to-end and robust to image noise and distortions; it can be applied directly without image preprocessing. We also find that transfer learning can act as a regulariser in some cases, leading to better overall classification accuracy (_p_ = 0.02). Transfer learning on our full training set leads to a lowered error rate from 0.038 &plusmn; 1 down to 0.032 &plusmn; 1, a relative improvement of 15%.
Finally, we perform a basic sanity-check by creating a merger sample with our method, and comparing with an already existing, manually created merger catalogue in terms of colour-mass distribution and stellar mass function.

<p align="center">
  <img src="../tf/true_positives.png?raw=true" width="400" />
</p>


_Examples of merger systems discovered by applying our method to SDSS images. The number above each galaxy image denotes the confidence of our classifier._


# Merger Sample

We created a sample of potential merger from all _Galaxy Zoo I_ objects in a certain redshift range (0.005 < z < 0.1). We supply a full list, [with](https://people.phys.ethz.ch/~blackhole/spaceml/transfer_learning/merger_probabilities.csv.gz) and [without](https://people.phys.ethz.ch/~blackhole/spaceml/transfer_learning/merger_probabilities_CALIBRATED.csv.gz) recalibration, of all _GZ I_ objects with their merger probability as rated by our classifiers.

# Trained models

The models trained with transfer learning on the full training set are available for download: [1](https://people.phys.ethz.ch/~blackhole/spaceml/transfer_learning/model_0), [2](https://people.phys.ethz.ch/~blackhole/spaceml/transfer_learning/model_1), [3](https://people.phys.ethz.ch/~blackhole/spaceml/transfer_learning/model_2), [4](https://people.phys.ethz.ch/~blackhole/spaceml/transfer_learning/model_3) (created with [Keras](https://keras.io/))


# Team Members

<table style="border:none;">
<tr>

<td><img src="../tf/sandro.png?raw=true" width="150"><br/>
<a href="https://github.com/sandroac">Sandro Ackermann</a></td>

<td><img src="../tf/kevin.png?raw=true" width="150"><br/>
<a href="http://www.astro.ethz.ch/schawinski">Kevin Schawinski</a></td>

<td><img src="../tf/ce.jpeg?raw=true" width="150"><br/>
<a href="https://www.inf.ethz.ch/personal/ce.zhang/">Ce Zhang</a></td>

</tr>
<tr>

<td><img src="../tf/anna.png?raw=true" width="150"><br/>
<a href="http://www.astro.ethz.ch/schawinski">Anna Weigel</a></td>


<td><img src="../tf/dennis.png?raw=true" width="150"><br/>
<a href="https://people.phys.ethz.ch/~rahimit/index.html">Dennis Turp</a></td>

</tr>

</table>
