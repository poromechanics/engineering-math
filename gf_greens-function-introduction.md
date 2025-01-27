---
author: Vikas Sharma, Ph.D.
date: 5 March 2022
---

# Greens Function

<!-- markdownlint-disable MD041 MD013 MD033 MD012 -->

## Differential operator

We will denote a differential operator by $\bf{L}$, then a differential equation can be written as:


$$
\mathbf{L}u=f
$$


Where $u$ and $f$ are functions from $[a,b]$ to $R$. Here $[a,b]$ is the domain of $u$ and $f$., and $\bf{L}$ is a  $n$th order linear ordinary differential operator. The differential operator satisfies the following conditions of linearity.



If $\alpha$ and $\beta$ are some arbitrary real numbers, and $u$ and $v$ are some functions, and let us assume that $Lu$ and $Lw$ exists, then


$$
\mathbf{L}\left(\alpha u+\beta v\right)=\alpha\mathbf{L}u+\beta\mathbf{L}v
$$


The generic form of $L$ is given by


$$
\mathbf{L}:=a_{0}(x)+a_{1}(x)\frac{d}{dx}+a_{2}(x)\frac{d^{2}}{dx^{2}}+\cdots+a_{n}(x)\frac{d^{n}}{dx^{n}}
$$

Example:

1. $\mathbf{L}u:=\frac{d^{2}u}{dx^{2}}+x^{2}\frac{du}{dx}+4u$, Linear
2. $\mathbf{L}u:=\frac{d^{2}u}{dx^{2}}+\cos u$​, Nonlinear
3. $\mathbf{L}u:=\frac{du}{dx}+abs(u)$​ , Non linear

## Boundary condition

Now we will consider the boundary condition associated with the linear ordinary differential equation described above. Note that if the order of ODE is n then we will need to specify n boundary conditions. These n boundary conditions can be written as follows.


$$
\mathbf{B}_{j}\left(u\right)=c_{j},\text{ for },j=1,2,{\cdots,n}
$$


The above form of boundary condition is called inhomogeneous if $c_j \ne 0$, and it is called homogeneous if $c_j = 0$. The boundary condition $\bf{B}_j$ is called linear if it satisfy the following conditions.



Let $\alpha$ and $\beta$ be some arbitrary real numbers, and let $u$ and $v$ be some real functions, then


$$
\mathbf{B}_{j}\left(\alpha u+\beta v\right)=\alpha\mathbf{B}_{j}u+\beta\mathbf{B}_{j}v
$$


We can represent a linear boundary condition as a linear combination of $u$ and its derivatives, through order $n-1$, at the two endpoints, $a.b$.



For $n=1$ boundary condition is given by


$$
\mathbf{B}_{1}u:=u(a)=c_{1}
$$


For $n=2$ boundary condition is given by


$$
\mathbf{B}_{1}u:=a_{10}u(a)+a_{11}\frac{du(a)}{dx} + b_{10}u(b)+b_{11}\frac{du(b)}{dx}=c_1
$$

$$
\mathbf{B}_{2}u:=a_{20}u(a)+a_{21}\frac{du(a)}{dx} + b_{20}u(b)+b_{21}\frac{du(b)}{dx}=c_2
$$

Examples:

1. $Bu=u(0)+2\frac{du(1)}{dx}$, linear functional
2. $Bu:= u^2(0)$, nonlinear functional
3. Bu := $\int_{0}^{1}{u(x)\cos(x)dx}$, linear functional

## Operator



An operator will be denoted by $\mathfrak{L}$, which will refer to the linear differential operator $\mathbf{L}$ and the boundary conditions $\mathbf{B}_{j}$. The linearity of differential operator and its boundary conditions leads to the linearity of the operator.






## Adjoint operator

The formal adjoint differential operator $\mathbf{L}^{*}$ Of a linear differential operator $\mathbf{L}$ Is obtained by performing integration by parts as show below


$$
\int_{a}^{b}v\mathbf{L}udx=\int_{a}^{b}u\mathbf{L}^{*}vdx+\left[\cdots\right]_{a}^{b}
$$


Where, the second term on the RHS denotes the boundary term. The integral in above equation denotes the inner product of two functional in inner-product space. We will use the operator $\langle \cdot, \cdot\rangle$ To denote an inner product, that is


$$
\left\langle v,\mathbf{L}u\right\rangle :=\int_{a}^{b}v\mathbf{L}udx
$$


Then, Eq. \ref{eq:eq-1} can be written as


$$
\left\langle v,\mathbf{L}u\right\rangle =\left\langle u,\mathbf{L}^{*}v\right\rangle +\left[\cdots\right]_{a}^{b}
$$




Note that in the above equation we have assumed the existence of $\mathbf{L}u$​  and $\mathbf{L}^{*}v$.



## Example

Consider the following differential operator


$$
\mathbf{L}u:=a(x)\frac{d^{2}u}{dx^{2}}+b(x)\frac{du}{dx}+c(x)u
$$
Then to get the adjoint differential operator we follow the procedure given below, which starts by integration by parts.


$$
\begin{aligned}\left\langle v,\mathbf{L}u\right\rangle  & :=\int_{a}^{b}v\mathbf{L}udx\\
 & =\int_{a}^{b}v\left(a(x)\frac{d^{2}u}{dx^{2}}+b(x)\frac{du}{dx}+c(x)u\right)dx\\
 & =\int_{a}^{b}va(x)\frac{d^{2}u}{dx^{2}}dx+\int_{a}^{b}vb(x)\frac{du}{dx}dx+\int_{a}^{b}vc(x)udx\\
 & =\left[va\frac{du}{dx}\right]_{a}^{b}-\int_{a}^{b}\frac{dva}{dx}\frac{du}{dx}dx+\int_{a}^{b}vc(x)udx\\
 & +\left[vbu\right]_{a}^{b}-\int_{a}^{b}\frac{dvb}{dx}udx\\
 & =\left[va\frac{du}{dx}\right]_{a}^{b}-\left[\frac{dva}{dx}u\right]_{a}^{b}+\int_{a}^{b}\frac{d^{2}va}{dx^{2}}udx+\int_{a}^{b}vc(x)udx\\
 & +\left[vbu\right]_{a}^{b}-\int_{a}^{b}\frac{dvb}{dx}udx\\
 & =\int_{a}^{b}u\left(\frac{d^{2}va}{dx^{2}}-\frac{dvb}{dx}+c(x)\right)dx+\left[va\frac{du}{dx}-\frac{dva}{dx}u+vbu\right]_{a}^{b}\\
 & =\left\langle u,\mathbf{L}^{*}v\right\rangle +\left[va\frac{du}{dx}-\frac{dva}{dx}u+vbu\right]_{a}^{b}
\end{aligned}
$$


Where the adjoint differential operator is given by


$$
\begin{aligned}\mathbf{L}^{*}v & =\frac{d^{2}va}{dx^{2}}-\frac{dvb}{dx}+c(x)\\
 & =a\frac{d^{2}v}{dx^{2}}+\left(2\frac{da}{dx}-b\right)\frac{dv}{dx}+\left(\frac{d^{2}a}{dx^{2}}-\frac{db}{dx}+c\right)
\end{aligned}
$$

## Formally self-adjoint operator

When $\mathbf{L} = \mathbf{L}^{*}$, then we say that $\mathbf{L}$​ Is formally self adjoint.

In above mentioned example the differential operator will be self adjoint if $b=\frac{da}{dx}$, therefore,  the following linear differential operator is self adjoint.

$$
\mathbf{L}u:=a(x)\frac{d^{2}u}{dx^{2}}+\frac{da}{dx}\frac{du}{dx}+c(x)u
$$

> First order differential operators cannot be formally self-adjoint.

For the case where the boundary conditions associated with $\mathbf{L}$ Are homogenous, we define not only a formal adjoint differential operator $\mathbf{L}^{*}$, but also an adjoint operator $\mathfrak{L}$, which is given by the following relationship.


$$
\langle Lu,v \rangle = \langle u, L^* v\rangle
$$


In this way, $\mathfrak{L}^{*}$, contains both $\mathbf{L}^{*}$, and boundary conditions which are such that the boundary terms, arising through the integration by parts, all vanish.


## Green's function method


In this section we will present the Green's function method for the solution of $n$th order linear ODE, with linear boundary conditions in the form of linear combination of the unknown and its derivatives through order $n-1$.

Consider a second order ODE which is given below.

$$
Lu:=\frac{d^2 u}{d x^2} = f(x); \quad u(0)=u(1)=0
$$

The problem represents the static deflection of a string, which is clamped at both ends. Here, $f(x)$ denotes the force per unit length of the string. Also note that the string is under tension.

From the adjoint linear operator, we know that

$$
\langle Lu,v\rangle=\left\langle u,L^{*}v\right\rangle +\left[\cdots\right]_{0}^{1}
$$

Here domain of integration is selected from 0 to 1.

## Delta function

The history of delta function is very rich, and can be found [on Wikipedia](https://en.wikipedia.org/wiki/Dirac_delta_function). A delta function is denoted by $\delta(x)$, it is a discrete function. Later, we will explain that it does not follow the classical definition of a function, and it is what we called as a *generalized function*. A $\delta(x)$ function is given by following equation

$$
\delta(x):=\begin{cases}
0 & x\ne0\\
\infty & x=0
\end{cases}
$$

In above definition delta function is zero everywhere but $x=1$​ where it is infinite. We can define a shifted definition of delta function as

$$
\delta(x-\xi):=\begin{cases}
0 & x-\xi\ne0\\
\infty & x-\xi=0
\end{cases}
$$

One of the important property of delta function is given below.

$$
\int_{-\infty}^{\infty}\delta(x-\xi)dx=1
$$

In mechanics Delta function is used to represent **a point force**, **a point source of heat or concentration**. In electrostatic, it is used to represent a point charge, and in gravitation it is used to denote a point mass.

Another important property of delta function is given below.

$$
\int\delta(x-\xi)f(x)dx=f(\xi)
$$

The above property is also called the collocation property.

Some other properties of delta functions are as follows.

- $x \delta(x)=0$
- $x^n \delta(x)=0$
- $\delta^n(x)=\delta(x)$

We can extend the definition of delta function to multi-dimensions as follows:

$$
\delta(x,y)=\begin{cases} +\infty & x^{2}+y^{2}=0\\ 0 & \text{otherwise} \end{cases}
$$

The shifted delta function is given by

$$
\delta({\bf x}-{\bf x}_{0})=\begin{cases} +\infty & \left\Vert {\bf x}-{\bf x}_{0}\right\Vert =0\\ 0 & \text{otherwise} \end{cases}
$$

The integral property is given below:

$$
\int_{\Omega}\delta({\bf x}-{\bf x}_{0})f({\bf x})=f({\bf x}_{0})
$$

## Generalized function

Consider the following functional:

$$
\mathfrak{F}\left(h\right):=\int_{-\infty}^{\infty}g\left(s\right)h\left(s\right)ds
$$

Here, $g$ and $h$ are some functions belonging to a functional space $V$.  It should be noted that the linear functional takes a function as argument and returns a real number. In this way, the set of $h$ functions (a subset of $V$) forms the domain of the functional $\mathfrak{F}$, and the range of this functional is located on real number line. In other words:

$$
\mathfrak{F}: V \rightarrow R
$$

The domain of $\mathfrak{F}$ will be denoted by $\mathfrak{D}$. Usually, the domain of the functional consist of functions which are "very smooth" and which decay rapidly at the infinity. Also, note that all these function in the domain of the functional are defined over $-\infty < x < \infty$. 

In the above definition function $g(x)$, is called the kernel of the functional if this function remains fixed. Also note that for different $g$ we will get different functionals. The collection of these linear functionals is called the dual space of $V$ and denoted by $V^*$. 

Now take the Heaviside step function as the kernel $g(x-\xi)$, which is defined as:

$$
H_{\xi}(x):=g(x-\xi)=\begin{cases}
1 & x-\xi>0\\
0 & x-\xi\le0
\end{cases}
$$

The, the functional $\mathfrak{F}$ takes the following form.

$$
\mathfrak{F}: V \rightarrow R \Rightarrow \int_{-\infty}^{\infty}g(s-\xi)h(s)ds=\int_{\xi}^{\infty}h(s)ds
$$

Now consider delta function $\delta(x-\xi)$ as the kernel, then we can obtain following functional.

$$
h(x)=\int_{-\infty}^{\infty}\delta\left(s-x\right)h(s)ds
$$

In this way the kernel  $\delta(x-\xi)$, can be understood as a generalized function, which is defined by its **action** on a given function $h(x)$, and we never talk about the values of a generalized function.

## Weak derivatives

In the framework of  generalized function theory, one often work with the so called weak-derivatives. This is because there may be situations where the derivatives of a generalized function is not defined in the classical sense. 

The weak-derivative of a generalized function is defined as follows.

$$
\int_{-\infty}^{\infty}\frac{dg(s)}{ds}h(s)ds=\left[g(s)h(s)\right]_{-\infty}^{\infty}-\int_{-\infty}^{\infty}g(s)\frac{dh}{ds}ds
$$

Now, if we select $h(x)$ such that they vanish outside a finite  interval (i.e., h has compact support) then the above equation becomes

$$
\int_{-\infty}^{\infty}\frac{dg(s)}{ds}h(s)ds=-\int_{-\infty}^{\infty}g(s)\frac{dh}{ds}ds
$$

In the aforesaid equation, let $g(s)=\delta(s-x)$, then:

$$
\begin{aligned}\int_{-\infty}^{\infty}\frac{d\delta(s-x)}{ds}h(s)ds & =\left[\delta(s-x)h(s)\right]_{-\infty}^{\infty}-\int_{-\infty}^{\infty}\delta(s-x)\frac{dh}{ds}ds\\
 & =-\frac{dh(x)}{dx}
\end{aligned}
$$

Let $g(s)=H(s-x)$, that is, Heaviside step function, then

$$
\begin{aligned}\int_{-\infty}^{\infty}\frac{dH(s-x)}{ds}h(s)ds & =-\int_{-\infty}^{\infty}H\left(s-x\right)\frac{dh}{ds}ds\\
 & =-\int_{x}^{\infty}\frac{dh}{ds}ds\\
 & =h(x)
\end{aligned}
$$

This suggest that

$$
\frac{dH(s-x)}{ds}=\delta(s-x)
$$

We can define the $k$th weak derivative as:

$$
\int_{-\infty}^{\infty}\frac{d^{k}g(s)}{ds^{k}}h(s)ds=(-1)^{k}\int_{-\infty}^{\infty}g(s)\frac{d^{k}h}{ds^{}k}ds
$$

where, $h=C_{0}^{\infty}$, i.e.,  infinitely differentiable with compact support.

## Test functions

We will denote by $\mathcal{D}$ the class of those functions in $C_{0}^{\infty}(R)$ which have compact support over the intervals of the form $\left [ -a, a\right ]$ and which approach the Dirac $\delta-function$   as $a \rightarrow 0$. The members of the class $\mathcal{D}$ are called the test functions.

- [ ] Some examples of test functions are given below.

## Delta function in Curvilinear coordinates

- [ ] Add definition of Delta function

