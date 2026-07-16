---
permalink: /research/
title: "Research"
layout: archive
author_profile: true

---

My research insterest lies broadly in Stochastic approximation, Computational algorithms in optimization, Monte Carlo methods, Statistical machine learning, Reinforcement learning, and Bayesian computation

- **Zero-Order Langevin Monte Carlo via SPSA under Noisy Function Measurements** Jan 2025--Present
  - <span style="font-weight:bold; text-decoration:underline;">Hongbo Li</span>, James C. Spall, *Zeroth-Order Langevin Monte Carlo via SPSA under Noisy Function Measurements.*  
Journal manuscript in final preparation.
  - <span style="font-weight:bold; text-decoration:underline;">Hongbo Li</span>, James C. Spall, *Zeroth-Order Langevin Sampling for Bayesian Applications.*  
Manuscript under review, 2026.
  - Supervised by Prof. James Spall, Johns Hopkins University
<div style="margin-left:20px; text-align:center;">
  <figure style="display:inline-block; margin:10px; width:45%; max-width:520px; text-align:center;">
    <img src="/images/jan 24,roy-spsa 1.png" style="width:100%; height:auto; display:block; margin:auto;"/>
  </figure>

  <figure style="display:inline-block; margin:10px; width:45%; max-width:520px; text-align:center;">
    <img src="/images/Jan 24 roy-spsa 3.png" style="width:100%; height:auto; display:block; margin:auto;"/>
  </figure>
  
  <figure style="display:inline-block; margin:10px; width:45%; max-width:520px; text-align:center;">
    <img src="/images/jan 24 average simulation.png" style="width:100%; height:auto; display:block; margin:auto;"/>
  </figure>
</div>
  - **Motivation & method:** Bridged gradient-based samplers and gradient-inaccessible settings in practice (simulation- based inference, model-free reinforcement learning, and stochastic control) by proposing Langevin Monte Carlo-Simultaneous Perturbation Stochastic Approximation (LMC-SPSA) in noisy settings-gradient-free Langevin sampler with only two noisy function queries per iteration (dimension-independent)
  
**Theoretical development:** 
  - **Convergence:** Proved Wasserstein-2 convergence of LMC-SPSA under noise and resolved open step size question by deriving diminishing-step size window ensuring convergence, extending prior constant-step size analysis
  - **Sharper dimension dependence:** IImproved theoretical dominant dimension dependence of the Wasserstein-2 error bound from quartic to quadratic, with numerical results supporting the theoretical scaling
  - **Sharper oracle complexity:** Reduced theoretical noisy-oracle complexity needed to reach target Wasserstein accuracy relative to Roy et al.’s zeroth-order LMC method (Bernoulli, 2022), improving accuracy dependence from fourth order to second order.
  - **Theory-guided shrinking schedule:** Derived coupled diminishing step-size and perturbation schedules that balance Langevin discretization error, SPSA bias, and residual error terms, giving practical tuning rules for LMC-SPSA.
  - **Budget-matched numerical validation:** Conducted oracle-call-matched experiments against LMC-Finite Difference Stochastic Approximation and Roy et al.’s zeroth-order LMC, showing that LMC-SPSA attains lower and more stable MSE and higher-order moment errors under fixed function-evaluation budgets.
  
**Bayesian applications and empirical evaluation:** 
  - **Black-box Bayesian sampling:** Adapted LMC-SPSA to black-box Bayesian posterior sampling settings where gradients are unavailable and only posterior-density evaluations are accessible.
  - **Empirical comparison:** Designed fixed-budget experiments on Bayesian classification on MNIST 3-vs-8 and Bayesian regression on UCI Energy Efficiency data set, showing that LMC-SPSA outperforms random-walk Metropolis-Hastings and diagonal adaptive Metropolis under matched posterior-density evaluation budgets.


---
- **Downstream Adversarial Robustness of Frozen Foundation Models** Jan 2026--May 2026
  - Supervised by Prof. Yue Xing and Prof. Young-geun Kim, Michigan State University
  - **Motivation & method:** Investigated whether label-free robust preprocessing and generated training data can improve downstream adversarial robustness in frozen foundation-model pipelines without full model fine-tuning.
  - **Synthetic-data evaluation pipeline:** Extended CIFAR-10 pipelines to support DDPM/DDIM synthetic data and synthetic-real mixtures across preprocessor training, linear-head training, and PGD-based robustness evaluation.
  - **Synthetic data quality analysis:** Designed CIFAR-10 ablation studies with DDPM/DDIM-generated datasets of varying quality, showing that higher complementarity, coverage, and Inception Score, together with lower FID, are positively associated with downstream robust accuracy, and identified an intermediate synthetic-real mixing ratio that outperforms fully real or fully synthetic data.
  - **Wasserstein proof refinement:** Refined the downstream adversarial-loss proof by reducing the conditional Wasserstein term to clean–adversarial encoder displacement under deterministic-Dirac representations, and derived a lower-bound interpretation via optimal transport between aggregated latent distributions.


---

- **Fine-tuning FinBERT with Few-Shot Weak Supervision for Financial News Sentiment** Aug 2024--Feb 2025
  - Supervised by Prof. Helyette Geman, Johns Hopkins University
<div style="margin-left:20px; text-align:center;">
  <figure style="display:inline-block; margin:10px; width:45%; max-width:520px; text-align:center;">
    <img src="/images/finbert.jpg" style="width:100%; height:auto; display:block; margin:auto;"/>
  </figure>
</div>
  - **Motivation & method:** Applied few-shot in-context labeling with gold examples to generate weak labels at scale, using consistency voting and confidence filtering for denoising; then fine-tuned FinBERT (LoRA) with temporal splits and probability calibration. The fine-tuned model outperformed the baseline FinBERT in accuracy
  - **Multi-ticker disambiguation:** Designed three datasets for multi-ticker articles (single-ticker, most-mentioned, and mention-share weighting); most-mentioned gave the highest accuracy and strongest 2-day Granger-prediction
  - **Exploratory identification:** Applied Difference-in-Differences around pre-specified shocks and Regression Discontinuity Design at set thresholds, uncovering potential causality between sentiment factors and stock returns


---

- **Causal Inference on High-Dimensional Time Series using LLM-Guided Discovery** 10/24-2/25
  - Supervised by Prof. Helyette Geman, Johns Hopkins University
  - Developed novel framework leveraging causal order priors generated by LLMs to constrain discovery algorithms, enabling efficient learning of sparse structures and mitigating the curse of dimensionality
  - Designed and implemented soft constraints, conflict checks, and multi-round prompting, to minimize impact of spurious directions from imperfect LLM outputs, ensuring robustness and reliability of the inferred graphs


---
