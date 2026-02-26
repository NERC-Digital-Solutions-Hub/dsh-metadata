# Scottish Pinewood regeneration survey, 1973 Dataset Summary

## Overview
- Follow-up regeneration survey of seven woodlands previously surveyed in 1971 Scottish Pinewood Survey.
- 419 plots, each 200 m2, surveyed across the selected woods to assess regeneration using standardized procedures.
- Data collected cover habitat, vegetation (trees, saplings, shrubs; vascular plants; bryophytes in Abernethy), regeneration metrics, and soil characteristics.

## Survey Design and Scope
- Seven woods selected from 27 pinewoods in the 1971 survey, organized into eastern, southwestern, central, northwestern groupings.
- Approximate survey start dates in 1973: late July to August 1973 (with site-by-site start dates and descriptions).
- Sampling: 419 plots distributed across the seven woods; each plot described by site, plot number, and descriptive metadata.
- Sites include Mar, Abernethy, Barisdale, Glen Affric, Shieldaig, Loch Maree, and Tyndrum.
- Followed Bunce & Shaw (1973) standardized survey methods; additional regeneration-focused procedures supplement the original 1971 field methods.

## Data Collected and Key Variables
- Habitat Data
  - Habitat types per plot; slope and aspect measured; some site-wide attributes recorded.
- Vegetation Data
  - Trees, saplings, and shrubs recorded by individual tree and by quadrats; vascular plants recorded across nested quadrats (4 m2, 25 m2, 50 m2, 100 m2, 200 m2) with percent cover estimates.
  - Bryophytes recorded for Abernethy only.
- Regeneration Data
  - Marking and sampling of the first 20 seedlings per species (up to 1.3 m tall) within each plot; followed by regeneration quadrat sampling of up to five seedlings per species.
  - For each regeneration quadrat: tallest vegetative shoot height, seedling height, ground flora (>5% cover), ground/soil descriptive classes, and soil attributes.
  - Soil samples taken from the top 10 cm beneath regenerating seedlings and non-regenerating quadrats.
- Soil Data
  - Soil pH samples from various seedling-type quadrats and non-regeneration areas; soil descriptions include various ground/soil classes and related attributes.
- Data per site
  - Comprehensive per-site and per-plot descriptors, including start dates, plot descriptions, and site descriptions.

## Methods and Procedures
- Nested quadrat system used for vegetation assessment within each 200 m2 plot.
  - Trees, saplings, and shrubs recorded by individual and by quadrat.
  - Vascular plants: species lists by progressively larger nested quadrats; percent cover recorded.
  - Bryophytes (Abernethy only) recorded by plot.
- Habitat classification and site attributes
  - Pre-defined habitat categories with detailed classifications; slope measured with clinometer; aspect measured bearing down slope with a Silva compass.
- Regeneration methodology
  - Seedlings marked with pins; regeneration quadrats placed to sample the first five seedlings of each species; measurements include heights and ground/soil characteristics; soil sampled from seedling and non-seedling quadrats.
- Data encoding
  - Data sheets and field handbooks (notably Bunce & Shaw, 1973; National Woodland Classification, 1971) guided the recording and coding of habitat, vegetation, and regeneration data.

## Data Files and Structure
- SPRS_1973_PLOT_SITE_DESCS.csv
  - Plot and site descriptions; site number, name, start date; plot number; coding and sheet metadata; descriptive text fields.
- SPRS_1973_PLOTS.csv
  - Plot-level data: site, plot number, date, plot slope, plot aspect; soil pH values by seedling type and non-regeneration plots.
- SPRS_1973_GROUND_FLORA.csv
  - Vascular plants and bryophytes (Abernethy only); species codes, names (common and scientific), growth form, total cover, seedling counts; nest/plot identifiers.
- SPRS_1973_TREE_DATA.csv
  - Trees, saplings, and shrubs: site, plot, nest, tree number, tree category, species, DBH, height, dead indicator.
- SPRS_1973_REGEN.csv
  - Scots Pine regeneration data: per site/plot/sheet/nest; regeneration type, species codes, descriptions, measurements (heights, ground/soil descriptors), and related data.
- Data coverage notes
  - Highlights where bryophyte data exist (Abernethy) and the detailed regeneration/soil descriptors per quadrat and per plot.

## Provenance and References
- Originators and contributors include R.G.H. Bunce, M.W. Shaw, and C.M. Wood, with collaborators from Aberdeen University and Merlewood.
- Related foundational works:
  - Bunce & Shaw (1971) National Woodland Classification 1971: Handbook of Field Methods
  - Bunce & Shaw (1973) A Standardized Procedure for Ecological Survey
  - Steven & Carlisle (1959) The Native Pinewoods of Scotland
- The 1973 dataset is part of a continuum from the 1971 Scottish Pinewood Survey; follow-up data link to the NERC Environmental Information Data Centre (EIDC) for the 1971 data.

## Data Governance, Access, and Openness
- The dataset is organized with explicit metadata fields and standardized codes to facilitate reuse.
- Data provenance includes detailed method references and site-level context, aiding reproducibility and cross-study comparability.
- While the 1973 data describe structure and fields comprehensively, explicit public access policies are not detailed in the summary; related datasets (1971) are referenced as stored with a data centre (NERC EIDC).

## Relevance for Monitoring Frameworks
- Demonstrates a robust, standardized monitoring approach with:
  - A clear objective (assessing regeneration in native pinewoods against prior baseline data).
  - A multi-layered data model (habitat, vegetation, regeneration, soil) enabling environmental health assessments.
  - Standardized field methods traceable to published handbooks, supporting comparability over time.
  - Comprehensive metadata and data structure to support governance, quality checks, and data sharing.
- Provides baseline data against which policy or management interventions could be evaluated for effectiveness on regeneration and habitat quality.

## Key Limitations and Considerations for Practitioners
- Bryophyte data are limited to Abernethy, reducing comparability across all sites for that component.
- The dataset reflects a single point in time (1973) and the preceding 1971 survey, so temporal trend analysis requires careful integration with the 1971 data.
- The complexity of codes and the depth of classifications require careful data management and documentation to ensure correct interpretation and reuse.
- Potential data gaps or inconsistencies inherent in legacy field data and the need for metadata curation when integrating with modern monitoring frameworks.