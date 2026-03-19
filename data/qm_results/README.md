# Quantum Pioneer QM Results

## DFT Results

### Schema

```json
{
    "smiles": "SMILES (with atom mapping indicating xyz and force order)",
    "route_section": "Level of theory",
    "charge": "Molecular formal charge",
    "multiplicity": "Electron multiplicity",
    "max_steps": "Maximum allowed steps",
    "cpu_time": "CPU time in seconds",
    "wall_time": "Wall time in seconds",
    "e0_h": "Enthalpy at 298K",
    "hf": "E0 for non-wavefunction methods",
    "zpe_per_atom": "Per-atom zero point energy",
    "e0_zpe": "Gibbs free energy at 0K",
    "gibbs": "Gibbs free energy at 298K",
    "dipole_au": "Molecular dipole in Atomic Units (AU)",
    "homo_lumo_gap": "HOMO-LUMO energy gap",
    "beta_homo_lumo_gap": "HOMO-LUMO energy gap for beta orbitals",
    "dipole_moment_debye": "X, Y, and Z components of dipole moment in debye",
    "aniso_polarizability_au": "Anisotropic polarizability in Atomic Units (AU)",
    "iso_polarizability_au": "Isotropic polarizability in Atomic Units (AU)",
    "scf": "Self-consistent field energy after optimization",
    "mulliken_charges_summed": "Mulliken charges with protons summed into heavy atoms",
    "frequencies": "Vibrational frequencies",
    "frequency_modes": "Vibrational modes",
    "initial_xyz": "Input XYZ coords",
    "std_xyz": "Standardized XYZ coords after optimization",
    "std_forces": "Standardized forces after optimization",
}
```

**Note**: The beta orbital HOMO-LUMO energy gap is `None` when `multiplicity` is 1
(i.e. closed-shell species).

## Semiempirical Results

### Schema

```json
{
    "smiles": "Species SMILES (with atom mapping indicating xyz and force order)",
    "route_section": "Level of theory",
    "charge": "Molecular formal charge",
    "multiplicity": "Electron multiplicity",
    "max_steps": "Maximum allowed steps",
    "cpu_time": "CPU time in seconds",
    "wall_time": "Wall time in seconds",
    "e0_h": "Enthalpy at 298K",
    "hf": "E0 for non-wavefunction methods",
    "zpe_per_atom": "Per-atom zero point energy",
    "e0_zpe": "Gibbs free energy at 0K",
    "gibbs": "Gibbs free energy at 298K",
    "frequencies": "Vibrational frequencies",
    "frequency_modes": "Vibrational modes",
    "initial_xyz": "Input XYZ coords",
    "std_xyz": "Standardized XYZ coords after optimization",
    "std_forces": "Standardized forces after optimization",
}
```

**Note**: Standardized forces from semiempirical calculations are only provided for
transition states. In the species dataset, this column is included for consistency, but
all values are set to `None`.

## DLPNO Results

### Schema

```json
{
    "smiles": "Species SMILES (with atom mapping indicating xyz and force order)",
    "route_section": "Level of theory",
    "charge": "Molecular formal charge",
    "multiplicity": "Electron multiplicity",
    "energy": "Final single point energy",
    "run_time": "Total run time",
    "input_coordinates": "Input xyz coords",
    "dipole_au": "Molecular dipole in Atomic Units (AU)",
    "t1_diagnostic": "T1 diagnostic",
}
```
