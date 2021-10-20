---
description: Here the concept of tensor is introduced.
---

# 😀 Tensor Algebra

## Tensor

### Zeroth and first order tensors

A tensor of order zero is a scalar $$\alpha\in\mathbb{R}$$, where $$\mathbb{R}$$ is the real space.

A tensor of order one is a vector $$\mathbf{v}\in\mathcal{V}$$, where $$\mathcal{V}$$ is a vector space (could be $$\mathbb{R}^2$$or $$\mathbb{R}^3$$).

#### Index notation

A first order tensor in any basis $$\left\{\mathbf{e}_i \right\}$$ (not necessarily orthonormal) can be written as:

$$
\mathbf{v}=v_i\mathbf{e}_i,\quad \text{sum over}\left\{1,2,3\right\},
$$

which adapts the _Einstein_ summation convention.

#### Kronecker delta and permutation symbols

To any right-handed orthonormal basis $$\left\{\mathbf{e}_i \right\}$$, we associate a **Kronecker delta** defined by:

$$
\delta_{ij}=\mathbf{e}_i\cdot\mathbf{e}_j=\begin{cases} 1 \quad\text{$i=j$}, \\ 0 \quad \text{$i\neq j$}, \end{cases}
$$

and a **permutation symbol** $$\epsilon_{ijk}$$​ defined by:

$$
\epsilon_{ijk}=\mathbf{e}_i\times \mathbf{e}_j\cdot \mathbf{e}_k=\begin{cases} 1 \quad \text{if $ijk=123,231,312$}, \\ -1 \quad \text{if $ijk=321,213,132$},\\ 0 \quad \text{else}. \end{cases}
$$

We can deduce the following identity:

$$
\epsilon_{ijk}\mathbf{e}_k=(\mathbf{e}_i\times \mathbf{e}_j\cdot \mathbf{e}_k)\mathbf{e}_k=\mathbf{e}_i\times \mathbf{e}_j.
$$

{% hint style="info" %}
Note that $$(\mathbf{v}\cdot \mathbf{e}_k)\mathbf{e}_k=(v_i\mathbf{e}_i\cdot \mathbf{e}_k)\mathbf{e}_k=v_i\delta_{ik}\mathbf{e}_k=v_k\mathbf{e}_k=\mathbf{v}$$.
{% endhint %}

#### Scalar product (dot product)

$$
\mathbf{a}\cdot \mathbf{b}=a_ib_j\mathbf{e}_i\cdot \mathbf{e}_j=a_ib_j\delta_{ij}=a_ib_i
$$

#### Vector product (cross product)

$$
\mathbf{a}\times\mathbf{b}=a_ib_j\mathbf{e}_i\times \mathbf{e}_j=a_ib_j\epsilon_{ijk}\mathbf{e}_k.
$$

#### Triple scalar product

$$
\mathbf{a}\times\mathbf{b}\cdot \mathbf{c}=a_ib_jc_k\mathbf{e}_i\times \mathbf{e}_j\cdot \mathbf{e}_k=a_ib_jc_k\epsilon_{ijl}\mathbf{e}_l\cdot\mathbf{e}_k=a_ib_jc_k\epsilon_{ijk}=\mathbf{b}\times\mathbf{c}\cdot \mathbf{a}=\mathbf{c}\times\mathbf{a}\cdot \mathbf{b}
$$

### Second order tensors

A second order tensor $$\mathbf{T}$$​ is a linear mapping $$\mathbf{T}\colon \mathcal{V}\rarr\mathcal{V}$$, which means:

$$
\begin{align*}\mathbf{T}(\mathbf{u}+\mathbf{v})&=\mathbf{Tu}+\mathbf{Tv}\\\mathbf{T}(\alpha\mathbf{v})&=\alpha\mathbf{TV}\end{align*}
$$

​dfd
