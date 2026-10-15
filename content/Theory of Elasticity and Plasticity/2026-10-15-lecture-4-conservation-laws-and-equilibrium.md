---
title: "Lecture 4: Conservation Laws and Equilibrium"
course: Theory of Elasticity and Plasticity
date: 2026-10-15
tags: [conservation-laws, force-equilibrium, moment-equilibrium, indicial-notation, stress-symmetry]
source: incoming/Lecture 4.pdf
status: final
---

## Conservation laws

| Conservation of | Equation | Consequence |
| --- | --- | --- |
| Mass | $m = C$ | Continuity |
| Momentum | $\dfrac{d(m\vec{v})}{dt} = \sum \vec{F}$ | Force equilibrium |
| Moment of momentum | $\dfrac{d(\vec{r} \times m\vec{v})}{dt} = \sum (\vec{r} \times \vec{F}) + \sum \vec{M}$ | Moment equilibrium |

## Force equilibrium

In $x$:

$$
\frac{\partial \sigma_{xx}}{\partial x} + \frac{\partial \sigma_{yx}}{\partial y} + \frac{\partial \sigma_{zx}}{\partial z} + \rho b_x = 0
$$

In $y$:

$$
\frac{\partial \sigma_{xy}}{\partial x} + \frac{\partial \sigma_{yy}}{\partial y} + \frac{\partial \sigma_{zy}}{\partial z} + \rho b_y = 0
$$

In $z$:

$$
\frac{\partial \sigma_{xz}}{\partial x} + \frac{\partial \sigma_{yz}}{\partial y} + \frac{\partial \sigma_{zz}}{\partial z} + \rho b_z = 0
$$

In indicial notation (a "$,$" in index notation is a derivative):

$$
\sigma_{ji,j} + \rho b_i = 0
$$

Tensor format:

$$
\nabla \cdot \underline{\underline{\sigma}} + \rho \underline{b} = 0
\qquad \text{or} \qquad
\operatorname{div}\underline{\underline{\sigma}} + \rho \underline{b} = 0
$$

The $\nabla \cdot$ form holds only in a Cartesian reference frame. This may be different in other reference frames.

## Moment equilibrium

$$
\sigma_{xz} = \sigma_{zx}
\qquad
\sigma_{yz} = \sigma_{zy}
\qquad
\sigma_{xy} = \sigma_{yx}
$$

$$
\sigma_{ij} = \sigma_{ji}
\qquad
\underline{\underline{\sigma}}^T = \underline{\underline{\sigma}}
$$

These are independent of the reference frame.

Conservation laws are applicable to all materials, in all regimes, in all loading conditions.
