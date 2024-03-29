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
Note that for any orthonormal basis $$\left\{\mathbf{e}_i\right\}$$, $$(\mathbf{v}\cdot \mathbf{e}_k)\mathbf{e}_k=(v_i\mathbf{e}_i\cdot \mathbf{e}_k)\mathbf{e}_k=v_i\delta_{ik}\mathbf{e}_k=v_k\mathbf{e}_k=\mathbf{v},\quad \forall \mathbf{v}\in\mathcal{V}$$.
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

A second order tensor $$\mathbf{T}\in\mathcal{V}^2$$​ is a linear mapping $$\mathbf{T}\colon \mathcal{V}\rarr\mathcal{V}$$, which means:

$$
\begin{align*}\mathbf{T}(\mathbf{u}+\mathbf{v})&=\mathbf{Tu}+\mathbf{Tv}\quad \forall \mathbf{u}\mathbf{v}\in \mathcal{V}\\\mathbf{T}(\alpha\mathbf{v})&=\alpha\mathbf{Tv}\quad \forall\mathbf{v}\in \mathcal{V}\end{align*}
$$

We define two special tensors:

$$
\begin{align*} \mathbf{O}(\mathbf{v})&=\mathbf{0},\quad \forall\mathbf{v}\in\mathcal{V},\\ \mathbf{I}(\mathbf{v})&=\mathbf{v},\quad \forall\mathbf{v}\in\mathcal{V}, \end{align*}
$$

where $$\mathbf{O}$$ is the zero tensor and $$\mathbf{I}$$ is the identity tensor.

#### The dyadic product (the tensor product)

The dyadic product of two vectors is a second order tensor $$\mathbf{a}\otimes\mathbf{b}$$ defined by:

$$
(\mathbf{a}\otimes\mathbf{b})\mathbf{v}=(\mathbf{b}\cdot\mathbf{v})\mathbf{a},\quad\forall \mathbf{v}\in\mathcal{V},
$$

#### The matrix representation of a tensor by orthonormal basis

For a second order tensor $$\mathbf{S}$$ and a set of orthonormal basis $$\left\{\mathbf{e}_i \right\}$$, we can define a matrix $$\left[\mathbf{S}\right]$$ by:

$$
S_{ij}=\left[\mathbf{S}\right]_{ij}=\mathbf{e}_i\cdot\mathbf{Se}_j.
$$

We can define a new tensor $$\tilde{\mathbf{S}}$$ by:

$$
\tilde{\mathbf{S}}=S_{ij}\mathbf{e}_i\otimes\mathbf{e}_j.
$$

Indeed, $$\tilde{\mathbf{S}}$$ is identical to $$\mathbf{S}$$. To see this, we apply $$\tilde{\mathbf{S}}$$ to an arbitrary vector $$\mathbf{v}\in\mathcal{V}$$,

$$
\begin{align*}
    \tilde{\mathbf{S}}\mathbf{v}    &= S_{ij}\mathbf{e}_i\otimes\mathbf{e}_jv_k\mathbf{e}_k\\
                                    &= S_{ij}v_k\delta_{jk}\mathbf{e}_i\\
                                    &= S_{ij}v_j\mathbf{e}_i\\
                                    &= \mathbf{e}_i\cdot\mathbf{S}\mathbf{e}_jv_j\mathbf{e}_i\\
                                    &= (\mathbf{e}_i\cdot\mathbf{S}\mathbf{v})\mathbf{e}_i\\
                                    &= \mathbf{S}\mathbf{v}.
\end{align*}
$$

This implies that $$\mathbf{S}=S_{ij}\mathbf{e}_i\otimes\mathbf{e}_j.$$
