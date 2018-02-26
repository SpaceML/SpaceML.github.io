---
layout: proj_PSFGAN
title: "space.ml :: PSFGAN"
slogan: "A Generative Adversarial Network system for separating quasar point sources and host galaxy light"
projname: "PSFGAN"
paperbutton: "MNRAS 2018"
paperlink: #
---



<img src="../pg/PSFGAN_example_large.png?raw=true">
<I>Example of <tt>PSFGAN</tt> subtracting a simulated point source from an image in the test set. The left image is the original SDSS galaxy we use for comparison. The conditional input for the generator network is the original galaxy with a simulated point source (representing an unobscured AGN) in its center which is the second image in this chart.  <tt>PSFGAN</tt> learns to recover (image on the right) the original image and can generalize its knowledge in order to subtract point sources from galaxies it has never seen before.</I>

<b>Abstract:</b> 
The study of unobscured active galactic nuclei (AGN) and quasars depends on the reliable decomposition of the light from the AGN point source and the extended host galaxy light.  The problem is typically approached using parametric fitting routines using separate models for the host galaxy and the point spread function (PSF). We present a new approach using a Generative Adversarial Network (GAN) trained on galaxy images. We test the method using Sloan Digital Sky Survey (SDSS) *r*-band images with artificial AGN point sources added which are then removed using the GAN and with parametric methods using GALFIT. When the AGN point source PS is more than twice as bright as the host galaxy, we find that our method, <tt>PSFGAN</tt>, can recover PS and host galaxy magnitudes with smaller systematic error and a lower average scatter ({% raw %}$$49\%$$ {% endraw %}). <tt>PSFGAN</tt> is more tolerant to poor knowledge of the PSF than parametric methods. Our tests show that <tt>PSFGAN</tt> is robust against a shift in the PSF width of {% raw %}$$\pm 50\%$${% endraw %} if it is trained on multiple PSF's. We demonstrate that while a matched training set does improve performance, we can still subtract point sources using a <tt>PSFGAN</tt> trained on non-astronomical images. While initial training is computationally expensive, evaluation of <tt>PSFGAN</tt> on data is more than {% raw %}$$40$${% endraw %} times faster than <tt>GALFIT</tt> fitting two components. Furthermore, it is more robust and easy to use than parametric methods as it requires no input parameters.



# Potential for large pipelines and high redshift
Once <tt>PSFGAN</tt> is trained it is very fast in outputting the PS subtracted image. Furthermore it has a remarkable flexibility compared to parametric methods. Overall it is well-suited for automated analyses of large datasets. From a practical point of view it has a significand advantage over parametric methods for automated decomposition of quasars and host galaxies. 
Furthermore it is a promising tool for studying AGN and their host galaxies at higher redshift where classical methods tend to break down. With increasing redshift the contrast ratio between AGN and host galaxy tends to be higher as the intrinsic emission emerges from a bluer part of the Spectral Energy Distribution (SED) where the AGN is dominant. Furthermore the host galaxy is affected by surface brightness dimming while the PS is not. This again increases the probability of fnding high contrast systems with increasing redshift. The range of high contrasts is exactly the range where <tt>PSFGAN</tt> has demonstrated to be superior to parametric methods.


# Animals vs. Galaxies
We show that <tt>PSFGAN</tt> uses its generalized knowledge about galaxy light distributions to subtract their central point sources by running it on images of cats and dogs. Furthermore we train the same architecture on animal images and compare its ability to subtract point sources.

# Team Members

<table style="border:none;">
<tr>
<td><img src="../pg/dominic.png?raw=true" width="150"><br/>
<a href="#">Dominic Stark</a></td>

<td><img src="../pg/bart.png?raw=true" width="150"><br/>
<a href="http://www.astro.ethz.ch/schawinski">Barthelemy Launet</a></td>

<td><img src="https://github.com/SpaceML/SpaceML.github.io/blob/PSFGAN/gg/kevin.png?raw=true" width="150"><br/>
<a href="http://www.astro.ethz.ch/schawinski">Kevin Schawinski</a></td>

<td><img src="../pg/ce.png?raw=true" width="150"><br/>
<a href="https://www.inf.ethz.ch/personal/ce.zhang/">Ce Zhang</a></td>
</tr>

<tr>
<td><img src="../pg/mike.png?raw=true" width="150"><br/>
<a href="http://www.astro.ethz.ch/schawinski">Michael Koss</a></td>

<td><img src="../pg/dennis.png?raw=true" width="150"><br/>
<a href="https://people.phys.ethz.ch/~rahimit/index.html">Dennis Turp</a></td>

<td><img src="../pg/lia.png?raw=true" width="150"><br/>
<a href="http://www.astro.ethz.ch/schawinski">Lia Sartori</a></td>

<td><img src="https://github.com/SpaceML/SpaceML.github.io/blob/PSFGAN/gg/hantian.png?raw=true" width="150"><br/>
<a href="https://people.inf.ethz.ch/hanzhang/">Hantian Zhang</a></td>
</tr>

<tr>
<td><img src="../pg/anna.png?raw=true" width="150"><br/>
<a href="http://www.astro.ethz.ch/schawinski">Anna Weigel</a></td>
</tr>

</table>