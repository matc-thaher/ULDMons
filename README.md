# ULDMons

ULDMons is a MATLAB solver for ultralight dark matter bosons. It evolves the 3D Schroedinger-Poisson
system in a periodic box and tracks how a soliton moves, how the box size and resolution change the
result, and how test particles respond. Optional extras: self-interaction, mass and length rescaling,
and massive particles with CIC coupling for dynamical friction.

Files
- uldmons_run.m       solver (CPU or GPU), diagnostics, snapshots, checkpoints
- uldmons_selftest.m  mass, scaling, and particle-energy checks. Run first.
- uldmons_example.m   example configurations
- run_uldmons.sh      SLURM template

Quick start
    uldmons_selftest
    out = uldmons_run(struct('N',64,'Lbox',0.4,'duration_Gyr',2000));

Units: Mpc, Msun, km/s, time Mpc/(km/s) = 977.79 Gyr. Array order is ndgrid (x is the first index).
