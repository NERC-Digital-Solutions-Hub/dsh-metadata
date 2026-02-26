# Terrestrial habitat, vegetation and soil data from Cumbria, 1975 Ecological Survey of Cumbria 1975. Dataset Summary

## Overview
- Time period: 1975; geographic coverage: Cumbria, England (Lake District core).
- Purpose: fill information gap on overall ecological status to inform county land-use structure plans and nature conservation policies.
- Scope: survey of terrestrial habitats, soils and vegetation across Cumbria using standardized methods.
- Scale: stratified sampling with 1 km2 units; 16 strata; 768 potential plots, 642 actually surveyed (200 m2 each).
- Data types: vegetation (vascular plants, bryophytes, macro-lichens), soils (horizon depths, pH, descriptions), habitats (within-plot and edge), and physiography near plot edges.

## Dataset Contents and Structure
- CUMBRIA_1975_VEG.csv: presence and cover of plant species by plot, including growth forms and field sheet reference.
- CUMBRIA_1975_SOIL.csv: soil horizon descriptions and coded classifications by plot.
- CUMBRIA_1975_PLOTS.csv: plot-level measurements (slope, aspect, soil pH, litter/organic/mineral layers, horizon depths).
- CUMBRIA_1975_HABS.csv: habitat descriptions within plots and at the 50 m edge, including subgroups.
- CUMBRIA_1975_PHYS.csv: physiographical features within 50 m of plot edge.
- Full List of Species Recorded: extensive species list with codes, taxonomic and growth-form details; appendix-based reference.
- Note: specific site locations are not provided to protect landowner privacy.

## Methods and Survey Design
- Sample design: land area stratified using 150 attributes per 1 km2; 16 strata; 768 candidate points; 642 plots surveyed.
- Plot design: nested quadrat system for vegetation recording at progressively larger subplots (4 m2 to 200 m2); percentage cover estimated in bands.
- Vegetation data: all vascular plants, bryophytes, and macro-lichens recorded; species codes and growth forms captured.
- Soil data: soil horizons classified using standardized categories; top 10 cm pH measured; detailed horizon descriptors recorded.
- Habitat data: habitat classes recorded both within the 200 m2 plot and within 50 m of the edge; slope and aspect also documented.
- Data quality: surveyors were fully trained; field work checked by supervisors; standardized field handbook followed.

## Original Purpose and Context
- Cumbria’s 1974 county reorganization prompted a need for comprehensive habitat/wildlife information beyond 200 designated sites (SSSIs and reserves).
- The Ecological Survey aimed to provide broad ecological status to support future land-use policies and conservation planning.

## Data Quality, Access, and Provenance
- Originators: R.G.H. Bunce (field ecology) and collaborators; field surveyors included R. Bunce, R. Smith, M. Booy, among others.
- Quality control: data collected by trained surveyors with supervisory checks; study follows Bunce & Shaw (1973) standardized methods.
- Data lineage: linked to Land Classification of Cumbria 1975 (Bunce, Smith, Hill, 2015) for broader contextual datasets.
- Accessibility: provided as structured CSV files with explicit schema (STRATUM, SQUARE, PLOT, etc.) and field sheet references; metadata notes included.

## Practical Considerations for Analysts
- Scale and locality: data are county-wide for 1975 but plots are 200 m2, with edge features recorded up to 50 m; care needed when aligning with modern administrative boundaries.
- Data integration: multiple datasets (vegetation, soils, habitats, physiography) enable multi-factor analyses of correlations among vegetation, soil properties, and habitat types.
- Spatial privacy: exact site coordinates are withheld; analyses should rely on plot-level aggregations or stratified summaries.
- Documentation: extensive field handbook references and related publications available to support reproducibility and methodological replication.

## Related Publications and Documentation
- Foundational procedures: Bunce & Shaw (1973) standardized survey; 1975 Ecological Survey handbook (unpublished) and Cumbria Ecological Survey reports.
- Related dataset: Land Classification of Cumbria 1975 (Bunce, Smith, Hill, 2015) with DOI provided.
- Full species list and growth-form taxonomy included in the dataset Appendix.