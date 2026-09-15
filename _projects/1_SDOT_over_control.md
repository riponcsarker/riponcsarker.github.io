---
layout: page
title: Control Laguerre Tessellation
description: Semi-discrete Optimal Transport Over Control Systems
img: assets/img/projects/clt/clt_cover.png
importance: 1
category: research
related_publications: true
---

This research investigates **semi-discrete optimal transport (SDOT)** when the ground cost is induced by the optimal motion of controlled dynamical systems.

In classical SDOT, transport costs are commonly defined using geometric distances such as the squared Euclidean distance. In this work, we extend the framework to situations where the transportation cost is determined by an **optimal control problem**, such as minimum-energy or minimum-time motion.

The resulting partition of the state space is called a **Control Laguerre Tessellation (CLT)**.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid
           loading="eager"
           path="assets/img/CLT_background.png"
           title="Control Laguerre Tessellation"
           class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
Control Laguerre Tessellation for semi-discrete optimal transport over controlled dynamical systems.
</div>


## Research Objective

The objective of this work is to extend semi-discrete optimal transport to systems in which transporting an agent from an initial state $x$ to a target state $y_i$ requires solving an optimal control problem.

The transport problem is

$$
\min_{T_{\sharp}\mu=\nu}
\int_{\mathcal{X}} c(x,T(x))\,d\mu(x).
$$

where the ground cost $c(x,y_i)$ represents the optimal cost of steering a controlled dynamical system from $x$ to $y_i$.

Instead of defining cells only from geometric distance, the state space is partitioned according to

$$
\operatorname{Lag}_i(\psi)
=
\left\{
x\in\mathcal{X}
\;\middle|\;
c(x,y_i)+\psi_i
\leq
c(x,y_j)+\psi_j,
\quad \forall j\neq i
\right\}.
$$

These generalized Laguerre cells form the **Control Laguerre Tessellation**.

## Main Contributions

- Formulation of semi-discrete optimal transport with **optimal-control-induced ground costs**.
- Development of the **Control Laguerre Tessellation** framework.
- Characterization of the optimal transport map using generalized Laguerre cells.
- Analysis of **minimum-energy transport** for linear control systems.
- Analysis of **minimum-time transport** in the presence of an exogenous vector field.
- Numerical construction of the resulting tessellations.


<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid
           path="assets/img/projects/clt/min_energy.png"
           title="Minimum-energy Control Laguerre Tessellation"
           class="img-fluid rounded z-depth-1" %}
    </div>

    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid
           path="assets/img/projects/clt/min_time.png"
           title="Minimum-time Control Laguerre Tessellation"
           class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
Examples of Control Laguerre Tessellations generated using optimal-control-induced transport costs.
</div>


## Why This Matters

Classical optimal transport typically measures transportation effort using geometric distance.

In many engineering systems, however, the true cost of moving between two states depends on the system dynamics, actuator constraints, energy consumption, environmental disturbances, and other control-related factors.

Control Laguerre Tessellation allows these effects to be incorporated directly into the geometry of the optimal transport partition.

Potential applications include:

- Multi-robot coordination
- Robotic coverage control
- Resource allocation
- Micro-assembly
- Targeted drug delivery


## Publication

This work is available as:

{% cite sarker2026clt %}

**Ripon C. Sarker and Abhishek Halder**  
*Control Laguerre Tessellation: Semi-discrete Optimal Transport Over Control Systems*

[arXiv](https://arxiv.org/abs/2607.09139){:target="_blank"}
&nbsp;&nbsp;
[PDF](https://arxiv.org/pdf/2607.09139){:target="_blank"}
