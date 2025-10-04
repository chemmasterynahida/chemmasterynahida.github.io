---
title: 1.1. Blackbody Radiation
published: 2025-10-02
description: "What problem did blackbody radiation theory have, and how can it be solved?"
image: "./cover.jpeg"
tags: ["Quantum Chemistry"]
category: Quantum Chemistry
lang: en
draft: false
---

# Blackbody Radiation

## Quantum Chemistry: Intro

Hello, This is Chemistry Mastery Nahida. I'd like to start the first lecture about *Quantum Chemistry*.  

To start quantum chemistry, we need to understand what *Quantum* means. Everyone have been heard about *Quantum*, right? Do you feel the word *Quantum* somewhat high-technical or futuristic?  
Quantum computer also becomes famous today, isn't it?  
![quantum computer](qc.jpg "Quantum Computer by Google")

So, What is *Quantum*?  

Have you related to the word *quantity*? Right. The word *quantum* is from *quantity*, means *amount* of something. If you understand how quantum mechanics was founded, you can understand what *quantum* means.  

## Before Planck (as of 1900)

Today, I'd like to discuss about Blackbody Radiation. Is this related to *Quantum Physics*?  
Sir Issac Newton first mentioned blackbody from his publication, *Opticks*. He said,  

> "Do not black Bodies conceive heat more easily from Light than those of other Colours do, by reason that the Light falling on them is not reflected outwards, but enters the Bodies, and is often reflected and refracted within them, until it be stifled and lost?"

Black objects absorb all frequencies of visible light with no reflection. If light is once absorbed to the black body, where the light finally goes? To preserve energy, the energy of light should be released to somewhere.  

In 1858, Balfour Stewart did an experiment on radiation and denoted that blackbody absorbs and emits the greatest power.  
In 1859, Gustav R. Kirchhoff reported the spectrum of blackbody radiation, and he found it depends on only temperature of blackbody.  
After Kirchhoff, some equations based on experiments were reported. Among these equation, Wilhelm Wien's equation (1896) descrives the experimental result most.  

**Wien's (1896)**
$$u(\nu,T)=a\nu^{3}e^{-b\nu/T}$$  
$u$: energy density per unit volume at specific frequency  
$\nu$: frequency  
$T$: temperature  
$a, b$: some constants

There are some trials for theoretical explanation. In June 1900, Lord Rayleigh reported the equation based on theories.  
**Rayleigh-Jeans Law (1900)**
$$du(\nu,T)=\frac{8\pi\nu^{2}}{c^{3}}Ud\nu=\frac{8\pi\nu^{2}kT}{c^{3}}d\nu$$  
$c$: speed of light in vacuum ($c=299792458~m/s$)  
$k$: Boltzmann constant ($k=1.380649×10^{−23}~J/K$)  

The theory cannot explain experimental data. For high frequency, the blackbody energy become infinite. It's called **"Ultraviolet Catastrophe."**  
![ultraviolet catastrophe](ultraviolet-catastrophe.png "\"Ultraviolet catastrophe\"")  
The Rayleigh-Jeans law fits well in low frequency, but it predicts energy goes infinite for high frequency. Meanwhile Wien's law fit well in high frequency.  

## The Birth of Quantum Physics

In December 1900, Planck considered energy as **energy particles** to determine the entropy of system.  

**Quantum Hypothesis**  
$$E=n\epsilon=nh\nu$$  
$\epsilon$: the unit energy of the light  
$h=6.62607015\times10^{-34}J\cdot m$: Planck constant  
$\nu$: frequency  

This hypothesis after results to the foundation of **Quantum Physics**, therefore the **Quantum** means about **discrete amount of energy**.  

## The Law

Applying Boltzmann distribution to the system, the equation could be obtained.  
Boltzmann distribution is about energy distribution of the system, can be written as:  

**Boltzmann distribution**
$$f(E)\propto e^{\frac{E}{kT}}$$  
$f(E)$: number of molecules having energy E  
$E$: energy of the ensemble  
$k$: Boltzmann constant  
$T$: temperature  

From this relationship, we can derive mean energy of the system.  
$$<E>=<f(n\epsilon)>=\frac{\sum_{n=0}^{\infty}n\epsilon e^{-n\epsilon/kT}}{\sum_{n=0}^{\infty}e^{-n\epsilon/kT}}=\frac{\epsilon}{e^{\epsilon/kT}-1}=\frac{h\nu}{e^{h\nu/kT}-1}$$  
Therefore,  
$$du(\nu,T)=\frac{8\pi\nu^{2}}{c^{3}}Ud\nu=\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu$$  
We can convert this equation to having variable $\lambda$ using $\nu=c/\lambda$ and $d\nu=-cd\lambda/\lambda^{2}$  
$$du(\lambda,T)=\frac{8\pi hc}{\lambda^{5}}\cdot\frac{1}{e^{hc/\lambda kT}-1}d\lambda$$  

**Planck's law (variable $\nu$)**  
$$du(\nu,T)=\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu$$  
**Planck's law (variable $\lambda$)**  
$$du(\lambda,T)=\frac{8\pi hc}{\lambda^{5}}\cdot\frac{1}{e^{hc/\lambda kT}-1}d\lambda$$  

## Verification of Planck's law

As of Planck's publication, there are some experimental reports for blackbody radiation.  
**Stefan-Boltzmann law (1877)**  
*The radiation power of blackbody (or total energy of radiation) is proportional to the fourth power of its temperature.*  
$$M=\sigma T^{4}$$  
**Wien's displacement law (1896)**  
*The peak wavelength is inversely proportional to its temperature.*  
$$\lambda_{peak}=\frac{b}{T}$$  
The new equation must explain these properties and have no contradictions to Wien's and Rayleigh-Jeans law.  

### Stefan-Boltzmann law

Stefan-Boltzmann law is about total energy of radiation. We have derived the radiation energy distribution by frequency. It is derived by integrating energy distribution for all wavelength.  
$$\int du=\int_{0}^{\infty}\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu$$  
Let $x=h\nu/kT$ and $dx=hd\nu/kT$for the calculation.  
$$\int_{0}^{\infty}\frac{8\pi k^{3}T^{3}}{h^{2}c^{3}}\cdot\frac{x^{3}}{e^{x}-1}\cdot\frac{kT}{h}dx$$  
It is known for the value of this integration is given as:  
$$\int_{0}^{\infty}\frac{x^{3}}{e^{x}-1}dx=\frac{\pi^{4}}{15}$$  
Therefore,  
$$E=\int du=\frac{8\pi k^{3}T^{3}}{h^{2}c^{3}}\cdot\frac{\pi^{4}}{15}\cdot\frac{kT}{h}=\frac{8\pi^{5}k^{4}T^{4}}{15h^{3}c^{3}}$$  
We got **total energy of radiation** of blackbody. (unit=$J/m^{3}$) However, the Stefan-Boltzmann law asks about **radiation power**. (unit=$W/m^{2}$) We can convert from total energy to surface radiation power by multiplying $c/4$.  
$$M=E\cdot\frac{c}{4}=\frac{8\pi^{5}k^{4}T^{4}}{15h^{3}c^{3}}\cdot\frac{c}{4}=\frac{2\pi^{5}k^{4}T^{4}}{15h^{3}c^{2}}=\sigma T^{4}$$  
Finally we can get Stefan-Boltzmann law and the value of $\sigma$.  
**Stefan-Boltzmann law**
$$M=\sigma T^{4}=\frac{2\pi^{5}k^{4}}{15h^{3}c^{2}}T^{4}$$  

### Wien's displacement law

Wien's displacement law is about which wavelength (or frequency) have a maximum radiation. It is derived by finding maximum of energy distribution.  
$$\frac{d(du/d\nu)}{d\nu}=0$$  

### $\nu\rightarrow0$

Rayleigh-Jeans law can explain the experimental result for low frequency. For small $\nu$, Planck's law should be converged into Rayleigh-Jeans law.

### $\nu\rightarrow\infty$

Wien's law can explain the experimental result for high frequency. For large $\nu$, Planck's law should be converged into Wien's law.

***
***

## Planck's Idea 1 (Published in October 1900)

If the two equations are partially correct, Why don't we combine them?  
In October 1900, Max Planck first tried to combine two equations. He saw which parameters decide energy for two equations.  
For Wien's law, the energy is an exponential function of frequency and temperature. Otherwise, for Rayleigh-Jeans law, the energy is proportional to temperature itself.  
$$U_{Wien}\propto \nu e^{-b\nu/T}~(Wien)$$  
$$U_{RJ}\propto T~(RJ)$$  
He first applied thermodynamics for this work. It can be expressed as:  
$$dU=TdS-PdV$$  
The experiment was held in a box with tiny pinhole, so the volume of system is not changed.  
![experiment](experiment.png "Blackbody Radiation Experiment")  
So the thermodynamics can be written as:  
$$dU=TdS,~\frac{\partial S}{\partial U}=\frac{1}{T}$$  
Planck considered ${\partial S}/{\partial U}$ for the two laws:  
$$\frac{\partial S}{\partial U}=\frac{1}{T}\propto ln(U)~(Wien)$$  
$$\frac{\partial S}{\partial U}=\frac{1}{T}\propto\frac{1}{U}~(RJ)$$  
How about getting derivatives again?  
$$\frac{\partial^{2} S}{\partial U^{2}}\propto\frac{1}{U}~(Wien)$$  
$$\frac{\partial^{2} S}{\partial U^{2}}\propto\frac{1}{U^{2}}~(RJ)$$  
Therefore, we can get $(\partial^{2} S/\partial U^{2})^{-1}$ as polynomials of U for the two laws.  
$$(\frac{\partial^{2} S}{\partial U^{2}})^{-1}\propto U~(Wien's)$$  
$$(\frac{\partial^{2} S}{\partial U^{2}})^{-1}\propto U^{2}~(RJ)$$  
Planck combined two polynomials as:
$$(\frac{\partial^{2} S}{\partial U^{2}})^{-1}=C_{1}U+C_{2}U^{2}$$  
He concluded the form of the equation as:  
$$U=\frac{C_{1}C_{2}}{Ce^{C_{1}T}-1}$$  
where C is the integration constant. Planck reported this constant as 1.  

## Planck's Idea 2 (Published in December 1900)

Planck derived entropy of discrete energy particles from Boltzmann's theory.  
Boltzmann distribution dscribes energy distribution of ideal gas system as:  
$$\frac{p_{i}}{p_{j}}=exp(\frac{E_{j}-E_{i}}{kT})$$  
$p_{i},p_{j}$: number of molecules in ensemble i and j  
$E_{i},E_{j}$: energy of ensemble i and j  
$k$: Boltzmann constant  
$T$: temperature  

Boltzmann describes absolute entropy of system as:  
$$S=k\cdot ln(W)$$  
$S$: absolute entropy of the system  
$W$: "*Wahrscheinlichkeit*", probability of occurence of macrostates  

In blackbody radiation, we consider entropy of $N$ waves, which have several numbers of energy particles.  
Let $P$ the number of energy particle, therefore  
$$P=UN/\epsilon$$  
where $\epsilon$ is a unit of energy, and $U$ is energy of one wave.  

We can consider the system as:  
$$\epsilon\epsilon\epsilon|\epsilon\epsilon|\epsilon|\epsilon\epsilon\epsilon|\epsilon\epsilon|\cdots$$  
We have $P$ energy particles, and $N-1$ barriers. We assume that $P$ and $N$ is sufficiently large.  
The value of $W$ can be written as:  
$$W=\frac{(P+N-1)!}{P!(N-1)!}$$  
The $N$ is so many, so we can see $N-1$ as $N$.  
Meanwhile, for sufficiently large number $n$, $n!$ is approximated to:  
$$n!\approx\sqrt{2\pi n}(n/e)^{n}~(n\rightarrow\infty)$$  
Since $n^{n}$ is much larger than $\sqrt{n}$, we can write $W$ as:  
$$W=\frac{(P+N-1)!}{P!(N-1)!}\approx \frac{(P+N)^{P+N}}{P^{P}N^{N}}$$  

Let's remind the equation from the thermodynamics:
$$\frac{1}{T}=\frac{\partial S}{\partial U}=k\frac{\partial(ln(W))}{\partial U}$$  


## References

Blackbody Radiation: Wikipedia (<https://en.wikipedia.org/wiki/Blackbody%20Radiation>)  
Planck's Law: Wikipedia (<https://en.wikipedia.org/wiki/Planck%27s%20Law>)  
Planck, M. (1900). Über eine Verbesserung der Wien’schen Strahlungsgleichung. *Verhandlungen der Deutschen Physikalischen Gesellschaft*.  
Planck, M. (1900). Zur theorie des gesetzes der energieverteilung im normalspektrum. *VhDPG*, 2, 238.  
