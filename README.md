# Machine Learned Tracking of Crystallization in Glasses

## Overview
This is open-source project that leverages machine learning techniques to track and analyze crystallization processes in lithium niobate glass. This project aims to provide a tool for researchers and scientists in materials science to better quantify crystallization in glass materials using a machine learned approach. This is an improvement over the current trends of using bond-orientational order (Steinhardt Parameters). 

## Features
- Worked out using atomic positions trajectory file from DL-POLY3 (called HISTORY file).
- For the snapshots, the Steinhardt parameters and the coord/atom are calcuated using LAMMPS.
- Even though this technique has been applied to lithium niobate, the technique is readily transferrable to any other system with slight modifications in the code.

## Algorithm
- Suppose, you have a simulation trajectory for your system for 5 ns spaced 100 ps (50 snapshots) from any simulation software (it could be VASP, SIESTA, LAMMPS, CPMD, DL-POLY, etc.)
- Create the coordinate file for each snapshot in LAMMPS format
- Calculate the Steinhardt parameter and coord/atom for each snapshot (for details, check the LAMMPS input file commands)
- Download the dump file for each snapshot in the directory where your calculations are run
- Run Part_I_KMeans*.ipynb
- Run KM3_SCG_*.ipynb

## Contributing/Collaborating
We are open to suggestions and genuinely comitted to making the code better. If you wish to colloborate in future projects that may involve simulations on different simualation packages, please reach out the the author. 

![Growth Rates Predicted by ML for various seed size](https://github.com/rajendrathapa/Machine_Learned_Tracking_of_Crystalization_in_Glasses/blob/main/Growth_rates.png?raw=true)


