---
title: "Computational Chemistry: DFT basics"
published: 2026-05-10
description: "What is DFT, and how it is useful in chemistry?"
image: ""
tags: ["Computational Chemistry"]
category: Computational Chemistry
lang: en
draft: True
---

# DFT basics

Today we will discuss about how quantum mechanics predicts the chemical properties of molecules.  
Scientists have interest on how chemial properties are explained in theory.  
To do this, scientists develops quantum mechanics and quantum chemistry, which explains motion of electrons inside atoms.  
Using quantum interpretation of motion of electron, many physical properties and chemical properties of molecules can be explained.  
Today, computer technology is developed, so we can do some quantum calculation using computers.  
How do we order the quantum calculation to computer? Which values will be obtained from calculation?  

---

## Approximation in quantum chemistry

Scientists want to explain chemical properties using confined theories.  
One of the most remarkable work is **Schrödinger equation**, which explains motion of electrons using **wavefunction**.  
$$i\hbar\frac{\partial}{\partial t}\Psi=(-\frac{\hbar^2}{2m}\nabla^{2}+V)\Psi$$  
However, it is too hard... Scientists could solve it only for **hydrogen atom**.  
In case of more than two electrons, the problem becomes more complicated by repulsion between electrons.  

To reduce the complexity, they suggest several approximation methods which are physically acceptable.  

- **Born-Oppenheimer approximation**: Treat wavefunctions of nuclei and electrons separately  
- **Hartree-Fock approximation**: Split the problem into one-electron problem and electron-electron interaction  

## Hartree-Fock theory

---

## References
