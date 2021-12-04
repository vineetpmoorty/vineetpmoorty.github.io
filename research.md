---
permalink: /research/
title: Research
layout: default
---
Here I write about a few of my important research projects.

Contents:

1. [Size dependence of anomalous Hall effect in type-II superconductors](#superconductivity-proj)
2. [Modelling and simulation of a pressure-imaging hybrid nanoscale device](#magnetostriction-proj)
3. [GPU-accelerated implementation of spectral feature selection algorithm for unsupervised learning](#ml-proj)


<a name="superconductivity-proj">
</a>
### Size dependence of anomalous Hall effect in type-II superconductors

**Publication**: [1] <ins>V. Punyamoorty</ins>, A. Malusare, S. Sengupta, S. Pujari and K. Saha, “Size dependence in flux-flow Hall effect using time-dependent Ginzburg-Landau equations”, Physical Review
Research **3**, 033144 (Aug 2021) ([**URL**](https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.3.033144) | [**arXiv**](https://arxiv.org/abs/2102.02467))

Anomalous Hall effect refers to the sign-change of Hall voltage in a type-II superconductor when the magnetic field is swept. First observed in the 1970s, there exist multiple competing theories today, seeking to explain what is responsible for the sign reversal. In this study, we numerically simulate modified time dependent Ginzburg-Landau (TDGL) equations that describe a superconductor, to study the Hall effect. We are especially interested in mesoscopic samples, where each dimension is of the order of coherence length. We find a novel relationship between the size of a mesoscopic superconductor and its Hall behavior, arising from vastly different magnetic vortex flow dynamics. Visualization of the vortex dynamics resulting from the simulation gives us a novel picture of the precise transient vortex flow responsible for the sign change.

<table style="margin-left:auto;margin-right:auto;width:90%">
<tr>
<td width="60%"><img src="/imgs/hall_expt_ybco.png" width="100%"></td><td><img src="/imgs/vortex_simulated.png" width="100%"></td>
</tr>
<tr>
<td>Fig: Anomalous Hall effect in YBCO (Source: <a href="https://journals.aps.org/prb/abstract/10.1103/PhysRevB.41.11630">Hagen et al.</a>)</td><td>Fig: Simulation of magnetic vortices (Source: <a href="https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.3.033144">V. Punyamoorty et al. [1]</a>)</td>
</tr>
</table>

We build on the original TDGL equations and incorporate additional frameworks to (a) couple an externally applied current, (b) introduce normal state Hall effect by adding transverse conductivity and most importantly, (c) introduce flux-flow Hall effect, which is primarily responsible for the sign-change behavior. These additions entail a significant deviation from the original TDGL equations, and require the implementation of metal-superconductor boundary conditions, along with the original vacuum-superconductor BCs.



<a name="magnetostriction-proj">
</a>
magnetostriction<br>
Lots of text<br>
Lots of text<br>
Lots of text<br>
Lots of text<br>
Lots of text<br>
Lots of text<br>
Lots of text<br>
Lots of text<br>
Lots of text<br>

<a name="ml-proj">
</a>
