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

Here we name them as M1, M2, and M3.

1. [Simultaneous determination of the cosmic birefringence and miscalibrated polarisation angles from CMB experiments](https://arxiv.org/abs/1904.12440)
2. [Determination of miscalibrated polarization angles from observed CMB and foreground EB power spectra: Application to partial-sky observation](https://arxiv.org/abs/2002.03572)
3. [Simultaneous determination of the cosmic birefringence and miscalibrated polarization angles II: Including cross frequency spectra](https://arxiv.org/abs/2006.15982). 

- They do not use real CMB data, but simulations to validate the method.
- They use d1s1 model in their sky simulations.
- For the denominator in the likelihood, the variance of $$C_\ell^{EB,o}-({C}_\ell^{EE,o}-{C}_\ell^{BB,o}){\tan(4\alpha)}/{2}$$, M1 uses an approximation including $${C}_\ell^{EE/BB/EB,o}$$.
- M2 uses NaMASTER to estimate the covariance matrices of all pairs of $${C}_\ell^{EE/BB/EB,o}$$. They validate it by comaring with that from MC simulations.
- M3 ignores some of the covariance terms including $${C}_\ell^{EB,o}$$ given the high statistical fluctuations of $${C}_\ell^{EB,o}$$ (e.g. large fluctuations due to the large E-mode foreground, but the fg EB spectrum is not modeled).
- M2 introduces a dust EB spectrum parameterized by a rotation angle $$\gamma$$. To test if the method can determine $$\gamma$$, they prepare a Gaussian dust foreground map with given $${C}_\ell^{EE/BB/EB,fg}$$.
- M1 and M3 both ignore the foreground EB correlation.
- These works do not use simulations of data splits.

#### Planck (& WMAP) results

Here we name them as W1, W2, W3, and W4.

1. [New Extraction of the Cosmic Birefringence from the Planck 2018 Polarization Data](https://arxiv.org/abs/2011.11254)
2. [Cosmic Birefringence from Planck Data Release 4](https://arxiv.org/abs/2201.07682)
3. [Improved Constraints on Cosmic Birefringence from the WMAP and Planck Cosmic Microwave Background Polarization Data](https://arxiv.org/abs/2205.13962)
4. [Cosmoglobe DR1 results. II. Constraints on isotropic cosmic birefringence from reprocessed WMAP and Planck LFI data](https://arxiv.org/abs/2305.02268)

- W1 uses PR3 half-mission (HM) maps and thus they fit one miscalibration angle $$\alpha_\nu$$ for two HM maps of each frequency. They compute 16 cross spectra sets $$C_\ell^{EE/BB/EB/BE/...}$$ of ($$\nu$$,HM1)x($$\nu$$,HM2).
- W2/3/4 use PR4 A/B maps (full-mission, but half of the detector sets on the focal plane). Each split has an independent miscalibration angle. They compute cross spectra of 28 pairs.
- The masks are produced by masking 1) bad pixels that were not observed by any detectors 2) bright CO emssion regions to reduce T-P leakage due to the bandpass mismatch 3) point sources from the union of PR2 100/143/217/353 GHz PS masks. Using different Galactic masks, the final fsky ranges from 63% to 93%.
- W1 finds $$\beta=0.35\pm0.14 \deg$$ (68% C.L.) without assuming the dust EB spectrum. They use QuickPol method to remove the T-P leakage (while PR4 corrects it by fitting time-domain templates). They validate by CMB+N FFP10 simulations (they can only estimate $$\alpha_\nu+\beta$$ without fg) with input $$\alpha_\nu=\beta=0$$. They expect to estimate $$\alpha_\nu=0$$ by setting $$\beta=0$$, or vice versa.
- W2/3/4 all assume a dust EB model. W3 makes a small change from W2: W3 does not require multiplying a noisy factor $$C_\ell^{EE, \rm dust}/(C_\ell^{EE, \rm dust}-C_\ell^{BB, \rm dust})$$ estimated from 353 GHz. They all fit the frequency-dependent amplitudes $$A_\ell$$ for 4 multipole ranges.
- They compute the covariance matrices in the same way as M3.

#### Validation works

1. [Robustness of cosmic birefringence measurement against Galactic foreground emission and instrumental systematics](https://arxiv.org/abs/2210.07655)

#### Forecast works

1. [LiteBIRD Science Goals and Forecasts: constraining isotropic cosmic birefringence](https://arxiv.org/abs/2503.22322)
