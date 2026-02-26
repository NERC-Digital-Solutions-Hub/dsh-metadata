# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

## Overview
- Multidataset collection of soil hydraulic properties from the Climoor field site, Clocaenog Forest, North Wales.
- Captures 2010–2012 data across five data sets related to bulk density, unsaturated hydraulic conductivity, and soil water release curves.
- Quality-checked data with missing values annotated (no infilling) and preparation for analysis of drought and warming treatments.

## Datasets and Content
- 1) Bulk_density.csv
  - Dry bulk density for 0–5 cm depth; includes saturated water content measurements.
- 2) Minidisk_K.csv
  - Field-measured unsaturated hydraulic conductivity at tensions of -2 cm and -6 cm using a minidisk infiltrometer; includes plot and tension information.
- 3) Hyprop_K.csv
  - Laboratory-measured unsaturated hydraulic conductivity using HYPROP across multiple plots; detailed by suction levels and plot type.
- 4) Hyprop_SWRC.csv
  - HYPROP-derived soil water release curves (wet soil) with interpolated data points across suction values; includes VWC (volumetric water content) per plot.
- 5) WP4_SWRC.csv
  - WP4 potentiometer-based soil water release curves (dry soil) with corresponding temperature and moisture measurements.

## Data Provenance and Site Context
- Site: Clocaenog climate change field site, upland Atlantic heathland; automated drought and warming treatments across three replicate plots plus controls.
- Treatments:
  - Drought: retractable roofs reduce rainfall by ~20% during May–September; curtains and rain exclusion are automatically controlled.
  - Warming: retractable aluminum curtains reduce nighttime heat loss; automated to minimize rainfall exclusion (average ~14% rainfall reduction).
- Sampling and measurements:
  - HYPROP cores (250 cm3, 0–5 cm depth) collected from plot edges away from prevailing wind/rain; samples processed in lab for HYPROP SWRCs.
  - Minidisk and WP4 measurements collected in field or lab as specified; multiple instruments used (HYPROP, minidisk, WP4).
- Documentation and references accompany data (publications and dataCenter records).

## Data Processing and Quality Assurance
- QA/QC: data visually inspected; incorrect/missing values removed; no data infilling performed; NA values added where data were absent.
- Processing steps:
  - HYPROP data processed with HYPROP-FIT software; spline interpolation in R to align raw data to a common suction scale.
  - Minidisk measurements converted to hydraulic conductivity using standard procedures.
  - Bulk density calculated from oven-dried mass (105°C, 16 hours) and known sample volume.
- Supporting manuals and methods files included (HYPROP, HYPROP-FIT, minidisk, WP4) to document procedures.

## Data Structure and Documentation
- File-level structure:
  - (1) Bulk_density.csv: columns for plot, treatment, BD (g/cm3), SatVWC, FofS, EstPD, etc.
  - (2) Minidisk_K.csv: plot, treatment, h0 (cm), mean_k (cm/s and cm/day), etc.
  - (3) Hyprop_K.csv: suction and corresponding unsaturated conductivity by plot and treatment.
  - (4) Hyprop_SWRC.csv: interpolation number, suction (kPa), VWC values across plots.
  - (5) WP4_SWRC.csv: temperature, soil moisture (%), matric potential (MPa), pressure head (cm of water) across samples.
- Notes:
  - Interpolation_number in Hyprop_SWRC indicates data points interpolated (1–501 range).
  - Column headings include units and comments for clarity and interoperability.
- Metadata and supporting materials:
  - Manuals and data processing references included (HYPROP, HYPROP-FIT, WP4 operators manual, minidisk manual).
  - Key publications and DOIs cited for context and reuse (e.g., Domínguez et al. 2015; Robinson et al. 2016).

## Documentation, Access, and Reuse
- Key publications and data center records cited for broader context and reuse:
  - Domínguez et al. 2015; Robinson et al. 2016; Reinsch et al. 2016a, 2016b; other related literature.
- Data are organized for reuse in soil hydraulic property analyses, with explicit linkages to the experimental site and climate treatment design.
- Clear provenance and processing trail are provided to support reproducibility and interoperability with other Clocaenog datasets.

## Roles and Responsibilities
- D.A. Robinson: HYPROP measurements and soil water release curves.
- I. Lebron: HYPROP measurements, SWRCs, and bulk density.
- A.R. Smith: WP4 measurements.
- M.R. Marshall: Minidisk measurements.
- B.A. Emmett: Principal investigator, Clocaenog site.
- S. Reinsch: Field site science management.
- D.M. Cooper: Statistical interpolation in R.
- M. Brooks: Field site and roof maintenance.

## Limitations and Considerations for Data Stewards
- Multiple measurement methods/instruments require careful cross-calibration and metadata harmonization to ensure comparability.
- Data were collected under specific experimental treatments (drought and warming), which may influence interpretation and require contextual metadata.
- Interpolation to common suction scales (HYPROP) introduces modeled estimates; users should account for interpolation procedures and assumptions.
- Data not infilled; gaps are annotated as NA, which may affect downstream analyses and require handling in reproducible workflows.
- Documentation and manuals are provided to support methodological transparency and reproducibility.