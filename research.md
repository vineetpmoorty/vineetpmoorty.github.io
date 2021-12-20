---
permalink: /research/
title: Research
layout: default
order: 2
---
Here I write about a few of my important research projects.

Contents:

1. [Size dependence of anomalous Hall effect in type-II superconductors](#superconductivity-proj)
2. [Modelling and simulation of a pressure-imaging hybrid nanoscale device](#magnetostriction-proj)
3. [GPU-accelerated implementation of spectral feature selection algorithm for unsupervised learning](#ml-proj)


<a name="superconductivity-proj">
</a>
## Size dependence of anomalous Hall effect in type-II superconductors

**Publication**: [1] <ins>V. Punyamoorty</ins>, A. Malusare, S. Sengupta, S. Pujari and K. Saha, “Size dependence in flux-flow Hall effect using time-dependent Ginzburg-Landau equations”, Physical Review
Research **3**, 033144 (Aug 2021) ([**URL**](https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.3.033144) | [**arXiv**](https://arxiv.org/abs/2102.02467))

Anomalous Hall effect refers to the sign-change of Hall voltage in a type-II superconductor when the magnetic field is swept. First observed in the 1970s, there exist multiple competing theories today, seeking to explain what is responsible for the sign reversal. In this study, we numerically simulate modified time dependent Ginzburg-Landau (TDGL) equations that describe a superconductor, to study the Hall effect. We find a novel relationship between the size of a mesoscopic superconductor and its Hall behavior, arising from vastly different magnetic vortex flow dynamics. Induced electric field transients resulting from the simulation give us a novel picture of the precise dynamic vortex flow responsible for the sign change (Figs. 3, 4).

<table style="margin-left:auto;margin-right:auto;width:90%">
<tr>
<td width="60%"><img src="/imgs/hall_expt_ybco.png" width="100%"></td><td><img src="/imgs/vortex_simulated.png" width="90%"></td>
</tr>
<tr>
<td>Fig 1: Anomalous Hall effect in YBCO (Source: <a href="https://journals.aps.org/prb/abstract/10.1103/PhysRevB.41.11630">Hagen et al.</a>)</td><td>Fig 2: Simulation of magnetic vortices (Source: <a href="https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.3.033144">V. Punyamoorty et al. [1]</a>)</td>
</tr>
</table>

We build on the original TDGL equations and incorporate additional frameworks to (a) couple an externally applied current, (b) introduce normal state Hall effect by adding transverse conductivity and most importantly, (c) introduce flux-flow Hall effect, which is primarily responsible for the sign-change behavior. These additions entail a significant deviation from the original TDGL equations, and require the implementation of metal-superconductor boundary conditions, along with the original vacuum-superconductor BCs.

We find that at mesoscopic sizes, vortex flow dynamics are influenced greatly by the boundary, which in turn influence the induced electric Hall field. We obtain further insight from the transient induced electric fields and find that anomalous sign-change behavior is caused predominantly by the vortex flow occurring during the onset of normal state, rather than vortex flow itself.

<table style="margin-left:auto;margin-right:auto;width:90%">
<tr>
<td width="50%"><img src="/imgs/vortex_flow.png" width="100%"></td><td><img src="/imgs/field_transient.png" width="100%"></td>
</tr>
<tr>
<td>Fig 3: Vortex flow dynamics during the onset of normal state is predominantly responsible for anomalous Hall effect (Source: <a href="https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.3.033144">V. Punyamoorty et al. [1]</a>)</td><td>Fig 4: Resulting Hall field transient, when Hall effect is anomalous (red line) (Source: <a href="https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.3.033144">V. Punyamoorty et al. [1]</a>)</td>
</tr>
</table>

<a name="magnetostriction-proj">
</a>
## Modelling and simulation of a pressure-imaging hybrid nanoscale device

**Publication**: [2] <ins>V. Punyamoorty</ins>, S. Dasika and K. Saha “Modelling of Magnetostriction for Stress-Imaging via Nitrogen Vacancy Centers in Diamond”, 2019 IEEE Research and Applications of Photonics in Defense Conference (RAPID) (19 - 21 Aug 2019, Miramar Beach, FL, USA) ([**URL**](https://ieeexplore.ieee.org/document/8864357))

Acoustic pressure imaging has numerous applications in medicine, defence and other miscellaneous sensing applications. Nitrogen vacancy centers in diamond have emerged as an effective quantum system for highly sensitive magnetometry and quantum computing. NV centers also exhibit a direct coupling to pressure, but poor sensitivity prohibits measurements in the sub-MPa range. Cai et al. (HYPERLINK!) proposed a hybrid device consisting of a magnetostrictive layer on top of a diamond substrate consisting of NV centers. Magnetostriction refers to the transduction of changes in pressure to changes in magnetic fields. Due to the high sensitivity of NV center magnetometry (nT regime), this device promises to be highly sensitive for pressure imaging.

<table style="margin-left:auto;margin-right:auto;width:90%">
<tr>
<td width="57.5%"><img src="/imgs/hybrid_device.png" width="100%"></td><td><img src="/imgs/energy_surface_diagram.png" width="100%"></td>
</tr>
<tr>
<td>Fig 1: Hybrid device for pressure imaging, consisting of a magnetostrictive Terfenol-D layer and diamond with NV centers  (Source: <a href="https://ieeexplore.ieee.org/document/8864357">V. Punyamoorty et al. [2]</a>)</td><td>Fig 2: Numerical simulation of magnetostriction profile, by computing the energy surface diagram in 3D. (Source: <a href="https://ieeexplore.ieee.org/document/8864357">V. Punyamoorty et al. [2]</a>)</td>
</tr>
</table>

First, we model and numerically simulate the magnetostriction profile of a Terfenol-D thin film, using anisotropic domain rotation model. This provides crucial information on the transduction profile of the film, which would help in reconstruction of pressure, from the measured magnetic field profile. This would also inform us about the linearity of this transduction, and any limits on this linearity. We find that under the domain rotation model, transduction is linear and highly localized in space, enabling us to reconstruct the pressure.

Secondly, it is important to note that the aforementioned model only provides the magnetization of the Terfenol-D layer. This would be different from the magnetic field sensed by the NV centers, at a finite distance away. Thus, we consider a sample pressure profile, compute the resulting magnetization, and further the resulting magnetic field at <em>d</em> distance away (where <em>d</em> is the NV center depth). We observe the <em>reconstructability</em> of pressure, as a function of <em>d</em>, and notice that NV center depth highly influences the reconstructability of pressure profile (Fig. 4).

<table style="margin-left:auto;margin-right:auto;width:90%">
<tr>
<td width="54%"><img src="/imgs/field_at_distance.png" width="100%"></td><td><img src="/imgs/error_profile.png" width="100%"></td>
</tr>
<tr>
<td>Fig 3: Field as sensed by the NV centers at <em>d</em> distance away. At 100 nm, it can be seen that reconstructability of pressure deteriorates significantly. (Source: <a href="https://ieeexplore.ieee.org/document/8864357">V. Punyamoorty et al. [2]</a>)</td><td>Fig 4: We design an error metric for the reconstruction of pressure, and observe it as a function of <em>d</em>. (Source: <a href="https://ieeexplore.ieee.org/document/8864357">V. Punyamoorty et al. [2]</a>)</td>
</tr>
</table>

<a name="ml-proj">
</a>
## GPU-accelerated implementation of spectral feature selection algorithm for unsupervised learning

To be added
