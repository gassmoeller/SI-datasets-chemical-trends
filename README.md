# SI-datasets-chemical-trends
Input files and shared libraries to reproduces the results of Dannberg &amp; Gassmoeller (2018): Chemical trends in ocean islands explained by plume–slab interaction ([https://doi.org/10.1073/pnas.1714125115](https://doi.org/10.1073/pnas.1714125115)):

The .h and .cc files contain the shared libararies used for the 2d model runs and can be compiled using
the file CMakeLists.txt as described in the [ASPECT manual](http://www.math.clemson.edu/~heister/manual.pdf). 
The file 150Ma.prm can then be used to reproduce the first stage of the 2d models, where slow lower mantle
flow forms thermo-chemical piles. 
Finally, the files 0.1mm.prm, 5mm.prm and 15mm.prm can be used to run the second stage of the 2d models,
where a slab flow in from the left. Names of the file give the slab inflow velocity. In order to do this, 
the output of the first models stage first has to be copied an renamed to the name given under 
'set Output directory' in the respective input file (i.e. output\_0.1mm, output\_5mm and output\_15mm), 
so that the second stage can restart from the output of the first one. 

The files starting with azores\_, samoa\_ and easter\_galapagos\_ are the input files for the 3d regional
models, and the number in the file name gives the core-mantle boundary temperature (as detailed in the
manuscript). All files can be run with the version of ASPECT given under Model Setup in the 
Supporting Information. 
