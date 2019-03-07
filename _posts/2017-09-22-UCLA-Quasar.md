---
title: "UCLA Physics and Astronomy: Doubly Lensed Quasars"
date: 2017-09-21
tags: [Research]
header:
  #image: images/Experiences/Meteorite/MLab.png
excerpt: "Doubly Lensed Quasars"
mathjax: "true"
---
# Overview of Research
Under Professor Tommaso Treu, his graduate students, and his post-docs we worked on a prject that cronicled five years of follow up and confirmation lensed quasars through Keck-NIRC2, a camera at Keck Observatory. I learned how to perform image analysis with Python and how to run Markov Chain Monte Carlo (MCMC) to optimize parameters given a model attempting to describe observed data. I used an MCMC to estimate the amount of light, flux, of galaxies and quasars we objected in the images by assuming the distribution of light emitted by the objects followed a Gaussian Distribution.

A research [poster](https://drive.google.com/file/d/1r2oRGAJdwo8EXGQ4lBQLHF3bH76_fRS8/view?usp=sharing) I made presenting some of my work.

Furthermore, using [_lenstronomy_](https://github.com/sibirrer/lenstronomy), software developed by one of Professor Treu's post-doc's we reconstructed the images of quasars from our sample to improve our measurements of the magnitude of the lensing galaxies.


# Timeline
## September 2017 - May 2018
### Extracting Photometery
My initial task in this research project was to catalog the relative image positions and flux (brightness) of the doubly lensed quasars and galaxies. I accomplished this by modeling the distribution of light from the quasars and galaxies as Gaussian. Given this model, I used a Monte Carlo Markov Chain (MCMC) to fit this model to the data-the images. I used the package *emcee* to implement an MCMC.

Looking at the posterior distributions of my parameters, we can see that I got quite good results from a Gaussian model. The MCMC converged within a few hundred steps.

<div style="text-align:center"><img src="{{ site.baseurl }}/images/Experiences/Quasar/C0407-1931_Plot_5000_0Steps.png"></div> 

Once I had the positions and flux for the quasars and galaxies I used this information to perform a point spread function (PSF) subtraction. This involved creating a cutout of a point source in the image, ideally this would be some light source other than one the quasar images and lens galaxy. However, other sources of light was unavailable in most of the images. I ended up using one of the quasar images as a PSF. I normalized the flux (brightness) of this PSF against the image of the other quasar, then subtracted off the cutout I made where the other quasar was. That this does, ideally, is remove the light from bright sources in an image in order to reveal fainter objects in an image.

## June 2018 - Present
Using lenstronomy, a gravitational lensing software package written by Simon Birer, I reconstructed the image of the quasars I had. The lenses were models as Single Isothemal-Ellipsoids (SIE), a convenient lens model. An example of the reconstruction can be seen below. The left pane displays the observed image containing the lensing galaxy in the center surrounded by two images of quasars. The center pans represents the reconstuction calculated by *lenstronomy*. The caustic and critical lines I calcualted from another software package, [*gravlens*](http://physics.rutgers.edu/~keeton/gravlens/2012WS/), can be seen as red and yellow lines which tell us how many images of quasars we expect to see. The right most pane represents the differnece between the observed and the reconstructed image. We can see based on the color bar on the right that our reconstruction did pretty well as the residuals were very small.

<img src="{{ site.baseurl }}/images/Experiences/Quasar/J0047_Galfit_Reconst.png">
