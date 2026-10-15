---
title: "Lecture 3: Kinematics and Compatibility"
course: Theory of Elasticity and Plasticity
date: 2026-10-14
tags: [kinematics, strain, compatibility-equations, lagrangian, eulerian]
source: incoming/Lecture 3.pdf
status: final
---

## Kinematics

**Lagrangian** formulation refers the actual state $x$ back to the reference state $X$ $\rightarrow$ solid mechanics.

**Eulerian** formulation takes the actual state $x$ as the only reference $\rightarrow$ fluid mechanics.

## Compatibility equation

$$
u(X) = \begin{Bmatrix} u_x(x, y) \\ u_y(x, y) \end{Bmatrix}
$$

Displacement to strain: straightforward and unique.

$$
\epsilon_{xx} = \frac{\partial u_x}{\partial x}
\qquad
\epsilon_{yy} = \frac{\partial u_y}{\partial y}
\qquad
\epsilon_{xy} = \frac{1}{2}\left(\frac{\partial u_x}{\partial y} + \frac{\partial u_y}{\partial x}\right)
$$

Strain back to displacement: not always possible.

To have a unique strain-to-displacement solution, we must impose some compatibility equations.

In 2D, one condition:

$$
\frac{\partial^2 \epsilon_{xx}}{\partial y^2} + \frac{\partial^2 \epsilon_{yy}}{\partial x^2} = 2 \frac{\partial^2 \epsilon_{xy}}{\partial x \, \partial y}
$$

In 3D, in indicial notation (there are 6 equations):

$$
\epsilon_{ij,kl} + \epsilon_{kl,ij} - \epsilon_{ik,jl} - \epsilon_{jl,ik} = 0
$$

- $ij$ are the strain components
- $kl$ are the derivatives

$$
\epsilon_{ij,kl} = \frac{\partial^2 \epsilon_{ij}}{\partial x_k \, \partial x_l}
$$

## Example of an incompatible strain field

Strain tensor in 2D:

$$
\epsilon = \begin{bmatrix} 0 & \alpha x y \\ \alpha x y & 0 \end{bmatrix}
\qquad
\vec{u}(0) = 0, \quad u_y(L, 0) = 0
$$

Calculate the displacement field.

**Solution**

$$
\epsilon_{xx} = \frac{\partial u_x}{\partial x} = 0 \quad \Rightarrow \quad u_x(x, y) = f_1(y)
$$

$$
\epsilon_{yy} = \frac{\partial u_y}{\partial y} = 0 \quad \Rightarrow \quad u_y(x, y) = f_2(x)
$$

$$
\epsilon_{xy} = \frac{1}{2}\left(\frac{\partial u_x}{\partial y} + \frac{\partial u_y}{\partial x}\right) = \alpha x y
$$

There is no way this holds:

$$
\frac{1}{2}\left(\frac{\partial f_1(y)}{\partial x} + \frac{\partial f_2(x)}{\partial y}\right) \neq \alpha x y
$$

Continuity is broken. Compatibility equations are not satisfied.
