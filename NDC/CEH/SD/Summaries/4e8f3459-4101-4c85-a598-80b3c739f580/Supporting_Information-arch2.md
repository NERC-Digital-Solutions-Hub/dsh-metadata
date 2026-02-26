# Introduction

- Purpose of the dataset: Parameters used in the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system, to test new land surface parameterisations before full GCM implementation and to make projections for future emission scenarios where GCMs have not been run.
- Modelling approach: IMOGEN uses pattern-scaling to emulate GCMs, assuming local monthly meteorology changes scale linearly with global land warming. An Energy Balance Model (EBM) links evolving radiative forcing to land warming while accounting for oceanic thermal delays.
- Related work: A more detailed dataset description is forthcoming (Zelazowski et al., Climate pattern scaling set for an ensemble of 22 GCMs - adding uncertainty to the IMOGEN impacts system, in prep).

## Data Description

- EBM parameters (for each GCM): climate sensitivity over land λ_l and over ocean λ_o (W m^-2 K^-1), ocean effective thermal diffusivity κ (W m^-1 K^-1), ratio of mean land/ocean SST warming ν (dimensionless), and ocean fraction f.
- Calibration: IMOGEN EBM parameters and patterns calibrated against 22 GCMs in the CMIP3 CMIP3 ensemble. The parameters λ_l, λ_o, κ, ν, and f are provided in Table 1; local and monthly patterns are available for download in ASCII format.
- Table notes: The document lists the 22 GCMs (e.g., BCCR-BCM2.0, CGCM3.1(T47), CNRM-CM3, etc.) with their corresponding calibrated values for λ_l, λ_o, κ, ν, and f.

## Data Structure

- Directory layout: For each GCM, a directory named pattRelPR_d2_<GCM> exists (22 directories total).
- Monthly pattern files: Within each directory there are monthly ASCII files 'jan' through 'dec'.
- Spatial mapping: Every GCM is remapped to a common grid of 2.5° latitude × 3.75° longitude (HadCM3 original grid), consisting of 1631 land points.
- File content: Each file contains:
  1. Longitude
  2. Latitude
  3. Temperature change per degree global warming (Kelvin × Kelvin^-1)
  4. Relative humidity change per degree warming (% change × Kelvin^-1)
  5. Wind change per degree warming (m s^-1 × Kelvin^-1)
  6. Unused (0.0)
  7. Longwave change per degree warming (W m^-2 × Kelvin^-1)
  8. Shortwave change per degree warming (W m^-2 × Kelvin^-1)
  9. Unused (0.0)
  10. Precipitation change per degree warming (mm d^-1 × Kelvin^-1)
  11. Unused (0.0)
  12. Pressure change per degree warming (hPa × Kelvin^-1)
  13. Unused (0.0)
- Coupling: IMOGEN is routinely coupled to the JULES land surface model (examples in Huntingford et al., 2010; JULES described in Best et al., 2011; Clark et al., 2011).

## Quality Control

- Status: Patterns are part of a beta programme to extend IMOGEN EBM and pattern parameterisation to GCMs beyond the UK.
- Scope: Achieved against CMIP3; a new version is under development based on emulating CMIP5 GCMs.
- Standards: Aiming for full traceability and UK ISO standards.

## Acknowledgement and References

- Acknowledgements: Thanks to the modeling groups, PCMDI, and the WCRP WGCM for CMIP3 data; supported by the U.S. Department of Energy Office of Science.
- Key references (context and components):
  - Huntingford et al., 2010. IMOGEN: an intermediate complexity model to evaluate terrestrial impacts of a changing climate.
  - Huntingford & Cox, 2000. An analogue model to derive additional climate change scenarios from existing GCM simulations.
  - Meehl et al., 2007. The CMIP3 multimodel dataset.
  - Best et al., 2011; Clark et al., 2011. JULES model descriptions.
  - Zelazowski et al., 2016 (in prep). Climate pattern scaling set for an ensemble of 22 GCMs.