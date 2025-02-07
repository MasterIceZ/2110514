# REALTIME COMPUTER GRAPHICS AND PHYSICS SIMULATION

## Homework 1: Phong Shading

### Rendering Equation

$$
R = k_aI + k_dI\max(\hat{l} \cdot \hat{n}, 0) + k_sI\max(\hat{r} \cdot \hat{v}, 0)^p
$$

- $k_a, k_d, k_s$ and $p$ are the material properties
- $I$ is the intensity of the light source
- $\hat{l}$ is the unit vector pointing to the light source
- $\hat{n}$ is the unit normal vector of the surface
- $\hat{r}$ is the reflection vector
- $\hat{v}$ is the unit vector pointing to the viewer

### Diffuse Component

$$
I_d = \max(k_dI(\hat{l} \cdot \hat{n}), 0)
$$

### Specular Component

$$
I_s = k_sI\max(\hat{r} \cdot \hat{v}, 0)^p
$$

where $\hat{r} = -\hat{l} + 2(\hat{l} \cdot \hat{n})\hat{n}$
