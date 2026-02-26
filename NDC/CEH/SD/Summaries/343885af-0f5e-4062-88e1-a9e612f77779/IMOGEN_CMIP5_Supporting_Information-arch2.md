# IMOGEN parameters and monthly climatologies for the IMOGEN impacts modelling system

- Purpose: Documents updated parameters and monthly climatologies used in the IMOGEN impacts modelling system, which emulates GCM responses via pattern-scaling for land surfaces and informs projections for future emission scenarios.
- Use cases: Tests new land surface parameterisations before full GCM implementation; generates projections for climate targets; supports coupling with the JULES land surface model.

## Data Description

- Model framework: IMOGEN uses an Energy Balance Model (EBM) with five calibrated parameters per GCM.
- Five EBM parameters per GCM:
  - λ land (land climate sensitivity, W m^-2 K^-1)
  - λ ocean (ocean climate sensitivity, W m^-2 K^-1)
  - ν (constant ratio of mean land to ocean SST warming)
  - κ (ocean effective thermal diffusivity, W m^-1 K^-1)
  - f (ocean fraction, unitless)
- GCM coverage: Updated dataset based on CMIP5, includes 34 GCMs (expanded from CMIP3’s 22).
- Example data: Table 1 lists parameter values by centre/model (34 entries total).
- Pattern-scaling basis: Local monthly changes in meteorology scale linearly with global land temperature increase; uses an Energy Balance Model to relate radiative forcing to land warming with oceanic delays.
- Grid and data points:
  - Re-mapped to a common HadCM3 grid: 2.5° x 3.75° (1631 land points).
  - For each GCM: monthly ASCII files jan…dec.
  - Each file contains 1 header line plus 1631 data lines with 13 columns (longitude, latitude, various climate change columns per degree of warming, and unused columns).
  - Columns cover changes in temperature, relative humidity, wind, longwave/shortwave radiation, precipitation, and pressure per degree of warming; some columns are unused (0.0).
- Coupling: IMOGEN is routinely coupled to the JULES land surface model.

## Data Structure and Access

- Directory structure: For each GCM, directory named CEN_<Centre>_MOD_<Model> contains 34 subdirectories, each with monthly files.
- File organization: Monthly files named jan, feb, …, dec; regridded to a common grid for consistency across models.
- Accessibility: Local and monthly climate change patterns are available for download, enabling reuse in analyses and intercomparisons.

## Quality Control and Documentation

- Calibration and validation: Calibration against CMIP5 models with full numerical code documentation and traceability on demand.
- Standards: Meets ISO-like requirements for numerical model building; uses open-access software for reproducibility.
- Documentation and references: Comprehensive references to IMOGEN, JULES, CMIP5/CMIP3, and pattern-scaling methodology.

## Acknowledgements and References

- Acknowledges CMIP groups (CMIP3/CMIP5), PCMDI, WGCM, and supporting institutions (U.S. DoE).
- Key references include works on IMOGEN, pattern-scaling, JULES coupling, and CMIP design and analyses.

## Implications for Environmental Analysts

- Standardised outputs: Consistent, comparable IMOGEN parameters across 34 CMIP5 GCMs support robust environmental health and policy performance analyses.
- Data quality and reproducibility: Fully documented calibration and ISO-aligned quality control enhance trust and traceability.
- Data integration: Patterns are downloadable and can be combined with other datasets to enhance value beyond single-use analyses.
- Practical use: Facilitates scenario testing and understanding of land-surface responses to warming using a streamlined, reproducible framework with JULES coupling.