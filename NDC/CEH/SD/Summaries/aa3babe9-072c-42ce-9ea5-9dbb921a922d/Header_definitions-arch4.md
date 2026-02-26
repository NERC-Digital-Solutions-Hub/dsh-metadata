# Experimental design/Sampling regime

- Plots installed following standard RAINFOR protocols; reference to RAINFOR manuals in multiple languages and a field manual included with the data.
- Information about data structure, units, and interpretation is provided in accompanying tables and CSV metadata.

## Datasets Included

- Rio_forests_metadata_corrected_May2019.csv
- DryFlorBrazil_tree_census_data_corrected_May2019.csv

## Key Variables and Metadata

- Rio_forests_metadata_corrected_May2019.csv includes:
  - Plot-level identifiers and geography: PlotID, PlotCode, PlotName, PI Team, Country, Continent, Cluster, BiogeographicalRegion, PlotAreaLocation, Altitude, LatitudeDecimal, LongitudeDecimal, GroundArea, FragmentSize, ForestElevation, ForestStatus, EcoRegion, AllometricRegion, DateEstablished, LastCensusDate, No.ofCensuses, PlotDatabaseManager, ForestPlotsContact, Status, VerifiedBy, and other descriptive fields.
  - Plot characteristics: Minimum/MaximumDimension, TotalPlotEdge, NearestAnthropogenicEdge, AreaType, AveragePlotSlope, etc.
  - Data quality and governance fields: PlotDatabaseManager, ForestPlotsContact, DateEstablished, LastCensusDate, No.ofCensuses, Status, VerifiedBy.
- DryFlorBrazil_tree_census_data_corrected_May2019.csv includes:
  - Plot and view identifiers: Continent, Country, PlotID, PlotCode, PlotViewID, PlotName, PlotViewName, PI.
  - Tree-level data: TreeID, TagNumber, SubPlot T1, AllometricRegionID, Family, Genus, Species, OriginalIdentification, Authority, AcceptedFullSpeciesName, Family/APG IDs, CensusNo, CensusDate, VoucherCode.
  - Diameter/measurement history: D0, D1, DPOMtMinus1, D2, D3, D4, POM; Height; measurement flags F1–F5, LI (Liana Infestation), CI (Canopy Illumination), and post-field data management codes.
  - POM-change handling: D values reflect diameters before/after POM changes with an automated adjustment algorithm; DBH4 is derived as part of ongoing data processing.
  - Data provenance and quality indicators: Flags and codes referenced to Rainfor data coding documents and crown/liana protocols.

## Metadata, Standards, and Provenance

- All data adhere to Rainfor protocols; detailed field and measurement methods are described in the Rainfor manuals (linked in the dataset documentation).
- Units are explicitly defined (e.g., Ha, m, mm) and the metadata includes comprehensive definitions for each field.
- Species and taxonomy follow APGIII standards; cross-references to taxonomic identifiers (FamilyID, GenusID, SpeciesID) are provided.
- Key references for standards and classifications: Chave et al. 2005; Holdridge system; APGIII; Feldpausch et al. 2012.
- Data quality and interpretation governed by Rainfor data codes and Crown Liana protocols (with downloadable code documents linked in the dataset).

## Data Quality, Processing, and Access

- Data are published as corrected May 2019 versions, with clear documentation of field methods and data processing steps (e.g., POM changes, diameter adjustments, and DBH4 estimation).
- Plot views enable selective inclusion of stems (e.g., by DBH, census period, family/genus, or other criteria); download options include Main Plot View and Preferred Plot View.
- Data governance details include PlotDatabaseManager and ForestPlotsContact for inquiries and use in analysis/publications.
- Extensive metadata supports data discovery, reuse, and verification across sites and over time.

## Accessibility and Documentation

- Additional manuals and documentation are available via:
  - Rainfor manuals: http://www.rainfor.org/en/manuals
  - Specific field and data-code documentation (as referenced in the dataset notes)
- Clear identifiers (PlotID, PlotCode, PlotViewID) and standardized metadata support data discoverability and cross-dataset integration.

## Implications for Data Strategy and Governance

- Provides a well-structured, richly described data asset that supports end-to-end data governance: discovery, provenance, quality, and updates.
- Supports cross-site collaboration through ForestPlots.net identifiers and documented data standards.
- Enables analyses of forest structure, species composition, growth, mortality, and dynamics over time using both plot-level and tree-level data.
- Highlights the importance of maintaining updated metadata, transparent data codes, and access to standardized manuals to ensure consistent interpretation and reuse across teams and partners.