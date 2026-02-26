# Rainfall catch, Throughfall catch, Stemflow catch, Dissolved Constituents Dataset (Wallingford) 23-May-1990 to 06-Apr-1992

## Overview
- Comprehensive dataset combining hydrological catch measurements with dissolved chemical constituents from Wallingford, spanning 23-May-1990 to 06-Apr-1992.
- Aimed at enabling analysis and creation of self-service data products (dashboards, pivot tables, time-series exploration) for end users.
- Includes metadata and QA considerations to support data reliability and cross-variable analyses.

## Data types and coverage
- Hydrology measurements
  - Rainfall catch (units: ml s), Throughfall catch (ml), Stemflow catch (ml)
  - Sample methods include Gravimetric (catch) and Volumetric (stemflow)
  - Field and lab contexts noted (Field lab vs Wallingford lab)
- Dissolved constituents (representative subset)
  - Major/trace elements and ions (e.g., Al, B, Ba, Ca, Cl, Cu, Fe, Mn, Na, Sr, Zn, K, Mg, Ni, etc.)
  - Units vary (mg/L, µg/L, g/L); includes lower quantification limits (LQDC) and associated metadata
- Nutrients and related species
  - NH4, NO3, SRP, Si, SO4, among others; details on lab, filtration, preservation, and analytic method
- pH measurements
  - pH data with measurement context (meters/electrodes)
- Phosphorus metrics
  - SRP (soluble reactive phosphorus) with preservation and analytic method details

## Analytical methods and lab details
- Analytical techniques
  - ICP-OES for metals (e.g., Al, B, Ba, Fe, Mn, Cu, Ca, Mg, Zn, Na, K, Sr, etc.)
  - IC for dissolved bromide and related ions
  - Autoanalyzer (Technicon Autoanalyzer II) for Cl, NO3, NH4, F, and others
  - Radiometer pH meter for pH measurements
- Filtration and preservation
  - Filtration commonly via 47 mm GF/C or 0.45 µm membranes; field filtration noted for most dissolved constituents
  - Preservation typically involves acidification to 1% HNO3 for metals; some samples stored dark at 4°C
- Laboratories
  - Wallingford laboratory as primary lab; field lab details documented

## Metadata and data quality
- Start/End dates and LAB/METHOD metadata captured for many analytes; however, numerous entries show placeholders indicating missing data
- Units and detection limits
  - Varied units across analytes; need standardization for cross-analyte comparisons
  - LQDC values provided for several constituents
- Data completeness and QA
  - Significant data gaps suggested by placeholders; plan for QA and imputation during data preparation
  - ICP-OES accuracy assessment described using materials from Aquacheck LGC Interlaboratory Proficiency Testing Scheme

## How to use and build outputs
- Potential data products
  - Time-series dashboards by catch type (rainfall, throughfall, stemflow) and by analyte
  - Pivot tables linking hydrological inputs with dissolved constituents to explore relationships (e.g., runoff chemistry vs rainfall input)
  - Self-service exploration allowing filtering by date, catch type, and analyte
- Analytical approaches
  - Compare concentrations across hydrological pathways to understand leaching and mobilization
  - Examine seasonal/temporal trends within 1990–1992 window
  - Validate data quality by cross-referencing metal concentrations with filtration/preservation metadata

## Key data attributes to note
- Catch data: Rainfall catch, Throughfall catch, Stemflow catch with units and collection methods
- Analyte metadata: Units, LQDC, START/END dates, LAB, FILTRATION, PRESERVATION, METHOD
- Common analysis methods: ICP-OES, IC, Autoanalyzer, radiometer pH
- Filtration and preservation specifics: Filter type, field vs lab filtration, storage conditions, preservation reagents
- QA context: ICP accuracy validated via external proficiency testing; many entries with missing or placeholder metadata requiring careful QA during data preparation

## SRP-specific notes
- Preservation: SRP samples stored in the dark at 4°C
- Method: Automated colorimetry for SRP measurements
- Data completeness: Many SRP-related fields appear as placeholders, indicating potential gaps in metadata
- Quality assurance: ICP-OES element determinations (for other elements) have documented accuracy checks against proficiency testing materials, informing overall dataset reliability for multi-analyte analyses