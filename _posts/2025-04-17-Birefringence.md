---
title: Papers of Birefringence Estimation
description: Papers about using MK's method to estimate the isotropic cosmic birefringence angle.
date: 2025-04-17 20:11:00 +0800
categories: [CMB, cosmological parameter estimation]
tags: [birefringence]     # TAG names should always be lowercase
math: true
---

First, the observed EB spectrum (without intrinsic CMB EB correlation) can be expressed as:

$$
C_\ell^{EB,o}=\frac{\tan(4\alpha)}{2}\left({C}_\ell^{EE,o}-{C}_\ell^{BB,o}\right)+\frac{\sin(4\beta)}{2\cos(4\alpha)}\left({C}_\ell^{EE,\rm CMB}b_\ell^2-{C}_\ell^{BB,\rm CMB}b_\ell^2\right)+\frac{A}{\cos(4\alpha)}C_\ell^{EB,\rm fg}\,.
$$

The most commonly used method of estimating the birefringence angle, which we call the MK’s method (firstly introduced by Minami & Komatsu), is a Maximum Likelihood Estimator to simultaneously estimate $$\alpha_\nu$$ for all frequency bands and $$\beta$$ (and the amplitude of fg EB correlations).

One problem is how we model the fg EB spectrum, given that no signal-dominated EB observations are provided by now.

In this blog, we summarize some relevant papers which used this approach to make estimations from real CMB data or forecasts on simulations.

### Papers (in chronological order)

Note that, for each work, there are several points worthy of special notice: How do they model the dust EB spectrum? How do they produce the masks? What free parameters do they fit? What simulations do they use for validation?

#### Three papers from Minami (& Komatsu)

Here we name them as M1, M2, and M3.

1. [Simultaneous determination of the cosmic birefringence and miscalibrated polarisation angles from CMB experiments](https://arxiv.org/abs/1904.12440)
2. [Determination of miscalibrated polarization angles from observed CMB and foreground EB power spectra: Application to partial-sky observation](https://arxiv.org/abs/2002.03572)
3. [Simultaneous determination of the cosmic birefringence and miscalibrated polarization angles II: Including cross frequency spectra](https://arxiv.org/abs/2006.15982). 

- They do not use real CMB data, but simulations to validate the method.
- They use d1s1 model in their sky simulations.
- For the denominator in the likelihood, the variance of $$C_\ell^{EB,o}-({C}_\ell^{EE,o}-{C}_\ell^{BB,o}){\tan(4\alpha)}/{2}$$, M1 uses an approximation including $${C}_\ell^{EE/BB/EB,o}$$. 
<!-- See Physics/USTC2023AUT/birefringence_cov_mat.jpg -->
- M2 uses NaMASTER to estimate the covariance matrices of all pairs of $${C}_\ell^{EE/BB/EB,o}$$. They validate it by comaring with that from MC simulations.
- M3 ignores some of the covariance terms including $${C}_\ell^{EB,o}$$ given the high statistical fluctuations of $${C}_\ell^{EB,o}$$ (e.g. large fluctuations due to the large E-mode foreground, but the fg EB spectrum is not modeled).
- M2 introduces a dust EB spectrum parameterized by a rotation angle $$\gamma$$. To test if the method can determine $$\gamma$$, they prepare a Gaussian dust foreground map with given $${C}_\ell^{EE/BB/EB,fg}$$. They then fit $$\alpha$$ and $$\gamma$$ simultaneously, which successfully recover the input values.
- M1 and M3 both ignore the foreground EB correlation.
- These works do not use simulations of data splits.

#### Planck (& WMAP) results

Here we name them as W1, W2, and W3.

1. [New Extraction of the Cosmic Birefringence from the Planck 2018 Polarization Data](https://arxiv.org/abs/2011.11254)
2. [Cosmic Birefringence from Planck Data Release 4](https://arxiv.org/abs/2201.07682)
3. [Improved Constraints on Cosmic Birefringence from the WMAP and Planck Cosmic Microwave Background Polarization Data](https://arxiv.org/abs/2205.13962)

- W1 uses PR3 half-mission (HM) maps and thus they fit one miscalibration angle $$\alpha_\nu$$ for two HM maps of each frequency. They compute cross spectra $$C_\ell^{EE/BB/EB/BE/...}$$ of 16 pairs ($$\nu$$,HM1)x($$\nu$$,HM2).
- W2/3 use PR4 A/B maps (full-mission, but half of the detector sets on the focal plane). Each split has an independent miscalibration angle. They compute cross spectra of 28 pairs.
- The masks are produced by masking 1) bad pixels that were not observed by any detectors, 2) bright CO emssion regions to reduce T-P leakage due to the bandpass mismatch, 3) point sources from the union of PR2 100/143/217/353 GHz PS masks. Using different Galactic masks, the final fsky ranges from 63% to 93%.
- W1 finds $$\beta=0.35\pm0.14 \deg$$ (68% C.L.) without assuming the fg EB spectrum. They use QuickPol method to remove the T-P leakage (while PR4 corrects it by fitting time-domain templates). They validate by CMB+N FFP10 simulations (they can only estimate $$\alpha_\nu+\beta$$ without fg) with input $$\alpha_\nu=\beta=0$$. They expect to estimate $$\alpha_\nu=0$$ by setting $$\beta=0$$, or vice versa.
- W2/3 both assume a dust EB spectrum model. We hereafter call it the ‘**filament model**’. W3 makes a small change from W2: W3 does not require multiplying a noisy factor $$C_\ell^{EE, \rm dust}/(C_\ell^{EE, \rm dust}-C_\ell^{BB, \rm dust})$$ estimated from 353 GHz. They both fit the frequency-dependent amplitudes $$A_\ell$$ for 4 multipole ranges. Specifically, the dust EB spectrum is modeled as:

$$
C_\ell^{EB, \rm dust}=A_\ell C_\ell^{EE, \rm dust}\sin(4\psi_\ell)\,,
$$

- where

$$
\psi_\ell=\frac{1}{2}\arctan\left(\frac{C_\ell^{TB, \rm dust}}{C_\ell^{TE, \rm dust}}\right)\,.
$$

- Note that the dust EB model is only used for the cross spectra of two dust-dominated channels ($$\nu\gtrsim90$$GHz). If one (or two) of them is a synchrotron-dominated channel we assume the fg EB correlations are negligible.
- They compute the covariance matrices in the same way as M3.

#### Validation works

Here we name it D1.

1. [Robustness of cosmic birefringence measurement against Galactic foreground emission and instrumental systematics](https://arxiv.org/abs/2210.07655)

- This validation work takes *Commander* PR4 sky model as a template for polarized fg to compute the intrinsic fg EB $$A{C}_\ell^{EB,fg}$$, leaving its amplitude $$A$$ to fit. They use Commander SEDs to scale it to other frequencies. (You can also fit different $$A_\nu$$‘s for each band.)
- This approach, called the ‘Commander template’ method, warrants a couple of caveats, since the noise and systematics in the Commander template may lead to a spurious EB signal.
- To speed up the calculation, they first estimate the maximum likelihood solution analytically, applying the small-angle approximation. Then they recalculate the best-fit solution, which converges soon.
- They use NPIPE CMB+N simulations to test the robustness of the method against instrumental systematics (other than miscalibration angles). They use NPIPE CMB+FG+N simulations (where FG adopts the Commander sky model), rotated by randomly sampled $$\alpha_\nu$$ and $$\beta$$, to validate the method.
- They find the systematic effects including cross-polarization (E-B leakage) and beam leakage (T-P leakage) cause the spurious EB signal in CMB+N simulations.
- For a future experiment with a high S/N of E-mode measurements, we might include the auto spectra. But here, to avoid the noise bias in EE auto spectra, we better use cross spectra only. 

#### Forecast works

Here we name it L1.

1. [LiteBIRD Science Goals and Forecasts: constraining isotropic cosmic birefringence](https://arxiv.org/abs/2503.22322)

- The LiteBIRD Forecast work takes the MK’s method as a choice among 5 methods, but with a bit of changes.
- In fg EB spectrum model, they consider both synchrotron and dust, and their correlation. They compute their spectrum from the templates produced by parametric component separation methods (specifically, they use d0s0 and d1s1 models), and fit the amplitudes $$A^{\rm sync/dust/sync\times dust}$$.
- In their simulations, they use d0s0 and d1s1, which means the models that generated the simulations are also used as the templates in the MK estimator.
- They also show a small bias if using the s0 model in MK to apply estimation on simulations of s1, while d0 could well descirbe d1 in terms of its EB correlation.
- The assumptions like the Gaussian likelihood may fall for higher S/N data.
- They use the same semi-analytical method as D1 to estimate the maximum likelihood solution.
