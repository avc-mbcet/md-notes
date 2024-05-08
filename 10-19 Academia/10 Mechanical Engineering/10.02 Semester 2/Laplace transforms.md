---
date: 2024-05-04
title: Laplace transforms
---
# Introduction
$L(f(t))=\int_{0}^{\infty}f(t)e^{-\text{st}}\,dt$ 

Here $\text{s}$ is real or complex

# Transforms
## Basic Operations
$$L[a.f(t)]=a.L[f(t)]$$

Here $a$ is constant and $f(t)$ is a function

$$L[f(t)+g(t)]=L[f(t)]+L[g(t)]$$ Here $f(t)$ and $g(t)$ are two functions
## Function Transforms
- $$L(1)=\frac{1}{s}, s>0$$
- $$L(t)=\frac{1}{s^2}, s>0$$
- $$L(t^n)=\frac{n!}{s^{n+1}}$$
- $$L(e^{at})=\frac{1}{s-a}, s>a$$
- $$L(\sin{at})=\frac{a}{s^2+a^2},s>0$$
- $$L(\cos{at})=\frac{s}{s^2+a^2}s>0$$
- $$L(\sinh{at})=\frac{a}{s^2-a^2},s>a$$
- $$L(\cosh{at})=\frac{s}{s^2-a^2},s>a$$
# Note
To solve problems, trigonometry is required
