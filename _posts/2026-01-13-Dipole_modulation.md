---
title: Forecasts of dipole modulation --- local variance asymmetry
description: Papers about the anomaly of hemispherical asymmetry tested with the local variance estimator using future CMB data.
date: 2026-01-13 21:07:00 +0800
categories: [CMB]
tags: [anomaly]     # TAG names should always be lowercase
math: true
---

Dipole modulation, or hemispherical power asymmetry (HPA), was first discovered in *WMAP* temperature data. Subsequently, a power modulation of 7% at a direction around $$(209^\circ, -15^\circ)$$, being consistent between several estimation methods, was found in *Planck* temperature data with a significance approaching $$3\ \sigma$$. In a simplest way, one can calculate the local variance of the temperature map to estimate the dipole modulated in the isotropic CMB signal:
$$
T(\hat n)=\tilde T(\hat n)[1+A\hat\lambda \cdot\hat n]\,,\\
\sigma^2_r(\hat n)=\frac{1}{N_{i}}\sum_{i\in\bigodot_r}\big[T(\hat i)-\overline{T}(\hat i)\big]^2\approx\tilde \sigma_r^2(\hat n)[1+2A\hat\lambda \cdot\hat n]\,,
$$
where $$\tilde T$$ is the isotropic CMB, $$A\hat\lambda$$ is the dipole, $$\sigma_r^2$$ is defined as the local variance map (LVM), and $i$ includes all pixels within an $$r\gtrsim4^\circ$$ circular area centered at $$\hat n$$.

### Two Forecast Papers

It is still unclear whether the anomalies are simply statistical excursions (unusual but still possible), or due to some new physics. Given that the *Planck* temperature data are almost cosmic-variance limited, we look to the E-mode observations of future CMB experiments. Here are two forecast papers regarding the local variance estimator (LVE) for CLASS and LiteBIRD, respectively.

#### CLASS forecasts

[Shi et al. 2023](https://arxiv.org/abs/2206.05920)

- Simulations: CMB realizations from *Planck* best-fit ΛCDM model plus $$15\ \mu{\rm K}\cdot{\rm arcmin}$$ white noise. Ideal case: full-sky analyses with $$2\ \mu{\rm K}\cdot{\rm arcmin}$$ white noise for temperature and $0.02\ \mu{\rm K}\cdot{\rm arcmin}$ white noise for polarization. Special CMB: one CMB realization with PTEs of all E-mode anomaly estimators are over 95% or below 5%, to distinguish the CMB’s and noise’s contribution to the distributions. Constrained universe: sample E/B components from full-sky *Planck* SMICA data.
- Mask: *Planck* common mask combined with CLASS survey region of $$-70^\circ<{\rm DEC}<30^\circ$$. The E-mode mask is derived from the Q/U polarization mask by thresholding E/B residuals to reduce E/B mixing error due to masking.
- Results: we estimate dipole from [the Special CMB LVM dipole + LVM of isotropic CMB+noise simulations] to simulate the anomaly case. As expected, the distribution of the estimated dipole directions centers well at the Special CMB dipole (input dipole) direction. We then inserted dipoles with different directions (aligned with $$N_{\rm side}=4$$ pixels) and the amplitude of the Special CMB, to investigate the impacts of the mask shape. We found the fitted dipole directions are more concentrated for the input dipoles aligned with masked pixels (i.e., dipoles within the mask or outside the survey footprint) for CLASS and LiteBIRD. This is because when the true dipole is masked, its gradient is mostly unmasked and the fitting is more effective. For *Planck*, the fitted dipoles are more concentrated for dipoles aligned with the high-noise regions of *Planck* data. The results for the constrained universe are largely consistent with those for the unconstrained ones.
- Conclusions: the current SMICA-based constraints are noise dominated for E-mode hemispherical power asymmetry, but the situation will improve with future CLASS (LiteBIRD) data by a factor of 2 (3). The localization of the variance dipole estimated from the Special CMB improves from 30% ($$1\sigma$$) of the sky for *Planck* to 15% for CLASS. The localization depends on both the dipole amplitude and orientation with respect to masks and high-noise regions.

#### LiteBIRD forecasts

[Banday et al. 2025](https://arxiv.org/abs/2508.16451)

- Two simulation sets: unconstrained simulations are isotropic CMB generated from *Planck* 2018 baseline ΛCDM model (with FFP10 noise simulations added to only temperature maps for consistency); constrained E-mode simulations are generated from the inpainted *Planck* 2018 SMICA temperature maps. (Unconstrained temperature realizations are also inpainted for consistency.) No instrumental noise or foreground residuals are included in E-mode simulations to maximize the detection possibility.

- Mask: E-mode inpainting mask with $$f_{\rm sky}=83.9\%$$ at $$N_{\rm side}=64$$.

- Results: the distributions of the E-mode dipole amplitude derived from the constrained and unconstrained realisations are indiscernible. But the dipole amplitude of local TE covariance, and the angle between TE and T dipole directions are somewhat distinguishable.

- Conclusions: since the temperature dipolar modulation found in the SMICA data is insufficient to result in a statistically significant detection of modulation in the E-mode polarisation, any statistically significant dipolar modulation found therein by LiteBIRD, with an amplitude exceeding $$0.005\ \mu{\rm K}^2$$ would be independent evidence against the ΛCDM cosmological model.

