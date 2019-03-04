---
title: "UCLA Physics and Astronomy: Doubly Lensed Quasars"
date: 2017-09-21
tags: [Part Time]
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

Looking at the posterior distributions of my parameters, we can see that I got quite good results from a Gaussian model. The MCMC convered within a few hundred steps.

<img src="{{ site.baseurl }}/images/Experiences/Quasar/C0407-1931_Plot_5000_0Steps.png">


## June 2018 - Present
Using Lenstronomy
