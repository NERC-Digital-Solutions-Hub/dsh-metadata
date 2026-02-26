# Project Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- Investigates labile, recalcitrant, and refractory organic matter in UK saltmarsh soils.
- Dataset covers 1211 down-core soil samples collected across UK saltmarsh sites from 2018 to 2021.
- Includes a measure of organic matter reactivity via the Carbon Reactivity Index (CRI).

## Data Resource Details
- File: C_SIDE_organic_matter_pools_and_reactivity.csv
- Purpose: Quantification of three OM pools (labile, recalcitrant, refractory) and CRI.
- Location: United Kingdom; sites distributed around the UK coastline to represent saltmarsh diversity (WGS84 coordinates provided).
- Variables/Parameters: Latitude, Longitude, Core depth (cm), Depth interval mid-point (cm), Labile/Recalcitrant/Refractory/Total OM (%wt), CRI.
- File format: CSV.

## Methods and Data Processing
- Observation/ measurement approach: Thermogravimetric analysis (TGA) on freeze-dried, milled samples (~20 mg).
- Instrument and conditions: Mettler Toledo TGA2, 40–1000°C, 10°C/min under N2; thermograms adjusted to a common scale and clipped to 200–650°C; data normalized to mass loss for comparability.
- OM fraction definitions (thermal ranges): Labile (200–400°C), Recalcitrant/Refractory (400–650°C) with updated ranges (Labile 200–400°C; Recalcitrant+Refractory 400–650°C).
- CRI calculation: CRI = %OM_R / %OM_total; interprets as a continuum from fully biodegradable (CRI ~ 0) to non-biodegradable (CRI ~ 1).
- Calibration: Thermogravimetric analyses calibrated with standard substances.
- Quality control: Lab equipment calibrated per University of St Andrews practices.

## Variables and Data Dictionary
- Core Identification (Core_ID)
- Saltmarsh name
- Latitude (decimal degrees, WGS84)
- Longitude (decimal degrees, WGS84)
- Depth interval of sub-sample (cm)
- Depth interval mid-point (cm)
- Labile organic matter (%wt)
- Recalcitrant organic matter (%wt)
- Refractory organic matter (%wt)
- Total organic matter (%wt)
- CRI (carbon reactivity index)

## Data Quality and Documentation
- Data checked through standard laboratory QA/QC procedures; calibration performed for all equipment.
- Data dictionary provided with explicit formats for each field.
- References for methods and interpretation: Kristensen (1990) on STG-based OM characterization; Smeaton & Austin (2022) on management of sedimentary OM.

## Data Governance, Availability, and Stewardship
- Data Resource ID highlights dataset as a defined resource; dataset details and citations included for reproducibility.
- Emphasis on appropriate governance: metadata, standardization across sites, and clear documentation of methods and formats.
- Planned data use considerations include dataset usability for other researchers and potential updates, with attention to sharing limitations and interoperability.

## Key Challenges Addressed (relevant to Data Stewards)
- Standardization across multiple sites and years to enable comparability.
- Handling and documenting large, multi-component datasets with clear metadata.
- Managing data formats and ensuring robust data description (CSV + data dictionary).
- Providing transparent quality control and calibration procedures to support reuse.

## References
- Kristensen, E. (1990). Characterization of biogenic organic matter by stepwise thermogravimetry (STG). Biogeochemistry.
- Smeaton, C. & Austin, W.E.N. (2022). Quality not quantity: Prioritizing the management of sedimentary organic matter across continental shelf seas. Geophysical Research Letters.