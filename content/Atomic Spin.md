---
title: On Atomic Spin
tags:
  - Physics
---
Atomic spin is a fundamental feature of particles, with different elements oscillating at different rates, it is a quantised state, all of the classic subatomic particles have quantised spin of $\frac{1}{2}$, the net spin of a $^1H$ nucleus is $\frac{1}{2}$.  This net spin being non-zero is required for a nucleus to undergo resonance with an electromagnetic wave within a magnetic field.

This spin directly relates to the magnetic moment of a particle.
> $\hat{\mu} = \gamma \hat{S}$   

Whilst the precession rate of a particle inside of a magnetic field will be given by.
> $\omega^0 = -\gamma B^0$

Where B is the total magnetic field at the particle location and $\gamma$ is the gyromagnetic ratio of the particle (unique for any given particle or nuclei).  The most commonly used nuclei for MRI is $^1H$, it has a gyromagnetic ratio of $42.58\text{MHz}\cdot \text{T}^{-1}$.  You can remember this using the mnemonic that DC came up with:

> "I figured out a way of remembering the larmor frequency, it's like \[LK\], he's 42 and hes about 5'8"."
> 			-DC, Trainee RP$^2$ Clinical Scientist

This precession can be visualised using various classical equivalents, such as gyroscopes, basketballs, or driedels.
![[spinAnimation.gif]]
If we consider the many spins that are in any given voxel of space they will be distributed isotropically.  Their individual spins will be at random phases so the only magnetisation in the unexcited state is in the longitudinal direction, given they aren't directly measured it isn't correct to discuss individual spins as being in the spin up or down state, but as a function of temperature the ratio of these can be described using a boltzmann distribution.
> $\frac{N_\uparrow}{N_\downarrow} = \exp{\frac{\hbar \gamma B_0}{kT}}$

During excitation more spins are put into the spin-down state than the spin-up state, this is a population inversion state which has a hypothetically "negative" temperature, so will only last during the excitation period, after which the spin will de-excite.
