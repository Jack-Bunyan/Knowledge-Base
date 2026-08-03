---
title: Q-Brachytherapy TG43 graph
---
The TG43 graph shows how the dose rate from a HDR brachytherapy source varies with the distance from the source.  This graph does not take into effect the build-up region, yet despite this produces a build-up region to peak, as well as a smaller region at the centre of the region where dose falls off.
![[TG43 graph.png]]

When considering what causes this region, it is important to consider the structure of what this graph represents.  At any given point there are x-rays travelling from various points of the source, each of which must travel through the shielding of the applicator.

From our understanding of [[On Particle Interactions|Particle Interactions]] we know that
> $\Phi = \Phi_0 \exp(-\mu x)$ 

Where the particle flux $\Phi$ will be proportional to the [[Dose]].  For a path that travels through multiple materials the attenuation can be combined as follows
> $\Phi = \phi_0 \exp(-\mu_1 x_1)\cdot \exp(\mu_2 x_2) = \Phi_0 \exp(-\mu_1 x_1 -\mu_2 x_2)$

This takes into account the attenuation from the portion of travel both within the applicator and the tissue surrounding it.  
![[brachytherapy source question diagram.png]]
From the simple geometry of the situation the distances $x_1$ and $x_2$ can be calculated as

> $x_1 = \sqrt{A^2+\left(\frac{A}{x}y\right)^2}$
> $x_2 =\sqrt{(x-A)^2+\left(\frac{x-A}{x}y\right)^2}$

We can use an integral to consider a line source where the radiation path passes through materials with those distances.

> $D\propto \int_{-\infty}^{\infty}\exp\left(-\mu_1 \sqrt{A^2+\left(\frac{A}{x}y\right)^2}-\mu_2 \sqrt{(x-A)^2+\left(\frac{x-A}{x}y\right)^2}\right)\text{d}y$ 

The graph below shows that the increase in dose can be replicated with a purely analytical model using arbitrary figures.  Though, when including the distance falloff, the linear falloff dominates this attenuation affect (magnitudes in graph are arbitrary).
<iframe src="https://www.desmos.com/calculator/4zvgrovafk?embed" width="700" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>

The cause for this is that the capsule is the dominant attenuator in this situation; when the point is further from the source the rays that travel to the point are normal to the shielding, passing through and being attenuated by less of the material.  Closer to the source it must travel at a steeper angle, this means that a greater portion of the distance is through the attenuating material decreasing the dose.
