# Experimental design/Sampling regime

- Plots installed following standard RAINFOR protocols.
- RAINFOR manual available in multiple languages (English, Portuguese, Spanish) at the provided web address and included as a field in the accompanying file.

## Nature and Units of recorded values

- Units used across datasets include hectares (Ha), metres (m), and millimetres (mm).
- Diverse metadata fields specify the nature and purpose of each variable, with clear definitions for each column in the accompanying tables.

## Details of data structure and other information useful to interpretation

- Rio_forests_metadata_corrected_May2019.csv
  - Core metadata for each plot, including:
    - PlotID (unique ForestPlots.net identifier), PlotCode (3 letters + 2 numbers; e.g., ABC-12), PlotName.
    - PI Team (names of principal investigators, project grant holders, field leaders).
    - Geography: Country, Continent, Cluster, BiogeographicalRegion, PlotAreaLocation, LocationSource, Altitude, LatitudeDecimal, LongitudeDecimal, GroundArea, Minimum/Maximum/TotalPlotEdge, FragmentSize, NearestAnthropogenicEdge.
    - Plot characteristics: ForestMoisture, Classification, ForestElevation, ForestEdaphicType, ForestComposition, SubstrateGeology, ForestStatus.
    - Plot provisioning and status: PlotDatabaseManager, ForestPlotsContact, DateEstablished, LastCensusDate, No.ofCensuses, Status, VerifiedBy.
    - Plot geometry and sampling: AreaType, AveragePlotSlope, EcoRegion, AllometricRegion, and related plotting and census metadata.
  - Intended use: to catalog and interpret plot-level context, enable discovery, and support downstream analyses.

- DryFlorBrazil_tree_census_data_corrected_May2019.csv
  - Per-tree census data linked to plots and plot views, including:
    - Spatial and identifying fields: Continent, Country, PlotID, PlotCode, PlotViewID, PlotViewName, PlotName, PI.
    - Tree-level identifiers and taxonomy: TreeID, TagNumber, SubPlot T1, AllometricRegionID, Family, Genus, Species, OriginalIdentification, Authority, AcceptedFamilyName, AcceptedFullSpeciesName, FamilyAPGID, GenusID, SpeciesID, VoucherCode.
    - Census and temporal data: CensusNo, CensusDate.
    - Diameter and measurement fields across different measurement frames: D0 (original field diameter), D1 (best estimate), DPOMtMinus1, D2, D3, D4, POM (Point of Measurement), and several quality/processing flags (F1–F5) and other codes (LI, CI) related to liana infestation, canopy illumination, and measurement technique.
    - Data processing notes: D4 is an inferred diameter (average of D2 and D3) for censuses with POM changes; special handling where no POM changes occur (D4 equals D1). Some values (e.g., DBH4) are not stored but estimated on request.
  - Data collection contextualization: includes references to data codes and processing rules (Rainfor data codes) and links to CrownLiana protocols for additional indices.

## Timeframe and data provenance

- Both datasets are labeled as corrected May 2019 editions, indicating updated or reconciled records.
- Data are associated with ForestPlots.net and use standard Rainfor conventions for census timing and taxonomic resolution.

## Units, definitions, and interoperability

- Explicit unit definitions (Ha, m, mm) are provided.
- Extensive field-level definitions ensure consistent interpretation across datasets, including multiple identifiers, taxonomic authority, and standardized taxon naming aligned with APGIII.
- Allometric region and plot-level classifications rely on established schemes (e.g., Feldpausch et al. 2012) to enable cross-study comparability.

## Data access, sharing, and governance

- Manuals and methodological guidance are publicly accessible (RAINFOR manuals; ForestPlots.net data portal).
- Dataset fields include managerial and contact points (PlotDatabaseManager, ForestPlotsContact) to support data requests and reuse.
- Data sharing is oriented toward CIF-like cataloging and public accessibility via established portals; caution about access limits or embargoes is implied through standard governance practices.

## Data quality, limitations, and stewardship considerations

- Designed to capture comprehensive metadata and per-tree census data, enabling robust quality assurance (e.g., alignment of original and accepted taxonomic names, voucher codes, and consistent diameter measurements).
- The presence of multiple plot views (PlotViewID/PlotViewName) requires careful selection during analysis (Main vs. Preferred views) and awareness of potential differences in included stems or census timing.
- Taxonomic updates and provenance (OriginalIdentification vs. AcceptedFullSpeciesName) highlight the need to track changes over time.
- Potential challenges for data stewards include coordinating data from multiple plots and views, ensuring timely updates from data creators, and harmonizing legacy formats with current standards.

## Practical considerations for use

- Ensure consistent interpretation of POM-related changes and the D0–D4 diameter series when analyzing tree growth or biomass.
- Use provided data codes and appendices for data cleaning and quality checks; consult the Rainfor data codes and CrownLiana protocols as needed.
- Leverage PlotDatabaseManager and ForestPlotsContact for data access, updates, or clarifications, and reference the RAINFOR manuals for standardized field procedures.
- When combining plot metadata with census data, align taxonomic identifiers (Family, Genus, Species) with AcceptedFullSpeciesName and ensure consistent APG IDs.