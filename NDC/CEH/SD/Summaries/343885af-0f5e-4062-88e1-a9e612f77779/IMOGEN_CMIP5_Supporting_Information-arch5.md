# This dataset represents the updated parameters and monthly climatologies used in the Integrated Model Of Global Effects of climatic aNomalies (IMOGEN) impacts modelling system (Huntingford et al., 2010)

## Purpose and context
- Provides updated IMOGEN parameters and monthly climatologies for IMOGEN’s pattern-scaling impacts modelling system.
- Used to test new land surface parameterisations before integration into a full General Circulation Model (GCM) and to project future emission scenarios beyond those simulated by GCMs.
- IMOGEN relies on pattern-scaling to relate local monthly climatic changes to global warming, employing an Energy Balance Model (EBM) and taking oceanic delays into account.
- Updated dataset is based on CMIP5 (34 GCMs) versus the original CMIP3 (22 GCMs).

## Data model and parameters
- Five EBM calibration parameters per GCM:
  - λ_land: climate sensitivity over land (W m^-2 K^-1)
  - λ_ocean: climate sensitivity over ocean (W m^-2 K^-1)
  - ν: constant ratio of mean land and ocean surface warming
  - κ: ocean effective thermal diffusivity (W m^-1 K^-1)
  - f: ocean fraction (dimensionless)
- The 34 GCMs from CMIP5 are enumerated with these parameter values (Table 1 shows centre, model, and the five parameters).

## Data contents
- For each GCM, calibrated EBM parameters are provided.
- The dataset forms the basis for the local monthly climatologies used in IMOGEN and for pattern-scaling analyses.

## Data structure and access
- Directory structure: per GCM, there is a directory named CEN_<Centre>_MOD_<Model> (34 directories in total).
- Within each directory: monthly ASCII files for each month, named jan through dec.
- Grid: all GCMs re-mapped onto a common HadCM3 grid (2.5° x 3.75°; 1631 land points).
- Each monthly file contains:
  - 1 header line
  - 1631 data lines with 13 columns:
    1) Longitude
    2) Latitude
    3) Temperature change per degree global warming (K per K)
    4) Relative humidity change per degree warming (% per K)
    5) Wind change per degree warming (m s^-1 per K)
    6) Unused
    7) Longwave change per degree warming (W m^-2 per K)
    8) Shortwave change per degree warming (W m^-2 per K)
    9) Unused
    10) Precipitation change per degree warming (mm day^-1 per K)
    11) Unused
    12) Pressure change per degree warming (hPa per K)
    13) Unused

## Metadata, provenance, and standards
- The calibration against CMIP5 models is accompanied by full numerical code documentation and traceability on demand.
- Uses open-access software for quality control; aligned with ISO standards for numerical model building.
- IMOGEN is routinely coupled to the JULES land surface model.

## Quality control and reproducibility
- Documented QA/QC procedures with traceable workflows and scripts.
- Clear provenance: links to original CMIP datasets and related publications; reproducible data transformations and grid remapping.

## Reuse, interoperability, and updates
- Data are designed to be discoverable, reusable, and integrable with other climate model outputs (e.g., JULES coupling).
- The dataset represents an updated parameter set and monthly climatologies, enabling updated impact assessments and scenario projections beyond those simulated by constituent GCMs.
- Availability is tied to CMIP5-era data lineage, with proper citations and acknowledgments.

## Governance, acknowledgments, and references
- Acknowledges modeling groups, PCMDI, and WGCM for CMIP5/CMIP3 data contributions; U.S. Department of Energy support.
- Foundational references include Huntingford et al. (2010), Huntingford & Cox (2000), Best et al. (2011), Clark et al. (2011), and related CMIP publications.
- This dataset is contextualized by studies on natural methane and permafrost feedbacks affecting warming targets (e.g., Comyn-Platt et al., 2018).