---
title: "Quantum Chemistry: 1.1. Blackbody Radiation"
published: 2025-10-05
description: "What problem did blackbody radiation theory have, and how can it be solved?"
image: "https://gcore.jsdelivr.net/gh/chemmasterynahida/assets/common/blackbody-radiation/planck.png"
tags: ["Quantum Chemistry"]
category: Quantum Chemistry
lang: en
draft: false
---

# Blackbody Radiation

## Quantum Chemistry: Intro

Hello~ This is Chemistry Mastery Nahida.  
Today, we begin our very first lecture in *Quantum Chemistry* — a journey into the world where even light and energy follow mysterious, tiny rules.  

To begin, we must understand what *Quantum* means. You’ve probably heard this word before, right? It sounds a bit futuristic — like something from a high-tech laboratory. Quantum computers, for example, are quite famous today!  
![quantum computer](https://gcore.jsdelivr.net/gh/chemmasterynahida/assets/common/blackbody-radiation/qc.jpg "Quantum Computer by Google")

But what *is* a quantum, truly?  
If you think of the word *quantity*, you’re already close! The term *quantum* comes from it, meaning a small *amount* of something. Once we see how quantum mechanics was born, this meaning will make perfect sense.  

## Before Planck (~1900)

Let’s travel back in time to the late 19th century and explore a puzzle that led to the birth of quantum physics — **blackbody radiation**.  
Sir **Isaac Newton** mentioned the concept in his book *Opticks*:  

> "Do not black Bodies conceive heat more easily from Light than those of other Colours do, by reason that the Light falling on them is not reflected outwards, but enters the Bodies, and is often reflected and refracted within them, until it be stifled and lost?"

Black objects absorb all visible light without reflection. But if the light’s energy goes in — where does it go next? Energy must always be conserved, after all.  
In 1858, **Balfour Stewart** found that a blackbody both absorbs and emits energy most efficiently. A year later, **Gustav Kirchhoff** discovered that the spectrum of blackbody radiation depends only on the temperature, not the material itself.  
Over time, scientists proposed equations to describe this mysterious glow.  
Among them, **Wilhelm Wien’s (1896)** formula fit experiments quite well:  

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

But something went terribly wrong.  
At high frequencies, this equation predicted infinite energy!  
Physicists called it the **“Ultraviolet Catastrophe.”**  
![ultraviolet catastrophe](https://gcore.jsdelivr.net/gh/chemmasterynahida/assets/common/blackbody-radiation/planck.png "\"Ultraviolet catastrophe\"")  
Rayleigh–Jeans law matched experiments at low frequencies, while Wien’s worked at high ones — yet neither told the full story.  

---
## The Birth of Quantum Physics

In December 1900, **Max Planck** had a brilliant, daring thought:  
What if light’s energy isn’t continuous… but comes in *tiny packets*?  

He called these packets **quanta**.  

**Quantum Hypothesis**  
$$E=n\epsilon=nh\nu$$  
$\epsilon$: the unit energy of the light  
$h=6.62607015\times10^{-34}J\cdot m$: Planck constant  
$\nu$: frequency  

This was the seed of **quantum physics** — and the word *quantum* began to mean *a discrete amount of energy*.  

## The Law

To describe how energy is shared among these quanta, Planck applied the **Boltzmann distribution**:  

**Boltzmann distribution**  
$$f(E)\propto e^{\frac{E}{kT}}$$  
$f(E)$: number of molecules having energy E  
$E$: energy of the ensemble  
$k$: Boltzmann constant  
$T$: temperature  

From it, we can derive the average energy per mode. This idea is not from Planck, but Bose and Einstein proposed it in 1924.  
$$<E>=<f(n\epsilon)>=\frac{\sum_{n=0}^{\infty}n\epsilon e^{-n\epsilon/kT}}{\sum_{n=0}^{\infty}e^{-n\epsilon/kT}}=\frac{\epsilon}{e^{\epsilon/kT}-1}=\frac{h\nu}{e^{h\nu/kT}-1}$$  
Combining this with physical constants, we can obtain:  
**Planck's law (variable $\nu$)**  
$$du(\nu,T)=\frac{8\pi\nu^{2}}{c^{3}}Ud\nu=\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu$$  
and equivalently, by wavelength:  
**Planck's law (variable $\lambda$)**  
$$du(\lambda,T)=\frac{8\pi hc}{\lambda^{5}}\cdot\frac{1}{e^{hc/\lambda kT}-1}d\lambda$$  

At last, a single formula that bridged the gap between Wien’s and Rayleigh–Jeans laws — a harmonious melody between experiment and theory.  

## Verification of Planck's law

Any good theory must pass the test of experiment.  
Planck’s law gracefully explained earlier observations:  

**Stefan-Boltzmann law (1877)**  
*The radiation power of blackbody (or total energy of radiation) is proportional to the fourth power of its temperature.*  
$$M=\sigma T^{4}$$  
**Wien's displacement law (1896)**  
*The peak wavelength is inversely proportional to its temperature.*  
$$\lambda_{peak}=\frac{b}{T}$$  

Let’s see how Planck’s equation connects to both.  

### Stefan-Boltzmann law

The area under Planck’s law over all frequencies gives total emitted energy.  
We can also get surface radiation from it.  

**Stefan-Boltzmann law**  
$$M=\sigma T^{4}=\frac{2\pi^{5}k^{4}}{15h^{3}c^{2}}T^{4}$$  
$$\sigma=\frac{2\pi^{5}k^{4}}{15h^{3}c^{2}}=5.67\times10^{-8}W/m^{2}\cdot K^{4}$$  
and indeed, the constant $\sigma$ matches experiments beautifully!  

### Wien's displacement law

Wien's displacement law is about which wavelength (or frequency) have a maximum radiation.  

By finding where radiation peak is, we obtain:  
**Wien's displacement law**  
$$\lambda_{peak}=\frac{b}{T}\approx\frac{hc}{4.9651kT}=\frac{2.90mm/K}{T}$$  
So hotter objects glow with shorter wavelengths — from red, to yellow, to white-blue.  

### $\nu\rightarrow0$

Rayleigh-Jeans law can explain the experimental result for low frequency. For small $\nu$, Planck's law should be converged into Rayleigh-Jeans law.  

$$\lim_{\nu\rightarrow0}\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu=\frac{8\pi kT\nu^{2}}{c^{3}}d\nu$$  
For small frequency, the law converges into Rayleigh-Jeans law.  

### $\nu\rightarrow\infty$

Wien's law can explain the experimental result for high frequency. For large $\nu$, Planck's law should be converged into Wien's law.  

$$\lim_{\nu\rightarrow\infty}\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu=\frac{8\pi h\nu^{3}}{c^{3}}\cdot e^{-h\nu/kT}d\nu=a\nu^{3}e^{-b\nu/T}$$  
For large frequency, the law is similar to Wien's law.  

---
---

## Derivations

### Stefan-Boltzmann law: derivation

> $$\int du=\int_{0}^{\infty}\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu$$  
> Let $x=h\nu/kT$ and $dx=hd\nu/kT$for the calculation.  
> $$\int_{0}^{\infty}\frac{8\pi k^{3}T^{3}}{h^{2}c^{3}}\cdot\frac{x^{3}}{e^{x}-1}\cdot\frac{kT}{h}dx$$  
> It is known for the value of this integration is given as:  
> $$\int_{0}^{\infty}\frac{x^{3}}{e^{x}-1}dx=\frac{\pi^{4}}{15}$$  
> Therefore,  
> $$E=\int du=\frac{8\pi k^{3}T^{3}}{h^{2}c^{3}}\cdot\frac{\pi^{4}}{15}\cdot\frac{kT}{h}=\frac{8\pi^{5}k^{4}T^{4}}{15h^{3}c^{3}}$$  
> We got **total energy of radiation** of blackbody. (unit=$J/m^{3}$)
> However, the Stefan-Boltzmann law asks about **radiation power**. (unit=$W/m^{2}$)
> We can convert from total energy to surface radiation by multiplying $c/4$.  
> $$M=E\cdot\frac{c}{4}=\frac{8\pi^{5}k^{4}T^{4}}{15h^{3}c^{3}}\cdot\frac{c}{4}=\frac{2\pi^{5}k^{4}T^{4}}{15h^{3}c^{2}}=\sigma T^{4}$$  

### Wien's displacement law: derivataion

> $$\frac{d(du/d\lambda)}{d\lambda}=0$$  
> Planck's law can be described by wavelength as:  
> $$\frac{du(\lambda,T)}{d\lambda}=\frac{8\pi hc}{\lambda^{5}}\cdot\frac{1}{e^{hc/\lambda kT}-1}$$  
> To simplify the equation, let $\lambda=hc/xkT$ and $d\lambda=-hcdx/x^{2}kT$.  
> $$du(x,T)=-\frac{8\pi x^{5}k^{5}T^{5}}{h^{4}c^{4}}\cdot\frac{1}{e^{x}-1}dx$$  
> We should find which x satisfies this:  
> $$\frac{d}{dx}(\frac{x^{5}}{e^{x}-1})=\frac{5x^{4}(e^{x}-1)-x^{5}(e^{x})}{(e^{x}-1)^{2}}=0$$  
> $x=\frac{hc}{\lambda kT}\approx4.9651$(We can get numerical value only), so this relationship can be written as:  
> $$\lambda_{peak}=\frac{b}{T}\approx\frac{hc}{4.9651kT}=\frac{2.90mm/K}{T}$$  

### $\nu\rightarrow0$: derivation

> $$\lim_{\nu\rightarrow0}du(\nu,T)=\lim_{\nu\rightarrow0}\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu$$  
> It is known that the limit converges:  
> $$\lim_{x\rightarrow0}\frac{e^{x}-1}{x}=1$$  
> Therefore, the limit of equation becomes:  
> $$\lim_{\nu\rightarrow0}\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu=\frac{8\pi kT\nu^{2}}{c^{3}}d\nu$$  

### $\nu\rightarrow\infty$: derivation

> $$\lim_{\nu\rightarrow\infty}du(\nu,T)=\lim_{\nu\rightarrow\infty}\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu$$  
> Since exponential function grows fast, so we can consider $e^{h\nu/kT}-1$ as $e^{h\nu/kT}$.  
> $$\lim_{\nu\rightarrow\infty}\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu=\frac{8\pi h\nu^{3}}{c^{3}}\cdot e^{-h\nu/kT}d\nu=a\nu^{3}e^{-b\nu/T}$$  

## Planck's Ideas and Insights

### October 1900: Blending two laws

Planck noticed that Wien’s and Rayleigh–Jeans laws each worked in their own domain.  
He wondered: could they both be special cases of a deeper truth?  

He studied entropy and thermodynamics, and through elegant reasoning, found a new path that joined both behaviors smoothly.  

> For Wien's law, the energy is an exponential function of frequency and temperature. Otherwise, for Rayleigh-Jeans law, the energy is proportional to temperature itself.  
> $$U_{Wien}\propto \nu e^{-b\nu/T}~(Wien)$$  
> $$U_{RJ}\propto T~(RJ)$$  
> He first applied thermodynamics for this work. It can be expressed as:  
> $$dU=TdS-PdV$$  
> The experiment was held in a box with tiny pinhole, so the volume of system is not changed.  
> ![experiment](https://gcore.jsdelivr.net/gh/chemmasterynahida/assets/common/blackbody-radiation/experiment.jpg "Blackbody Radiation Experiment")  
> So the thermodynamics can be written as:  
> $$dU=TdS,~\frac{\partial S}{\partial U}=\frac{1}{T}$$  
> Planck considered ${\partial S}/{\partial U}$ for the two laws:  
> $$\frac{\partial S}{\partial U}=\frac{1}{T}\propto ln(U)~(Wien)$$  
> $$\frac{\partial S}{\partial U}=\frac{1}{T}\propto\frac{1}{U}~(RJ)$$  
> How about getting derivatives again?  
> $$\frac{\partial^{2} S}{\partial U^{2}}\propto\frac{1}{U}~(Wien)$$  
> $$\frac{\partial^{2} S}{\partial U^{2}}\propto\frac{1}{U^{2}}~(RJ)$$  
> Therefore, we can get $(\partial^{2} S/\partial U^{2})^{-1}$ as polynomials of U for the two laws.  
> $$(\frac{\partial^{2} S}{\partial U^{2}})^{-1}\propto U~(Wien's)$$  
> $$(\frac{\partial^{2} S}{\partial U^{2}})^{-1}\propto U^{2}~(RJ)$$  
> Planck combined two polynomials as:  
> $$(\frac{\partial^{2} S}{\partial U^{2}})^{-1}=C_{1}U+C_{2}U^{2}$$  
> He concluded the form of the equation in form of wavelength as:  
> $$U=\frac{C\lambda^{-5}}{e^{c/\lambda T}-1}$$  

### December 1900: Discrete Energy

Later that year, he applied Boltzmann’s theory of probability to radiation — imagining countless tiny “energy elements” inside a cavity.  
$$\epsilon\epsilon\epsilon|\epsilon\epsilon|\epsilon|\epsilon\epsilon\epsilon|\epsilon\epsilon|\cdots$$  
where $\epsilon$ is a unit of energy.  

He used combinatorics to count all possible arrangements of these quanta:  
$$W=\frac{(P+N-1)!}{P!(N-1)!}$$  
where  
$P=UN/\epsilon$: number of energy particle, $U$:energy of one light wave  
$N$: number of light waves  

> The $N$ is so many, so we can see $N-1$ as $N$.  
> Meanwhile, for sufficiently large number $n$, $n!$ is approximated to:  
> $$n!\approx\sqrt{2\pi n}(n/e)^{n}~(n\rightarrow\infty)$$  
> Since $n^{n}$ is much larger than $\sqrt{n}$, we can write $W$ as:  
> $$W=\frac{(P+N-1)!}{P!(N-1)!}\approx \frac{(P+N)^{P+N}}{P^{P}N^{N}}$$  

Then, with a touch of mathematical magic, based on Boltzmann's principle, he linked this to entropy:  
$$S=k\cdot ln(W)$$  
$S$: absolute entropy of the system  
$W$: "*Wahrscheinlichkeit*", number of microstates  

> Let's remind the equation from the thermodynamics:  
> $$\frac{1}{T}=\frac{\partial S}{\partial U}=k\frac{\partial(ln(W))}{\partial U}$$  
> We have derived the approximate value of $W$, so we can write $ln(W)$ as:  
> $$ln(W)=(P+N)ln(P+N)-Pln(P)-Nln(N)=\frac{N}{\epsilon}((U+\epsilon)ln(U+\epsilon)-\epsilon ln(\epsilon)-Uln(U))$$  
> So, the value of $k\frac{\partial(ln(W))}{\partial U}$ is:  
> $$\frac{kN}{\epsilon}(ln(U+\epsilon)-ln(U))$$  
> For one energy particle, the entropy is:  
> $$\frac{k}{\epsilon}(ln(U+\epsilon)-ln(U))=\frac{1}{T}$$  
> Therefore,  
> $$U=\frac{\epsilon}{e^{\epsilon/kT}-1}=\frac{hv}{e^{hv/kT}-1}$$  

From there emerged his groundbreaking result:  
$$du(\nu,T)=\frac{8\pi\nu^{2}}{c^{3}}Ud\nu=\frac{8\pi\nu^{2}}{c^{3}}\cdot\frac{h\nu}{e^{h\nu/kT}-1}d\nu=\frac{8\pi h\nu^{3}}{c^{3}}\cdot\frac{1}{e^{h\nu/kT}-1}d\nu$$  

---

This is Planck's famous equation. Each light wave could only possess energy in whole-number multiples of $h\nu$.  
It reveals that energy is not continuous but composed of discrete quanta.  

He was awarded the **Nobel Prize in Physics in 1918** for discovery of the energy quanta.  

> *The Nobel Prize in Physics 1918 was awarded to Max Karl Ernst Ludwig Planck "in recognition of the services he rendered to the advancement of Physics by his discovery of energy quanta"*  

From then on, human first touched the threshold of the quantum world. At that moment, the light of knowledge quietly shone in the night sky of science.  
This was the dawn of the quantum era and humanity’s first glimpse at the universe’s smallest secrets.  

## References

Blackbody Radiation: Wikipedia (<https://en.wikipedia.org/wiki/Blackbody%20Radiation>)  
Newton, I. (1704). Opticks: Or, a treatise of the reflections, refractions, inflections and colours of light. London: Sam. Smith and Benj. Walford.  
Planck's Law: Wikipedia (<https://en.wikipedia.org/wiki/Planck%27s%20Law>)  
Planck, M. (1900). Über eine Verbesserung der Wien’schen Strahlungsgleichung. *Verhandlungen der Deutschen Physikalischen Gesellschaft*.  
Planck, M. (1900). Zur theorie des gesetzes der energieverteilung im normalspektrum. *VhDPG*, 2, 238.  
