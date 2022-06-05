---
title: "Directional Derivatives"
date: 2022-06-05
draft: false
cover:
  #image: "/images/hello-world-2.png"
---

> [!NOTE] Definition: Directional Derivative with 2 Variables
> The directional derivative of a function $f(x, y)$ in the direction of the unit vector $\hat{u}$ at the point $(x, y)$ is given by
> $$
D_{\hat{u}} f(x, y)=\nabla f \cdot \hat{u}
= f_{x}u_{1}+f_{y}u_{2}$$
> It measures the rate of change of $f$ in $\hat{u}$ direction, at the point $(x,y)$.

> [!TLDR] Intuitive Proof: why directional derivative can measure the rate of change
> We can prove this by showing the linear approximation near a point $(x,y)$.
> Let $\vec{s}=\Delta s \hat{u}$ be a small change in direction $\hat{u}$. So the new point it arrived is
> $$(x+\Delta s u_{1},y+\Delta s u_{2})$$
> The linear approximation of this new point is:
> $$
\begin{aligned}
f\left(x+u_{1} \Delta s, y+u_{2} \Delta s\right) & \approx f(x, y)+f_{x} u_{1} \Delta s+f_{y} u_{2} \Delta s \\
&=f(x, y)+\underbrace{\left(f_{x} u_{1}+f_{y} u_{2}\right)}_{\text {slope of } f \text { in } u \text { direction }} \Delta s .
\end{aligned}
> $$
> 
> It gives us:
> $$
D_{\hat{u}} f(x, y)=f_{x}u_{1}+f_{y}u_{2}=\frac{f\left(x+u_{1} \Delta s, y+u_{2} \Delta s\right) - f(x, y)}{\Delta s} $$

A directional derivative is a scala.
And:
- $D_{(1,0)} f(x, y) = f_{x}(x,y)$
- $D_{(0,1)} f(x, y) = f_{y}(x,y)$

Since $\hat{u}=(\cos{\theta}, \sin{\theta})$, so we also have:
$$
D_{\hat{u}} f(x, y)=f_{x} \cos \theta+f_{y} \sin \theta
$$

> [!tip]
> Partial derivatives are spectial directional derivatives.

### Directional Derivatives with non-unit vectors
> [!NOTE] Fact
> If $\vec{v}$ is a vector with magnitude not equal to 1 , a compact way of writing the directional derivative of $f$ in the direction of a vector $\vec{v}$ is
> $$
D_{\vec{v}} f(x, y)=\frac{\nabla f \cdot \vec{v}}{|\vec{v}|}$$
> Which means, the directional derivatives in the same directions are aways equal.

### Directional Derivatives and Projection
? L7.3 in MITx 18.02.1x

## Direction of Maximal Change
> [!NOTE] Fact
> The gradient is the direction of the maximum rate of change of $f$ .
> 
> *Proof*:
> $$
D_{\hat{u}} f=\nabla f \cdot \hat{u}=|\nabla f||\hat{u}| \cos \theta=|\nabla f| \cos \theta .$$
> where the $\theta$ is the angle between $\nabla$ and $\hat{u}$. That means when $\theta$ is 0, $D_{\hat{u}} f$ is maximal.

## Notation
There are many kinds of notation for directional derivatives:
- $D_{\vec{v}} f(x, y)$
- $\nabla_{\vec{v}} f(x, y)$
- $f_{\vec{v}}^{\prime}(x, y)$
- $D f(x, y)(\vec{v})$
- $\hat{v} \cdot \nabla f(x, y)$
- $\left.\frac{\partial f}{\partial s}\right|_{\vec{v}}$

## Properties
The directional derivative behaves in nearly identical ways as partial derivatives, and satisfies the same general properties.
1. For a function $f$ and a real number $c$, we have $D_{\vec{v}}(c f)=c D_{\vec{v}} f$.
2. For functions $f$ and $g$, we have $D_{\vec{v}}(f+g)=D_{\vec{v}} f+D_{\vec{v}} g$.
3. For functions $f$ and $g$, we have $D_{\vec{v}}(f g)=g D_{\vec{v}} f+f D_{\vec{v}} g$.

## Higher Dimension
> [!NOTE] Definition: Directional Derivatives in Higher Dimension
> We would have an $n$-dimensional unit vector $\hat{u}=\left\langle u_{1}, u_{2}, \ldots, u_{n}\right\rangle$. Then

$$
\begin{aligned}
D_{\tilde{u}} f\left(x_{1}, x_{2}, \ldots, x_{n}\right) &=\nabla f\left(x_{1}, x_{2}, \ldots, x_{n}\right) \cdot \hat{u} \\\
&=\left\langle f_{x_{1}}, f_{x_{2}}, \ldots, f_{x_{n}}\right\rangle \cdot\left\langle u_{1}, u_{2}, \ldots, u_{n}\right\rangle \\\
&=f_{x_{1}}\left(x_{1}, x_{2}, \ldots, x_{n}\right) u_{1}+f_{x_{2}}\left(x_{1}, x_{2}, \ldots, x_{n}\right) u_{2}+\cdots+f_{x_{n}}\left(x_{1}, x_{2}, \ldots, x_{n}\right) u_{n} .
\end{aligned}
$$
> 
