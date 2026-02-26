# Structure and composition of woodlands across Mozambique: supporting documentation

## Overview
- Quantitative dataset measuring woodland structure and composition across 27 villages in three districts of Mozambique (Mabalane in Gaza, Marrupa in Niassa, Gurue in Zambezia).
- Data collected from 431 plots recording tree stems (>5 cm DBH), litter and grass biomass, coarse woody debris, and canopy cover.
- Timeframe: Mabalane (May–Sep 2014), Marrupa (May–Aug 2015), Gurue (Sep–Dec 2015).
- Sampling design: random plot selection within defined village areas; circular plots of 20 m radius (0.126 ha).
- Context: part of the ESPA-funded ACES project examining how land use changes affect ecosystem services and rural livelihoods; data linked with household surveys and remote sensing to scale to landscape level.
- Acknowledges evolving methods across sites; some methodological differences highlighted in dataset descriptions.

## Data collection design and sampling areas
- Village and plot selection:
  - Mabalane: 7 villages within a 5 km radius from village centers to capture immediate woodland resources.
  - Marrupa and Gurue: 10 villages per district chosen to reflect land-use intensity; boundaries determined with village leaders and GIS imagery.
- Plot design:
  - All sites: circular plots of 20 m radius; within each plot, all tree stems >5 cm DBH recorded; four 1 m² quadrats for leaf litter, woody litter, and grass biomass; four 20 m coarse woody debris transects; canopy cover estimated with a Densiometer.
  - Pilot study differed in plot design (nested sub-plots in some plots) to test optimal design.
- Fieldwork and instrumentation:
  - GPS for plot centers; DBH tapes for tree diameters; Densiometer for canopy cover; Android tablets with ODK for data capture; scales for biomass weighing.
  - Data collected and organized into six datasets with explicit plot, transect/quadrat, and tree identifiers to enable cross-linking.

## Data structure and content
- Six datasets:
  1. cwd.csv: measurements of each coarse woody debris piece along transects (length, diameter at intersection, decomposition class, local species name).
  2. cwd_decomposition.csv: qualitative decomposition classes with descriptions and decomposition correction factors for biomass adjustments.
  3. plot_metadata.csv: plot-level metadata (coordinates, radius, area, date, altitude, slope, canopy observations, completeness indicators for various data components, and notes on data quality).
  4. quadrat_data.csv: biomass data (grass, leaf litter, woody litter) within each of four 1 m² quadrats per plot plus canopy cover estimates.
  5. tree_stem_data.csv: measurements for all tree stems >5 cm DBH within plots (tree_id, stem_id, species, DBH, location of measurement, status, stump height, and quality notes).
  6. tree_stem_data_pilot.csv: tree-stem measurements for pilot subplots with slightly different sampling design.
- Data linkage:
  - Each record includes survey_id (4 = pilot, 5 = Mabalane, 6 = Marrupa, 7 = Gurue), plot_id, and where applicable subplot_id or transect/quadrat identifiers to integrate datasets.

## Quality control and data governance
- Quality assurance:
  - Lead author conducted global quality checks; field teams trained to ensure consistency; translators provided for field-to-Portuguese to English translation.
  - Post-collection data cleaning performed to identify extreme outliers and missing values; corrections made where possible or records removed.
- Documentation and transparency:
  - Methodological differences across sites are explicitly described; missing data are annotated in plot_metadata and other datasets.
  - Notes emphasize caution for pilot data due to design differences; soil data collected but not included in this release.
- Data accessibility and metadata:
  - Detailed metadata fields included for geolocation, plot size, date, and data completeness indicators (e.g., tree_stem_data, litter_data, canopy_data, cwd_data).
  - Data captured electronically in the field where possible (tablets + ODK) to support reproducibility.

## Limitations and challenges
- Method variation across sites and during the pilot phase; differences highlighted in the dataset descriptions.
- Some data gaps:
  - Not all plots have complete datasets; missing data explicitly recorded per plot.
  - Grass species identification was not robust due to dry-season inflorescence absence, so grass species data omitted.
  - Soil data collected but not included in this dataset; soil analyses submitted separately.
- Grass and canopy observations occasionally constrained by equipment availability (e.g., limited number of Densiometers).
- DBH estimation: for stems measured below 1.3 m, a correction function is used to estimate DBH at 1.3 m, introducing additional uncertainty.

## DBH adjustment and methodological notes
- A correction function is applied to estimate DBH at breast height (1.3 m) when measurements are taken lower on the stem.
- The height of measurement (p) must be less than 130 cm; the function accounts for taper in Miombo woodlands to adjust biomass estimates.

## References and context
- References to broader findings on charcoal production, land use impacts, and coarse woody debris methodology are provided to situate the dataset within existing literature.

## Relevance for monitoring frameworks
- Demonstrates a structured, multi-site woodland monitoring approach with standardized plots and comprehensive measurements (tree structure, ground vegetation, and coarse woody debris).
- Emphasizes:
  - Clear data governance, quality control, and metadata practices to support data reuse and transparency.
  - Challenges of cross-site methodological consistency and data completeness, guiding future harmonization efforts.
  - Explicit documentation of limitations and data availability to inform monitoring planning and data sharing policies.

## Potential improvements for future monitoring
- Harmonize methods across all sites and phases (including pilot) to minimize cross-site variability.
- Expand data sharing and governance: define licensing, access procedures, and data provenance to facilitate broader use while protecting sensitive information.
- Complete soil data integration and enhance grass species identification protocols for improved biomass estimation.
- Implement standardized completeness flags and automated checks to rapidly identify missing or inconsistent records.