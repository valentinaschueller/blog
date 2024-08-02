---
title: Coupled groundwater-surface flows
description: ""
date: 2024-03-01
tags:
  - research
  - english
---

> *I aim to have one short summary post for each of my active/finished research projects. This is one of them.*

In this project, we analyze coupled surface-subsurface flows for hydrological applications.
These are modeled using nonlinear partial differential equations: [Richards' equation](https://en.wikipedia.org/wiki/Richards_equation) for groundwater flow and a variant of the [shallow water equations](https://en.wikipedia.org/wiki/Shallow_water_equations) for surface flow.
Coupling them yields a model that can simulate effects of water management and flooding on the water table and aquifer.[^1]

Particularly, we have analyzed a linearized, coupled Richards-SWE model using methods developed by [Monge & Birken, 2018](https://doi-org.ludwig.lub.lu.se/10.1007/s00466-017-1511-3) and [Gander, Kwok & Mandal, 2014](https://doi-org.ludwig.lub.lu.se/10.1007/978-3-319-18827-0_51).
We study how well this analysis works for the fully nonlinear case:
For this purpose, I have developed a Python implementation for coupled surface-subsurface flow, using [DUNE](https://dune-project.org/) to generate the discretization and [preCICE](https://precice.org/) for coupling.

See also:
- the [code repository](https://gitlab.maths.lu.se/robertk/coupling)
- [slides](/research/upload/2024-02-06-pint_slides.pdf) from my talk at PinT 2024
- my [poster](/research/upload/2023_essence_poster.pdf) at the Swedish e-Science conference 2023

***Collaborators:** [Philipp Birken](https://www.maths.lu.se/staff/philipp-birken) and [Andreas Dedner](https://warwick.ac.uk/fac/sci/maths/people/staff/andreas_dedner/).*

[^1]: Bastian, P. et al. ([2012](https://doi-org.ludwig.lub.lu.se/10.1007/978-3-642-25100-9_65)); Maxwell, R. M. et al. ([2014](https://doi.org/10.1002/2013WR013725))