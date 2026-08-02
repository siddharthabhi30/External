# My Interpretation of the Mapping Particle Filter

## Particle Flow Filter

The Mapping Particle Filter (MPF) belongs to the family of particle flow filters. Instead of resampling the particles, a particle flow filter moves them continuously from the prior distribution toward the posterior distribution.

The movement takes place through an artificial pseudo-time $\lambda$. A velocity field moves the particles according to the ordinary differential equation:

$$
\frac{dx_\lambda}{d\lambda}
=
v_\lambda(x_\lambda).
$$

Here, $v_\lambda(x_\lambda)$ determines the direction and speed with which a particle moves at the current pseudo-time.

The movement happens iteratively. At every pseudo-time step, the method:

1. calculates the velocity field using the current particles;
2. moves each particle by a small step:

$$
x_{\lambda+\epsilon}
=
x_\lambda+\epsilon v_\lambda(x_\lambda);
$$

3. recalculates the velocity field using the moved particles;
4. repeats the process.

## Mapping Particle Filter

The difference in the MPF is how it chooses the velocity field. It chooses the direction that reduces the KL divergence between the current intermediate particle distribution and the target posterior distribution.

The negative KL gradient is used as the velocity field:

$$
v_\lambda(x_\lambda)
=
-\nabla KL(x_\lambda).
$$

Therefore, the MPF particle update is:

$$
x_{\lambda+\epsilon}
=
x_\lambda-\epsilon\nabla KL(x_\lambda).
$$

The final velocity field used by the MPF is the negative KL gradient:

$$
v(x)
=
-\nabla KL(x)
=
\frac{1}{N_p}
\sum_{l=1}^{N_p}
\left[
K(x^{(l)},x)\nabla_{x^{(l)}}\log p(x^{(l)})
+
\nabla_{x^{(l)}}K(x^{(l)},x)
\right].
$$

The kernel-gradient term provides the repelling force intended to prevent particle collapse. Hu and van Leeuwen (2021) show that, with the scalar kernel in a high-dimensional system, this repelling force can become too weak.

Hu and van Leeuwen (2021) explain the failure of the scalar kernel by stating that:

> “the repelling force is too weak”

They connect this weak repulsion with particles collapsing toward the posterior mode in the observed component.

## Gaussian Scalar Kernel

The original MPF experiments use the Gaussian scalar kernel:

$$
K(x,x')
=
\exp\left[
-\frac{1}{2}
(x-x')^T A^{-1}(x-x')
\right].
$$

## Scalar-Kernel Limitation

Hu and van Leeuwen (2021) summarize the earlier Pulido and van Leeuwen (2019) result as follows:

> “the scalar kernel works well for the 40-variable Lorenz 96 system”

That experiment used 20 observations, corresponding to 50% of the system being observed.

Hu and van Leeuwen (2021) later state that when the ensemble size is much smaller than the system dimension, care is needed in formulating the kernel. For their 1,000-variable system with 250 observations:

> “problems arise when using the scalar kernel”

They therefore generalize the scalar kernel to a matrix-valued kernel. The original scalar-kernel MPF was demonstrated on the lower-dimensional 40-variable system, while the later work addresses the difficulty of applying that scalar kernel to a much higher-dimensional system.

## Paper Links

- [Pulido and van Leeuwen (2019), “Kernel Embedding of Maps for Sequential Bayesian Inference: The Variational Mapping Particle Filter”](https://arxiv.org/pdf/1805.11380)
- [Hu and van Leeuwen (2021), “A Particle Flow Filter for High-Dimensional System Applications”](https://rmets.onlinelibrary.wiley.com/doi/epdf/10.1002/qj.4028)
- [Hu et al. (2024), “An Implementation of the Particle Flow Filter in an Atmospheric Model”](https://journals.ametsoc.org/downloadpdf/view/journals/mwre/152/10/MWR-D-24-0006.1.pdf)

## TODO

- Understand the mathematics of particle flow filters end to end.
- Read [Hu and van Leeuwen (2021), “A Particle Flow Filter for High-Dimensional System Applications”](https://rmets.onlinelibrary.wiley.com/doi/epdf/10.1002/qj.4028).
- Read the 2024 PFF-DART paper: [“An Implementation of the Particle Flow Filter in an Atmospheric Model”](https://journals.ametsoc.org/downloadpdf/view/journals/mwre/152/10/MWR-D-24-0006.1.pdf).
