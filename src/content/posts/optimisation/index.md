---
title: "Computational Chemistry: Optimisation"
published: 2026-03-02
description: "How we decide the potentials of molecular systems, and how we optimise them?"
image: ""
tags: ["Computational Chemistry"]
category: Computational Chemistry
lang: en
draft: True
---

# Optimisation

Today we will discuss about molecular dynamics simulation.  
The simulation mimics the natural molecular system into computer based on physical principle.  
If the system is well-simulated, it tells us how the molecules in nature interact each other.  

Molecular dynamics is one of the core parts of computational chemistry.  
It helps us how chemical phenomena are theoretically explained, and verify whether the phenomana are valid before experiment.  

---

## Intro

In molecular dynamics simulation, optimisation is the process that makes the molecular system more physically acceptable.  
According to the **second law of thermodynamics**, **the entropy of the system must increase**.  
To increase entropy, the molecular system would naturally fall into the **minimum energy**, like a ball falling into the lowest pit.  

Our computer is very inflexible, so it is not just understanding the nature.  
Just *ordering* represent the nature computer cannot simply do it.  
We need to prepare some **algorithms** for our purpose.  
Fortunately, most of the important algorithms have been prepared by several physicists, mathematicians, computational chemists, and computer scientists.  

## The types of potential

To understand the optimisation, we need to understand how we decide the potential of the molecular system.  
We call it the **force field**, the method of deciding the potential of the system.  
Deciding the force field is the most crucial and the most considerate process of the molecular mechanics.  
Modern force fields have been invented for the accurate simulation that is fit on the experimental results.  
However, all force fields share the basic concepts.  

$$E_{total}=E_{stretch}+E_{bend}+E_{torsion}+E_{coulomb}+E_{vdw}$$

It is the basic form of the potential of the molecular system.  

$E_{stretch}$ is the bond stretching potential, typically written as harmonic form:  
$$E_{stretch}=\frac{1}{2}k_{r}(r-r_{0})^{2}$$  

$E_{bend}$ is the bending potential, decided by connection of three atoms, it is also typically written as harmonic form:  
$$E_{bend}=\frac{1}{2}k_{\theta}(\theta-\theta_{0})^{2}$$  

$E_{torsion}$ is about torsion, decided by four atoms, it means how much angle distributed between atom 1 and atom 4.  
$$E_{torsion}=E_{0}\sum_{n} (1+\cos(n\phi-\delta))$$  
![Torsion](https://gcore.jsdelivr.net/gh/chemmasterynahida/assets/common/optimisation/torsion.png "Torsion")  

$E_{coulomb}$ is electrostatic potential between charged particles.  
$$E_{coulomb}=\frac{1}{4\pi\epsilon_{0}}\frac{q_{1}q_{2}}{r}$$  

$E_{vdw}$ is potential from other nonbonding potential (van der Waals), typically uses Lennard-Jones form.  
$$E_{vdw}=4\epsilon((\frac{\sigma}{r})^{12}-(\frac{\sigma}{r})^{6})$$  

To decide the force field, we need to decide some parameters. They should fit to experiment and quantum computation result.  
> $r_{0}$: The most stable bond lengths in single molecule  
> $k_{r}$: Force constants of stretching  
> $\theta_{0}$: The most stable bond angles in single molecule  
> $k_{\theta}$: Force constants of bending  
> $E_{0}$: Energy parameter of torsion  
> $n$: Periodicity (Fourier sum parameter)  
> $\delta$: Phase difference  
> $\epsilon$: Ground potential of nonbonding interaction  
> $\sigma$: Length parameter  

## More advanced potential

### Morse potential

The harmonic stretching model is a rough approximation. We can derive the harmonic model from Taylor expression.  
$$E=E_{0}+\frac{dE}{dr}(r-r_{0})+\frac{1}{2}\frac{d^{2}E}{dr^{2}}(r-r_{0})^{2}+\cdots$$
Since $E_{0}$ and $\frac{dE}{dr}$ become zero at the minimum potential, so we can write the stretching energy as:  
$$E\approx\frac{1}{2}\frac{d^{2}E}{dr^{2}}(r-r_{0})^{2}$$  
The second derivative becomes the force constant of stretching.  

To get accurate potential, Philip Morse suggested a new energy function.  
$$E=D_{e}(1-e^{-a(r-r_{0})})^{2}$$  
where  
$$\alpha=\sqrt{\frac{k_{r}}{2D}}$$  
![Morse potential](https://gcore.jsdelivr.net/gh/chemmasterynahida/assets/common/optimisation/Morse-potential.svg.png "Morse potential")  
It is called **Morse potential**.  
Morse potential shows more accurate potential for long-range.  
However, due to high sensitivity to initial state, and harmonic model fits well for short-range, still the harmonic model is widely used.  

### Out-of-plane potential

### exp-6 van der Waals potential

### Cross terms

## Optimisation method

If we have a full potential map, we can find a minimum by finding the first derivative becomes zero.  
The minimum point has the value that first derivative becomes zero, and second derivative in all direction become positive.  
$$\frac{dE}{dr}=0,~\frac{d^{2}E}{dr^{2}}>0$$  
However, we do not know the potential map of the new system.  

### First derivative methods

First method is **steepest descent (SD)** method.  
It finds the maximum decreasing path in all directions, and then move along the path in certain step, and so on.  
This method always lowers the energy, so that therefore eventually falls into the local minimum.  

$$\bold{x}_{i+1}=\bold{x}_{i}-\gamma\nabla f(\bold{x}_{i})$$  
where  
$\gamma$: step size  

The steepest descent method is easy and widely used, but there are some problems.  
For practical minimisation, we need to set appropriate step size.  
Too large step can lead to overshot, too small step converges too slow.  
Moreover, near the local minimum, the energy converges slower due to small gradient, therefore it needs high number of steps.  

To guarantee convergency, Barzilai-Borwein method suggests a seqence of step size.  
$$\gamma_{n}=\frac{|(\bold{x}_{n}-\bold{x}_{n-1})^{T}(\nabla f(\bold{x}_{n})-\nabla f(\bold{x}_{n-1}))|}{||\nabla f(\bold{x}_{n})-\nabla f(\bold{x}_{n-1})||^{2}}$$  
This decreasing step size will eventually lead to the minimum within infinite steps.  

![Steepese descent](https://gcore.jsdelivr.net/gh/chemmasterynahida/assets/common/optimisation/Steepest_descent_convergence_path_for_A_=_2_2,_2_3.png "Steepest descent")  

People have suggested other methods to get minimum for resolving the problems of steepest descent method.  

Second method is **conjugate gradient (CG)** method.  

From the quadratic function:  
$$f(x)=\frac{1}{2}x^{T}Ax-b^{T}x$$  
It first decides two orthogonal directions $d_{i},d_{j}$ satisfying:  
$$d_{i}^{T}Ad_{j}=0$$  

![Conjugate gradient](https://gcore.jsdelivr.net/gh/chemmasterynahida/assets/common/optimisation/Conjugate_gradient_illustration.svg.png "Conjugate gradient")  

It first optimises in one direction, and then in another direction so that it finds the minimum.  
Therefore we can avoid unnecessary zigzag in steepest descent method.  
It can be also used for non-quadratic or nonlinear system because they can be approximated to certain quadratic function.  

### Second derivative methods

Third method is **Newton-Raphson (NR)** method.  

From Taylor expression of current point:  
$$f(\bold{x})=f(\bold{x}_{0})+\nabla f(\bold{x}_{0})^{T}(\bold{x}-\bold{x}_{0})+\frac{1}{2}(\bold{x}-\bold{x}_{0})^{T}\bold{H}(\bold{x}-\bold{x}_{0})+\cdots$$  
If the expression is quadratic, it will give the exact minimum value at once.  
$$\bold{x}=\bold{x}_{0}-\bold{H}^{-1}\nabla f(\bold{x}_{0})$$  
where  
$\bold{H}=\nabla(\nabla f(\bold{x}_{0}))$: Hessian matrix (second derivates of all directions)  

This method converges fast to the minimum within a few steps.  
However, it needs to calculate **Hessian**, which means a set of second derivates of all direction, therefore one step becomes expensive.  

Fourth method is **quasi-Newton** method.  

Quasi-Newton is similar to Newton-raphson method, but it avoids calculating expensive Hessian.  
It estimates the Hessian by:  
$$\bold{B}_{n+1}=\frac{\nabla f(\bold{x}_{n+1})-\nabla f(\bold{x}_{n})}{\bold{x}_{n+1}-\bold{x}_{n}}$$  

Then use the same Newton method to approximate the minimum for each step.  
$$\bold{x}_{n+1}=\bold{x}_{n}-\bold{B}_{n}^{-1}\nabla f(\bold{x}_{n})$$  

No one can give the exact minimum value in general. They are giving a converging value of the process.  
There are various methods for minimisation, each methods has its own pros and cons.  
One method is easy but converges slow, the other converges fast but expensive.  

|Method|Derivatives|speed|Memory|Use|
|---|---|---|---|---|
|Steepest descent|1st|Slow|Low|Very large problems|
|Conjugate gradient|1st|Medium|Low|Large quadratic systems|
|Newton-Raphson|2nd|Very fast|High|Small-medium problems|
|Quasi-Newton|1st|Fast|Medium|General nonlinear optimisation|

The simulation programs suggest various methods for minimisation, but steepest descent method is the most widely used.  

---

## References

Gradient descent - Wikipedia  
<https://en.wikipedia.org/wiki/Gradient_descent>  
Conjugate gradient method - Wikipedia  
<https://en.wikipedia.org/wiki/Conjugate_gradient_method>  
Quasi-Newton method - Wikipedia  
<https://en.wikipedia.org/wiki/Quasi-Newton_method>  
Essentials of computational chemistry. Theories and Models, C. J. Cramer, (2nd Ed. Wiley, 2004)  
Introduction to Computational Chemistry, F. Jensen (1999)  
