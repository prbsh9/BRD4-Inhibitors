# 04_MD

GROMACS input files for the 100 ns BRD4 BD1 simulations.

| Folder | System |
|---|---|
| `mdp/complex/` | BRD4 BD1 + CNP0301965.2, 23,645 atoms |
| `mdp/apo/` | apo BRD4 BD1, 23,612 atoms |

## Protocol

| Step | File | Settings |
|---|---|---|
| Energy minimization | `EM.mdp` | steepest descent, ≤ 50,000 steps, `emtol` 1000 |
| NVT | `NVT.mdp` | 100 ps, V-rescale, 300 K |
| NPT | `NPT.mdp` | 100 ps, C-rescale, 1 bar |
| Production | `MD.mdp` | 100 ns (50,000,000 × 2 fs), V-rescale 300 K, Parrinello-Rahman 1 bar |

Force field `charmm36-feb2026_cgenff-4.6.ff` with TIP3P water; PME electrostatics with a
1.2 nm cutoff; Lennard-Jones force-switch from 1.0 to 1.2 nm; LINCS on bonds to hydrogen;
`DispCorr = no`.

The apo run used the same protocol — only `mdp/apo/MD.mdp` and `mdp/apo/NPT.mdp` differ
from the complex set.
