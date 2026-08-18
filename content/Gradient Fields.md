---
title: On Spatial Encoding
tags:
  - Imaging
  - Physics
---
> Spins in this page are shown to be rotating vertically.  This is not physical and is done for ease of figure-making.  All rotation is done in the x-y transverse plane.

The [[K-Space]] map formed by the [[Atomic Spin|Atomic Spin's]] of the patient would—without gradient fields—all be oscillating at the same rate.  While the [[Signal]] produced would contain information about the mass of the volume, it would contain no spatial information.

To encode spatial information into the signal that is produced by the spins, 3 different encoding methods are used: slice selection, only exciting a select region; frequency encoding, altering the frequency of the produced signals over space; and phase encoding, altering the phase of the produced signals over space.

![[typical sequence image.png]]

Title: [Sequences - Radiology Cafe](https://www.radiologycafe.com/frcr-physics-notes/mr-imaging/sequences/)
Authors: 
Year: 2017
DOI: 

# Slice Selection G$_{ss}$
![[FIgure_Slice Selection.gif]]
The Slice selection Gradient field is the first of the fields that is applied to the MRI sequence, this is done during the excitation of spins using the [[Radiofrequency Pulse]] to selectively excite only a certain region of the scan.  To ensure that there is no additional phase encoding introduced by this, the pulse is ran in reverse after the excitation is complete.

This can be used outside of the region that is being imaged such as in [[Arterial Spin Labelling]] to show the movement of resonant materials.
# Frequency Encoding G$_{FE}$
![[Figure_Frequency-Encode.gif]]
Frequency encoding is done during the acquisition stage of the image.  While the radiofrequency coils are receiving the signal from the excited spins, a gradient field is applied to the volume that varies across the slice, this means that spins in different locations will contribute different different frequency sine waves to the signal.  Similarly to the slice selection gradient, prior to application of frequency encoding, it is ran in reverse so that at the time of image acquisition there is no phase difference from the frequency encoding gradient.

While there aren't many fancy things done with frequency encoding specifically, the slight differences in the frequencies that are already present within the image enable the use of techniques such as [[dixon]] for fat-water imaging, or [[spectroscopy]] to image other elements within the image. 
Imaging a patient at multiple bandwidths can be used to suppress metal artefacts within the image, with sequences such as Mavric

Title: [MRI Near Metallic Implants Using MAVRIC SL: Initial Clinical Experience at 3T](https://pmc.ncbi.nlm.nih.gov/articles/PMC4323867/)
Authors: Luis B. Gutierrez, Bao H. Do, Garry E. Gold, Brian A. Hargreaves, Kevin M. Koch, Pauline W. Worters, Kathryn J. Stevens
Year: 2015
DOI: 10.1016/j.acra.2014.09.010

# Phase Encoding G$_{PE}$
![[Figure_Phase-encode.gif]]
Phase Encoding is done by temporarily increasing the frequency of the spins in a given direction before removing the phase encoding an allowing them to return to their initial frequency.  Phase encoding can also be done multiple times within a single acquisition, this technique is used for motion-sensing imaging such as [[4D flow imaging]] and [[Diffusion weighted Imaging]].

In [[3D MRI|3D]] images phase encoding is used twice to produce images where the phase direction is encoded out of plane, producing a 3-dimensional k-space.

---
By using each of these encoding strategies, each voxel in the volume is assigned a unique signal ($sin(\omega t+\theta)$) that it will produce ($\omega _x, \theta_y$).  Creating a K-space where each region contributes uniquely having both contrast and resolution data.
