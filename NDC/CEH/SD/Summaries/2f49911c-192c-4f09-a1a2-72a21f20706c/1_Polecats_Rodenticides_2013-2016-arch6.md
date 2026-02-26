# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

## Overview
- Dataset supplement to the 2018 Environmental Pollution paper, providing detailed chemical and contextual data for European polecats in Great Britain.
- Covers secondary exposure to second-generation anticoagulant rodenticides (SGARs) via liver residues, with additional carcass metadata and isotopic measurements from whiskers.
- Temporal scope: carcass collection year range 2013–2016; links to the main study on long-term exposure in GB polecats.
- Primary resource for data reuse: chemical concentrations, rodenticide detection, sample metadata, and geographic context for analysis and visualization.

## Dataset contents and structure
- Primary file described: PolecatRodenticidesFINAL2013-2016March2019EIDC.csv, with a comprehensive column header explanation.
- Data types include:
  - Batch and sample identifiers: Batch, the chemical analysis batch; # as the sample number within a batch; record as unique animal identifier.
  - Temporal data: month, year, season, halfYear (FIRST = Dec–May; SECOND = Jun–Nov).
  - Spatial data: x and y coordinates (OSGB36); region (North, South, East, West); 1 km-land-cover context derived from CEH Land Cover map (2007) with predominant land class (arable vs pastoral).
  - Biological metadata: sex, age category, alive status, kidney fat score.
  - Chemical residues and detection: concentrations for bromadiolone (brom), difenacoum (difm), flocoumafen (floc), brodifacoum (brod), difethialone (dife); detection flags for each compound (bBrom, bDifm, bFloc, bBrod, bDife); total number of rodenticides detected in liver residues (cRods); total concentration sum (sumALL).
  - Isotopic measurements (liver residues): meanN (δ15N), sdN; meanC (δ13C), sdC; dN15Max (max δ15N across whisker segments).
  - Additional data: region and landClass notes, resistance area indicator (resistance) indicating known SGAR resistance regions.
- Data quality notes:
  - NA indicates no data for an individual.
  - Certain fields use coded schemes (e.g., 1/2/3 for categories) with explicit explanations.
  - Some fields have non-detects indicated by zero concentrations or binary flags (e.g., 0 = none detected).

## Variables and units (highlights)
- Location and environment:
  - x, y: coordinates in metres (OSGB36); region; landClass (based on 1 km buffer overlay with CEH Land Cover map 2007).
  - Season, halfYear, month, year (temporal context).
  - region categorized as North, South, East, West.
- Biological/demographic:
  - sex (gender), age (age category), alive (status/age data), fat (kidney fat score, 0–4 scale).
- Chemical exposure:
  - brom, difm, floc, brod, dife: concentrations in liver tissue (µg/g); detection flags bBrom, bDifm, bFloc, bBrod, bDife (1 = detected, 0 = not detected).
  - bRods: whether one or more SGARs detected (1 = yes).
  - sumALL: total concentration of detected rodenticides (µg/g); cRods: number of detected compounds (1–4).
- Isotopes (tissue-specific):
  - meanN (δ15N), sdN; meanC (δ13C), sdC; dN15Max (max δ15N value across whisker segments).
- Data provenance and notes:
  - Batch, record, and sample identifiers; notes on data availability and methodology as referenced in the dataset notes and linked literature.

## Data collection and processing methods
- Carcass collection locations mapped to the CEH Land Cover map (2007); 1 km buffers used to assign predominant land class (arable vs pastoral) for each location.
- Geographic context extracted to enable regional and land-use analyses (North/South/East/West; arable vs pastoral).
- Chemical analysis captured concentrations and detection of five SGARs in liver residues; ancillary endpoints include total rodenticide burden and multi-residue counts.
- Isotopic analyses conducted on whisker segments to derive mean and variability for δ15N and δ13C.

## Geographic and environmental context
- Scope: Great Britain (polecats in GB).
- Regions defined as North, South, East, West to enable spatial analyses.
- Land-use context developed via CEH Land Cover map (2007), with a 1 km buffering approach to determine predominant land class at collection sites.

## Data quality, interpretation, and caveats
- NA used to denote missing data; some fields use coded categories that should be interpreted per the column explanations.
- Measurements reflect both presence/absence (binary detection) and concentration (continuous) data for five SGARs, with total burden available.
- Isotopic data provide supplementary ecological context but may not be available for all individuals.
- The dataset is a supplement to a peer-reviewed study; where applicable, methodology and interpretation should align with the cited 2018 Environmental Pollution paper and the 1998 McDonald et al. reference for fat scoring.

## How this dataset supports data use and analysis (Data Support archetype)
- Enables self-serve analyses of SGAR exposure across GB polecats, by region and land-use context.
- Supports data integration with geographic information systems (GIS) to map exposure patterns and identify hotspots.
- Facilitates multi-criteria analyses combining chemical exposure, carcass metadata, and environmental context (region, land class, resistance area).
- Allows correlation analyses between SGAR burden and isotopic markers (δ15N/δ13C) for ecological or dietary inferences.
- Useful for quality assurance and product development (dashboards or reports) that summarize exposure prevalence, per-compound incidence, and overall rodenticide load across time and space.

## Summary of key value for use
- A richly labeled data dictionary for an SGAR exposure study in GB polecats, with comprehensive metadata, concentration and detection data for five rodenticides, carcass metadata, and environmental context to support robust, spatially-aware analyses and data product development.