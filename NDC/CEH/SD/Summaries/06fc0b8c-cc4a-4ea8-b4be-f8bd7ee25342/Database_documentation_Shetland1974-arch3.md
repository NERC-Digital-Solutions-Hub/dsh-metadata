# Survey of the terrestrial habitats and vegetation of Shetland, 1974

- Purpose and context
  - Part of a larger project to assess Shetland’s natural environment and monitor change, enabling local authorities to evaluate potential environmental impacts of oil exploration and related developments.
  - Aimed to: (i) describe the range of variation in Shetland vegetation and define habitat types; (ii) provide a structural basis for monitoring future vegetation change.

- Dataset scope and contents
  - Geographic coverage: Shetland Islands, Scotland.
  - Time period: 1974.
  - Data categories:
    - Vegetation data: vascular plants, bryophytes, lichens; species lists and percent cover per plot.
    - Soil data: horizon depths and descriptions; soil pH (top 10 cm sample).
    - Habitat data: habitat types inside plots and within 50 m of plots; slope and aspect.
  - Sampling and design basis:
    - Stratified sampling across 16 strata using Bunce & Shaw (1973) standardized methods.
    - Selection: 927 plots across 1 km2 areas, with 911 surveyed (some inaccessible or cropped fields).
    - Plot design: each 1 km2 area divided into 16 sub-squares; a 200 m2 plot per sub-square was randomly selected (5 plots per 1 km2 on average).
  - Data collection methods:
    - Nested quadrat system for vegetation (4 m2, 25 m2, 50 m2, 100 m2, then full 200 m2), with all unfound species recorded as quadrat size increases; % cover estimated in defined bands.
    - Soil sampling: center pit, auger samples for horizons, top 10 cm for pH (field meter).
    - Habitat and slope data collected for each plot; outer area surveyed for surrounding habitat types.
  - Data products and structure:
    - SHETLAND_SURVEY_PLOT_DATA.csv: plot descriptions including vegetation and general plot data.
    - SHETLAND_SURVEY_PLOT_INFO.csv: plot-level metadata (slope, aspect, soil layers, pH, etc.).
    - SHETLAND_SURVEY_GROUND_FLORA.csv: species list per nested plot with percentage cover.
    - Appendix I–Plot Codes: coding for plot strata, codes, and field sheet references.
    - Appendix II–Full Species List: comprehensive species nomenclature and codes.
  - Data management and governance:
    - Originators: R.G.H. Bunce, Woodlands Research Section (ITE Merlewood) and collaborators; data management by C. Wood, C. Hallam, D. Caffrey.
    - Privacy and data sensitivity: precise locations of survey squares withheld to protect landowner privacy; squares are representative of broader land classes; location details provided in Bunce & Bassett (2015) for context.

- Original purpose, methods, and standards
  - Original aim to create a baseline for monitoring change and to inform environmental impact assessments related to oil-related activities.
  - Field methods documented in Bunce & Shaw (1973) with a field handbook (Shetland Vegetation Survey: Handbook of Field Methods).
  - Sampling and data capture emphasized standardized procedures, metadata documentation, and the potential for future comparability.

- Data quality, metadata, and accessibility considerations
  - Metadata included for plots, habitats, soils, and vegetation, with standardized coding schemes.
  - Data transformation may be required to harmonize with modern datasets; top-level descriptors and field sheet provenance are documented.
  - Privacy constraints limit precise geolocations, though the dataset remains usable as a representative baseline for monitoring change.

- Related outputs and references
  - Related publications and datasets: Bunce & Shaw (1973) standardized ecological survey procedure; Bunce & Bassett (2015) Land Classification of Shetland 1974; Milner (1975) Shetland project monitoring report; Milner (1975) Shetland project monitoring report.
  - Core methodologies and nomenclature align with Flora of the British Isles and related bryology and lichen references.

- Practical relevance for monitoring framework authors
  - Demonstrates a comprehensive, stratified baseline survey designed for long-term monitoring of vegetation, habitats, and soils.
  - Highlights the integration of multiple data streams (vegetation, soils, habitats) and the importance of standardized field methods for comparability over time.
  - Illustrates data governance considerations, including data accessibility constraints and metadata requirements, relevant to contemporary monitoring framework design and data-sharing policies.
  - Provides concrete data products (CSV datasets and appendices) and a clear data lineage from field collection to publication.