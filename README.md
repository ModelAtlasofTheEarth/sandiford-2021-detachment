# New [M@TE](https://mate.science/)! model: 
 _we have provided a summary of your model as a starting point for the README, feel free to edit_
## Section 1: Summary of your model   

**Model Submitter:**  

Dan Sandiford ([0000-0002-2207-6837](https://orcid.org/0000-0002-2207-6837))

**Model Creator(s):**  

- Dan Sandiford ([0000-0002-2207-6837](http://orcid.org/0000-0002-2207-6837))  
- Sascha Brune ([0000-0003-4985-1810](http://orcid.org/0000-0003-4985-1810))  
- Anne Glerum ([0000-0002-9481-1749](http://orcid.org/0000-0002-9481-1749))  
- John Naliboff ([0000-0002-5697-7203](http://orcid.org/0000-0002-5697-7203))  
- Joanne M. Whittaker ([0000-0002-3170-3935](http://orcid.org/0000-0002-3170-3935))  
  
**Model name:**  

`sandiford-2021-detachment-1` 

(this will be the name of the model repository when created) 

**Model long name:**  

_Kinematics of Footwall Exhumation at Oceanic Detachment faults: Solid‐Block Rotation and Apparent Unbending_  

**License:**  

[Creative Commons Attribution 4.0 International]( https://creativecommons.org/licenses/by/4.0/legalcode.txt)

**Model Category:**  

- model published in study   
- forward model   
  
**Model Status:**  

  
**Associated Publication title:**  

_[Kinematics of Footwall Exhumation at Oceanic Detachment faults: Solid‐Block Rotation and Apparent Unbending](http://dx.doi.org/10.1029/2021gc009681)_ 

**Abstract:**  

Seafloor spreading at slow rates can be accommodated on large‐offset oceanic detachment faults (ODFs), that exhume lower crustal and mantle rocks in footwall domes termed oceanic core complexes (OCCs). Footwall rocks experience large rotation during exhumation, yet important aspects of the kinematics—particularly the relative roles of solid‐block rotation and flexure—are not clearly understood. Using a high‐resolution numerical model, we explore the exhumation kinematics in the footwall beneath an emergent ODF/OCC. A key feature of the models is that footwall motion is dominated by solid‐block rotation, accommodated by the nonplanar, concave‐down fault interface. A consequence is that curvature measured along the ODF is representative of a neutral stress configuration, rather than a “bent” one. Instead, it is in the subsequent process of “apparent unbending” that significant flexural stresses are developed in the model footwall. The brittle strain associated with apparent unbending is produced dominantly in extension, beneath the OCC, consistent with earthquake clustering observed in the Trans‐Atlantic Geotraverse at the Mid‐Atlantic Ridge.

**Scientific Keywords:**  

- tectonics   
- faulting   
- detachment faults   
  
**Funder(s):**  
- Australian Research Council (https://ror.org/05mmh0f86)  
-  (https://www.helmholtz.de/)  
  
## Section 2: your model code, output data  

** No embargo on model contents requested****Include model code:**   

True 

**Model code existing URL/DOI:**   

https://github.com/dansand/odf_paper 

**Model code notes:**   

ASPECT Input files for model. Input file has been updated for compatibility with more recent ASPECT versions. Input file tested on  ASPECT version 2.6.0-pre (fix_stresses_elasticity, 621dd61f2), using deal.II 9.4.2. 

**Include model output data:**   

True 

**Model output data notes:**   

Data directory contains output data for 2 simulations stored in the following directories: ref_model_hires, alt_model_hires. Top level contains typical ASPECT output files, including log.txt and restart files. Topography and mesh variables were output at 100 Kyr intervals. Model end time is 5 Myr. Main output data consists of of plain text files representing model topography (e.g. topography.00000), vtu files (in the ./solution sub-directory) representing model output fields (e.g. solution-00000.0000.vtu). At each output step, there are 16 vtu files written. These can be opened with Paraview using the solution.pvd file in the top level. 

## Section 3: software framework and compute details   
**Software Framework DOI/URL:**  

Found software: _[geodynamics/aspect: ASPECT 2.5.0](https://doi.org/10.5281/zenodo.8200213)_ 

**Name of primary software framework:**  

geodynamics/aspect: ASPECT 2.5.0 

**Software & algorithm keywords:**  

- C++   
- finite-element   
- mesh-refinement   
  
## Section 4: web material (for mate.science)   
**Landing page image:**  

Caption: ![fig1](https://github.com/ModelAtlasofTheEarth/Model_Submission/assets/10967872/7f203806-1aed-4952-9b12-63e3b76ddd3d)
Deviatoric stresses and vorticity in reference model.  
  
**Animation:**  

Caption: https://github.com/ModelAtlasofTheEarth/Model_Submission/assets/10967872/1f89632e-53ee-4b34-8eaf-2f8a8ce351a4
Animation for alternative model showing vorticity.  
  
**Graphic abstract:**  

Caption: ![fig4](https://github.com/ModelAtlasofTheEarth/Model_Submission/assets/10967872/ca7dd23e-aa3b-4809-9a35-b2b9c26dbf89)
Schematic showing the stress state that would be generated assuming elastic constitutive response of the ODF footwall (top). Bottom shows the strain-rate due to "advective" component of the curvature rate.  
  
**Model setup figure:**  

Caption: ![initialconds](https://github.com/ModelAtlasofTheEarth/Model_Submission/assets/10967872/bbc016ba-3da5-4135-b0e8-594d6fac89d0)
Initial conditions, showing mesh refinement.  
Description:  The domain is $400 \; \mathrm{km}$ wide and $100 \; \mathrm{km}$ deep, and includes five levels of mesh refinement, as shown in the figure. The model is initialised with a symmetric temperature structure, defined by a transient 1-D cooling profile, with an age of $0.5 \; \mathrm{Myr}$ in the center of the domain. The thermal profile ages outwardly in proportion to the applied spreading rate of $2 \; \mathrm{cm\,{yr}^{-1}}$ (full rate), which is representative for slow spreading ridges. Uniform inflow at the bottom boundary balances the outward flux of material at the side boundaries. The model has a true free surface, and a diffusion process is applied to the surface topography in order to counteract strong mesh deformation. A simplification here is that the effect of the water column is ignored, i.e. the detachment system is modeled as sub-aerial. There is no compositional differentiation in the model (i.e. no crust/mantle) and all parts of the domain are subject to the same constitutive model. The constitutive model incorporates viscous (dislocation creep), elastic and plastic (pseudo-brittle) deformation mechanisms, hereafter referred to as visco-elastic plastic (VEP) rheology, following the approach of Moresi et al. (2003). The advection-diffusion equation included an anomalously- high diffusivity $(3 \times {10}^{-6} \; \mathrm{m^2 \, s^{-1}})$ which is intended to model the near axis cooling effect of hydrothermal circulation (cf. Lavier and Buck, 2002). As implemented here, the higher diffusivity applies throughout the domain, rather than being localized at the ridge (as in Lavier and Buck, 2002). The parameters chosen here result in $\sim 10 \; \mathrm{km}$ lithosphere at the ridge axis, which is in the range identified for ODF development. Due to the difference in diffusivity values in the initial conditions $({10}^{-6} \; \mathrm{m^2 \, s^{-1}})$, and temperature evolution equation $(3 \times {10}^{-6})$, the thermal structure is not in steady state and some cooling of the off-axis lithosphere occurs.

  
