# Methane fluxes from peatland plateaus and thawing peatland plateaus and from burnt and unburnt forests from permafrost in subarctic Canada

## Overview
- A dataset of methane flux measurements collected during the summers of 2013 and 2014.
- Compare methane fluxes across peatland plateaus, thawing peatland features, and burnt vs unburnt forests in subarctic Canada.
- Includes multiple sites, replicates, and standardized measurement protocols to enable cross-site comparisons.

## Scope and Context
- Temporal coverage: summers 2013 and 2014.
- Spatial coverage:
  - 2013 Teslin, Yukon: Teslin Peatland Plateau (TPP) with five replicates; thawing features (TWM, T5M, TMID) with three replicates each.
  - 2013 FireFox sites near Whitehorse, Yukon: FFU (unburnt) and FFB (burnt) with five replicates each.
  - 2014 White Truck, Northwest Territories: White Truck Plateau (WTP) with five replicates; thawing features WTM, WTS, WTW with 3 replicates each (WTM and WTS) and a single feature WTW with 3 replicates.
- Note: 2014 measurements did not include burnt vs unburnt forest comparisons.

## Methods and Measurements
- Flux measurement approach:
  - Ground collars made of PVC (160 mm diameter for plateau/forest sites; 315 mm for thawing features).
  - Chambers (15–35 cm high) placed on collars; connected to a Detecto Pak-Infrared (DP-IR) methane analyser.
  - Methane concentration tracked over up to 4 hours; flux estimated from the slope of concentration vs time.
  - Calibration and QA: DP-IR self-test; 100 ppm CH4 standard used; performance within 2 ppm of standard; intercept and R^2 recorded.
- Environmental context:
  - Air temperature recorded on site; soil temperature measured at 5 cm and 10 cm inside the collar after chamber removal.
  - Volumetric soil moisture at the surface (0–6 cm) using ML3 ThetaKit; thaw depth measured with a metal rod; water table depth measured relative to a site datum rod.
- Data recording specifics:
  - Flux rates expressed as mg CH4 day^-1 m^-2 and mg CH4-C day^-1 m^-2.
  - All measurements include units for each column; GPS coordinates provided in the dataset (note: flux and soil core data originate from different locations).

## Data Structure and Coding
- Codes for site features:
  - Peatland plateau: TPP (Teslin) and WTP (White Truck)
  - Thawing features: TWM, T5M, TMID; WTM, WTS, WTW
  - Forest sites: FFU (unburnt), FFB (burnt)
- Replicates:
  - Peatland plateau: TPP1–TPP5
  - Thawing features: three locations per feature with replicates (e.g., TWM1–TWM3, T5M1–T5M3, TMID1–TMID3)
  - Forest sites: FFU1–FFU5, FFB1–FFB5
- Note on data alignment:
  - Methane flux coding aligns with the soil profiles dataset; however, soil core and flux data come from different locations (GPS coordinates provided in the file).

## Data Quality and Documentation
- Calibration and QA:
  - Use of certified gas standard; measurement accuracy checked against standard (within 2 ppm).
  - Flux estimation supported by regression metrics (slope, intercept, R^2) for transparency and reproducibility.
- Documentation practices:
  - Comprehensive on-site metadata including site name, year, feature type, replicate identifiers, and measurement particulars.
  - Clear description of measurement protocol to enable reproducibility across studies.

## Data Governance and Stewardship Considerations
- Discoverability and interoperability:
  - Standardized site/feature codes and replicates facilitate dataset discovery and cross-study comparisons.
  - GPS coordinates enable geospatial querying and integration with related datasets (e.g., soil profiles), though flux and soil-core data may originate from different locations.
- Metadata needs for reuse:
  - Ensure metadata capture includes site, year, feature type, replicate ID, method details (collar/chamber dimensions, DP-IR model, calibration), QA/QC results (R^2, slope, intercept), environmental covariates (temperature, moisture, thaw depth, water table), and datum references for depths.
- Potential data governance considerations:
  - Align naming conventions with related datasets to support interoperability.
  - Maintain traceability between flux measurements and associated soil/vegetation context.
  - Plan for data updates or corrections and record provenance to preserve an audit trail.
- Relevance to Data Stewards’ aims:
  - The dataset exemplifies multi-site data collection with clear standards, facilitating data governance, usability by data users, and proper metadata for discovery and reuse.