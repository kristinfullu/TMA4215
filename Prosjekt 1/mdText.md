# Project 1
- Submitted by Kristin Fullu
- Note: Many integrals throughout the project are computed with the help of Rottmann

## Task 1
### 1 a)

We want to prove that for any $k, h \in \mathbb{Z}$ we have 

$$
\langle e^{2\pi i k \cdot}, e^{2\pi i h \cdot}\rangle =
\begin{cases}
1 &\text{if  } k=h \\
0 &else.
\end{cases}
$$

$\underline{\text{Case: }k \neq h}$

$$
\langle e^{2\pi i k \cdot}, e^{2\pi i h \cdot}\rangle = \int_0^1 e^{2\pi i k \cdot}\overline{e^{2\pi i h \cdot}} d\cdot = \int_0^1 e^{2\pi i k \cdot}\cdot e^{-2\pi i h \cdot} d\cdot = \int_0^1 e^{2\pi i (k-h) \cdot} d\cdot.
$$


$$
\frac{e^{2\pi i (k-h)\cdot}}{2\pi i(k-h)}\bigg|_0^1 = \frac{e^{2\pi i (k-h)}-1}{2\pi i(k-h)} = \frac{\cos(2\pi(k-h))+i\sin(2\pi (k-h))-1}{2\pi i(k-h)} = 0
.$$

As both $k$ and $h$ are integers, the cosine term always equals 1, and the sine term always equals 0. Because of this, the numerator becomes 0.

<br/>

$\underline{\text{Case: } k= h}$

$$\langle e^{2\pi i k \cdot}, e^{2\pi i k \cdot}\rangle = \int_0^1 e^{2\pi i k \cdot}\overline{e^{2\pi i k \cdot}} d\cdot = \int_0^1 e^{2\pi i k \cdot}\cdot e^{-2\pi i k \cdot} d\cdot = \int_0^1 e^0 d\cdot = 1.$$ 

Thus, we have proved our introductory statement.

## 1 b)

We now have the following functions,

$$\sqrt{2}\sin(2\pi mx), m = 1,2,\dots \\ 
\quad \sqrt{2}\cos(2\pi nx), n = 1,2,\dots \\
\cos(2\pi 0x)$$

$x \in \mathbb{T}.$

We want to prove that these functions form an orthonormal system.

We first check for orthogonality. To do this, we check that the inner product of any two functions that are not the same is equal to 0.

$\underline{\langle \sqrt{2}\sin(2\pi m \cdot), \sqrt{2}\cos(2\pi n \cdot)\rangle}$

$$\int_0^1 \sqrt{2}\sin(2\pi m \cdot)\; \overline{\sqrt{2}\cos(2\pi n \cdot)}\; d\cdot= 0$$

<br/>

$\underline{\langle \sqrt{2}\sin(2\pi m \cdot), \cos(2\pi 0 \cdot)\rangle}$

$$\int_0^1 \sqrt{2}\sin(2\pi m \cdot) \; \overline{\cos(2\pi 0 \cdot)} \;d\cdot= 0$$

<br/>

$\underline{\langle \sqrt{2}\sin(2\pi m \cdot), \sqrt{2}\sin(2\pi n \cdot)\rangle}$

$$\int_0^1 \sqrt{2}\sin(2\pi m \cdot)\; \overline{\sqrt{2}\sin(2\pi n \cdot)}\; d\cdot = 2[\frac{\sin((2\pi m-2\pi n)\cdot)}{2(2\pi m-2\pi n)}-\frac{\sin((2\pi m + 2\pi n)\cdot)}{2(2\pi m + 2\pi n)}]\bigg|_0^1 = 0$$

<br/>

$\underline{\langle \sqrt{2}\cos(2\pi m \cdot), \sqrt{2}\cos(2\pi n \cdot)\rangle}$

$$\int_0^1 \sqrt{2}\cos(2\pi m \cdot)\; \overline{\sqrt{2}\cos(2\pi n \cdot)}\; d\cdot = 2[\frac{\sin((2\pi m-2\pi n)\cdot)}{2(2\pi m-2\pi n)}+\frac{\sin((2\pi m + 2\pi n)\cdot)}{2(2\pi m + 2\pi n)}]\bigg|_0^1 = 0$$

<br/>

$\underline{\langle \sqrt{2}\cos(2\pi m \cdot), \cos(2\pi 0 \cdot)\rangle}$

$$ = \int_0^1 \sqrt{2}\cos(2\pi m \cdot) \cdot \overline{1} \;d\cdot= \frac{\sqrt{2}\cos(2\pi m\cdot)}{2\pi m}\bigg|_0^1 = 0,$$

As we now have checked all possibilities, we can state that the functions form an orthogonal system.

We then check for orthonormality. A function is orthonormal the inner product of the function with itself equals 1.

<br/>

$\underline{\langle \sqrt{2}\sin(2\pi m \cdot), \sqrt{2}\sin(2\pi m \cdot)\rangle}$

$$\int_0^1 \sqrt{2}\sin(2\pi m \cdot)\; \overline{\sqrt{2}\sin(2\pi m \cdot)}\; d\cdot = 2\int_0^1 \sin^2(2\pi m \cdot)\; d\cdot.$$

We have the following integral rule:

$$\int \sin^2(kx)dx = \frac{x}{2}-\frac{\sin(2kx)}{4k}+C,$$ 
where k is an arbitrary constant. Applying this, we get that

$$2\int_0^1 \sin^2(2\pi m \cdot)\; d\cdot = 2[\frac{\cdot}{2}-\frac{\sin(4\pi m \cdot)}{8\pi}]\bigg|_0^1 = 2\cdot\frac{1}{2} - 0 -(0-0) = 1.$$

<br/>

$\underline{\langle \sqrt{2}\cos(2\pi m \cdot), \sqrt{2}\cos(2\pi n \cdot)\rangle}$

$$\langle \sqrt{2}\cos(2\pi m \cdot), \sqrt{2}\cos(2\pi m \cdot)\rangle = 2\int_0^1 cos^2(2\pi m \cdot)\; d\cdot $$

We have the following integral rule:

$$\int \cos^2(kx)dx = \frac{x}{2}+\frac{\sin(2kx)}{4k}+C,$$ 
where k is an arbitrary constant. Applying this, we get that

$$\int_0^1 \cos^2(2\pi m \cdot)\; d\cdot = 2[\frac{\cdot}{2}+\frac{\sin(4\pi m \cdot)}{8\pi}]\bigg|_0^1 = 1 + 0 -(0+0) = 1.$$

<br/>

$\underline{\langle \cos(2\pi 0 \cdot), \cos(2\pi 0 \cdot)\rangle}$


$$ \langle 1, 1 \rangle = \int_0^1 1 \; d\cdot = 1.$$

Because all of the functions are also orthonormal, we have proved that the functions form an orthonormal system.

## 1 c)

In this task, we want to use the previous results to find orthonormal bases for the given spaces $\mathcal{T_n}$ and $\mathcal{S_n}$. To do this, we use the Gram-Schmidt method.

$\underline{\text{For space }\mathcal{T_n}:}$

We choose $u_1 = e^{-2\pi i n \cdot}$. In a) we already proved this function was orthonormal, and therefore we can set $e_1 = u_1 = e^{-2\pi i n \cdot}.$

Next, we choose $v_2 = e^{-2\pi i (n+1) \cdot}$.  Gram-Schmidt tells us that

$$u_2 = v_2 - \frac{\langle v_2, u_1\rangle}{\langle u_1,u_1\rangle}u_1.$$

Plugging our values into this formula, we get

$$u_2 = e^{-2\pi i (n+1) \cdot} - \frac{\langle e^{-2\pi i (n+1) \cdot}, e^{-2\pi i n \cdot}\rangle}{\langle e^{-2\pi i n \cdot},e^{-2\pi i n \cdot}\rangle}e^{-2\pi i n \cdot}.$$


Using the results from a), the inner product in the numerator becomes zero, and thus that whole term is zero. We are then left with only 

$$u_2 = v_2 = e^{-2\pi i (n+1) \cdot}$$

If we set $-n+1 = k$, we see that this function is also orthonormal as shown in a), and we can set $e_2 = u_2 = e^{-2\pi i (n+1) \cdot}.$

If we continue our calculations, we see that our pattern repeats, and the fraction term will always end up being zero. We can therefore conclude that an orthonormal basis for $\mathcal{T_n}$ is

$$
\mathcal{{B_T}_n} = \{ e^{2\pi i m \cdot}, \; m=-n, -n+1,\dots,n-1,n\}
$$

<br/>

$\underline{\text{For space }\mathcal{S_n}:}$

We choose $u_1 = \cos(0\cdot) = 1$ to be our first function. In b) we already proved this function was orthonormal, and therefore we can set $e_1 = u_1 = 1.$

Next, we choose $v_2 = \cos(2\pi\cdot)$. With Gram-Schmidt, this gives us 

$$u_2 = \cos(2\pi\cdot) - \frac{\langle \cos(2\pi\cdot), 1\rangle}{\langle 1,1\rangle}1.$$

From b) we have that 
$$\langle \sqrt{2}\cos(2\pi m \cdot), 1\rangle = 0,$$
and seeing as cosine is $2\pi$ periodic and $\sqrt{2}$ only scales the integral, the inner product in our numerator also equals zero. This leaves us with $u_2 = \cos(2\pi\cdot)$, which we need to normalize. 

From the project introduction we have that $\lVert f\rVert = \sqrt{\langle f,f \rangle}$. From b), we also have that $\langle \sqrt{2}\cos(2\pi m \cdot), \sqrt{2}\cos(2\pi m \cdot)\rangle = \sqrt{2}\cdot\sqrt{2}\cdot \frac{1}{2} = 1.$ This means that 

$$\langle \cos(2\pi \cdot), \cos(2\pi \cdot)\rangle =  \frac{1}{2} \Rightarrow \lVert \cos(2\pi \cdot)\rVert = \frac{1}{\sqrt{2}}$$

$$\Rightarrow e_2 = \frac{u_2}{\lVert \cos(2\pi \cdot)\rVert} =\sqrt{2}\cos(2\pi \cdot).$$

We can see that this pattern repeats until we reach the term $\cos(2\pi n)$ in the span.

We now choose $v_{n+1} = \sin(2\pi \cdot)$. Again, using Gram Schmidt, we get

$$u_{n+1} = \sin(2\pi\cdot) - \frac{\langle \sin(2\pi\cdot), \cos(2\pi n)\rangle}{\langle \cos(2\pi n),\cos(2\pi n)\rangle}\cos(2\pi n).$$

In b), we proved that 
$$\langle \sqrt{2} \sin(2\pi n\cdot), \sqrt{2} \cos(2\pi m)\rangle = 0 \; \Rightarrow \langle \sin(2\pi \cdot), \cos(2\pi n)\rangle = 0.$$

We are then left with $u_{n+1} = \sin(2\pi\cdot)$, which we then normalize.

$$\lVert \sin(2\pi \cdot)\rVert = \sqrt{\langle \sin(2\pi \cdot), \sin(2\pi \cdot) \rangle} = \frac{1}{\sqrt{2}},$$

which we obtained by using the same thought process as we did for $\lVert \cos(2\pi \cdot)\rVert$.

$$\Rightarrow e_{n+1} = \frac{u_{n+1}}{\lVert \sin(2\pi \cdot)\rVert} =\sqrt{2}\sin(2\pi \cdot).$$

As for the cosine terms, this pattern of calculating the sine terms repeats until we reach the final term, $\sin(2\pi n \cdot)$.

From our calculations, we can therefore conclude that an orthonormal basis for $\mathcal{S_n}$ is


$$
\mathcal{{B_S}_n} = \{ \cos(0 \cdot), \sqrt{2}\cos(2\pi m \cdot), \sqrt{2}\sin(2\pi m \cdot),\; m= 1, 2,\dots,n\}
$$
<br/>

$\underline{\text{Are both spaces the same?}:}$

If we rewrite $\mathcal{{B_T}_n}$ using eulers identity, we get 

$$
\mathcal{{B_T}_n} = \{ \cos(2\pi m\cdot)+i\sin(2\pi m \cdot), \; m=-n, -n+1,\dots,n-1,n\}
$$


and we have

$$
\mathcal{{B_S}_n} = \{ \cos(0 \cdot), \sqrt{2}\cos(2\pi m \cdot), \sqrt{2}\sin(2\pi m \cdot),\; m= 1, 2,\dots,n\}
$$

The first term of $\mathcal{{B_S}_n}$ equals 1, and when $m=0$ in $\mathcal{{B_T}_n}$, it also equals 1.

If we look at the case where $m=-n$ in $\mathcal{{B_T}_n}$, we get 

$$ \cos(-2\pi n\cdot)+i\sin(-2\pi n \cdot) = \cos(2\pi n\cdot)-i\sin(2\pi n \cdot)$$

<br/>

$\underline{\text{The dimension of }\mathcal{T_n}:}$

Seeing as $\mathcal{T_n}$ is spanned by $n+n+1$ functions, we conclude that the dimension of $\mathcal{T_n} = 2n+1$. 

## 1 d)

We now want to prove that

$$a_k = 2\langle f, \cos(2\pi k \cdot)\rangle = 2\int_{-\frac{1}{2}}^{\frac{1}{2}}f(x)\cos(2\pi k x) dx, \quad k=0,1,\dots,n$$

and 
$$b_k = 2\langle f, \sin(2\pi k \cdot)\rangle = 2\int_{-\frac{1}{2}}^{\frac{1}{2}}f(x)\sin(2\pi k x) dx, \quad k=1,2,\dots,n$$

by using $\mathcal{S_n}$ from 1 c).

$\underline{\text{Proof }a_k: }$

$$2\int_{-\frac{1}{2}}^{\frac{1}{2}}f(x)\cos(2\pi k x) dx
= 2\int_{-\frac{1}{2}}^{\frac{1}{2}}(\frac{a_0}{2}+\sum_{m=1}^na_m\cos(2\pi m x)+b_m \sin(2\pi m x))\cos(2\pi k x) \;dx$$

$$= 2\int_{-\frac{1}{2}}^{\frac{1}{2}}\frac{a_0\cdot\cos(2\pi k x)}{2}+\sum_{m=1}^na_m\cos(2\pi k x)\cos(2\pi m x)+b_m\cos(2\pi k x)\sin(2\pi m x) \;dx.$$

We can see that the first and last terms equals zero by their symmetry on the integration interval, and we are left with

$$2\sum_{m=1}^n a_m\int_{-\frac{1}{2}}^{\frac{1}{2}}\cos(2\pi k x)\cos(2\pi m x) \;dx.$$

(We can swap the sum and integration symbols without altering the expression.)

From previous calculations, we have shown that 

$$
\langle \cos(2\pi m x),\cos(2\pi k x)\rangle =\int_0^1 \cos(2\pi m x)\cos(2\pi k x) =
\begin{cases}
\frac{1}{2}&\text{if  } m=k \\
0 &else.
\end{cases}
$$

This means that each element in the sum will be zero, except the one where $m=k$, and we get

$$2\cdot a_k\int_{-\frac{1}{2}}^{\frac{1}{2}}\cos(2\pi k x)\cos(2\pi k x) \;dx = 2\cdot a_k \cdot \frac{1}{2}= a_k.$$

<br/>


$\underline{\text{Proof }b_k: }$

$$2\int_{-\frac{1}{2}}^{\frac{1}{2}}f(x)\sin(2\pi k x) dx
= 2\int_{-\frac{1}{2}}^{\frac{1}{2}}(\frac{a_0}{2}+\sum_{m=1}^na_m\cos(2\pi m x)+b_m \sin(2\pi m x))\sin(2\pi k x) \;dx$$

$$= 2\int_{-\frac{1}{2}}^{\frac{1}{2}}\frac{a_0\cdot\sin(2\pi k x)}{2}+\sum_{m=1}^na_m\sin(2\pi k x)\cos(2\pi m x)+b_m\sin(2\pi k x)\sin(2\pi m x) \;dx.$$

We can see that the first and second terms equals zero by their symmetry on the integration interval, and we are left with

$$2\sum_{m=1}^n b_m\int_{-\frac{1}{2}}^{\frac{1}{2}}\sin(2\pi k x)\sin(2\pi m x) \;dx.$$

We again have that 

$$
\langle \sin(2\pi m x),\sin(2\pi k x)\rangle =\int_0^1 \sin(2\pi m x)\sin(2\pi k x) =
\begin{cases}
\frac{1}{2}&\text{if  } m=k \\
0 &else.
\end{cases}
$$

This means that each element in the sum will be zero, except the one where $m=k$, and we get

$$2\cdot b_k\int_{-\frac{1}{2}}^{\frac{1}{2}}\sin(2\pi k x)\sin(2\pi k x) \;dx = 2\cdot b_k \cdot \frac{1}{2}= b_k.$$

## 1 e)

We want to use the composite trapezoidal rule to show that 

$$
c_k(f) \approx \hat{f}_k := \frac{1}{N} \sum_{j=0}^{N-1} f_j e^{-2\pi ijk/N}.
$$


The composite trapezoidal rule is given by

Certainly! Here's the composite trapezoidal rule written in LaTeX notation:

$$
\int_{a}^{b} f(x) \, dx \approx \frac{h}{2} \left[ f(a) + 2\sum_{j=1}^{n-1} f(a+jh) + f(b) \right]
$$

Looking at equidistant points, $h= \frac{1}{N}$, and we get

$$c_k(f) \approx  \frac{1}{2N}\left[ f(x_0)e^{-2\pi i0k} + 2\sum_{j=1}^{N-1-1} f(x_0+x_j)e^{-2\pi ik(0+\frac{j}{N})} + f(x_{N-1})e^{-2\pi ik(N-1)} \right]$$

$$=\frac{1}{2N}\left[ f_0e^{-2\pi i0k} + 2\sum_{j=1}^{N-2} f_je^{-2\pi ikj/N} + f_{N-1}e^{-2\pi ik(N-1)} \right]$$

We now change the limits of the sum, and add and subtract the corresponding terms.

$$=\frac{1}{2N}\left[ f_0e^{-2\pi i0k} -2f_0e^{-2\pi i0k} + 2\sum_{j=0}^{N-1} f_je^{-2\pi ikj/N} + f_{N-1}e^{-2\pi ik(N-1)} - 2f_{N-1}e^{-2\pi ik(N-1)}\right]$$

THIS TERM IS NOT RIGHT SE PÅ PERIODISK!!!!!!!!!!!!!!!!!!!!!

$$=\frac{1}{2N}\left[ 2\sum_{j=0}^{N-1} f_je^{-2\pi ikj/N}\right] = \frac{1}{N}\sum_{j=0}^{N-1} f_je^{-2\pi ikj/N}$$


$\underline{\text{Show that }\hat{f_k} \text{ is }N \text{-periodic}:}$

$$\frac{1}{N}\sum_{j=0}^{N-1} f_je^{-2\pi i(k+N)j/N} = \frac{1}{N}\sum_{j=0}^{N-1} f_je^{-2\pi ikj/N}e^{-2\pi ij}.$$

We can rewrite the last e-term as $\cos(-2\pi j)+i\sin(-2\pi j).$ Since j is a positive integer, this is equal to $\cos(-2\pi)+i\sin(-2\pi) = 1 + 0=1.$

This leaves us with 
$$\frac{1}{N}\sum_{j=0}^{N-1} f_je^{-2\pi ikj/N}e^{-2\pi ij} = \frac{1}{N}\sum_{j=0}^{N-1} f_je^{-2\pi ikj/N}\cdot 1 =\frac{1}{N}\sum_{j=0}^{N-1} f_je^{-2\pi ikj/N},$$

which shows us that $\hat{f_k}$ is $N$-periodic.

## 1 f)
We want to prove that
$$
\frac{1}{N}\sum_{j=0}^{N-1} e^{-2\pi ijk/N} =
\begin{cases}
1 & \text{if } k \mod N \equiv 0, \\
0 & \text{otherwise}.
\end{cases}
$$

$\underline{\text{Case: }k \mod N \equiv 0:}$

If $k \mod N \equiv0$, $k$ is either 0 or a multiple of $N$. We can therefore rewrite the sum as

$$\frac{1}{N}\sum_{j=0}^{N-1} e^{-2\pi ijs},$$

where s is an integer. Rewriting this in cosines and sines, we see that each entry of the sum equals 1, giving us $\frac{1}{N}\cdot N = 1$, which was what we wanted to prove.

$\underline{\text{Case: }0 \text{ otherwise}:}$

To prove this we use properties of geometric series.

We know that for a geometric series,

$$ \sum_{k=0}^{n-1}ar^k=
\begin{cases}
\frac{a(1 - r^n)}{1 - r} & \text{if } r \neq 1\\
an & \text{if } r=1
\end{cases}.
$$

We rewrite our sum and get

$$
\sum_{j=0}^{N-1} \frac{1}{N}(e^{-2\pi ik/N})^j = \frac{\frac{1}{N}(1 - (e^{-2\pi ik/N})^N)}{1 - e^{-2\pi ik/N}} = \frac{\frac{1}{N}(1 - e^{-2\pi ik})}{1 - e^{-2\pi ik/N}} = \frac{\frac{1}{N}(1 - 1)}{1 - e^{-2\pi ik/N}} = 0.
$$

## 1 g)

We want to prove

$$
\text{circ}(\textbf{a}) = \frac{1}{N} \overline{\text{F}_N} \text{diag}(\hat{\textbf{a}}) \text{F}_N
$$

We know that 

$$\hat{\textbf{a}}=\text{F}_N\textbf{a}= (e^{-2\pi ikl/N})_{k,l=0}^{N-1}\times(a_0, ..., a_{N−1})^T = (\sum_{l=0}^{N-1}a_le^{-2\pi ikl/N})_{k=0}^{N-1},$$

$\Rightarrow \text{diag}(\hat{\textbf{a}})$ has these elements on the diagonal. We denote these elements $\hat{\textbf{a}}_q$

Next we calculate 

$$\text{diag}(\hat{\textbf{a}}) \text{F}_N = 
\begin{bmatrix}
\hat{\textbf{a}}_0 & 0 & \dots & 0 \\
0 & \hat{\textbf{a}}_1 & \dots & 0 \\
\vdots & \dots & \ddots & \vdots \\
0 & \dots & 0 & \hat{\textbf{a}}_{N-1}
\end{bmatrix} \times (e^{-2\pi ikl/N})_{k,l=0}^{N-1}

=

\begin{bmatrix}
\hat{\textbf{a}}_0e^{-2\pi i00/N} & \hat{\textbf{a}}_0e^{-2\pi i01/N} & \dots & \hat{\textbf{a}}_0e^{-2\pi i0(N-1)/N} \\
\vdots & \ddots &  & \vdots \\
\vdots &  & \ddots & \vdots \\
\hat{\textbf{a}}_{N-1}e^{-2\pi i(N-1)0/N} & \hat{\textbf{a}}_{N-1}e^{-2\pi i(N-1)1/N} & \dots & \hat{\textbf{a}}_{N-1}e^{-2\pi i(N-1)(N-1)/N}
\end{bmatrix},
$$

And use this to calculate 

$$\frac{1}{N}\overline{\text{F}_N}\text{diag}(\hat{\textbf{a}}) \text{F}_N = 
\begin{bmatrix}
e^{2\pi i00/N} & e^{2\pi i01/N} & \dots & e^{2\pi i0(N-1)/N} \\
\vdots & \ddots &  & \vdots \\
\vdots &  & \ddots & \vdots \\
e^{2\pi i(N-1)0/N} & e^{2\pi i(N-1)1/N} & \dots & e^{2\pi i(N-1)(N-1)/N}
\end{bmatrix}\times
\begin{bmatrix}
\hat{\textbf{a}}_0e^{-2\pi i00/N} & \hat{\textbf{a}}_0e^{-2\pi i01/N} & \dots & \hat{\textbf{a}}_0e^{-2\pi i0(N-1)/N} \\
\vdots & \ddots &  & \vdots \\
\vdots &  & \ddots & \vdots \\
\hat{\textbf{a}}_{N-1}e^{-2\pi i(N-1)0/N} & \hat{\textbf{a}}_{N-1}e^{-2\pi i(N-1)1/N} & \dots & \hat{\textbf{a}}_{N-1}e^{-2\pi i(N-1)(N-1)/N}
\end{bmatrix},
$$

and the result of the matrix multiplication we will denote as matrix $A$.

We will now look at a few of the elements in A.

$$A_{10}= \frac{1}{N}(\sum_{q=0}^{N-1}\hat{\textbf{a}}_qe^{-2\pi iq0/N}e^{2\pi i1q/N}) = \frac{1}{N}\sum_{q=0}^{N-1}\hat{\textbf{a}}_qe^{2\pi iq/N} = \frac{1}{N}\sum_{q=0}^{N-1}\sum_{s=0}^{N-1}a_se^{-2\pi iqs/N}e^{2\pi iq/N} $$

$$
=\frac{1}{N}\sum_{s=0}^{N-1}a_s\sum_{q=0}^{N-1}e^{-2\pi iq(s-1)/N}.$$

We know from before that this sum only equals 1 if $s-1 \mod N \equiv 0$, and equals 0 for any other values. Since the sum only goes to $N-1$, this is only true when $s-1 = 0 \Rightarrow s=1.$ Therefore, we get

$$
\frac{1}{N}\sum_{s=0}^{N-1}a_s\sum_{q=0}^{N-1}e^{-2\pi iq(s-1)/N} = \frac{1}{N}a_1\sum_{q=0}^{N-1}e^0= a_1.$$


Next, we look at $A_{01}$

$$A_{01}= \frac{1}{N}(\sum_{q=0}^{N-1}\hat{\textbf{a}}_qe^{-2\pi iq1/N}e^{2\pi i0q/N}) = \frac{1}{N}\sum_{q=0}^{N-1}\hat{\textbf{a}}_qe^{-2\pi iq/N} = \frac{1}{N}\sum_{q=0}^{N-1}\sum_{s=0}^{N-1}a_se^{-2\pi iqs/N}e^{-2\pi iq/N} $$

$$
=\frac{1}{N}\sum_{s=0}^{N-1}a_s\sum_{q=0}^{N-1}e^{-2\pi iq(s+1)/N}.$$

This sum only equals 1 if $s+1 \mod N \equiv 0$. Since the sum starts in 0 and goes to $N-1$, this is only true when $s+1 = N \Rightarrow s=N-1.$ Therefore, we get

$$
\frac{1}{N}\sum_{s=0}^{N-1}a_s\sum_{q=0}^{N-1}e^{-2\pi iq(s+1)/N} = \frac{1}{N}a_{N-1}\sum_{q=0}^{N-1}e^{-2\pi iq} = a_{N-1}.$$

Having showed these two elements, we can assume these properties extend to the rest of the matrix, and we have proved what we wanted.

Further, we want to derive an expression for $\text{F}_N^{-1}$

We know that a property of matrices is that $\text{F}_N^{-1}\text{F}_N = \text{F}\text{F}_N^{-1} = I$.

If we assume that $\text{F}_N^{-1}$ is on the same form as $\text{F}_N$, we can calculate

$$\text{F}_N\text{F}_N^{-1} = (e^{-2\pi ikl/N})_{k,l=0}^{N-1}\times (e^{-2\pi iab/N})_{a,b=0}^{N-1}=\text{F}.
$$

If we look at F$_{00}$ we get

$$
\text{F}_{00}= \sum_{l=0}^{N-1}e^{-2\pi i0l/N}e^{-2\pi ia0/N} = \sum_{l=0}^{N-1}1 = \frac{1}{N}.
$$

However, we want this to equal 1, and we can conclude that the expression for the inverse contains a $\frac{1}{N}$.

Next, we look at F$_{11}$:

$$
\text{F}_{11}= \sum_{l=0}^{N-1}e^{-2\pi i1l/N}e^{-2\pi il1/N} = \sum_{l=0}^{N-1} e^{-2\pi i(l+l)/N}.
$$

But for this to equal 1,  we want $-2\pi i(l+l)/N =0$, which only holds if $l=-l$. This we can fix by taking the complex conjugate of our matrix we use for $\text{F}_N^{-1}$, and we can conlude that 

$$\text{F}_N^{-1}=\frac{1}{N}\overline{\text{F}_N}.$$

## 1 h)

For which cases does $\textit{\textbf{f}}$ approximate $\textit{f}$ well?

We see that for all $\textit{\textbf{f}}$ with $N=257$, $\textit{\textbf{f}}$ approximates $\textit{f}$ well. However, for $\textit{f}_3$ and $\textit{f}_4$, $\textit{\textbf{f}}$ with $N=5$ and $N=17$ also approximates well.

## 1 i)

i)

We know from c) that 
$$f(x)= \frac{a_0}{2}+\sum_{k=1}^{n}a_k\cos(2\pi k x) + b_k\sin(2\pi k x)$$

which should also equal

$$f_2 = \sin(32 \pi x) + \cos(128 \pi x).$$

From this we see that $a_64 = 1, b_16 = 1$ and all others equal 0. 

ii)
We also know that 

$$f(x)= \sum_{k=-n}^{n}c_ke^{2\pi i k x}.$$

If we rewrite $f_2$ as

$$f(x) = \frac{e^{2\pi 16 x}-e^{-2\pi 16 x}}{2i}+\frac{e^{2\pi 64 x}+e^{-2\pi 64 x}}{2}$$

$c_0 = 1$

iii)

The fftshift function simply moves the 0 on the frequency axis to the middle of the axis(in our case the x-axis).

iv) 


## Task 2

### 2 a)

We have that 
$$c_0 =(\textbf{a}\ast\textbf{b})_0 = \sum_{k=0}^{N-1}a_kb_{0-k \mod N} = a_0b_0 + a_1b_{N-1} + a_2b_{N-2} +\dots$$

and 

$$c_1=(\textbf{a}\ast\textbf{b})_1 = \sum_{k=0}^{N-1}a_kb_{1-k \mod N} = a_0b_1 + a_1b_0 + a_2b_{N-1} +\dots$$


Then, if we calculate 

$$c'_1=(\textbf{a}\ast\textbf{b'})_1 = \sum_{k=0}^{N-1}a_kb'_{1-k \mod N} = \sum_{k=0}^{N-1}a_kb_{1-1-k \mod N}= a_0b_0 + a_1b_{N-1} + a_2b_{N-2} +\dots.$$

From this we see that $c'_1 = c_{0}$ and we can conclude that $c'_j=c_{j-1}$.

### 2 b)
i)
We want to prove that $c_k(f\ast)g$ = $c_k(f)c_k(g)$.

We have that 
$$c_k(f\ast)g = \int_0^1 (f\ast g)(x)e^{-2\pi i k x}\; dx = \int_0^1 \int_0^1 f(y)g(x-y)e^{-2\pi i k x}\; dy dx = \int_0^1 f(y) \int_0^1g(x-y)e^{-2\pi i k x}\; dx dy.$$

Using $u=x-y$, we get $x = u+y$, and $du=dx$.

$$\int_0^1f(y)e^{-2\pi i k y}\int_0^1g(u)e^{-2\pi i k u}\; du dy = c_k(f)c_k(g)$$

ii)

We now want to prove that $\hat{(\textbf{a}\ast\textbf{b})}=\hat{\textbf{a}}\circ\hat{\textbf{b}}.$

$$\hat{(\textbf{a}\ast\textbf{b})} = \mathcal{F}_N(\textbf{a}\ast\textbf{b}) = \mathcal{F}_N(\sum_{k=0}^{N-1}a_kb_{j-k \mod N})_{j=0}^{N-1}.$$

If we look at $\hat{(\textbf{a}\ast\textbf{b})}_0$, we get

$$\hat{(\textbf{a}\ast\textbf{b})}_1= \sum_{k=0}^{N-1}e^{-2\pi i 0k/N}(\sum_{k=0}^{N-1}a_kb_{j-k \mod N})_{j=0}^{N-1}= \sum_{k=0}^{N-1}e^{-2\pi i 0k/N}a_k(\sum_{k=0}^{N-1}b_{j-k \mod N})_{j=0}^{N-1}$$

We want to look at $\hat{\textbf{a}}\circ\hat{\textbf{b}}$. We have that $\hat{\textbf{a}} = \mathcal{F_N}\textbf{a}$ and $\hat{\textbf{b}} = \mathcal{F_N}\textbf{b}$

We can rewrite this matrix as 

$$\hat{\textbf{a}} = 
\begin{bmatrix}
\sum_{l=0}^{N-1}e^{-2\pi i 0l/N}a_l\\
\vdots \\
\sum_{l=0}^{N-1}e^{-2\pi i (N-1)l/N}a_l
\end{bmatrix}
$$

and similarly:

$$\hat{\textbf{b}} = 
\begin{bmatrix}
\sum_{l=0}^{N-1}e^{-2\pi i 0l/N}b_l\\
\vdots \\
\sum_{l=0}^{N-1}e^{-2\pi i (N-1)l/N}b_l
\end{bmatrix}
$$

which gives us for instance

$$(\hat{\textbf{a}}\circ \hat{\textbf{b}})_0 = \sum_{l=0}^{N-1}e^{-2\pi i 0l/N}a_l\cdot\sum_{l=0}^{N-1}e^{-2\pi i 0l/N}b_l.$$

We see that this is the same as before, and thus we have proved that $\hat{(\textbf{a}\ast\textbf{b})}=\hat{\textbf{a}}\circ\hat{\textbf{b}}.$

This simplifies the prouct $\text{circ}(\textbf{a})\text{circ}(\textbf{b})$ because if we write out this product, we get 

$$\frac{1}{N} \overline{\text{F}_N}\text{diag}(\hat{\textbf{a}}) \text{F}_N\frac{1}{N} \overline{\text{F}_N} \text{diag}(\hat{\textbf{b}}) \text{F}_N = \frac{1}{N^2} \overline{\text{F}_N} \text{diag}(\hat{\textbf{a}}) I \text{diag}(\hat{\textbf{b}}) \text{F}_N = \frac{1}{N^2} \overline{\text{F}_N} \text{diag}(\hat{\textbf{a}}\circ\hat{\textbf{b}}) \text{F}_N.$$

# 2 c)

We want to compute the Fourier coefficients of the Dirichlet kernel given by

$$D_n(x)= 1 + 2 \sum_{k=1}^n \cos(2\pi k x), n \in \mathbb{N}.
$$

We get the expression

$$c_k(D_n(x)= \int_0^1 (1 + 2 \sum_{s=1}^n \cos(2\pi s x))e^{-2\pi i k x}\;dx = \int_0^1e^{-2\pi i k x}\; dx + 2\int_0^1 e^{-2\pi i k x}\sum_{s=1}^n \cos(2\pi s x)$$

Looking at the first integral, this yields

$$
\begin{cases}
1 & \text{if } k=0 \\
0 & else.
\end{cases}
$$

Looking at the second term, we can rewrite this as 

$$
\int_0^1e^{-2\pi i k x}\sum_{s=1}^n(e^{2\pi i s x}+e^{-2\pi i s x})\; dx = \sum_{s=1}^n\int_0^1e^{-2\pi i k x}e^{2\pi i s x}+e^{-2\pi i k x}e^{-2\pi i s x}\; dx 
$$

$$
= \sum_{s=1}^n\langle e^{-2\pi i k x},e^{-2\pi i s x}\rangle+\langle e^{-2\pi i k x},e^{2\pi i s x}\rangle.
$$

From earlier in the assignment, we know that these inner products are only equal 

