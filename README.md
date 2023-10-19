# Z1+ code

The Z1+ code creating the shortest multiple disconnected path for the analysis of entanglements in macromolecular systems is available for download [here at mendeley](https://data.mendeley.com/datasets/m425t6xtwr/1)
The related publication describing all features is available for free [here at Comput. Phys. Commun.](https://www.sciencedirect.com/science/article/pii/S0010465522002867?via%3Dihub)

Here we collect questions, answers, and additional scripts that may be useful for Z1+ users. 

## How to extract linear backbones from fully atomistic LAMMPS models 

Question: I am simulating atomistically detailed PMMA via LAMMPS, and have saved both a LAMMPS data file and a LAMMPS dump trajectory. Z1+ crashes as the LAMMPS files carry branched structures (chemical formula below). How to make it work? 

<img src="images/PMMA-chemical-formula.jpg" width="25%">

Answer: I created a script that automatically recognizes and extracts the linear backbones from your LAMMPS data file, and saves the linear conformation as Z1-formatted file config.Z1. The Z1+ code can then be directly applied to config.Z1. If you have both a LAMMPS data file and LAMMPS dump trajectory for the same system, this script creates a Z1-formatted trajectory file. The script is available for download in the scripts folder. Call it via

    perl ./extract-backbone.pl

or 

    perl ./extract-backbone.pl <lammps-data-file>

or

    perl ./extract-backbone.pl <lammps-data-file> <lammps-dump-trajectory>

## How to cite the Z1+ code?

    M. Kröger, J. D. Dietz, R. S. Hoy and C. Luap,
    The Z1+package: Shortest multiple disconnected path for the analysis of entanglements in macromolecular systems,
    Comput. Phys. Commun. 283 (2023) 108567. DOI 10.1016/j.cpc.2022.108567

or if you are using bibtex:

    @article{Z1+,
     author = {M. Kr\"oger and J. D. Dietz and R. S. Hoy and C. Luap},
     title = {The Z1+package: Shortest multiple disconnected path for the analysis of entanglements in macromolecular systems},
     journal = {Comput. Phys. Commun.},
     volume = {283},
     pages = {108567},
     year = {2023},
     doi = {10.1016/j.cpc.2022.108567}
    }
