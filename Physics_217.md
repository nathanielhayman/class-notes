# Physics 217 Notes

[217 Equation Sheet](https://www.notion.so/217-Equation-Sheet-79fff44d99e54c83b2c48ca5904ab013?pvs=21)

### The Postulates of Quantum Mechanics

1. The state of a physical system and all that you can determine about it is represented mathematically by a normalized ket $\ket{\psi}$
2. A physical observable is represented mathematically by a operator $\hat{A}$ that acts on kets
3. The only possible result of a measurement of an observable is one of the eigenvalues  $a_n$ of the corresponding operator $\hat{A}$
4. The probability of obtaining the eigenvalue $a_n$ in a measurement of the observable $\hat{A}$ on the system state $\ket{\psi}$ is (where $\ket{a_n}$ is the normalized eigenvector)

$$
P_{a_n}=|\braket{a_n|\psi}|^2
$$

1. After a measurement of $\hat{A}$ that yields the result $a_n$, the quantum system is in a new state that is the normalized projection of the original system ket onto the ket or kets corresponding to the result of the measurement

$$
\ket{\psi'}=\frac{P_n\ket{\psi}}{\sqrt{\braket{\psi|P_n|\psi}}}
$$

1. The time evolution of a quantum system is determined by the Hamiltonian of total energy operator $H(t)$ through the Shrodinger equation

$$
i\hbar\frac{d}{dt}\ket{\psi(t)}=H(t)\ket{\psi(t)}
$$

### Quantum State Vectors

Quantum state vectors are defined in a Hilbert Space, with a dimensionality of 2 in the most basic case.

- Spin $\frac{1}{2}$ system: $\ket{\plusmn}$ basis (in the $S_z$ basis)

We define the quantum state as the ***ket*** $\ket{\psi}$:

$$
\ket{\psi}=a\ket{+}+b\ket{-}
$$

Where the complex conjugate is defined as the ***bra*** $\bra{\psi}$

$$
\bra{\psi}=a^*\bra{+}+b^*\bra{-}
$$

The scalar product (analogous to the dot product between spatial vectors) between a bra and a ket forms the *************inner product************* or *******projection*******:

$$
\braket{bra|ket} = \bra{bra}\cdot\ket{ket}
$$

In a spin $\frac{1}{2}$ system:

$$
\text{\footnotesize normalization: } \begin{cases} \braket{+|+}=1\\
 \braket{-|-}=1 \end{cases}\\

\text{\footnotesize orthogonality: } \begin{cases} \braket{+|-}=0\\
 \braket{-|+}=0 \end{cases}\\

\text{\footnotesize completeness: } \ket{\psi}=a\ket{+}+b\ket{-}
$$

Thus, we define the spin $\frac{1}{2}$ system as orthonormal

Also,

$$
\braket{\phi|\psi}=\braket{\psi|\phi}^*
$$

All kets are defined to be normalized, so

$$
|a|^2+|b|^2=1\\
|\braket{+|\psi}|^2+|\braket{-|\psi}|^2=1
$$

These coefficients represent probabilities since they add to $1$:

$$
|\braket{\plusmn|\psi}|^2=P_{S_z=\plusmn\frac{\hbar}{2}}\\
$$

Physical measurements are defined by

$$
\braket{\hat{M}_{out}, \hat{M}_{in}}
$$

### Describing different spin orientations

In the spin $\frac{1}{2}$ system, the quantum state for spin along the $x$ axis can be derived as follows:

$$
\ket{+}_x=a'\ket{+}+b'\ket{-}\\

P_{1,+x}=|{}_x{\braket{+|+}}|^2=\frac{1}{2}\\

|a|^2=\frac{1}{2}\\

\ket{+}_x=\frac{1}{\sqrt{2}}[\ket{+}+e^{i\alpha}\ket{-}]\\
\ket{-}_x=\frac{1}{\sqrt{2}}[\ket{+}+e^{i\beta}\ket{-}]\\
$$

And since $\ket{\plusmn}_x$ are orthonormal on the $S_x$ basis:

$$
{}_x\braket{-|+}_x=0\implies e^{i\alpha}=-e^{i\beta}
$$

Resulting in

$$
\ket{\plusmn}_x=\frac{1}{\sqrt{2}}(\ket{+}\plusmn\ket{-})
$$

### General Quantum States

For quantized measurement results $a_n$ (on finite range $n$):

$$
\braket{a_i|a_j}=\delta_{ij}=\begin{cases}0 & i\neq j\\1 & i=j\end{cases}\\

\ket{\psi}=\sum_i\braket{a_j|\psi}\ket{a_j}\\

P_{a_n}=|\braket{a_n|\psi_{in}}|^2
$$

Note that the above defines the Kronecker Delta $\delta_{ij}$

### Matrix Representation

We can represent a general matrix $\hat{A}$ on the $S_z$ basis as follows

$$
\hat{A}\space\dot{=}\space\begin{pmatrix}a & b\\c & d\end{pmatrix}\\
$$

With the vector definition of a quantum state we can operate on said state with this matrix representation of a quantum operator, such as with the vector definition of the spin-up state

$$
\hat{A}\ket{+}=\begin{pmatrix}a & b\\c & d\end{pmatrix}\begin{pmatrix}1 \\0\end{pmatrix}=\begin{pmatrix}a\\c\end{pmatrix}
$$

It can be quickly noticed now that operating on this resultant vector element with a bra row vector in the same basis will yield a singular element of the operator matrix

$$
\braket{+|\hat{A}|+}=\begin{pmatrix}1 & 0\end{pmatrix}\begin{pmatrix}a \\ c\end{pmatrix}=a
$$

   Thus,

$$
\hat{A}\space\dot{=}\begin{pmatrix}\braket{+|\hat{A}|+} & \braket{+|\hat{A}|-}\\
\braket{-|\hat{A}|+} & \braket{-|\hat{A}|-}
\end{pmatrix}
$$

The above can then be generalized for a generic basis:

$$
\hat{A}_{ij}=\braket{i|\hat{A}|j}, \space\ket{\psi}=\sum_ic_i\ket{i}\\

\ket{\phi}=\hat{A}\ket{\psi}=\sum_i\sum_j\hat{A}_{ij}c_j\ket{i}
$$

Using this generalization, we can derive the *************eigenvectors************* and **eigenvalues** of a quantum state from its matrix representation using basic rules of matrix algebra

$$
\hat{A}\ket{a_n}=a_n\ket{a_n}\dot{=}\begin{pmatrix}\hat{A}_{11} & \hat{A}_{12}\\ \hat{A}_{21} & \hat{A}_{22}\end{pmatrix}\begin{pmatrix}c_{n1}\\c_{n2}\end{pmatrix}=a_n\begin{pmatrix}c_{n1}\\c_{n2}\end{pmatrix}
$$

Resulting in the following system of equations

$$
\begin{cases}
\begin{aligned}
(\hat{A}_{11}-a_n)c_{n1}+\hat{A}_{12}c_{n2}=0\\
\hat{A}_{21}c_{n1}+(\hat{A}_{22}-a_n)c_{n2}=0
\end{aligned}
\end{cases}
$$

This confirms the basic assumption of eigenvalues and eigenvectors for a classical example:

$$
\underbrace{\det(A-\lambda\mathbb{I})}_{\text{classical}}\to\underbrace{\det(\hat{A}-\lambda\mathbb{I})}_{\text{quantum}}=0
$$

### Spin Component in a General Direction

For polar and azimuthal angles $\theta$ and $\phi$, the projection $\hat{n}$ is defined as

$$
\hat{n}=\hat{i}\sin{\theta}\cos{\phi}+\hat{j}\sin{\theta}\sin{\phi}+\hat{k}\cos{\phi}
$$

Making the spin component along $\hat{n}$:

$$
S_{\hat{n}}=S\cdot\hat{n}=\hat{n}=S_x\sin{\theta}\cos{\phi}+S_y\sin{\theta}\sin{\phi}+S_z\cos{\phi}
$$

Thus,

$$
S_{\hat{n}}=\frac{\hbar}{2}\begin{pmatrix}\cos{\theta} & \sin{\theta}e^{-i\phi}\\ \sin{\theta}e^{i\phi} & -\cos{\theta}\end{pmatrix}
$$

Diagonalizing $S_{\hat{n}}$ yields

$$
\begin{aligned}\ket{+}_n=\cos{\frac{\theta}{2}}\ket{+}+\sin{\frac{\theta}{2}}e^{i\phi}\ket{-}\\
\ket{-}_n=\sin{\frac{\theta}{2}}\ket{+}-\cos{\frac{\theta}{2}}e^{i\phi}\ket{-}\end{aligned}
$$

The above represents ***all*** possible kets in a spin $\frac{1}{2}$ system given $0\leq\theta<\pi$ and $0\leq\phi<2\pi$