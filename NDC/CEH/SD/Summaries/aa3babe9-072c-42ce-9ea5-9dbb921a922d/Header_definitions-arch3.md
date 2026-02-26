# Rio_forests_metadata_corrected_May2019.csv

## Overview
- Provides standardized metadata for forest plots following the RAINFOR protocol.
- Defines identifiers, location, ecological attributes, and plot management details to ensure data are interpretable, comparable, and reusable for monitoring and evaluation.

## Experimental design and data collection
- Plots installed and surveyed using standard RAINFOR procedures; manuals available in English, Portuguese, Spanish.
- Data structures and fields are designed to support cross-site comparisons and longitudinal monitoring of forest plots.
- Metadata is complemented by data dictionaries and codes for data quality and measurement methods.

## Data structure and units
- Recorded values use defined units (e.g., hectares, metres, millimetres).
- Key identifiers and attributes are documented to enable traceability and interpretation of plots and their census data.
- Metadata table includes a wide range of fields to describe plot location, environmental context, and data management.

## Rio_forests_metadata_corrected_May2019.csv: Key fields and definitions
- PlotID: Unique forest plot identifier (ForestPlots.net)
- PlotCode: ForestPlots.net code for the plot (e.g., ABC-12)
- PlotName: Name of the plot
- PITeam: Names of the principal investigators and field leaders for the plot
- Country, Continent, BiogeographicalRegion: Geographic and biogeographic context
- Cluster, EcoRegion, AllometricRegion: Groupings and regions used for analyses
- PlotAreaLocation, State/County/Province, LocationSource: Spatial location details and data sources for coordinates
- Altitude, LatitudeDecimal, LongitudeDecimal: Elevation and precise geographic coordinates
- GroundArea, MinimumDimension, MaximumDimension, TotalPlotEdge: Plot size and footprint characteristics
- ForestMoisture, ForestElevation, ForestEdaphicType: Environmental descriptors
- ForestComposition, SubstrateGeology, AreaType: Vegetation and substrate classifications
- ForestStatus: Disturbance or succession status (e.g., Old-growth, Logged, Secondary)
- Data management and governance: PlotDatabaseManager, ForestPlotsContact
- Temporal context: DateEstablished, LastCensusDate, No.ofCensuses
- Plot usage and access: No.ofextraplotviews, PlotDatabaseManager, PlotPlotsContact
- Additional metadata fields: FragmentSize, NearestAnthropogenicEdge, %determinedatspecieslevel, %determinedatgenuslevel, etc.
- Notes: Contains numerous fields with detailed definitions to support accurate interpretation and future data integration.

## DryFlorBrazil_tree_census_data_corrected_May2019.csv: Key fields and definitions
- PlotID, PlotCode, PlotViewID, PlotName, PlotViewName, PI: Identifiers and plot view references
- TreeID, TagNumber, SubPlot T1: Stem-level identifiers and subplot location
- AllometricRegionID: Allometric region for the plot
- Family, Genus, Species, OriginalIdentification, Authority, AcceptedFamilyName, AcceptedFullSpeciesName: Taxonomic information and nomenclatural updates
- FamilyAPGID, GenusID, SpeciesID: Unique taxon identifiers
- CensusNo, CensusDate: Census sequencing and timing
- VoucherCode: Voucher reference for collected specimens
- D0, D1, DPOMtMinus1, D2, D3, D4, POM: Diameter measurements and changes across measurement positions (POMs)
- F1–F5: Data quality and field-management flags (alive status, mode of death, measurement technique, etc.)
- LI, CI: Liana infestation and canopy illumination indices
- Height: Tree height
- Additional fields: Notes on measurement methods, post-field data handling, and RAINFOFOR data codes
- Data linkage: Designed to support stem-level growth and mortality analyses, DBH change handling across POM changes, and integration with plot-level metadata

## Data governance and monitoring-framework considerations
- Demonstrates rigorous metadata practices, including unique identifiers, standardized units, and comprehensive field definitions.
- Highlights the importance of detailed data quality codes and provenance (flags F1–F5, voucher codes) to support transparent monitoring and auditability.
- Shows explicit data sharing readiness: rich metadata, versioning (corrected May 2019), and clear data ownership/contacts (PlotDatabaseManager, ForestPlotsContact).
- Facilitates reproducibility and cross-site comparability essential for environmental health monitoring and policy evaluation.

## Practical takeaways for monitoring framework authors
- Use standardized protocols (RAINFOR) to ensure consistency across sites and time.
- Provide extensive metadata with explicit field definitions, units, and versioning to enable data reuse and governance.
- Include unique identifiers for plots, subplots, and taxa to support traceability and longitudinal analyses.
- Incorporate data quality flags and lineage information (e.g., measurement changes, POM transitions) to manage methodological variability.
- Ensure data access details and governance roles are documented to reduce barriers to data sharing and collaboration.
- Align taxonomic updates and synonym management with accepted nomenclature (e.g., APGIII) to maintain data integrity over time.