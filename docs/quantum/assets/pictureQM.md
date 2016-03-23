> Read on [StackEdit](https://stackedit.io/viewer#!url=https://raw.github.com/emptymalei/quantum/master/QM2/pictureQM.md).


$\newcommand{\bra}[1]{\left\langle #1\right|}
\newcommand{\ket}[1]{\left| #1\right\rangle}$

Three pictures in QM.

| Aspects        | Schrödinger Picture           | Heisenberg Picture  | Dirac Picture   |
|:-------------:|:-------------:|:-----:|:-----------:|
| Hamiltonian   | $$\hat H$$  |  $$\hat H_H$$  | $$\hat H_0+\hat W(T)$$ |
| State      |  \begin{equation*}\ket{\psi}_S = \ket{\psi(t)}\end{equation*}  |  \begin{align*}\ket{\psi}_H &=\hat U(t,t_0)^{-1}\ket{\psi}_S\\&= \ket{\psi(t_0)}  \end{align*}  |  \begin{align*} \ket{\psi}_I & = \hat U_0^{-1} \ket{\psi}_S  \\  &= e^{i\hat H_0 (t-t_0)/\hbar} \ket{\psi}_S \end{align*}  |
| Operators   | $$\hat \Omega_S = \hat \Omega(t)$$  |  \begin{align*} \hat \Omega_H &= \hat \Omega(t) \\ & = \hat U^{-1} \hat\Omega_S \hat U \end{align*}  | \begin{align*} \hat \Omega_I &= \hat U_0^{-1}\Omega_S \hat U_0   \end{align*} |
| EoM      | \begin{equation*}i\hbar \frac{d}{dt}\hat U = \hat H \hat U \end{equation*} | \begin{align*} \frac{d}{dt}\hat \Omega_H = \frac{1}{i\hbar} [\hat \Omega_H,\hat H_H] + \frac{\partial}{\partial t} \hat \Omega_H \end{align*} | \begin{align*} i\hbar \frac{d}{dt} \ket{\psi}_I &= \hat W_I \ket{\psi}_I \\  \frac{d}{dt} \hat\Omega_I &= \frac{1}{i\hbar} \left[\hat\Omega_I, \hat H_0 \right] + \frac{\partial}{\partial t}\hat\Omega_I \end{align*}  |
| Observables      |  |  |  |
| Propagator      | $$\hat U$$  | $$\hat U$$  |  $$\hat U_I$$  |
| Equation of Propagator      | \begin{equation*}i\hbar\frac{d}{dt}\hat U= \hat H\hat U\end{equation*} | -  | \begin{equation*}i\hbar \frac{d}{dt}\hat U_I = \hat W_I \hat U_I\end{equation*} |
| Observables      |  |  |  |

Notice that in Dirac picture, $\hat W_I = \hat U_0 ^{-1}\hat W \hat U_0 $, $\ket{\psi(t)}_I = \hat U_I \ket{\psi(0)}_I$.


