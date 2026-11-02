# BRD4-Inhibitors

Code for the manuscript:

> *In Silico Identification of Natural BRD4 Inhibitors with Machine Learning, Virtual
> Screening, Applicability Domain Analysis, Docking, Molecular Dynamics, Quantum
> Mechanical Analysis and ADMET Evaluation*
> Prabesh Gautam, Unique Acharya, Arjun Acharya

This repository contains code and run settings only. No data, structures or simulation
outputs are included — see **Before you start**.

## Contents

| Folder | What it is |
|---|---|
| `01_ML/` | Curation, model benchmarking and virtual-screening notebook |
| `02_Docking/` | Docking box and protocol (AutoDock Tools, Meeko, OpenBabel, Vina, PLIP) |
| `03_DFT/` | Gaussian 16 input files for CNP0301965.2 |
| `04_MD/` | GROMACS `.mdp` run settings for the complex and apo simulations |

## Before you start

| Input | Where to get it |
|---|---|
| ChEMBL activities for BRD4, target `CHEMBL1163125` | ChEMBL web services |
| COCONUT natural-product library, 09-2026 snapshot | https://coconut.naturalproducts.net |
| BRD4 BD1 structure, PDB `3MXF` | RCSB PDB |

Tools used: RDKit, scikit-learn, AutoDock Tools, Meeko, OpenBabel, AutoDock Vina 1.2.7,
PLIP, Gaussian 16, GROMACS 2026, gmx_MMPBSA 1.7.0.


## License

MIT — see `LICENSE`.
