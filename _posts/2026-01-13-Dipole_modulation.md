---
title: Forecasts of dipole modulation: local variance asymmetry
description: Papers about the anomaly of hemispherical asymmetry tested with the local variance estimator using future CMB data.
date: 2026-01-13 21:07:00 +0800
categories: [CMB]
tags: [anomaly]     # TAG names should always be lowercase
math: true
---

Dipole modulation, or hemispherical power asymmetry (HPA), was first discovered in *WMAP* temperature data. Subsequently, a power modulation of 7% at a direction around $$(209^\circ, -15^\circ)$$, being consistent between several estimation methods, was found in *Planck* temperature data with a significance approaching $$3\ \sigma$$. In a simplest way, one can calculate the local variance of the temperature map to estimate the dipole modulated in the isotropic CMB signal:
$$
T(\hat n)=\tilde T(\hat n)[1+A\hat\lambda \cdot\hat n]\,,\\
\sigma^2_r(\hat n)=\sum_{i\in\bigodot_r}\big[T(\hat i)-\overline{T}(\hat i)\big]^2\approx\tilde \sigma_r^2(\hat n)[1+2A\hat\lambda \cdot\hat n]\,.
$$
where $$\tilde T$$ is the isotropic CMB, $$A\hat\lambda$$ is the dipole, $$\sigma_r^2$$ is defined as the local variance map, and $i$ includes all pixels within an $$r\gtrsim4^\circ$$ circular area centered at $$\hat n$$.

### Two Forecast Papers

It is still unclear whether the anomalies are simply statistical excursions (unusual but still possible), or due to some new physics. Given that the *Planck* temperature data are almost cosmic-variance limited, we look to the E-mode observations of future CMB experiments. Here are two forecast papers regarding the local variance estimator (LVE) for CLASS and LiteBIRD, respectively.

#### CLASS forecasts

[Testing CMB Anomalies in E-mode Polarization with Current and Future Data](https://arxiv.org/abs/2206.05920)

- They 

#### LiteBIRD forecasts

[LiteBIRD Science Goals and Forecasts. E-mode Anomalies](https://arxiv.org/abs/2508.16451)

- Two simulation sets: unconstrained simulations are isotropic CMB generated from *Planck* 2018 baseline cosmological model (with FFP10 noise simulations added to only temperature maps for consistency); constrained E-mode simulations are generated from the inpainted *Planck* 2018 SMICA temperature maps. (Unconstrained temperature realizations are also inpainted for consistency.) No instrumental noise or foreground residuals are included in E-mode simulations to maximize the detection possibility.

- Mask: E-mode inpainting mask with $$f_{\rm sky}=83.9\%$$ at $$N_{\rm side}=64$$.

- Results: the distributions of the E-mode dipole amplitude derived from the constrained and unconstrained realisations are indiscernible. But the dipole amplitude of local TE covariance, and the angle between TE and T dipole directions are somewhat distinguishable.

- Conclusions: since the temperature dipolar modulation found in the SMICA data is insufficient to result in a statistically significant detection of modulation in the E-mode polarisation, any statistically significant dipolar modulation found therein by LiteBIRD, with an amplitude exceeding $$0.005\ \mu{\rm K}^2$$ would be independent evidence against the ΛCDM cosmological model.

