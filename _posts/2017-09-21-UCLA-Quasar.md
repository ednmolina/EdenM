---
title: "UCLA Physics and Astronomy: Doubly Lensed Quasars"
date: 2017-09-21
tags: [Research]
header:
  #image:
excerpt: "I extracted photometry and astrometry from images of doubly lensed quasars from the Keck Observatory."
mathjax: "true"
---
<!-- ![Quasar ](/images/J2211+1929_Galfit_Reconst.png) -->

<!-- <p align="center">
<img src="/images/J2211+1929_Galfit_Reconst.png" height="50"/></p> -->

# Overview
Beginning September 2017, under Professor Tommaso Treu, his graduate students, and his post-docs, we worked on a project that chronicled five years of follow up and confirmation lensed quasars through NIRC2, a camera at Keck Observatory--the world's largest optical telescope. The project revolved around reconstructing images of gravitationally lensed quasars to improve measurements on the photometry of the quasar systems.

I learned how to process images with Python, how to use Markov Chain Monte Carlo (MCMC) to optimize parameters given a model, and to reconstruct images of gravitationally lensed quasars using *lenstronomy*.

# Timeline of Work
## September 2017 - May 2018
From September 2017 - May 2018 I worked on extracting photometry and astrometry from images of gravitationally lensed quasars from observing campaigns from the years: 2013, 2016, 2017, and 2018.

My first task in this project was to perform Point Spread Function (PSF) subtractions on the images. This was done because in some cases, the lensing galaxy was not visible because the image of the quasars was so bright. Furthermore, the Einstein rings of doubly lensed quasars might also be revealed.

On May 2018, I presented the work I had accomplished up until that point at UCLA's undergraduate research week where undergraduates on campus present the research they have been working on. My research [poster](https://drive.google.com/file/d/1r2oRGAJdwo8EXGQ4lBQLHF3bH76_fRS8/view?usp=sharing) showcased my progress.

## August 2018 - Present
In order to extract better measurements of the magnitudes, or the brightness of the galaxies we observed, I used [_lenstronomy_](https://github.com/sibirrer/lenstronomy) to reconstruct the images of the quasar systems I had.
