---
title:  "Diffilqrax: Differentiable optimal control package published on github"
date: 2024-12-18
permalink: /posts/2024/12/blog-diffilqrax/
tags:
  - Differentiable iLQR
  - Optimal control
  - Code
  - Jaxx
---

![Diffilqrax](/images/diffilqrax/diffilqrax_logo_dm.png "Jax-based python package implementing fully differentiable iLQR algorithm, used for optimal control and neural networks.")

<!-- <div style="text-align: center;">
  <img src="/images/diffilqrax/diffilqrax_logo_dm.png" alt="Mode evolution" width="250"/>
</div> -->

## What is DiffiLQRax?

During my PhD, I developed DiffiLQRax – an open source Python package that provides a differentiable implementation of the iterative Linear Quadratic Regulator (iLQR) algorithm using the JAX library. The goal of this library bridges the gap between classical optimal control theory and modern machine learning frameworks, enabling researchers and engineers to solve complex control problems with the power of automatic differentiation.

Given the package is built in JAX, it adopts automatic differentiation  features making the iLQR solver fully differentiable. This opens up possibilities for gradient-based optimization of control policies and integration with neural networks.

## Key Features and Implementation

DiffiLQRax offers several compelling features that make it stand out:

### Core Algorithms

* Linear Quadratic Regulator (LQR): For linear systems with quadratic costs
* Iterative LQR (iLQR): Extends LQR to handle nonlinear dynamics through iterative linearization
* Full JAX Integration: Built on JAX for automatic differentiation, JIT compilation, and GPU acceleration

### Practical Examples

The library comes with a rich set of examples that demonstrate its capabilities:

* Basic LQR Control: LQR optimal control of integrator dynamics
* Tracking Problems: LQR tracking optimal control of integrator dynamics
* Nonlinear Systems: iLQR solver for simple pendulum
* Comparative Analysis: iLQR Optimal Control compared with Gradient Descent
* Advanced Techniques: iLQR solver Implicit vs. Direct gradients

## Getting Started

Installation is straightforward with pip:

```bash
pip install diffilqrax
```
Or for development:

```bash
git clone git@github.com:ThomasMullen/diffilqrax.git
cd diffilqrax
python -m build
pip install -e .
```

---

*DiffiLQRax is actively maintained and welcomes community contributions. Visit the [documentation](https://diffilqrax.readthedocs.io/) to explore examples and get started with your own optimal control projects.*