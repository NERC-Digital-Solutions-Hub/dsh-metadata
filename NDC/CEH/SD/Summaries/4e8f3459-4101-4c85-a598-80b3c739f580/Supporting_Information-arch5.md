# Introduction

- Describes the parameters used in the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system, used to test land surface parameterisations and to project future emissions scenarios beyond existing GCM runs.
- IMOGEN employs pattern-scaling to emulate Global Circulation Models (GCMs), linking local monthly meteorology changes to global warming over land via an Energy Balance Model (EBM).
- A detailed description of the dataset will be available in Zelazowski et al. (In Prep).

## Data Content

- Five EBM parameters fitted per GCM:
  - λl: climate sensitivity over land (W m^-2 K^-1)
  - λo: climate sensitivity over ocean (W m^-2 K^-1)
  - κ: ocean effective thermal diffusivity (W m^-1 K^-1)
  - ν: constant ratio of mean land and ocean SST warming (dimensionless)
  - f: ocean fraction (one minus land fraction, including Antarctica)
- Calibration against CMIP3 GCMs (22 models) with parameter values shown in Table 1.
- For each GCM, local monthly patterns (patterns of change per degree of global warming) are provided for download in ASCII format.
- Patterns are available on a common grid (2.5° x 3.75° HadCM3) and cover 1631 land points.
- Data include per-point fields for various climate responses (e.g., temperature, humidity, wind, longwave/shortwave radiation, precipitation, pressure) per degree of warming.

## Data Structure and Access

- Directory structure: pattRelPR_d2_<GCM> for each of the 22 GCMs.
- Within each GCM directory: monthly ASCII files named jan through dec.
- Each file contains:
  - A header line followed by 1631 land-point records.
  - Data fields include longitude, latitude, and multiple climate-change response variables per degree of warming.
- The IMOGEN-EBM patterns are routinely coupled to the JULES land surface model; coupling examples are documented in related IMOGEN and JULES publications.
- Data are prepared for reuse and sharing via common formats; ongoing work aims to extend to CMIP5 with full traceability and UK ISO-aligned standards.

## Quality Control, Provenance, and Standards

- Patterns are part of a beta program to extend IMOGEN EBM and pattern parameterisation beyond the CMIP3 set; development is planned for CMIP5-based emulations.
- A focus on full traceability and alignment with UK ISO standards.
- Data provenance includes explicit linkage to CMIP3 multi-model datasets and collaborators (PCMDI, WGCM) and funding/administrative support from the U.S. Department of Energy.

## Acknowledgements and References

- Acknowledges modeling groups, PCMDI, and WGCM for CMIP3 data access; contributions supported by the U.S. Department of Energy.
- Key references include works describing IMOGEN, JULES, and CMIP3 multi-model dataset, as well as related pattern scaling literature and the forthcoming Zelazowski et al. (In Prep) study.