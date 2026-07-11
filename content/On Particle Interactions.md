---
tags:
  - Physics
title: On Particle Interactions
---

# Photons
Photon interactions with matter consist of 3 main kinds:
- Pair production
- Photoelectric effect
- Compton Scatter
- Elastic Scatter
![[Photon-cross-section-RTBible.png]]
Overall, this leads to 3 main regions in most materials, a low energy region where the photo-electric effect is dominant, and intermediate region where Compton scatter is dominant, and a final region where pair production becomes dominant.
## Pair-production
![[feynman-Pair-Production.png]]
Pair production is only possible for photons that have a total mass greater than 1.022MeV (twice the fundamental mass of an electron).  When this is reached there is a probability that when interacting with the electric field of a charge they will produce a positron and electron.

The probability of an with the [[Atom#nucleus|Nucleus]] of an atom occurring is proportional to the square of the charge of the nucleus ($\sigma_{pp-n} \propto Z^2$), while occurring within the field of it's electrons (a process known as triplet production) is proportional to the number of electrons ($\sigma_{pp-e} \propto Z$).

[[Hubbell and Seltzer - 2004 - Cross section data for electron–positron pair production by photons a status report.pdf]]
## Photo-electric effect
![[feynman-Photo-Electric.png]]

The photo-electric effect is the process by which a photon is completely absorbed by an electron in the [[Atom#Orbital Shell|Orbital Shell]] of an [[Atom]].  This is the dominant process at low energies with the cross section of the interaction being inversely proportional to the cube of energy and the 4-5th power of the nucleus charge ($\sigma_{pe} \propto \frac{Z^{4\rightarrow 5}}{E^3}$).  This cross-section increases significantly when close to the transmission level of an orbital electron, this can be used by [[Photon Counting CT]] to perform spectroscopy on low Z contrast agents.
![[Ray-Spectrum_Iodine.png|697]]
The locations of these spikes will depend on the orbital energy levels of the atoms, this means that in elements (e.g. [[Iodine]], [[Calcium]], [[Lead]]) there will be sharp peaks at the locations of orbital transitions.  Whereas in more complex mediums (e.g. [[Bone]], soft tissue) these sharp transitions will overlap, creating a more continuous attenuation function.

## Compton Scatter
![[feynman-Compton_Scatter.png]]
Unlike the photo-electric effect where the energy from the photon is absorbed completely by the electron into kinetic and electrostatic energy; Compton scatter is a process by which the photon scatters from an electron, changing angle.
![[Figure_Compton-Scatter.gif]]
This results in a deflection of the photon by an angle $\theta_\gamma$, and a electron travelling away at an angle $\theta_e$ from the initial path of the photon.  Given the conservation of momentum and energy the transfer of energy to the electron can be calculated based on the angles of these deflections.
$$\lambda'-\lambda =\frac{h}{m_ec}(1-\cos\theta_\gamma)$$
For photon energies lower than the electron mass, the cross section of photon scatter remains relatively constant ($\sigma_{cs} =\frac{8}{3} \pi r_e^2$), and remains the dominant photon interaction within the 1-10MeV range for photons.

## Rayleigh and Thompson Scatter
Rayleigh and Thomspon scatter are both forms of elastic scattering from charges.  In the case of Rayleigh scatter this is a result of scatter from an entire atom, whereas Thompson is from an unbound electron.  The cross-section of Rayleigh is proportional to the inverse square of energy ($\sigma_{rs}\propto E^{-2}$), whereas the cross section of Thompson is more complex the correlation is slightly stronger than the inverse square.

# Electrons
The majority source of energy loss in charged particle interactions are collisions, electrons being the lightest of these charged particles have 3 main interactions:
- Moller scattering- collisions with bound electrons
- Bremsstrahlung- radiative losses from charge acceleration
- Elastic scattering- mostly a result of collisions with heavy charged particles
![[Electron-Stopping-Power-RTBible.png]]

# Cross-section

The Cross-section of an interaction will be dependant on the nature of the particle, its energy, and the medium that it is passing through.   Analytically, if the cross section of a particle is described as $\sigma$ the total flux of particles passing through a medium can be described to be:
$$\Phi  =\Phi_0 e^{-n\sigma z}$$
This comes from the idea that the rate of interaction within the medium is described as 
$$\frac{d\Phi}{dz}=-n\sigma \times \Phi$$
Since this is a probabilistic situation it will correlate with the total number of events when it could happen, and the more particles are in a medium the more likely an interaction.
