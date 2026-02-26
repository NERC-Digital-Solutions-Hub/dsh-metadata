# Terrestrial habitat, vegetation and soil data from Cumbria, 1975 Ecological Survey of Cumbria 1975. Dataset Summary

## Overview
- Provides baseline ecological data for Cumbria collected in 1975 to inform land-use policy and wildlife habitat assessments.
- Time period: 1975; Geographic coverage: Cumbria, England (including Lake District National Park area).
- Data were collected to address information gaps about overall ecological conditions beyond designated sites (SSSIs/nature reserves).

## Dataset contents and structure
- Data files:
  - CUMBRIA_1975_VEG.csv — vascular plants, bryophytes, and macro-lichens by plot, with presence and cover.
  - CUMBRIA_1975_SOIL.csv — soil horizon descriptions by plot, with horizon codes and groups.
  - CUMBRIA_1975_PLOTS.csv — plot-level physical and environmental measurements (slope, aspect, pH, horizon depths, litter/organic/mineral layers, etc.).
  - CUMBRIA_1975_HABS.csv — habitat descriptions and classifications within plots and at plot edges (50 m).
  - CUMBRIA_1975_PHYS.csv — physiographical features within 50 m of the plot edge.
- Full list of species recorded is provided (extensive species list appended as Appendix).
- Metadata and field-collection context are included (field sheets, codes, growth forms, etc.).

## Data categories and variables
- Vegetation data (Plot-level):
  - Nested quadrat sampling (4 m2, 25 m2, 50 m2, 100 m2, and 200 m2) with species presence and percent cover (5% bands, 1%, few).
  - Growth forms, codes, and field-sheet references included.
- Soil data:
  - Horizon descriptions and depths; pH of top 10 cm; detailed horizon-level descriptors (organic matter, decomposition, colour, texture, moisture, etc.).
- Habitat data:
  - Habitat types within the 200 m2 plot and within 50 m of the plot edge; slope and aspect for both within-plot and edge contexts.
  - Detailed coding for ground habitats, vegetation habitats, and associated categories (e.g., ground features, roads/boundaries, vegetation types).
- Physiographical data:
  - Features within 50 m of plot edge (streams, wetlands, rocky features, intertidal zones, etc.).
- Temporal and spatial metadata:
  - STRATUM (land classification stratum 1–16), SQUARE (survey square 1–4), PLOT (plot within square 1–16), DATE of survey, and field-sheet provenance.

## Sampling design and methods
- Purpose: to quantify ecological extent and habitat types across Cumbria to support structure planning and wildlife habitat policies.
- Sample design:
  - Stratified sampling across entire county; 16 strata based on 150 land-class attributes per 1 km2.
  - Within each stratum, 3 x 1 km2 units selected; 16 random points per land class to locate the 200 m2 plots.
  - Initially 768 plots selected; 642 actually surveyed due to inaccessibility or cropland; some adjustments in sampling were made (e.g., lakes/sea treatment).
- Field methods:
  - Vegetation: nested quadrats with species recorded and percent cover by plot; standard field methods per Bunce & Shaw (1973) and field handbook.
  - Soil: surface horizon excavation and auger sampling; horizon classification using predefined categories; top 10 cm soil sampled for pH.
  - Habitat: classification within plot and edge; slope and aspect measured with clinometer and compass.
- Quality control:
  - Data collected by fully trained surveyors; supervisory checks throughout; standardized methods with field handbook references.

## Data management and governance
- Originators and field team:
  - Originator: R.G.H. Bunce; field surveyors include R. Bunce, R. Smith, M. Booy, etc.
- Metadata and codes:
  - Detailed data dictionaries and field sheets referenced; dataset uses standardized codes for species, horizons, habitat categories, and physical features.
- Data sharing considerations:
  - Specific site locations are not disclosed to protect landowner privacy; underlying data and metadata are prepared for public sharing with appropriate governance.
- Data quality aspects:
  - Methods and horizon descriptors are standardized; data are designed for transparency, reproducibility, and linkage to related datasets (e.g., Land Classification of Cumbria 1975).

## Related datasets and references
- Related dataset: Bunce, R.G.H.; Smith, R.S.; Hill, M.O. (2015). Land Classification of Cumbria 1975. NERC Environmental Information Data Centre. DOI: 10.5285/0ac6249c-a6f2-4147-8ae9-50d576e85fc5
- Core methodological references:
  - Bunce R.G.H & Shaw M.W. (1973). A Standardized Procedure for Ecological Survey. Journal of Environmental Management.
  - Bunce, R.G.H.; Smith, R.S.; Hill, M.O. (1978). An ecological survey of Cumbria. Kendal/Cumbria County Council publication.

## Original purpose and policy relevance
- Objective: to supply information for the Cumbria Structure Plan policies on land use and wildlife habitats.
- Rationale: although many SSSIs and nature reserves existed, there was a lack of information on the overall ecological status of Cumbria; the Ecological Survey aimed to fill this gap.

## Considerations for monitoring frameworks
- Strengths for monitoring:
  - Standardized survey methods and a structured sampling framework enable trend analyses and cross-site comparability.
  - Rich, multi-taceted data (vegetation, soils, habitats, and physiography) support comprehensive environmental health assessments.
  - Publicly documented provenance, field methods, and data dictionaries facilitate reproducibility and governance.
- Limitations and considerations:
  - Data are historical (1975); baseline applicability needs careful interpretation for current monitoring.
  - Plot locations are generally not disclosed at precise coordinates to protect landowner privacy; may require access approvals for site-specific analyses.
  - Some plots were inaccessible; notable gaps may influence spatial representativeness.
  - Metadata completeness and harmonization with modern data standards may require mapping (codes, horizon descriptors, habitat categories) to current schemas.
- Governance and openness:
  - Clear lineage from standardized field protocols to dataset delivery; links to related data Centre resources support openness while maintaining privacy protections.