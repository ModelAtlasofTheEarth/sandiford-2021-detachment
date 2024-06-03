### -> submitter ORCID (or name)

0000-0002-2207-6837

### -> slug

sandiford-2021-detachment

### -> license

CC-BY-4.0

### -> model category

model published in study, forward model

### -> associated publication DOI

http://dx.doi.org/10.1029/2021gc009681

### -> model creators


### -> model contributors

_No response_

### -> title

_No response_

### -> description

This model was developed in order to study the rotation of footwall rocks beneath oceanic detachment faults (ODFs). It showed that solid-block rotation dominates beneath a concave-down fault, while significant flexural stresses form later during "apparent unbending," causing both compression and extension-related brittle strain within oceanic core complexes (OCCs).

### -> abstract

_No response_

### -> scientific keywords

tectonics, faulting, detachment faults

### -> funder

https://ror.org/05mmh0f86, DP180102280
https://www.helmholtz.de/, VH-NG-1132

### -> include model code ?

- [X] yes

### -> model code/inputs DOI

https://github.com/dansand/odf_paper

### -> model code/inputs notes

ASPECT Input files for model. Input file has been updated for compatibility with more recent ASPECT versions. Input file tested on  ASPECT version 2.6.0-pre (fix_stresses_elasticity, 621dd61f2), using deal.II 9.4.2.

### -> include model output data?

- [X] yes

### -> data creators

0000-0002-2207-6837

### -> model output data DOI

_No response_

### -> model output data notes

Data directory contains output data for 2 simulations stored in the following directories: ref_model_hires, alt_model_hires. Top level contains typical ASPECT output files, including log.txt and restart files. Topography and mesh variables were output at 100 Kyr intervals. Model end time is 5 Myr. Main output data consists of of plain text files representing model topography (e.g. topography.00000), vtu files (in the ./solution sub-directory) representing model output fields (e.g. solution-00000.0000.vtu). At each output step, there are 16 vtu files written. These can be opened with Paraview using the solution.pvd file in the top level.

### -> model output data size

Model output data total about 11Gb

### -> software framework DOI/URI

https://doi.org/10.5281/zenodo.8200213

### -> software framework source repository

_No response_

### -> name of primary software framework (e.g. Underworld, ASPECT, Badlands, OpenFOAM)

_No response_

### -> software framework authors

_No response_

### -> software & algorithm keywords

C++, finite-element, mesh-refinement

### -> computer URI/DOI

https://dx.doi.org/10.25914/608bfd1838db2

### -> add landing page image and caption

![fig1](https://github.com/ModelAtlasofTheEarth/Model_Submission/assets/10967872/7f203806-1aed-4952-9b12-63e3b76ddd3d)
Deviatoric stresses and vorticity in reference model.

### -> add an animation (if relevant)


https://github.com/ModelAtlasofTheEarth/Model_Submission/assets/10967872/1f89632e-53ee-4b34-8eaf-2f8a8ce351a4
Animation for alternative model showing vorticity. 


### -> add a graphic abstract figure (if relevant)

![fig4](https://github.com/ModelAtlasofTheEarth/Model_Submission/assets/10967872/ca7dd23e-aa3b-4809-9a35-b2b9c26dbf89)
Schematic showing the stress state that would be generated assuming elastic constitutive response of the ODF footwall (top). Bottom shows the strain-rate due to "advective" component of the curvature rate.  

### -> add a model setup figure (if relevant)

![initialconds](https://github.com/ModelAtlasofTheEarth/Model_Submission/assets/10967872/bbc016ba-3da5-4135-b0e8-594d6fac89d0)
Initial conditions, showing mesh refinement.

### -> add a description of your model setup

The domain is $400 \; \mathrm{km}$ wide and $100 \; \mathrm{km}$ deep, and includes five levels of mesh refinement, as shown in the figure. The model is initialised with a symmetric temperature structure, defined by a transient 1-D cooling profile, with an age of $0.5 \; \mathrm{Myr}$ in the center of the domain. The thermal profile ages outwardly in proportion to the applied spreading rate of $2 \; \mathrm{cm\,{yr}^{-1}}$ (full rate), which is representative for slow spreading ridges. Uniform inflow at the bottom boundary balances the outward flux of material at the side boundaries. The model has a true free surface, and a diffusion process is applied to the surface topography in order to counteract strong mesh deformation. A simplification here is that the effect of the water column is ignored, i.e. the detachment system is modeled as sub-aerial. There is no compositional differentiation in the model (i.e. no crust/mantle) and all parts of the domain are subject to the same constitutive model. The constitutive model incorporates viscous (dislocation creep), elastic and plastic (pseudo-brittle) deformation mechanisms, hereafter referred to as visco-elastic plastic (VEP) rheology, following the approach of Moresi et al. (2003). The advection-diffusion equation included an anomalously- high diffusivity $(3 \times {10}^{-6} \; \mathrm{m^2 \, s^{-1}})$ which is intended to model the near axis cooling effect of hydrothermal circulation (cf. Lavier and Buck, 2002). As implemented here, the higher diffusivity applies throughout the domain, rather than being localized at the ridge (as in Lavier and Buck, 2002). The parameters chosen here result in $\sim 10 \; \mathrm{km}$ lithosphere at the ridge axis, which is in the range identified for ODF development. Due to the difference in diffusivity values in the initial conditions $({10}^{-6} \; \mathrm{m^2 \, s^{-1}})$, and temperature evolution equation $(3 \times {10}^{-6})$, the thermal structure is not in steady state and some cooling of the off-axis lithosphere occurs.