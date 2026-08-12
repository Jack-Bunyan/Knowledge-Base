---
title: On Dose
tags:
  - Imaging
  - Physics
  - Therapy
  - Radiotherapy
  - Nuclear_Medicine
---
Dose describes the absorbed energy density of a material, with units of Gy \[Jkg$^{-1}$\].  This is one of the most important aspects of radiation physics and is how radiation protection is managed, and medical exposures are optimised.

Measurements of dose are taken in [[Radiotherapy]] using various different [[Chambers]], these measure the ionisation of the air as a current between two conductors, and convert this to a measurement of the dose in air.


# Equivalent Dose
Equivalent Dose is a a metric that is used to convert from the energy dose deposition that is measured using physical instruments, into one that takes into account the does deposition mechanisms in tissue.  They are normalised against the biological effectiveness of photons having a radiation weighting factor ($\omega_r$) of 1.  Heavier particles such as protons or heavy ions have larger values of $\omega_r$.  This increases their effect within [[Hypoxic]] environments and is one of the advantages of [[Proton Therapy]] compared to photons.  While measured using the same units (Jkg$^{-1}$) as absorbed dose, both equivalent and effective dose use the units of sieverts rather than grays.

> $\omega_r = \begin{cases} \text{Photons}: 1 \\ \text{Electrons and Muons}: 1 \\ \text{Protons and charged pions} = 2 \\ \text{Alpha particles, fission fragments, and heavy ions} = 20 \\ \text{Neutrons: See below}\end{cases}$

![[Neutron dose curve.png]]

These specific values are tragically, a bit scuffed and not real.
# Effective Dose
Effective dose is used exclusively for the determination of the stochastic cancer risk that a patient is exposed to.  It is calculated from the multiplication of the equivalent dose to an organ by its tissue weighting factor
# Deterministic 


Title: [The 2007 Recommendations of the International Commission on Radiological Protection. ICRP publication 103]()
Authors: 
Year: 2007
DOI: 10.1016/j.icrp.2007.10.003
