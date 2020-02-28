## CBIOMES Project
####  Constraint-based Modeling of Marine Microbial Community Metabolism and Physiology

> With Mick Follows and collaborators within the [CBIOMES Project](https://cbiomes.org), I am designing detailed models of microbial metabolism and physiology and using these models to simulate microbial community dynamics in the marine environment. 

> Two MATLAB toolboxes are under development for this project: The **M**icrobiome **S**imulation **E**nvironment toolbox ([MSE](https://github.com/jrcasey/mse)) and the **PanGE**nome-scale **M**etabolic model toolbox PanGEM (sorry, currently private). Lots more on them in time!    

##### Mesoscale dynamics of *Prochlorococcus*

> **Update:** Our first full-scale simulation -- *Prochlorococcus* growth across an eddy dipole transect -- is complete! We are thrilled with the results and are currently sifting through all the data to develop a compelling story. 

> The model was run using *in situ* data collected on the [2017 MESO-SCOPE Cruise](http://scope.soest.hawaii.edu/data/mesoscope/),
including depth profiles of flow cytometry cell counts and scattering properties, ITS-based relative abundances, nutrient concentrations, spectral irradiance, and temperature. These data are fed at each grid point to genome-scale metabolic models (GSMMs) for 48 sequenced isolate strains. Each GSMM goes through a series of bilevel optimizations which **allow the cell to physiologically acclimate to its environment** by altering its size, its macromolecular composition, its pigment composition, and the abundance and types of transporters on the cell surface. Using the acclimated GSMM and the associated constraints, flux balance analysis is then run to predict growth rates and metabolic fluxes. Finally, we apply a modified Arrhenius function using optimal 
growth temperatures derived from a machine learning algorithm. Here is a teaser: 

![useful image]({{ jrcasey.github.io }}/images/MSE_Pro_MESO-SCOPE.jpg)
*Ecotype averaged growth rates (h<sup>-1</sup>), predicted at local noon across the MESO-SCOPE transect. Station 6 is the center of the anti-cyclone; Station 12 is the center of the cyclone. 5 Ecotypes are shown: **H**igh-**L**ight adapted ecotypes **I** and **II**, and **L**ow-**L**ight adapted ecotypes **I** **II/III** and **IV**. Don't worry about that HLI at the bottom lol.*   


> There seems to be either a boundless flow of genes or a jaw-dropping amount of persistent micro-diversity within the  *Prochlorococcus* community. We could never hope to capture all the instances in GSMMs, so instead we are evolving *in silico*
strains synthesized from the pangenome using our PanGEM Toolbox. In addition to the 48 isolates, the pangenome also includes genes from 97 strains built from MAGs and SAGs, and we plan to include an additional 489 SAGs recently published by [Berube et al., 2018](https://www.nature.com/articles/sdata2018154).     


## Biological thermodynamics
> Something "heating up" here... yuk yuk yuk.