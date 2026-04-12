---
title: Toy Examples with ClimaCoupler.jl
description: ""
date: 2025-07-11
tags:
  - research
  - english
---

> *I aim to have one short summary post for each of my active/finished research projects. This is one of them.*

After hearing [Valeria Barra's](https://valeriabarra.org/) talk at PASC 2024, I became interested in playing around with the coupler developed as part of the Climate Modeling Alliance ([CliMA](https://clima.caltech.edu/)).
It explicitly supports checkpointing, which is the coupler-side feature that makes iterative coupling algorithms fairly straightforward to implement.

These are the questions I work on with this project:
- Modeling & Analysis: What is a good toy model to explain waveform relaxation convergence rates I observe in EC-Earth? Which convergence rates can I obtain theoretically (and under which assumptions)?
- Numerical Experiments: How do discretization choices and model complexity affect the convergence rates? Do these fit the theoretical analysis?
- Software Development: What design and implementation choices in CliMA and ClimaCoupler.jl can I make use of?


See also:
- my [code on GitHub](https://github.com/valentinaschueller/clima-playground)
- [slides](/research/upload/2025-06-27_DD29.pdf) from my talk at DD29
- the [article](/research/upload/2025_dd29-proceedings.pdf) that will appear in the DD29 proceedings


***Collaborators:** [Philipp Birken](https://www.maths.lu.se/staff/philipp-birken), [Hanna Kjellson](https://portal.research.lu.se/en/persons/hanna-kjellson/), [Liu-Di Lu](https://liudi-lu.github.io) (Lund University); the CliMA community, in particular [Julia Sloan](https://github.com/juliasloan25) and [Jeff Yoder](https://github.com/jefftyoder).*
