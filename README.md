# ML-PB-Covid-drug
[![DOI](https://zenodo.org/badge/334097696.svg)](https://zenodo.org/badge/latestdoi/334097696)

This repository contains data and simulation input from the paper:

"Pandemic Drugs at Pandemic Speed: Accelerating COVID-19 Drug Discovery with Hybrid Machine Learning- and Physics-based Simulations on High Performance Computers"

Agastya P. Bhati, Shunzhou Wan, Dario Alfè, Mathis Bode, Matteo Turilli, Shantenu Jha, Roger R. Highfield, Walter Rocchia, Nicola Scafuri, Sauro Succi, Dieter Kranzlmüller, Gerald Mathias, David Wifling, Yann Donon, Alberto Di Meglio, Sofia Vallecorsa, Anda Trifan, Arvind Ramanathan, Rick Stevens, Peter V. Coveney

https://arxiv.org/abs/2103.02843

What follows is a brief description of the contents

# Naming conventions 

Molecular models for four target proteins of SARS-CoV-2 were created for molecular simulations and free energy calculations. They are: 3C like protease (3CLPro), papain-like protease (PLPro), ADP-ribose phosphatase (ADRP), and non-structural protein 15 (NSP15).

100 compounds are studied for each of the proteins, which were chosen from 10,000 docked small molecules, based on their docking scores from the high throughput docking study.

Two apprpaches are applied for the free energy calculatiions:

- ESMACS: Enhanced Sampling of Molecular Dynamics with Approximation of Continuum Solvent
- TIES: Thermodynamic Integration with Enhanced Sampling

# Directories

## initial-pdbs

Contains .csv files for top 10,000 compounds to each protein target from docking studies, and PDB files for the proteins and the top 100 compounds. The latter are used to create starting structures for the MD simulations.

## ligand-ff-params

Forcefield files (`mol2` and `prep`) describing parameterized ligands.

## ESMACS

Files related to MMPBSA analysis in tab separated values format.

- `input` - contains the MMPBSA input file used for all analyses
- `3clpro`, `plpro`, `adrp` and `nsp15` - contain results for the four protein targets

## simulated-topologies

Amber forcefield topology (`prmtop`) and coordinate (`inpcrd` and `pdb`) files for all ligands (for ESMACS) or ligand pairs (for TIES).
