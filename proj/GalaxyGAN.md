---
layout: proj
title: "space.ml :: GalaxyGAN"
slogan: "Generative Adversarial Networks recover features in astrophysical images of galaxies beyond the deconvolution limit"
projname: "GalaxyGAN"
paperbutton: "MNRAS 2017"
paperlink: "https://academic.oup.com/mnrasl/article-lookup/doi/10.1093/mnrasl/slx008"
---


<img src="https://github.com/SpaceML/SpaceML.github.io/blob/master/gg/GAN_example.png?raw=true">
<I>Example results achieved with the GAN. From left to right: the original SDSS image, the degraded image with a worse PSF and higher noise level (indicating the PSF and noise level used), the image as recovered by the GAN, and for comparison, the result of a deconvolution. This figure visually illustrates the GAN's ability to recover features which conventional deconvolutions cannot.</I>

<b>Abstract:</b> Observations of astrophysical objects such as galaxies are limited by various sources of random and systematic noise from the sky background, the optical system of the telescope and the detector used to record the data. Conventional deconvolution techniques are limited in their ability to recover features in imaging data by the Shannon-Nyquist sampling theorem. Here we train a generative adversarial network (GAN) on a sample of 4,550 images of nearby galaxies at 0.01\<z\<0.02 from the Sloan Digital Sky Survey and conduct 10X cross validation to evaluate the results. We present a method using a GAN trained on galaxy images that can recover features from artificially degraded images with worse seeing and higher noise than the original with a performance which far exceeds simple deconvolution. The ability to better recover detailed features such as galaxy morphology from low-signal-to-noise and low angular resolution imaging data significantly increases our ability to study existing data sets of astrophysical objects as well as future observations with observatories such as the Large Synoptic Sky Telescope (LSST) and the Hubble and James Webb space telescopes. 

<!--<b><a href="http://space.ml/res/gan_paper.pdf">Paper PDF</a></b>-->

# Selected Press Coverage

<ul>
<li> <a href="https://www.theatlantic.com/technology/archive/2017/03/machines-will-do-our-stargazing-for-us/518319/">
        <strong>The Atlantic</strong>: Machine Learning Is Bringing the Cosmos Into Focus</a><br/>
        </li>
<li> <a href="https://www.wired.com/2017/03/astronomers-deploy-ai-unravel-mysteries-universe/">
        <strong>WIRED Science</strong>: Astronomers Deploy AI to Unravel the Mysteries of the Universe</a><br/>
        </li>
<li> <a href="https://www.theregister.co.uk/2017/02/23/galaxies_to_drugs_ai_hype_makes_its_way_to_science/?mt=1488825917133">
        <strong>The Register</strong>: From drugs to galaxy hunting, AI is elbowing its way into boffins' labs</a><br/>
        </li>
<li> <a href="https://phys.org/news/2017-02-neural-networks-sharpest-images.html">
        <strong>Phys.org</strong>: Neural networks promise sharpest ever images</a><br/>
        </li>
</ul>

# Weakly Supervised Neural Network with Astrophysics Knowledge

One limiting factor in training deep neural networks is often the number of training examples one can get. The folklore often tells us “the more, the better.” In GalaxyGAN, one training example is a pair of two images: one clear image without space noise and one that we can observe in the presence of space noise.

Direct acquisition of such training pairs could be difficult because our ability to get clear images is limited by the throughput of a few high-quality telescopes. Instead, we choose to weakly supervise a neural network to generate training images automatically. The observations are simple; astrophysicists have been studying sky noises for hundreds of years, and they already have some physical models to describe their current understanding of such noises. Why not take advantage of such noise models to automatically degrade a relatively clear image as the training set? This observation allows us to generate a large-enough training set in just a couple of hours to train our generative adversarial network. You can see in our paper that the results obtained by this weak supervision mechanism: they are quite good!

# Applications to astrophysics data sets
The GAN method presented here opens up the possibility of recovering <i>more</i> information from existing and future imaging data. Applying this GAN to images of galaxies as demonstarted in the paper de-noises data and effectively improves the seeing. The method is thus similar to obtaining a deeper image with better seeing.  The reliability of the method relies heavily on the training set: the GAN generally can only produce useful improvements for features it has been trained on. It can attempt to reconstruct previously unknown features though with a lower degree of reliability. We propose that the GAN presented here, and methods based on it can be applied to a wide range of existing and future sky surveys (such as <a href="http://panstarrs.stsci.edu/">Pan-STARRS</a>, <a href="https://www.lsst.org/">LSST</a>, <a href="http://www.naoj.org/Projects/HSC/">HSC</a> and others).


# Team Members

<table style="border:none;">
<tr>

<td><img src="https://github.com/SpaceML/SpaceML.github.io/blob/master/gg/lucas.jpg?raw=true" width="150"><br/>
<a href="#">Lucas Fowler</a></td>

<td><img src="https://github.com/SpaceML/SpaceML.github.io/blob/master/gg/hantian.png?raw=true" width="150"><br/>
<a href="#">Hantian Zhang</a></td>

<td><img src="https://github.com/SpaceML/SpaceML.github.io/blob/master/gg/gokul.jpg?raw=true" width="150"><br/>
<a href="#">Gokula Santhanam</a></td>

</tr>


<tr>

<td><img src="https://github.com/SpaceML/SpaceML.github.io/blob/master/gg/kevin.png?raw=true" width="150"><br/>
<a href="http://www.astro.ethz.ch/schawinski">Kevin Schawinski</a></td>

<td><img src="https://github.com/SpaceML/SpaceML.github.io/blob/master/gg/ce.jpeg?raw=true" width="150"><br/>
<a href="https://www.inf.ethz.ch/personal/ce.zhang/">Ce Zhang</a></td>

</tr>
</table>





