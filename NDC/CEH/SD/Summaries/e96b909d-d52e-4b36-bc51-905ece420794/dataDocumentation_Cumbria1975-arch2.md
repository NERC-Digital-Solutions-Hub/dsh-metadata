# Terrestrial habitat, vegetation and soil data from Cumbria, 1975 Ecological Survey of Cumbria 1975. Dataset Summary

- aims and purpose
  - Document the extent and nature of wildlife habitats in Cumbria (1975) to inform county land-use policies and nature conservation planning.
  - Fill information gaps on ecological condition beyond site-designated biological/geological importance sites (SSSIs and nature reserves).
  - Provide standardized, comparable data to support monitoring of environmental health and policy performance over time.

- geographic and temporal scope
  - Location: Cumbria, England (includes areas around the Lake District National Park).
  - Time period: 1975; data collected using standardized methods in that year.
  - Coverage: nearly 650 plots selected via stratified sampling; 642 actually surveyed (some inaccessible or in crop fields); related to broader Land Classification work for Cumbria 1975.

- sampling design and field methods
  - Stratified sampling across Cumbria using 1 km2 squares, defined by 150 attributes; analysis produced 16 strata.
  - Within each stratum, 3 plots of 200 m2 were selected (total 768 plots; 642 surveyed).
  - Plot-level methods:
    - Vegetation: nested quadrats (4 m2, 25 m2, 50 m2, 100 m2, then full 200 m2) with successive species listing and 5% cover bands (plus small-band estimates).
    - Soil: shallow central pit and auger samples to classify horizons; top 10 cm samples for pH.
    - Habitat: within plot and within 50 m of plot edge; slope and aspect measured; predefined habitat categories recorded inside and around plots.
  - Survey team and quality control: trained surveyors; supervision checks; field handbook and Bunce & Shaw (1973) methods guided the survey.

- data assets and structure
  - CUMBRIA_1975_VEG.csv
    - Vegetation data for vascular plants, bryophytes, and macro-lichens.
    - Key fields: STRATUM, SQUARE, PLOT, NEST, COVER, CODE, BRC_NUMBER, SCIENTIFIC_NAME, COMMON_NAME, GROWTH_FORM, FIELD_SHEET.
  - CUMBRIA_1975_SOIL.csv
    - Soil horizon descriptions by horizon codes.
    - Key fields: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP, FIELD_SHEET.
  - CUMBRIA_1975_PLOTS.csv
    - Plot-level physio-chemical and topographic data.
    - Key fields: STRATUM, SQUARE, PLOT, DATE, SLOPE, ASPECT, PH, plus depth ranges for litter, organic, mineral/organic, leached, weathered layers, and underlying depth.
  - CUMBRIA_1975_HABS.csv
    - Plot habitat descriptions (within plot; and habitat subcategories) and related attributes.
    - Key fields: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP, SUBGROUP.
  - CUMBRIA_1975_PHYS.csv
    - Main physiographic features within 50 m of plot edge.
    - Key fields: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP.
  - Related context files and field sheets published as part of the dataset package.

- data content and themes
  - Vegetation: presence and cover of vascular plants, bryophytes, and macro-lichens; species lists include scientific and common names, growth forms, and coded entries for analysis.
  - Soil: horizon depth data, horizon descriptions, and top-soil pH values per plot.
  - Habitat: classification of habitat types inside plots and in surrounding edge areas, including slope and aspect as ecological context.
  - Physiography: broader landscape features within 50 m of plot edges to aid habitat interpretation.

- data quality, provenance and privacy
  - Data collected by fully trained surveyors; quality-checked by supervisors; standardized field methods used.
  - Landowner privacy: specific site locations are not provided to protect privacy; most sites were on private land.
  - Original purpose linked to county structure planning and ecological assessment; aligned with Bunce & Shaw (1973) standardized procedures.

- related resources and provenance
  - Related datasets: Land Classification of Cumbria 1975 (Bunce, Smith, Hill; NERC EIDC DOI provided in related documents).
  - Key publications: Bunce & Shaw (1973) standardized ecological survey procedure; field handbook (unpublished 1975); Bunce & Smith (1978) Ecol. Survey Cumbria; numerous framework documents for the Structure Plan.
  - Prepared by: C.M. Wood (CEH Lancaster) and R.G.H. Bunce (Institute of Terrestrial Ecology, Merlewood).

- potential uses for environmental monitoring and analysis
  - Establish baseline conditions for Cumbria’s terrestrial habitats, vegetation, and soils from 1975 to support temporal trend analyses and policy evaluation.
  - Enable cross-dataset integration with standardized habitat classifications and land-classification frameworks.
  - Support spatially explicit monitoring by linking plot-level data to habitat types, soil properties, and physiographic context.
  - Provide a dataset with underlying species and soil data suitable for data-curation, long-term preservation, and broader reuse (as underlying data sources for reports, maps, and decision-making tools).

- access and reuse considerations
  - Files and metadata are organized for reuse in monitoring contexts; underlying data (species lists, horizon descriptions, and habitat classifications) are provided in structured CSV formats with explicit field definitions.
  - The dataset emphasizes standardized methods and documentation to facilitate comparability with other periods or regions following Bunce & Shaw’s frameworks.