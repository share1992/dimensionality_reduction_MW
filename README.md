# dimensionality_reduction_MW

This notebook does dimensionality reduction on an xyz [intrinsic reaction coordinate (IRC) or trajectory] file in three possible ways:

(1) Classical Multidimensional Scaling (CMDS) via the Taketsugu group's method (doi: 
(2) A new method of dimensionality reduction, using mass-weighted coordinates
(3) A new method of dimensionality reduction (same as above), without mass-weighting

For example, to compare results for the three different methods on the same xyz file, and example of the syntax for each of these methods would be:

file = 'examples/malondialdehyde/malondialdehydeTS_IRC.xyz'
ndim = 3

GoF_old,strain_old = Old_Way(file,ndim)
GoF_newMW,stress_newMW=New_Way_MW(file,ndim)
GoF_new_noMW,stress_new_noMW=New_Way_noMW(file,ndim)

Note: In my examples folder, the xyz files have the energy of each point in the "Title" line of the file, which is how the relative energies are able to be plotted.
