---
layout: single
title:  "Decomposing a swim with dynamic mode decomposition"
header:
  teaser: "unsplash-gallery-image-2-th.jpg"
categories: 
  - Jekyll
tags:
  - edge case
---


#### Apply DMD
Assume there is a linear transform from 10 timestep to the next.

I.e. $\bm{Y}= \bm{A}\bm{X}$

So we can determine $\bm{A}$ as:

$\bm{A} = \bm{Y}\bm{X^{\dagger}}$

1. Compute SVD of $\bm{X}$

$\bm{X} =\bm{U}\bm{\Sigma}\bm{V^{*}} \rightarrow \bm{Y} = \bm{A}\bm{U}\bm{\Sigma}\bm{V^{*}}$

2.  Compute $\bm{\tilde{A}}$, the porojection of the full matrix A onto U:

$\tilde{\bm{A}} = \bm{U^{*}}\bm{A}\bm{U} = \bm{U^{*}}\bm{Y}\bm{V}\bm{\Sigma^{-1}}$

3. Compute the eigenvalues $\lambda_{i}$ and eigenvectors $w_{i}$ of A:

$\bm{\tilde{A}}\bm{W} = \bm{W}\bm{\Lambda}$

4. Reconstruct the eigendecomposition of A from W and $\Lambda$

$\bm{A}\bm{\Phi} = \bm{\Phi}\bm{\Lambda}$ where $\bm{\Phi} = \bm{Y}\bm{V}\bm{\Sigma^{-1}}\bm{W}$

**Dynamical system**

$x_{i+1} = \bm{A}x_{i}$

$x_{k} = \Phi\Lambda^{k}\Phi^{\dagger}x_{0}$

or in the continuous case:

$x(t) = \bm{\Phi}\bm{\Lambda}^{\frac{t}{\Delta t}}\bm{\Phi ^{\dagger}}x(0)$

Reconstruct:


$\bm{\Psi} =  \bm{\Lambda}^{\frac{t}{\Delta t}} * \bm{\Phi^{-1}} * \bm{X(0)}$

$\bm{X} = \bm{\Phi} * \bm{\Psi}$
