# Experimental design/Sampling regime

- All plots were installed following standard RAINFOR protocols, with the accompanying manuals and field guides available in multiple languages (English, Portuguese, Spanish, Portugese). References and PDFs are provided for detailed procedures.

## Data collection and documentation

- The document describes the nature and units of recorded values and points readers to the tables below for interpretation.
- Detailed metadata and dataset structure are provided to support analysis, replication, and data reuse.

## Data files and structure

- Two primary CSV files are referenced, each with extensive metadata and field definitions:
  - Rio_forests_metadata_corrected_May2019.csv
  - DryFlorBrazil_tree_census_data_corrected_May2019.csv

### Rio_forests_metadata_corrected_May2019.csv (plot-level metadata)
- Key fields include:
  - Plot identifiers: PlotID, PlotCode, PlotName
  - Team and governance: PITeam
  - Location: Country, Continent, Cluster, BiogeographicalRegion, PlotAreaLocation, State/County/Province
  - Geography and area: Altitude, LatitudeDecimal, LongitudeDecimal, GroundArea, MinimumDimension, MaximumDimension, TotalPlotEdge
  - Ecological classifications: ForestMoisture, ForestElevation, ForestEdaphicType, ForestComposition, SubstrateGeology, EcoRegion, AllometricRegion
  - Plot status and history: ForestStatus, AreaType, AveragePlotSlope, PlotDatabaseManager, PlotNumber of censuses, LastCensusDate, Status, VerifiedBy
  - Data quality and accessibility: PlotContacts, PlotDatabaseManager, DateEstablished, No.ofCensuses, No.ofextraplotviews
- Units and definitions are specified (e.g., Ha for hectares, m for metres, mm for millimetres).

### DryFlorBrazil_tree_census_data_corrected_May2019.csv (tree-level census data)
- Key fields include:
  - Identifiers and plot context: Continent, Country, PlotID, PlotCode, PlotViewID, PlotName, PlotViewName, PI
  - Tree-level identifiers: TreeID, TagNumber, SubPlot (T1)
  - Taxonomy and identification: AllometricRegionID, Family, Genus, Species, OriginalIdentification, Authority, AcceptedFamilyName, AcceptedFullSpeciesName, FamilyAPGID, GenusID, SpeciesID
  - Census information: CensusNo, CensusDate, VoucherCode
  - Diameter measurements and measurement history: D0 (field diameter), D1 (best estimate at current POM), DPOMtMinus1 (previous POM), D2, D3, D4, POM (Point of Measurement), and derived values
  - POM change handling: D4 is an estimated value used when POM changes; specific algorithms automate changes when POM shifts
  - Data quality flags: F1–F5 (various Rainfor data codes for alive status, mode of death, measurement technique, and post-field data management)
  - Additional indices: LI (Liana Infestation index), CI (Canopy Illumination index)
  - Measurement technique and provenance: Flags F1–F5 and references to Rainfor guidelines and protocols

## Units and interpretation

- Recorded values use consistent units as indicated in the tables, including:
  - Area: hectares (Ha)
  - Distance/length: metres (m)
  - Diameter: millimetres (mm)
  - Other context-specific measurements and flags as defined by Rainfor data codes

## Data usage, provenance, and access

- Data are prepared for analysis, reporting, and publication, with explicit mappings to plot IDs, census dates, and standardized species nomenclature.
- The metadata and census data are intended to be traceable to original field measurements, with explicit links to documentation on data codes and measurement protocols.
- Access and reuse guidance are provided via ForestPlots.net, including links to manuals and data-dictionary resources for interpreting the codes and fields.

## Additional notes for analysts

- Many fields rely on standardized taxonomic and allometric references (e.g., APGIII nomenclature, Feldpausch et al. 2012 regional classifications).
- POM changes require careful interpretation of diameter history (D0–D4, DPOMtMinus1) to ensure accurate growth estimates.
- Data quality codes (F1–F5) and domain-specific indices (LI, CI) are documented in accompanying Rainfor PDFs and CrownLianaProtocols_EN.pdf.