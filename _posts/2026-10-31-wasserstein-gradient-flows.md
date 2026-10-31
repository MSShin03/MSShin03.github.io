---
title: "A short note on Wasserstein gradient flows"
date: 2026-10-31
category: "Optimal transport"
summary: "A brief demonstration of mathematical exposition and equation rendering."
math: true
demo: true
---

> **Demonstration content.** This sample is not represented as an original or previously published article by Minseop Shin. Replace it before announcing the site.

## Free energy

Consider a probability density \(\rho\) on the flat torus \(\mathbb T^d\). Formally, the free energy is

\[
\mathcal F(\rho)=\int\rho\log\rho\,dx+\int V\rho\,dx+\frac12\iint W(x-y)\rho(x)\rho(y)\,dx\,dy.
\]

The Wasserstein gradient-flow equation is

\[
\partial_t\rho=\Delta\rho+\nabla\cdot(\rho\nabla(V+W*\rho)).
\]

Under suitable smoothness assumptions, the formal dissipation identity is

\[
\frac{d}{dt}\mathcal F(\rho_t)=-\int\rho_t\left|\nabla\frac{\delta\mathcal F}{\delta\rho_t}\right|^2dx.
\]

To add your own notes, create new date-prefixed Markdown files under `_posts/`.
