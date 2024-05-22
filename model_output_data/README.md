# Model Output Data

**Note Output Data will often be too large to host on Github.**

To access output data for this model, check the M@TE collection on NCI (http://dx.doi.org/10.25914/yrzp-g882), or refer to this model on the M@TE website (http://mate.science)


## Notes:

Data directory contains output data for 2 simulations stored in the following directories: ref_model_hires, alt_model_hires. Top level contains typical ASPECT output files, including log.txt and restart files. Topography and mesh variables were output at 100 Kyr intervals. Model end time is 5 Myr. Main output data consists of of plain text files representing model topography (e.g. topography.00000), vtu files (in the ./solution sub-directory) representing model output fields (e.g. solution-00000.0000.vtu). At each output step, there are 16 vtu files written. These can be opened with Paraview using the solution.pvd file in the top level.
