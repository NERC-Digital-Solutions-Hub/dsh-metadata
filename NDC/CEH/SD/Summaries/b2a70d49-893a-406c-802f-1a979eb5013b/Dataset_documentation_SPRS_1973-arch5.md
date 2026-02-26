# Scottish Pinewood regeneration survey, 1973 Dataset Summary

## Overview
- Follow-up regeneration survey conducted in 1973 across 7 native Scottish pinewoods, expanding on the 1971 Scottish Pinewood Survey.
- Total of 419 plots, each 200 m2, surveyed across the selected woods to document trees, ground flora, habitat types, soil characteristics, and regeneration.
- Data categories include habitat data, vegetation data (trees, saplings, shrubs; vascular plants; bryophytes at Abernethy), regeneration data, and soil data.
- Methods and field procedures follow standardized Bunce & Shaw (1973) procedures; detailed field handbook referenced for exact classifications and recording.
- Data were prepared and documented by C.M. Wood and R.G.H. Bunce, with supporting field staff and laboratories; linked to the broader Scottish Pinewood Survey series.

## Scope and Coverage
- Geographic: 7 pinewood sites in Scotland (Mar, Abernethy, Barisdale, Glen Affric, Shieldaig, Loch Maree, Tyndrum).
- Time period: Start dates in 1973 (approx. July–September for respective sites).
- Site descriptions and plot-level details recorded; site coordinates provided (OSGR).
- Purpose: investigate regeneration in the selected woods, following the 1971 survey.

## Data Collected and Variables
- Habitat Data
  - Habitat categories for plots; slope and aspect measurements.
  - Site-level habitat attributes; pre-defined classifications per field handbook.
- Vegetation Data
  - Trees, saplings, and shrubs: recorded by individual and quadrat; DBH and height for widest tree; coppice information.
  - Vascular plants: species lists by nested quadrats; percent cover estimates.
  - Bryophytes: data available for Abernethy site only.
- Regeneration Data
  - First 20 seedlings per species (up to 1.3 m height) marked and sampled; includes immobilized circular quadrats for the first five specimens per species per plot.
  - Measurements: height of tallest shoot, seedling height, ground flora with >5% cover, ground/soil descriptive classes, soil attributes; soil sampled from top 10 cm for seedling and non-seedling quadrats.
- Soil Data
  - Soil pH from top 10 cm for each seedling type and for plot overall.
- Data capture framework
  - Nested quadrat system for vegetation; detailed recording of species, codes, and cover; standardized regeneration sampling and soil collection procedures.

## Data Files and Schema
- SPRS_1973_PLOT_SITE_DESCS.csv
  - Plot and site descriptions; site number, site name, start date, plot number, code fields, sheet reference.
- SPRS_1973_PLOTS.csv
  - Plot aspect and slope; soil pH data (non-regeneration, and per seedling type: birch, rowan, Scots pine, Salix); site and plot identifiers.
- SPRS_1973_GROUND_FLORA.csv
  - Vascular plants and bryophytes (Abernethy); site and plot identifiers; nest number; species codes (BRC numbers), common names, growth forms, total cover, seedling count where appropriate.
- SPRS_1973_TREE_DATA.csv
  - Trees, saplings, and shrubs data; site/plot identifiers; tree number; category (tree/sapling/shrub); species; DBH; dead indicator; height of widest tree.
- SPRS_1973_REGEN.csv
  - Scots Pine regeneration data; per plot and per regenerating species (or none); includes regeneration type, heights, seedling measurements, soil attributes, and related code descriptions.

## Provenance and Related Datasets
- Original purpose: regeneration assessment in 7 woodlands from the 1971 Scottish Pinewood Survey.
- Methods: Bunce & Shaw (1971, 1973) standardized field methods; field handbook provides precise classifications and procedures.
- Related datasets: 1971 Scottish Pinewood Survey dataset (Habitat, vegetation, tree, and soil data) published and catalogued via NERC Environmental Information Data Centre (EIDC). Link referenced: https://doi.org/10.5285/56a48373-771c-4d4a-8b5a-45ef496c6e55
- Key contributors: R.G.H. Bunce (survey management), C.M. Wood (documentation), field surveyors and laboratory staff; data management and documentation by Wood, Dodd, Hallam.

## Access, Usage, and Metadata
- Data are documented with explicit site, plot, and metric-level fields; CSV format supports re-use and integration with other pinewood datasets.
- Related publications provide methodological context and historical baseline (e.g., National Woodlands Classification 1971; Standardized Procedure for Ecological Survey 1973).
- Suggested use: combine with the 1971 dataset for longitudinal regeneration analysis; appropriate for studies on habitat change, regeneration success, and long-term pinewood dynamics.
- Portal and licensing: References to NERC EIDC indicate access through environmental data centres; ensure citation of Bunce et al. and Wood et al. when reusing.

## Quality, Limitations, and Considerations for Data Stewards
- Data quality in older surveys may reflect past field methods and documentation standards; ensure metadata clearly communicates field methods, units, and coding schemes.
- Some data elements have site-specific completeness (e.g., bryophytes only at Abernethy; multiple pH measurements per plot/seedling type).
- Complex, domain-specific taxonomy and habitat classifications require careful mapping to modern vocabularies; maintain original codes (SPRS_1973_*) with crosswalks to current standards.
- Data integrity depends on accurate linking across files (site, plot, nest, species codes); robust data dictionaries and schema documentation are essential.
- Potential updates or harmonization may be needed to integrate with contemporary data portals or data models.

## Acknowledgements
- Survey management: R. Bunce; laboratory assistance: C. Barr; field surveyors: named Aberdeen University postgraduate students; data management and documentation: C. Wood, B. Dodd, C. Hallam.