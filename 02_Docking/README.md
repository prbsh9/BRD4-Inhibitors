# 02_Docking

Docking of the 150 ML-selected compounds and 7 reference inhibitors into BRD4 BD1.

## Tools

| Step | Tool |
|---|---|
| Receptor preparation | AutoDock Tools |
| Ligand preparation (SMILES → 3D, protonation at pH 7.4) | Meeko |
| Ligand conversion (SDF → PDBQT) | OpenBabel |
| Docking | AutoDock Vina 1.2.7 |
| Protein–ligand interactions | PLIP |


Docking command used for every ligand:

```bash
vina --receptor receptor.pdbqt --ligand ligand.pdbqt \
     --config vina_box.txt \
     --exhaustiveness 32 --num_modes 9 --seed 42 \
     --out ligand_docked.pdbqt
```
