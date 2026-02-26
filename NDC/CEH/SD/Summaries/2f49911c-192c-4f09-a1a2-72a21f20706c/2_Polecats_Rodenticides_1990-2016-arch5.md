# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

## Overview
- Supplement to the 2018 Environmental Pollution paper on long-term increase in secondary exposure to anticoagulant rodenticides in British polecats.
- Provides column explanations and metadata for the PolecatRodenticidesFINAL1990-2016March2019EIDC.csv dataset.
- Encodes data on rodenticides detected in polecat liver tissue across multiple surveys from 1990 to 2016.
- Includes provenance from two key studies (Shore et al. 2003; Sainsbury et al. 2018) and notes on data processing and spatial assignment.

## Dataset structure and content
- Core fields (with examples of meaning):
  - record: unique dataset-wide identifier for each animal (Vincent Wildlife Trust ID).
  - data: origin of chemical analyses (NEW = Sainsbury et al. 2016; OLD = Shore et al. 2003).
  - year: carcass collection year (1990–2016).
  - time: years since first collected animal (time measure).
  - survey: which rodenticide analysis survey (1990–1995; 1995–1998; 2013–2016).
  - season / halfYear: season of collection and half-year period (FIRST: Dec–May; SECOND: Jun–Nov).
  - x / y: OSGB36 geographic coordinates (metres).
  - region: north, south, east, west partition of Britain.
  - expansio n: inside or outside the 1990s range.
  - sex: male or female (if known).
  - landClass: predominant land use at carcass site (derived from CEH Land Cover map; arable vs pastoral dominating 1 km buffer).
  - hBrom / hDifm / hBrod: concentrations of bromadiolone, difenacoum, brodifacoum (µg/g); LOD applied as in Shore 2003 to Sainsbury 2018 data.
  - hBBrom / hBDifm / hBBrod: detection indicators (0 = none detected; 1 = detected; LOD-based).
  - hBRods: number of rodenticides detected in liver.
  - hCRods: count of detected rodenticide compounds (1/2/3).
  - hConcT: total concentration of rodenticide compounds (µg/g; uses LODs from Shore 2003).
- Data were processed to harmonize across studies and time periods; units and NA semantics clarified.

## Data processing, quality, and standards
- Spatial processing: carcass locations overlaid onto CEH Land Cover map (2007); 1 km buffers around each point; majority land class determined by comparing arable vs pastoral classification.
- Coordinate system: OSGB36 coordinates provided for mapping.
- Analytical metadata: LODs for each chemical are those from Shore et al. 2003 and applied to the 2018 dataset.
- Data provenance: original analyses from Shore et al. (2003) and Sainsbury et al. (2018); the 2018 dataset used for the supplement.
- Documentation: explicit notes explain when data were missing (NA) and how new entries relate to the 1990s baseline.

## Metadata, provenance, and references
- Notes accompany fields to clarify data origins, units, and interpretation.
- References:
  - Shore RF, et al. (2003). Spatial and temporal analysis of second-generation anticoagulant rodenticide residues in polecats in Britain, 1992–1999. Environmental Pollution.
  - Sainsbury KA, et al. (2018). Long-term increase in secondary exposure to anticoagulant rodenticides in European polecats in Great Britain. Environmental Pollution.
- Software/processing tools: Quantum GIS (version 2.12.3) used for land class mapping.

## Access, reuse, and governance implications for Data Stewards
- The dataset is a structured, well-documented supplement enabling discovery and reuse for studies on anticoagulant exposure in wildlife, with clear provenance and harmonized fields.
- Key governance considerations:
  - Ensure ongoing data provenance tracing (original studies, LOD assumptions, and harmonization rules).
  - Maintain metadata clarity around units, missing data (NA), and the meaning of each indicator (detection vs. concentration).
  - Preserve spatial metadata (OSGB36 coordinates, land-cover context) while acknowledging any privacy or sensitivity constraints related to location data.
  - Document updates or expansions to the dataset (e.g., inclusion of new survey periods or revised LODs) to maintain data interoperability with prior versions.

## Limitations and cautions
- LOD-based imputation for several chemical measurements; interpretation should account for detection limits.
- Potential biases due to uneven sampling across regions, surveys, and time periods.
- Missing data indicated by NA; users should consider how gaps affect longitudinal analyses.
- Land-class assignment relies on a 1 km buffer around coordinates and a specific land-cover map (2007), which may affect classification for some sites.