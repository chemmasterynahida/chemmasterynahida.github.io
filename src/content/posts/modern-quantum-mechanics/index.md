---
title: "Quantum Chemistry: 2.1. Heisenberg's quantum mechanics"
published: 2025-12-11
description: "How Heisenberg explained the quantum world?"
image: "heisenberg.jpg"
tags: ["Quantum Chemistry"]
category: Quantum Chemistry
lang: en
draft: False
---

# Heisenberg's quantum mechanics

Hello~ This is Chemistry Mastery Nahida.  
Last time, we talked about how atomic model was changed by time.  
**Bohr-Sommerfeld model** could explain the spectrum of hydrogen atom using **quantum hypothesis of angular momentum**.  
However, it did not focus on fine structures of spectrum, so the model was fail to explaining them.  
Even de Broglie provided the reason of the quantum hypothesis, but it is not related to the fine structure.  
The **modern quantum mechanics** are developed along explaining the small properties of the atom.  

Three physicists, **Werner Heisenberg**, **Erwin Schrödinger**, and **Paul Dirac**, tried to represent quantum nature of the atom in their own style.  

---

## Heisenberg's insight

Werner Heisenberg, a young physicist (born in 1901) in that time, proposed an outstanding idea:  

> What if there were no orbits from the first?  

He thought the Bohr model failed because Bohr has assumed the orbit. There is no evidence the orbit is necessary.  
He founded **modern quantum mechanics** by expressing the nature in very unique way.  

He wants to represent the nature only with observable amounts.  

He used very brilliant math for explaining quantum world. He suggested the matrix form of observables.  

In his *Umdeutung* (*reinterpretation* in German) paper, he noted the some physical amounts as:  
$$p=\{p_{nm}\},~x=\{x_{nm}\}$$

He noted observables between quantum number $n$ and $m$. The time dependence can be expressed using **discrete Fourier transformation**:  
$$A=\sum_{n,m}(A_{nm}e^{2\pi i\nu_{nm}t})$$
where $A$ is any type of physical amounts.  
(Fourier transformation is the expression of the observables from by time to by sum of frequencies.)  
![Fourier transformation](fourier-transform.png "Fourier transformation")  
Fourier transformation  

The position $x$ can be also written as:  
$$x(t)=\sum_{n,m}(x_{nm}e^{2\pi i\nu_{nm}t})$$
In matrix form:  
$$X(t)=(x_{nm}e^{2\pi i\nu_{nm}t})$$

How about $x^{2}$?  
He represented $x^{2}$ as:  
$$(x^{2})_{nm}(t)=\sum_{k}x_{nk}(t)x_{km}(t)=\sum_{n,m}(\sum_{k}x_{mk}x_{kn}e^{i(\omega_{nk}+\omega_{kn})t})$$
In matrix form:  
$$(X(t))^{2}=X(t)X(t)=(\sum_{k}x_{mk}x_{kn}e^{i(\omega_{nk}+\omega_{kn})t})$$
It seems complicated, but it's just a square of the **matrix** $X(t)$.  

How about $xy$ and $yx$?  
$xy$ can be represented as:  
$$(xy)_{nm}(t)=\sum_{k}x_{nk}(t)y_{km}(t)=\sum_{n,m}(\sum_{k}x_{mk}y_{kn}e^{i(\omega_{nk}+\omega_{kn})t})$$
$yx$ is:  
$$(yx)_{nm}(t)=\sum_{k}y_{nk}(t)x_{km}(t)=\sum_{n,m}(\sum_{k}y_{mk}x_{kn}e^{i(\omega_{nk}+\omega_{kn})t})$$
They are also **matrix multiplications** of $XY$ and $YX$.  
Like matrices, $xy\neq yx$.  

## Bohr-Sommerfeld model

Before this work, Bohr-Sommerfeld model has suggested the quantum hypothesis as:  
$$2\pi J=\oint_{c}pdx=nh$$
where $p$ is momentum, $q$ is position, and $J$ is action (unit=$J\cdot s$).  
(Action is time integration of Lagrangian ($J:=\int Ldt$, $L=T-V$). By Hamilton's principle, nature follows the route that minimising the value of action.)  
Please note that:  
> The definition above is from Hamiltonian mechanics. Bohr noted the action for periodic conitions as $J=\oint pdx$.  
> Heisenberg used Bohr's notation, so we must consider additional $2\pi$ for his actual paper.  
> I use action from Hamiltonian mechanics, so additional $2\pi$ is already applied.  

He noted frequency between $n$ and $m$ as:  
$$\nu(n,m)=\frac{E_{n}-E_{m}}{h}$$

He suggested **quantum frequency** between quantum numbers $n$, $m$, and $k$:  
$$\nu(n,m)=\frac{E(n)-E(m)}{h},~\nu(n,m)=\nu(n,k)+\nu(k,m)$$
For example, the energy for quantum number 1 to 3 is equal to sum of energies for 1 to 2 and 2 to 3.  
![Energy diagram](excitation.png "Energy diagram")  
Since energy is proportional to frequency, we can write frequency as sum of its components.  

Meanwhile, the classical frequency can be represented as:  
$$2\pi\nu(n,n-1)=\frac{dE}{dJ}$$

Therefore,  
$$2\pi\nu(n,n-1)=\frac{E_{n}-E_{m}}{\hbar}=\lim_{\Delta J\rightarrow 0}\frac{\Delta E}{\Delta J}=\frac{dE}{dJ}$$
Since quantum intervals are very small to observe classically, so we can say:  
$$\Delta J=J_{n}-J_{n-1}=\hbar$$

Each steps of action has its interval $\hbar$.  
Without using any orbits, we derived that **Bohr-Sommerfeld hypothesis** was true!  

## Quantum harmonic oscillator (July 1925)

Further, Heisenberg explained how the **harmonic oscillators** act in **quantum**.  
We imagine how the object with spring is moving in the quantum world.  

The **quantum motion**, seems nobody haven't thought and tested before.  
Let's try what happens to physical objects which are as small as single atom!  
It's quite **different** to conventional Newtonian mechanics!  

From the differential equation  
$$\frac{d^2}{dt^2}x+\omega_{0}^{2}x=0$$
The classical solution is:  
$$x=a_{1}\cos(\omega_{0} t)$$
with total energy:  
$$E=T+V=\frac{1}{2}m\dot{x}^{2}+\frac{1}{2}m\omega_{0}^{2}x^{2}$$

He applied quantum forms to $a_{1}$ and $\omega_{0}$.  

He concluded the energy of quantum harmonic oscillator as:  
$$E=\frac{h\omega_{0}}{2\pi}(n+\frac{1}{2})$$
It means the energy of harmonic oscillator is **discrete**, having the **constant intervals** $\hbar\omega_{0}$!  
Moreover, the **zero point energy is not absolutely zero**!  
The object has some energy even in zero temperature.  
So we have to define **zero point energy(ZPE)** to describe where is the exact zero point.  
![harmonic oscillator](zpe.png "Quantum harmonic oscillator has nonzero zero-point energy")  

## Born-Jordan quantisation postulate (September 1925, November 1925)

Another notable physicists, **Max Born**, and **Pascual Jordan**, want to find relationship between classical and quantum mechanics.  
Based on Hamiltonian mechanics and Heisenberg's idea, they suggested the relation as:  
$$\bold{x}\bold{p}-\bold{p}\bold{x}=\frac{ih}{2\pi}\bold{I}$$
where

* $\bold{p}$ is the matrix form of momentum
* $\bold{x}$ is the matrix form of position
* $\bold{I}$ is the identity matrix

This relation is simply written using commutator operator.  
$$[x,p]=i\hbar$$
where $[x,p]:=xp-px$. (Since $x$ and $p$ are matrices, so they do not commute in multiplication. ($xp\neq px$))  

By writing this relation in quantum form, we can get quantum condition as:  
$$\sum_{n}(x_{n,n+1}p_{n+1,n}-p_{n,n+1}x_{n+1,n})=i\hbar$$

## Uncertainty principle (1927)

Heisenberg wants to know **how accuracy is represented** in quantum.  
If we measure $\eta$, how is the **probability distributed** by how accurate the position is measured?  
He first considered probability amplitude $S(\eta,x)$.  
Near specific position $x'$, the error of position becomes $x_{1}$.  
The probability $S(\eta,x)$ follows **Gaussian distribution**:  
$$S(\eta,x)\propto\exp(-\frac{(x-x')^{2}}{2x_{1}^{2}}-\frac{2\pi i}{h}p'(x-x'))$$
And then, let's consider $S(\eta,p)$.  
We can write $S(\eta,p)$ as:  
$$S(\eta,p)=\int_{-\infty}^{\infty} S(\eta,x)S(x,p)dx$$
He has done work with Born and Jordan, so he already knows $S(x,p)$ is written as:  
$$S(x,p)=\langle x|p\rangle \propto e^{2\pi ipx/h}$$
The form is based on Born and Jordan's quantisation postulate $[x,p]=i\hbar$.  
Therefore, we can write $S(\eta,p)$ as:  
$$S(\eta,p)\propto\int_{-\infty}^{\infty} \exp(\frac{2\pi i(p-p')x}{h}-\frac{(x'-x)^{2}}{2x_{1}^{2}})dx$$
He obtains $S(\eta,p)$ having the same structure as $S(\eta,x)$.  
$$S(\eta,p)\propto \exp(-\frac{(p-p')^{2}}{2p_{1}^{2}}+\frac{2\pi i}{h}x'(p-p'))$$
From analysis of Gaussian distribution, he finally derived the famous **uncertainty principle** (*Unschärferelation*)!
$$p_{1}x_{1}=\frac{h}{2\pi}$$

From his theory, the accuracy of momentum and position are **inverse-proportional**.  
If we measure momentum accurately, we don't know where exactly the particle is.  
Otherwise, if we measure position accurately, we don't know how fast the particle passes its position.  

![uncertainty principle](uncertainty-principle.png "It is impossible to measure position and momentum accurately at the same time.")  

Meanwhile, Earle Kennard and Hermann Weyl have done further research and today we write uncertainty principle as:  
$$\Delta x \Delta p \geq \frac{\hbar}{2}$$
where

* $\Delta x$ is the standard deviation of position  
* $\Delta p$ is the standard deviation of momentum  

This revolutionary thought changed our mind on measurement.  
In quantum, we **cannot measure** both momentum and position **accurately at the same time**!  

## Heisenberg in chemistry

Actually, chemists **do not directly use** Heisenberg's theories. Chemists feel his theories are too **abstract**.  
He pursued using **only observables**, so there are **no wavefunctions**, and **no orbitals**.  
Chemists prefer **Schrödinger equation** in practical ways for explaining chemistry.  
Schrödinger's method, **equivalent** to Heisenberg, is more **intuitive** to understand Chemistry.  
After theoretical chemists, such as Linus Pauling, Kenichi Fukui, have suggested how to explain chemistry using orbitals.  

However, Heisenberg's theories are the bedrock for understanding further theories, such as Hartree-Fock, are essential to understand quantum chemistry.  

## Derivation of quantum harmonic oscillator

> He first described the position as:  
> $$x(n,t)=\sum_{\alpha}x(n,\alpha)e^{i\omega(n)\alpha t}$$
> Then, the action is written as:  
> $$2\pi J=\oint_{c}pdx=m\oint_{c}\dot{x}^{2}dt=2\pi m\sum_{\alpha}|x(n,\alpha)|^{2}\alpha^{2}\omega(n)$$
> From Bohr-Sommerfeld's hypothesis, we can write the classical action as:  
> $$2\pi dJ=hdn$$
> He wrote the classical Planck constant $h$ using the action:  
> $$h_{classical}=2\pi\frac{dJ}{dn}=2\pi m\sum_{\alpha}\alpha\frac{d}{dn}(\alpha\omega(n)|x(n,\alpha)|^{2})$$
> By Kramers' dispersion theory, we can write the quantum form of differentiation as:  
> $$\alpha\frac{dA(n,\alpha)}{dn}=A(n+\alpha,n)-A(n,n-\alpha)$$
> Therefore, the **quantum Planck constant** becomes:  
> $$h_{quantum}=4\pi m\sum_{\alpha}(|x(n,n+\alpha)|^{2}\omega(n,n+\alpha)-|x(n,n-\alpha)|^{2}\omega(n,n-\alpha))$$

The differential equation of the system is given as:  
$$\frac{d^2}{dt^2}x+\omega_{0}^{2}x=0$$
The classical solution is:  
$$x=a_{1}\cos(\omega_{0} t)$$

In classical mechanics, $a_{1}$ and $\omega_{0}$ are constant.  
> Let's assume that $a$ and $\omega$ only depends on quantum number.  
> We write:  
> $$a_{1}=a(n,n-1)$$
> $$\omega_{0}=\omega(n,n-1)$$
> We can write the quantum form as:  
> $$x=a(n,n-1)\cos(\omega(n,n-1)t)=\frac{a(n,n-1)}{2}e^{i\omega(n,n-1)t}+\frac{a(n-1,n)}{2}e^{i\omega(n-1,n)t}$$
> From quantum Planck constant, we can get:  
> $$(a(n,n+1))^{2}-(a(n,n-1))^{2}=\frac{h}{\pi m\omega_{0}}=k$$
> Since $x$ is real number, so $x$ satisfies commutativity.  
> $$x(n,n-\alpha)=x(n-\alpha,n)$$
> If we have an initial value of $a(n,n-1)$, we can get a general form.  
> For $a(0,-1)$, since the state with negative quantum number does not exist, we can set the initial condition:  
> $$a(0,-1)=0$$
> From this, we can get:  
> $$a(n,n-1)=\sqrt{\frac{nh}{\pi m\omega_{0}}}$$

Let's apply them into the total energy!  
The total energy of harmonic oscillator is written as:  
$$E=T+V=\frac{1}{2}m\dot{x}^{2}+\frac{1}{2}m\omega_{0}^{2}x^{2}$$
Since the total energy is conserved, so  
$$E(n,t)=\sum_{\alpha}E(n,n-\alpha)e^{i\omega(n,n-\alpha)t}=H(n,n)$$

He concluded the energy of quantum harmonic oscillator as:  
$$E=\frac{h\omega_{0}}{2\pi}(n+\frac{1}{2})$$

## Derivation of Born-Jordan quantisation postulate

Born and Jordan first reminded Hamilton equation:  
$$\dot{x}=\frac{\partial H}{\partial p}=\frac{p}{m},~\dot{p}=-\frac{\partial H}{\partial x}=-\frac{\partial U}{\partial x}$$
Where $U$ is internal energy of system.  
It's the same as Newtonian mechanics. $p=m\dot{x}$ and $dU=-\dot{p}dx$.  
They started to use concepts of matrix from Heisenberg's notation.  
Heisenberg noted $p$ and $x$ as:  
$$p=\sum_{\tau=-\infty}^{\infty}p_{\tau}e^{2\pi i\nu\tau t},~x=\sum_{\tau=-\infty}^{\infty}x_{\tau}e^{2\pi i\nu\tau t}$$
Apply it to classical action  
$$2\pi J=\oint pdq=\int_{0}^{1/\nu}p\dot{q}dt$$
The relation of $p$ and $x$ can be written as:  
$$1=i\sum_{\tau=-\infty}^{\infty}\tau\frac{\partial}{\partial J}(x_{\tau}p_{-\tau})$$
Let's apply the quantum term into above.  
$\sum_{\tau=-\infty}^{\infty}\tau\frac{\partial}{\partial J}(x_{\tau},p_{-\tau})$ can be written as quantum form:  
$$\frac{1}{h}\sum_{\tau=-\infty}^{\infty}(x(n+\tau,n)p(n,n+\tau)-x(n,n-\tau)p(n-\tau,n))$$
Therefore, we can finally get:  
$$\sum_{k}(p(nk)x(kn)-x(nk)p(kn))=\frac{h}{2\pi i}$$
It's equivalent to  
$$[\bold{p},\bold{x}]=-i\hbar\bold{I}$$

## References

Umdeutung paper - Wikipedia  
<https://en.wikipedia.org/wiki/Umdeutung_paper>  
Matrix mechanics - Wikipedia  
<https://en.wikipedia.org/wiki/Matrix_mechanics>  
Uncertainty principle - Wikipedia  
<https://en.wikipedia.org/wiki/Uncertainty_principle>  
Bohr-Einstein devates - Wikipedia  
<https://en.wikipedia.org/wiki/Bohr%E2%80%93Einstein_debates>
Heisenberg, W. (1925). Über quantentheoretische Umdeutung kinematischer und mechanischer Beziehungen. Zeitschrift für Physik, 33, 879–893.  
<https://doi.org/10.1007/BF01328377>  
Born, M., Jordan, P. Zur Quantenmechanik. Z. Physik 34, 858–888 (1925).  
<https://doi.org/10.1007/BF01328531>  
Born, M., Heisenberg, W. & Jordan, P. Zur Quantenmechanik. II.. Z. Physik 35, 557–615 (1926).  
<https://doi.org/10.1007/BF01379806>  
Heisenberg, W. Über den anschaulichen Inhalt der quantentheoretischen Kinematik und Mechanik. Z. Physik 43, 172–198 (1927).  
<https://doi.org/10.1007/BF01397280>  
