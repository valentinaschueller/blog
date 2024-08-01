---
title: Coupled Groundwater-Surface Flows
description: ""
date: 2024-03-01
tags:
  - research
  - english
---

In this project, we are analyzing coupling algorithms for the Richards equation coupled to the shallow water equations (SWE).
These are nonlinear partial differential equations which can model groundwater and surface flows, respectively.
Coupling them yields a model that can simulate effects of water management and flooding on the water table and aquifer.[^1]
Particularly, I am working on a fully discrete and continuous analysis of Dirichlet-Neumann Waveform Relaxation (DNWR) for a linearized, coupled Richards-SWE model.
Here I have used methods developed by [Monge & Birken, 2018](https://doi-org.ludwig.lub.lu.se/10.1007/s00466-017-1511-3) and [Gander, Kwok & Mandal, 2014](https://doi-org.ludwig.lub.lu.se/10.1007/978-3-319-18827-0_51).

I have developed an [implementation of the fully nonlinear model](https://gitlab.maths.lu.se/robertk/coupling).
Both are written in Python, using [DUNE](https://dune-project.org/) to generate the discretization and [preCICE](https://precice.org/) for coupling.

***Collaborators:** [Philipp Birken](https://www.maths.lu.se/staff/philipp-birken) and [Andreas Dedner](https://warwick.ac.uk/fac/sci/maths/people/staff/andreas_dedner/).*

[^1]: Bastian, P. et al. (2012). Adaptive Modelling of Coupled Hydrological Processes with Application in Water Management. In: Günther, M., Bartel, A., Brunk, M., Schöps, S., Striebel, M. (eds) Progress in Industrial Mathematics at ECMI 2010. Mathematics in Industry, vol 17. Springer, Berlin, Heidelberg. https://doi-org.ludwig.lub.lu.se/10.1007/978-3-642-25100-9_65