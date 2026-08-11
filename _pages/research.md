---
permalink: /research/
title: "Research"
layout: archive
author_profile: true

---

My research insterest lies broadly in Stochastic approximation, Computational algorithms in optimization, Monte Carlo methods, Statistical machine learning, Reinforcement learning, and Bayesian computation

### Zeroth-Order Langevin Monte Carlo via SPSA under Noisy Function Measurements  
*Jan 2025–Present*  
Supervised by Prof. James C. Spall, Johns Hopkins University

**Publications and manuscripts**
- <span style="font-weight:bold; text-decoration:underline;">Hongbo Li</span>, James C. Spall.  
  *Zeroth-Order Langevin Monte Carlo via SPSA under Noisy Function Measurements.*
  Preprint, arXiv:2608.07837, 2026. https://arxiv.org/abs/2608.07837.
  Journal manuscript in final preparation.

- <span style="font-weight:bold; text-decoration:underline;">Hongbo Li</span>, James C. Spall. 
  *Zeroth-Order Langevin Sampling for Bayesian Applications.*  
  Accepted at the 4th IEEE International Conference on Artificial Intelligence, Blockchain and Internet of Things (AIBThings), 2026.
  
**Motivation & method:** Bridged gradient-based samplers and gradient-inaccessible settings in practice (simulation- based inference, model-free reinforcement learning, and stochastic control) by proposing Langevin Monte Carlo-Simultaneous Perturbation Stochastic Approximation (LMC-SPSA) in noisy settings-gradient-free Langevin sampler with only two noisy function queries per iteration (dimension-independent)
<div style="margin-left:20px; text-align:center;">
  <figure style="display:inline-block; margin:10px; width:90%; max-width:520px; text-align:center;">
    <img src="/images/feb-22-msebig.png" style="width:100%; height:auto; display:block; margin:auto;"/>
  </figure>
 
  <figure style="display:inline-block; margin:10px; width:45%; max-width:520px; text-align:center;">
    <img src="/images/energy_poly_regression_rmse_curve_density_label.png" style="width:100%; height:auto; display:block; margin:auto;"/>
  </figure>

  <figure style="display:inline-block; margin:10px; width:45%; max-width:520px; text-align:center;">
    <img src="/images/mnist_logistic_nll_curve_density_label.png" style="width:100%; height:auto; display:block; margin:auto;"/>
  </figure>
</div>
<div class="figure-grid">
  <figure class="figure-main">
    <img src="/images/feb-22-msebig.png" alt="MSE comparison">
  </figure>

  <figure>
    <img src="/images/energy_poly_regression_rmse_curve_density_label.png"
         alt="Energy regression RMSE">
  </figure>

  <figure>
    <img src="/images/mnist_logistic_nll_curve_density_label.png"
         alt="MNIST logistic regression NLL">
  </figure>
</div>

<style>
.figure-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 20px;
  width: 90%;
  max-width: 1080px;
  margin: 20px auto;
}

.figure-grid figure {
  margin: 0;
  text-align: center;
}

.figure-grid .figure-main {
  grid-column: 1 / -1;
  width: 75%;
  justify-self: center;
}

.figure-grid img {
  display: block;
  width: 100%;
  height: auto;
}
**Theoretical development**
- **Convergence:** Proved Wasserstein-2 convergence of LMC-SPSA under noise and derived diminishing step-size schedules ensuring convergence.
- **Sharper dimension dependence:** Improved dominant dimension dependence of the Wasserstein-2 error bound from quartic to quadratic.
- **Sharper oracle complexity:** Reduced noisy-oracle complexity relative to Roy et al.’s zeroth-order LMC method (Bernoulli, 2022), improving accuracy dependence from fourth order to second order.
- **Theory-guided shrinking schedule:** Derived coupled diminishing step-size and perturbation schedules, giving practical tuning rules for LMC-SPSA.
- **Budget-matched numerical validation:** Conducted oracle-call-matched experiments showing lower and more stable sampling errors.

**Bayesian applications and empirical evaluation**
- **Black-box Bayesian sampling:** Adapted LMC-SPSA to posterior sampling settings where gradients are unavailable and only posterior-density evaluations are accessible.
- **Empirical evaluation:** Designed fixed-budget experiments on Bayesian MNIST 3-vs-8 classification and UCI Energy Efficiency regression, showing stronger predictive performance than random-walk Metropolis-Hastings and diagonal adaptive Metropolis.

---
### Downstream Adversarial Robustness of Frozen Foundation Models  
*Jan 2026–May 2026*  
Supervised by Prof. Yue Xing and Prof. Young-geun Kim, Michigan State University

**Publications and manuscripts**
- Meiqi Liu, Zhuoqun Huang, <span style="font-weight:bold; text-decoration:underline;" >Hongbo Li</span>, Young-geun Kim, and Yue Xing. 
  *How to Enhance Downstream Adversarial Robustness (Almost) Without Touching the Pre-trained Foundation Model?*  
  Manuscript in preparation.

**Motivation & method:** Investigated whether label-free robust preprocessing and generated training data can improve downstream adversarial robustness in frozen foundation-model pipelines without full model fine-tuning.
- **Synthetic-data evaluation pipeline:** Extended CIFAR-10 pipelines to support DDPM/DDIM synthetic data and synthetic-real mixtures across preprocessor training, linear-head training, and PGD-based robustness evaluation.
- **Synthetic data quality analysis:** Designed CIFAR-10 ablation studies with DDPM/DDIM-generated datasets of varying quality, showing that synthetic data quality correlates with downstream robust accuracy, and identified an intermediate synthetic-real mixing ratio that outperforms fully real data.
- **Wasserstein proof refinement:** Refined the downstream adversarial-loss proof by reducing the conditional Wasserstein term to clean–adversarial encoder displacement, and derived a lower-bound interpretation via optimal transport between aggregated latent distributions.
  
---
### Additional Research Project
### Fine-tuning FinBERT with Few-Shot Weak Supervision for Financial News Sentiment
*Aug 2024--Feb 2025*  
Supervised by Prof. Helyette Geman, Johns Hopkins University
<div style="margin-left:20px; text-align:center;">
  <figure style="display:inline-block; margin:10px; width:45%; max-width:520px; text-align:center;">
    <img src="/images/finbert.jpg" style="width:100%; height:auto; display:block; margin:auto;"/>
  </figure>
</div>
- **Motivation & method:** Applied few-shot in-context labeling with gold examples to generate weak labels at scale, using consistency voting and confidence filtering for denoising; then fine-tuned FinBERT (LoRA) with temporal splits and probability calibration. The fine-tuned model outperformed the baseline FinBERT in accuracy
- **Multi-ticker disambiguation:** Designed three datasets for multi-ticker articles (single-ticker, most-mentioned, and mention-share weighting); most-mentioned gave the highest accuracy and strongest 2-day Granger-prediction
