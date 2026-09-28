---
title: "Lecture 1: Vector and Tensor Notation"
course: Theory of Elasticity and Plasticity
date: 2026-09-28
tags: [tensor-notation, vector-algebra, index-notation]
source: incoming/Theory Of Elasticity And Plasticity lecture 1.pdf
status: final
---

## Notation conventions

- $x$ → scalar number
- $\mathbf{x}$ → vector
- $a_i$ → component $i$ of vector $\mathbf{a}$
- $\mathbf{A}$ → matrix
- $A_{ij}$ → component $ij$ of matrix $\mathbf{A}$
- $\sigma, \mathbf{C}$ → tensor
- $\sigma_{ij}$ → component $ij$ of tensor $\sigma$ (order 2)
- $C_{ijkl}$ → component $ijkl$ of tensor $\mathbf{C}$ (order 4)

## Vectors and the Einstein summation convention

$$
\mathbf{u} = u_x \mathbf{e}_x + u_y \mathbf{e}_y + u_z \mathbf{e}_z = \begin{Bmatrix} u_x \\ u_y \\ u_z \end{Bmatrix}
$$

where $\mathbf{e}_x, \mathbf{e}_y, \mathbf{e}_z$ are unit vectors.

$$
= u_1 \mathbf{e}_1 + u_2 \mathbf{e}_2 + u_3 \mathbf{e}_3 = u_i \mathbf{e}_i \quad \Rightarrow \text{Einstein Summation Convention}
$$

Example: $a_{ij} b_{ij}$ has 9 terms.

## Scalar product

Vector · Vector = Scalar

$$
\mathbf{u} \cdot \mathbf{v} = \mathbf{v} \cdot \mathbf{u} = \|\mathbf{u}\| \cdot \|\mathbf{v}\| \cdot \cos\theta = u_i \mathbf{e}_i \cdot v_j \mathbf{e}_j = u_i v_i = u_1 v_1 + u_2 v_2 + u_3 v_3
$$

## Kronecker delta

$$
\delta_{ij} = \begin{cases} 1 & \text{if } i = j \\ 0 & \text{if } i \neq j \end{cases}
$$

## Vector product

Vector × Vector → Vector

$$
\mathbf{u} \times \mathbf{v} = -\mathbf{v} \times \mathbf{u} = u_i \mathbf{e}_i \times v_j \mathbf{e}_j = \begin{vmatrix} \mathbf{e}_x & \mathbf{e}_y & \mathbf{e}_z \\ u_x & u_y & u_z \\ v_x & v_y & v_z \end{vmatrix} = \begin{Bmatrix} u_y v_z - u_z v_y \\ u_z v_x - u_x v_z \\ u_x v_y - u_y v_x \end{Bmatrix}
$$

## Tensor product (dyadic product)

$$
\mathbf{u} \otimes \mathbf{v} = u_i \mathbf{e}_j \otimes v_j \mathbf{e}_j
$$

> Flagged for review: the repeated $\mathbf{e}_j$ on the $u_i$ term above is exactly as written on the page, but it doesn't quite match the surrounding convention (basis vectors indexed by their own component's index). Worth double-checking against the source — it may be a slip of the pen for $u_i \mathbf{e}_i \otimes v_j \mathbf{e}_j$.

A vector dyadic vector is a second-order tensor:

$$
\mathbf{u} \otimes \mathbf{v} = \begin{bmatrix} u_1v_1 & u_1v_2 & u_1v_3 \\ u_2v_1 & u_2v_2 & u_2v_3 \\ u_3v_1 & u_3v_2 & u_3v_3 \end{bmatrix}
$$

A second-order tensor refers to two orientations in space.

## Transformation of Cartesian tensors

$123 \to 1'2'3'$ rotates to new unit vectors $\mathbf{e}_i'$, with orientation cosines $a_{ij}$:

$$
a_{ij} = \cos\theta_{ij} = \mathbf{e}_i' \cdot \mathbf{e}_j
$$

$$
\mathbf{e}_1' = a_{11} \mathbf{e}_1 + a_{12} \mathbf{e}_2 + a_{13} \mathbf{e}_3
$$
$$
\mathbf{e}_2' = a_{21} \mathbf{e}_1 + a_{22} \mathbf{e}_2 + a_{23} \mathbf{e}_3
$$
$$
\mathbf{e}_3' = a_{31} \mathbf{e}_1 + a_{32} \mathbf{e}_2 + a_{33} \mathbf{e}_3
$$

(mutually perpendicular), or:

$$
\mathbf{e}_i' = a_{ij} \mathbf{e}_j \quad \text{— the transformation matrix}
$$

$$
A = \begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{bmatrix}
$$

$A$, with elements $a_{ij}$, transforms a vector or a tensor from the original reference frame $123$ to $1'2'3'$:

$$
A \begin{Bmatrix} \mathbf{e}_1 \\ \mathbf{e}_2 \\ \mathbf{e}_3 \end{Bmatrix} = \begin{Bmatrix} \mathbf{e}_1' \\ \mathbf{e}_2' \\ \mathbf{e}_3' \end{Bmatrix}
$$

The opposite is also true:

$$
\begin{Bmatrix} \mathbf{e}_1 \\ \mathbf{e}_2 \\ \mathbf{e}_3 \end{Bmatrix} = A^T \begin{Bmatrix} \mathbf{e}_1' \\ \mathbf{e}_2' \\ \mathbf{e}_3' \end{Bmatrix}, \qquad AA^T = I
$$

## Orthogonality of a matrix

$$
A^T A = A A^T = I
$$

Key properties:
- Preserves lengths. Only rotates or reflects a vector, never stretches or skews it.
- Determinant $= 1$
- Eigenvalue is $1$

## Tensor transformation

A tensor requires 2 multiplications with the transformation matrix. Tensor $T$, transformed tensor $T'$, transformation matrix $A$:

$$
T = A^T T' A \qquad \text{or} \qquad T' = A T A^T
$$

**An important property!** — because the order is 2.

$C_{ijkl}$ would require 4 multiplications, since its order is 4.
