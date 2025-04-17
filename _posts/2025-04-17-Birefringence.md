---
title: Papers of Birefringence Estimation
description: Papers about using MK's method to estimate the isotropic cosmic birefringence angle.
date: 2025-04-17 20:11:00 +0800
categories: [CMB, cosmological parameter estimation]
tags: [birefringence]     # TAG names should always be lowercase
math: true
---

### Papers (in chronological order)

Note that, for each work, there are several points worthy of special notice: How do they model the dust EB spectrum? What masks do they use for Planck PR4 maps? What parameters do they fit? Do they assume same or different miscalibration angle for each band? What simulations do they use for validation?

#### Three papers from Minami (& Komatsu)

Here we name them as W1, W2, and W3.

1. [Simultaneous determination of the cosmic birefringence and miscalibrated polarisation angles from CMB experiments](https://arxiv.org/abs/1904.12440)
2. [Determination of miscalibrated polarization angles from observed CMB and foreground EB power spectra: Application to partial-sky observation](https://arxiv.org/abs/2002.03572)
3. [Simultaneous determination of the cosmic birefringence and miscalibrated polarization angles II: Including cross frequency spectra](https://arxiv.org/abs/2006.15982). 

- They do not use real CMB data, but simulations to validate the method.
- They use d1s1 model in their sky simulations.
- For the denominator in the likelihood, the variance of $$C_\ell^{EB,o}-({C}_\ell^{EE,o}-{C}_\ell^{BB,o}){\tan(4\alpha)}/{2}$$, W1 uses an approximation including $${C}_\ell^{EE/BB/EB,o}$$.
- W2 uses NaMASTER to estimate the covariance matrices of all pairs of $${C}_\ell^{EE/BB/EB,o}$$. They validate it by comaring with that from MC simulations.
- W3 ignores some of the covariance terms including $${C}_\ell^{EB,o}$$ given the high statistical fluctuations of $${C}_\ell^{EB,o}$$ (e.g. large fluctuations due to the large E-mode foreground, but the fg EB spectrum is not modeled).
- W2 introduces a dust EB spectrum parameterized by a rotation angle $$\gamma$$. To test if the method can determine $$\gamma$$, they prepare a Gaussian dust foreground map with given $${C}_\ell^{EE/BB/EB,fg}$$.
- W1 and W3 both ignore the foreground EB correlation.
- These works do not use simulations of data splits.


#### WMAP or Planck results

1. [New Extraction of the Cosmic Birefringence from the Planck 2018 Polarization Data](https://arxiv.org/abs/2011.11254)
2. [Cosmic Birefringence from Planck Data Release 4](https://arxiv.org/abs/2201.07682)
3. [Improved Constraints on Cosmic Birefringence from the WMAP and Planck Cosmic Microwave Background Polarization Data](https://arxiv.org/abs/2205.13962)
4. [Cosmoglobe DR1 results. II. Constraints on isotropic cosmic birefringence from reprocessed WMAP and Planck LFI data](https://arxiv.org/abs/2305.02268)

#### Forecast works

1. [LiteBIRD Science Goals and Forecasts: constraining isotropic cosmic birefringence](LiteBIRD Science Goals and Forecasts: constraining isotropic cosmic birefringence)
