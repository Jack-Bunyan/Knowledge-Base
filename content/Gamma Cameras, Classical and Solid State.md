---
title: On Gamma Cameras
permalink: GammaCameras
date: 2026-07-07
tags:
  - Physics
  - Nuclear_Medicine
  - Imaging
  - CB_Notion
---
Gamma Cameras are used to detect the [[Decay Events]] from the [[Radioisotopes]] used within [[Radio-pharmaceuticals]].

There are 2 main technologies that can be used to create a gamma camera, these being a solid state or scintillation event camera.  Typically a solid state camera is better, however the nature of crystal growth means that they will cost a lot more.

# Scintillation Camera
Scintillation Cameras are made up of 4 main structures, these being the [[Collimator]], the Scintillation Crystal, Photomultiplier tubes, and the Anger Logic.
![[Gamma_Camera-SystemDiagram.png|697]]
## Basic Process

| ![[entire system diagram of the gamma camera.png\|3000]] | 1)Patient is injected with radioactive tracer (uptake time may be required).<br><br>2)Patient is positioned under the camera.<br><br>3)Radiation emitted from the patient travels through the [[Collimator]].<br><br>4)Scintillation crystal is hit by radiation which creates a light.<br><br>5)Light is converted to electrical signal through photomultiplier tubes (PMTs) and signal amplifiers which is converted into an image on the screen. |
| ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |




## Scintillation Crystal
The main purpose of the Scintillation Crystal is to convert the high energy gamma rays released by the isotope into the visible light wavelength range.  They have a lower limit of around 30keV (limited by the bandgap of the crystal),and an upper range of 360keV (limited by the attenuation of the crystal).  Clinically these are roughly 9.5mm thick, balancing the sensitivity of the gamma camera with the spatial resolution.

Generally use a single, large-area NaI(Tl) scintillation crystal. There is a light guide which permits light to travel to PMTs. Hermetically sealed as crystal is hygroscopic (crystal discolours and loses effectiveness if moisture is absorbed).

>💡 Hygroscopic = tends to pull in moisture from air.

![[Scintillator Crystal charlie f9igure.png]]
Crystal is hit by a gamma photon which emits visible blue light photons.

These tend to be optimised for the detection of the [[Tc99m]] isotope, which has a gamma ray emission of 140.5keV, as this is the most frequently used isotope within nuclear medicine.

[[Cosmi et al. - 2024 - NaI gamma camera performance for high energies Effects of crystal thickness, photomultiplier tube g.pdf]]

The mechanism behind this is based of a Sodium Iodide Crystal doped with some Thallium.  This thallium creates activation sites where the band-gap is in the visible light range; this means that the photons are compatible with photo-multiplier tubes,  less likely to re-interact with the crystal, and it improves the likelihood of radiative transfers. ![[Figures_Crystal.gif]]
Since the number of electrons that are excited and therefore the number of photons released is related to the energy of the incoming gamma photon.  
![[scintillation_crystal_technetrium_spectrum.png]]
[[Aoun et al. - 2008 - Validation of the Small Animal Biospace Gamma Imager Model Using GATE Monte Carlo Simulations on the.pdf]]
An ideal spectrum would be a single spectral line at 140keV, however, due to [[On Particle Interactions#Photons|Interactions]] within the crystal there are spectral features.
- Scatter: the region from 60-100keV in the image above is due to to scatter events within both the crystal and the patient tissue.  The upper and lower bounds of this are defined by complete backscatter (lower bound) and the [[On Particle Interactions#Cross-section|Cross-section]] of the interaction (upper bound)
- Pile-up: if two events occur at similar times in a similar area the amplitudes of the pulses will add together, resulting in a double height pulse.
- Thermal-noise: while not necessarily a result of the crystal, thermal electrons will be picked up, causing a spike near 0keV

[[The Gamma Camera-A comprehensive Guide_Richard Lawson_Crystals.pdf]]

## Photo-multiplier Tube
Though the crystal produces more than one photon, due to the large loss of signal from the collimator, cross-section of interaction, attenuation, and inverse square law.  In order to increase the total signal of the event the visible light photons are fed into a photo-multiplier tube.
![[PMT-image-self-1.jpg|330]]![[PMT-image-self-2.jpg|330]] 
![[PMT diagram structure charlie.png]]
![[Figures_PMT-cascade.gif|720]]
There are 4 main components of the photo-multiplier tube
- Photo-cathode: Converts the incoming photon to an electron
- Focusing Electrode: directs the electron produced at the photo-cathode towards the dynodes 
- Dynodes: Exponentially increase the number of electrons at each event, amplifying signal
- Anode: Measures the total number of electrons produced, proportional to the original number

Light photons from NaI(Tl) crystal hit photoemissive surface (photocathode). The photoelectric effect converts these photons into photoelectrons. There is ~1/5 chance for this to happen. When dynodes are hit by photoelectrons, several secondary electrons are emitted (3-6x electrons emitted).

>A voltage is applied to every dynode which increases along the PMT which allows for attraction and progression of electrons.

## Electronics
The signals produced by the photo-multiplier tubes are converted into three distinct pulses:
- X: x-coordinate of the event
- Y: y-coordinate of the event
- Z: total signal

The actual layout of a gamma camera collimator system is typically a hexagonal array, due to the size of each individual one they do not independently represent individual pixels.  Instead, since the visible light photons spread out to adjacent PMTs, the system can perform statistical processing to find the relative intensities to different locations.

The electronics also allow for selection of what energy bands are accepted for creating the image, this is typically done as 10% around the peak energy of the isotope, and is done to reduce the impact of scatter on the image, as these would appear to occur from a different location within the patient, reducing the [[Resolution]].
![[scintillator signal scale.png]]

# Solid State
# JAQs
[[Q-Anger Logic Relative vs Individual]]

