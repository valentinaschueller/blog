---
title: An Energy Efficiency Perspective on Coupled Models
description: ""
date: 2025-11-10
tags:
  - research
  - english
---

> *I aim to have one short summary post for each of my active/finished research projects. This is one of them.*

As global electricity demand rises, there has been a push for energy awareness in high performance computing and numerical method development.
This requires users to know about power consumption of their codes and how they can affect it without
compromising on accuracy and wallclock time. 
Climate simulations are energy-intensive coupled simulations, affected by static and dynamic load imbalances both in
and between the components. 

In this project, we particularly investigate whether dynamic frequency and voltage scaling (DVFS) is a viable method to reduce energy use for coupled simulations with dynamic load imbalance.
We plan to run small-scale simulations with memory-bound node-level microbenchmarks on EuroHPC clusters.
The aim is to systematically study how energy efficiency can be affected with MERIC, which allows changing CPU frequency and voltage at runtime (and how this differs from optimizing for time to solution). 
As real-world cases, I plan to look at exemplary runs with [EC-Earth 4](https://ec-earth.org/).

See also:
- the [MERIC](https://code.it4i.cz/vys0053/meric) code on IT4I's Gitlab
- [how I want to use preCICE](https://github.com/precice/precice/issues/2544) in this context
- the [proof-of-concept project](https://gitlab.maths.lu.se/valentinaschueller/timeadaptiveqnwr) where I try all of this

***Collaborators:** [Philipp Birken](https://www.maths.lu.se/staff/philipp-birken); [Roman Iakymchuk](https://www.uu.se/en/contact-and-organisation/staff?query=N23-1275) (Uppsala University); [Ondřej Vysocký](https://orcid.org/0000-0001-7849-2744) (VSB – Technical University of Ostrava); the preCICE group, in particular [Frédéric Simonis](https://www.cs.cit.tum.de/sccs/personen/frederic-simonis/).*
