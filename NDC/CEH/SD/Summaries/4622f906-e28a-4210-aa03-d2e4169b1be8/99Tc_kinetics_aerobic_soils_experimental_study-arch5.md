# Supporting documentation

## Overview
- Study of technetium-99 (99Tc) in soils: measurements of soluble, adsorbed, and organically bound 99Tc after laboratory addition of 99TcO4 and long-term incubation (897 days) under controlled conditions.
- Objective: understand long-term bioavailability of 99Tc in aerobic soils and inform models under temperate conditions.
- Context: 20 soils from central England with varying land uses (arable, grassland, moorland/woodland).

## Dataset contents
- Soil sampling
  - Topsoils (0–15 cm) from multiple central England locations; composites formed from ~4 sub-samples per site.
  - For each soil: location, land use, coordinates, organic carbon (%), and pH.
- Experimental setup
  - Soils contaminated with 99TcO4 at ~108 µg 99Tc per kg dry soil.
  - Microcosms incubated in darkness at 10.0 ± 1.0°C for 897 days; gas exchange allowed, moisture maintained.
- Sequential extraction data
  - At sampling times, soil is subjected to three-step extraction to quantify 99Tc fractions:
    - Soluble 99Tc (0.01 M KNO3)
    - Specifically adsorbed 99Tc (0.16 M KH2PO4)
    - Organically bound 99Tc (10% tetramethylammonium hydroxide, 90°C, 14 h)
  - Results reported as µg 99Tc per kg dry weight (DW).
- Analytical method
  - ICP-MS (iCAP-Q) with collision-cell He, internal standards (Ge, Rh, Ir), and NIST SRM 4288B for calibration.
  - Sample introduction via autosampler with rapid uptake module; detailed instrument parameters provided.

## Data structure and metadata
- Data records per soil and per sampling time, with three extract fractions measured.
- Key identifiers: soil code (XX-X), incubation days, fraction type, concentration (µg 99Tc kg−1 DW).
- Table 1: soil properties (land use, latitude/longitude, organic C %, pH).
- Table 2: description of the sequential extraction steps and corresponding data fields.
- Notable missing data: cells denoted by '-' indicate data not available.

## Temporal aspects
- Longitudinal data across the incubation period; sampling occurred at multiple time points, enabling kinetics assessment of Tc transformation in each soil.

## Quality assurance and governance
- Use of standardized extraction protocol and validated ICP-MS methodology with certified reference material for calibration.
- Comprehensive metadata for provenance and reproducibility (locations, land use, soil properties, extraction scheme).
- Explicit indication of missing data to support transparent data quality assessment.

## Usage considerations and governance
- Suitable for modelling 99Tc mobility and bioavailability in aerobic soils of temperate regions.
- Soil properties (pH, organic carbon) and land use context are important covariates.
- Ensure consistent unit handling (µg 99Tc kg−1 DW) and account for missing data in analyses.
- Appropriate for deposition in data repositories with rich metadata to support discoverability and reuse.

## Limitations and caveats
- Limited to 20 soils from central England; laboratory incubation conditions may limit direct environmental extrapolation.
- Some data gaps exist (as indicated by '-' entries) that require careful handling in analyses.

## Citation and contact
- Authors: M. Izquierdo, E. Bailey, N. Crout, H. Sanders, S. Young, G. Shaw; School of Biosciences, University of Nottingham, UK.