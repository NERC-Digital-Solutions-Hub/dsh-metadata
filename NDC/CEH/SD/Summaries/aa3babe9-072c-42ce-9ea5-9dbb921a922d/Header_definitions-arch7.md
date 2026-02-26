# Rio_forests_metadata_corrected_May2019.csv and DryFlorBrazil_tree_census_data_corrected_May2019.csv – Metadata and census data descriptions

- The document describes two related datasets drawn from Rainfor/ForestPlots.net:
  - Rio_forests_metadata_corrected_May2019.csv: plot-level metadata for forest plots, following standard RAINFOR protocols.
  - DryFlorBrazil_tree_census_data_corrected_May2019.csv: per-tree census data within those plots, including taxonomic and diametric measurements.
- Access and guidance:
  - Rainfor manuals are available in English, Portuguese, Spanish, etc. at http://www.rainfor.org/en/manuals; a dedicated file (RAINFOR_field_manual_EN.pdf) accompanies the dataset.
  - Additional data handling and codes are documented via Rainfor/ForestPlots.net resources (e.g., RAINFO R_data_codes_EN.pdf, CrownLianaProtocols_EN.pdf).
- Purpose and audience:
  - Designed to support GIS-oriented data products and map-based visualizations for researchers, policy colleagues, clients, and the public.
  - Enables spatial understanding of plot locations, forest types, and forest structure through standardized metadata and census data.

## Experimental design and data scope

- Plots installed and surveyed according to standard RAINFOR protocols.
- Documentation includes the nature and units of recorded values and guidance for interpreting the data.
- Data cover multiple dimensions (spatial, ecological, temporal) to support map-based analyses and cross-dataset integration.

## Rio_forests_metadata_corrected_May2019.csv — Key fields and meanings

- Identifiers and codes:
  - PlotID (unique ForestPlots.net identifier)
  - PlotCode (ForestPlots.net code; e.g., ABC-12)
  - PlotName; PITeam (names of PI team members)
  - PlotDatabaseManager; ForestPlotsContact (points of contact)
- Spatial location and geography:
  - Country; Continent; BiogeographicalRegion; EcoRegion
  - LatitudeDecimal; LongitudeDecimal (plot center coordinates)
  - Altitude; ForestElevation
  - GroundArea (plot area on the ground); FragmentSize (area of old-growth fragment at first census)
  - NearestAnthropogenicEdge (distance to nearest human-made edge)
  - LocationSource; PlotAreaLocation; AreaType; AveragePlotSlope
- Environmental and thematic classifications:
  - ForestMoisture; ForestEdaphicType; ForestComposition
  - SubstrateGeology; ForestStatus
  - Continent/Region-specific classifications (AllometricRegion; AllometricRegionID)
- Plot characteristics and history:
  - DateEstablished; LastCensusDate; No.ofCensuses
  - PlotView-related fields: No.ofextraplotviews; Status; VerifiedBy
  - Additional plot descriptors: State/County/Province; Location details; Plot edge metrics (TotalPlotEdge; MinimumDimension; MaximumDimension)
- Data quality and standardization:
  - Metadata definitions and units (e.g., Ha, m, mm)
  - Definitions for each field, enabling consistent downstream GIS usage and data joins

## DryFlorBrazil_tree_census_data_corrected_May2019.csv — Key fields and meanings

- Plot and view identifiers:
  - Continent; Country; PlotID; PlotCode
  - PlotViewID; PlotViewName (identifies specific plot view configurations)
  - PlotName; PI (Principal Investigator)
- Tree-level identifiers and taxonomy:
  - TreeID; TagNumber
  - Family; Genus; Species; OriginalIdentification; Authority
  - AcceptedFamilyName; AcceptedFullSpeciesName
  - FamilyAPGID; GenusID; SpeciesID (unique taxon identifiers)
- Census and measurement details:
  - CensusNo; CensusDate
  - D0, D1, D2, D3, D4; DPOMtMinus1 (diameter measurements and changes across POM/DBH definitions)
  - POM (Point of Measurement for DBH)
  - SubPlot T1 (plot sub-division where the tree is located)
- Data quality, flags, and post-field processing:
  - F1, F2, F3, F4, F5 (Rainfor data quality and method flags; see RAINFO R_data_codes_EN.pdf)
  - LI (Liana Infestation index); CI (Canopy Illumination index)
  - VoucherCode (voucher for collected specimen)
  - D0, D1, DPOMtMinus1, D2, D3, D4 capture diameter measurements and adjustments during census changes
- Additional context and attributes:
  - AllometricRegionID; FamilyAPGID; GenusID; SpeciesID (linking to higher-level taxonomic frameworks)
  - CensusDate (mean date per census number)
  - Advanced search/plot views:
    - Main plot view vs. Preferred Plot view; options available via the ForestPlots.net interfaces
- Data standards and references:
  - Values and codes align with Rainfor data dictionaries and associated protocol documents
  - Referenced sources and protocols for canopy/liana measurements and post-field data management

## Data standards, access, and references

- Projections and classifications align with recognized schemes (e.g., Biogeographical Regions, WWF EcoRegions, Holdridge-inspired elevation classifications, Chave et al. 2005 allometric framework).
- Comprehensive data dictionaries and manuals are provided to facilitate consistent interpretation and GIS-ready usage.
- The dataset links to external resources for data codes and canopy/liana protocols, enabling standardized mapping and filtering.

## GIS relevance and practical usage

- Spatial richness:
  - Plot-level coordinates, areas, elevations, slopes, and edge distances support mapping of forest distribution, fragmentation, and habitat types.
  - EcoRegion and AllometricRegion fields enable regional comparisons and ecosystem-type mapping.
- Structure and composition:
  - Tree-level data with taxonomic identifications, diameters, census history, and measurement flags enable species distribution mapping and forest structure analysis across plots.
- Data integration:
  - Standardized identifiers (PlotID, PlotCode, TreeID) and cross-references to taxonomic IDs (FamilyID, GenusID, SpeciesID) support joins with other GIS datasets.
- Practical GIS workflows:
  - Create map layers for plots, edges, and ecological classifications; generate species richness or basal area maps from tree-level data; visualize census timing and plot-level dynamics.
- Considerations and challenges:
  - Data are distributed across multiple files with extensive metadata; ensure careful joins using PlotID, PlotCode, PlotViewID, and TreeID.
  - Variations in data resolution and quality flags require attention to data cleaning and filtering before map production.