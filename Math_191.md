# Calculus II Notes

Washington University in St. Louis

Created for ‘Calculus II’ (Math 191)

Nathaniel Hayman

## Integration Techniques

### *Integration by Parts*

$$
\int_a^budv=uv|_a^b-\int_a^bvdu
$$

A helpful trick for solving integration by parts problems is the acronym **********ILATE**********:

- **Inverse Trigonometric Functions** ($\sin^{-1}x,\cos^{-1}x$)
- ************Logarithmic Functions************ ($\log x, \ln x$)
- **********************Algebraic Functions********************** ($x,x^2,\sqrt x$)
- ********************************Trigonometric Functions******************************** ($\sin x,\cos x$)
- ******************************************Exponential Functions****************************************** ($e^x,2^x$)

$$
\begin{pmatrix}
      I & u\\
      L & u\\
      A & u\lor v\\
      T & v\\
      E & v
\end{pmatrix}
$$

### *Trigonometric Substitution*

$$
\sqrt{a^2-b^2x^2}\Rightarrow x=\frac{a}{b}\sin\theta
$$

$$
\sqrt{a^2+b^2x^2}\Rightarrow x=\frac{a}{b}\tan\theta
$$

$$
\sqrt{b^2x^2-a^2}\Rightarrow x=\frac{a}{b}\sec\theta
$$

## Sequences

### *Convergence*

A given sequence $a_n$ is said to converge if

$$
\lim_{n\to\infty}a_n=k
$$

Where $k\in\R$ is finite (not $-\infty$ or $\infty$).

If $\lim_{n\to\infty}a_n$ is not finite, then $a_n$ is said to diverge.

## Series

For some series $\sum a_n$:

### *P-Series Definition*

$$
a_n=\frac{1}{n^p}\land p>1\implies \sum_{n=0}^{\infty}a_n\small\text{ converges}
$$

### *Geometric Series Definition*

$$
(a_n=ar^n\lor a_n=ar^{n+1})\land|r|<1\implies\sum_{n=0}^{\infty}a_n\small\text{ converges}
$$

### *Divergence Test*

$$
\lim_{n\to\infty}a_n\nless\infty\implies \sum_{n=0}^{\infty}a_n\small\text{ diverges}
$$

Note that the divergence test does not guarantee convergence, just divergence or lack thereof

### *Integral Test*

For $f(n)=a_n$:

$$
\int_{k}^{\infty}f(x)dx<\infty\implies\int_{k}^{\infty}f(x)\small\text{ converges}
$$

$$
\int_{k}^{\infty}f(x)\small\text{ converges}\implies\normalsize \sum_{n=k}^{\infty}\small\text{ converges}
$$

$$
\int_{k}^{\infty}f(x)\small\text{ diverges}\implies\normalsize \sum_{n=k}^{\infty}\small\text{ diverges}
$$

### ***************Comparison Test***************

If some series $\sum a\prime_n$ is known to converge,

$$
a_n<a\prime_n\implies \sum_{n=0}^{\infty}a_n\small\text{ converges}
$$

If that same series were instead known to ********diverge********,

$$
a_n\prime<a_n\implies \sum_{n=0}^{\infty}a_n\small\text{ diverges}
$$

### *Limit Comparison Test*

If some series $\sum a\prime_n$ is known to converge,

$$
0<\lim_{n\to\infty}\frac{a_n}{a\prime_n}<\infty\implies\small\text{both series either converge or diverge}
$$

### *Alternating Series Test*

If $a_n=(-1)^nb_n$ or $a_n=(-1)^{n+1}b_n$ for some $b_n\geq0$ for all $n$,

$$
\lim_{n\to\infty}b_n=0\land \{b_n\}\small\text{ is decreasing}\implies \sum_{n=0}^{\infty}a_n\small\text{ converges}
$$

### *Conditional Convergence*

- If $\sum a_n$ is convergent and $\sum|a_n|$ is convergent, $a_n$ is absolutely convergent
- If $\sum a_n$ is convergent and $\sum|a_n|$ is divergent, $a_n$ is conditionally convergent

### *Ratio Test*

$$
L=\lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|
$$

$$
L<1\implies\sum_{n=0}^{\infty}a_n\small\text{ is absolutely convergent}
$$

$$
L>1\implies\sum_{n=0}^{\infty}a_n\small\text{ is divergent}
$$

$$
L=1\implies \small\text{no conclusion}
$$

### *Root Test*

$$
L=\lim_{n\to\infty}\sqrt[n]{|a_n|}
$$

$$
L<1\implies\sum_{n=0}^{\infty}a_n\small\text{ is absolutely convergent}
$$

$$
L>1\implies\sum_{n=0}^{\infty}a_n\small\text{ is divergent}
$$

$$
L=1\implies \small\text{no conclusion}
$$

## Taylor Series

### *Definition*

A Taylor Series is defined as follows:

$$
\sum_{n=0}^{\infty}\frac{f^{(n)}(a)(x-a)^n}{n!}
$$

A McLaurin Series is Taylor Series centered around $a=0$:

$$
\sum_{n=0}^{\infty}\frac{f^{(n)}(0)x^n}{n!}
$$