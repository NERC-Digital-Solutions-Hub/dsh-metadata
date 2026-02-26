# Rio_forests_metadata_corrected_May2019.csv and DryFlorBrazil_tree_census_data_corrected_May2019.csv

## Overview
- Standardized, long-term environmental monitoring data following RAINFOR protocols.
- Two primary datasets described:
  - Rio_forests_metadata_corrected_May2019.csv: per-plot metadata for rainforest plots.
  - DryFlorBrazil_tree_census_data_corrected_May2019.csv: stem-level census data for plots in Brazil.
- Data are prepared for reproducibility, quality assurance, and integration with other datasets via ForestPlots.net.

## Experimental design and data collection
- Plots installed following established RAINFOR protocols; field methods and manuals available (RAINFOR_field_manual_EN.pdf and related languages).
- Measurements structured around 1 ha plots with subplots; diameters tracked across censuses with a Point of Measurement (POM) system.
- POM changes documented and managed (DPOMtMinus1, D2, D3, D4 fields handle diameter updates when POM changes occur).
- Data capture supports time series: census numbers, census dates, last census date, number of censuses, and plot status.

## Datasets and key fields
- Rio_forests_metadata_corrected_May2019.csv
  - Plot-level identifiers: PlotID, PlotCode, PlotName, PlotDatabaseManager, PlotAreaLocation, GroundArea, FragmentSize, ForestElevation, Altitude, LatitudeDecimal, LongitudeDecimal, etc.
  - Location and contextual data: Country, Continent, BiogeographicalRegion, EcoRegion, AllometricRegion, etc.
  - Plot characteristics: DateEstablished, LastCensusDate, No.ofCensuses, FragmentSize, NearestAnthropogenicEdge, ForestMoisture, ForestStatus, AreaType, AveragePlotSlope, etc.
  - Data governance and quality cues: Status, VerifiedBy, PlotView contacts, and metadata fields describing data provenance.
  - References to classifications and schemes: Holdridge, Chave et al. (2005) wood-density, WWF EcoRegion, AllometricRegion, etc.
- DryFlorBrazil_tree_census_data_corrected_May2019.csv
  - Plot and view identifiers: PlotID, PlotCode, PlotViewID, PlotViewName, PlotName, PI.
  - Tree-level data: TreeID, TagNumber, Family, Genus, Species, OriginalIdentification, AcceptedFullSpeciesName, CensusNo, CensusDate, VoucherCode.
  - Diameter and measurement history: D0, D1, DPOMtMinus1, D2, D3, D4, POM; related measurement fields including height and measurement techniques (F1–F5 flags, LI, CI).
  - Taxonomy resolution: FamilyID, GenusID, SpeciesID, AcceptedFamilyName, etc., with cross-references to ForestPlots.net identifiers.
  - Data quality and processing notes: Flags for alive/dead status, measurement technique, post-field data management, and references to RAINFO R_data_codes_EN.pdf for coding.
  - Special notes: D4 is not stored in the database and is computed on demand during plot data dumps; Plot views allow customized subsetting (e.g., by DBH, census start/end, taxonomic level).

## Units and interpretation
- Units used across datasets: Ha (hectares), m (metres), mm (millimetres); geographic coordinates in decimal degrees.
- Spatial and environmental descriptors follow standard schemes (Chave 2005, Holdridge classification, WWF EcoRegions, etc.).
- Data use relies on consistent coding from RAINFO R_data_codes_EN.pdf and associated manuals.

## Data provenance, quality, and accessibility
- Data generated under standardized protocols with explicit metadata to support reproducibility.
- ForestPlots.net serves as the primary portal for data access, plot views, and metadata; examples include Main Plot View vs Preferred Plot View.
- Documentation and references provided:
  - RAINFOR manuals and field protocols
  - RAINFO R_data_codes_EN.pdf and CrownLianaProtocols_EN.pdf
  - Relevant DOIs for background schemes (Chave 2005; Holdridge; Feldpausch et al. 2012)
- Data corrected May 2019 (versioned metadata and census data).

## How this supports environmental monitoring and policy evaluation
- Enables consistent, time-series assessment of forest structure, composition, and edge effects (e.g., NearestAnthropogenicEdge, FragmentSize).
- Facilitates cross-site comparisons and integration with other datasets for regional to global environmental health analyses.
- Clear data lineage and standardized variables support transparent reporting and policy performance scrutiny.

## Practical guidance for analysts
- Use ForestPlots.net to access Main vs Preferred Plot Views and to download required data slices.
- Be mindful of POM changes when interpreting diameter histories; DBH adjustments (D0–D4) are computed with explicit flags and methodologies.
- Leverage taxonomy fields with accepted names and voucher information to ensure consistent species identification.
- Refer to the provided manuals and data codes for interpretation of flags (F1–F5, LI, CI) and measurement techniques.
- When combining with other datasets, align on standardized units, geographic classifications, and plot identifiers (PlotID, PlotCode).