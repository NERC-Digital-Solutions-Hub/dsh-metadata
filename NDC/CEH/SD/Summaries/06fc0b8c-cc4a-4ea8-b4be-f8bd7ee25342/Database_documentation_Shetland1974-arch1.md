# Survey of the terrestrial habitats and vegetation of Shetland, 1974

- A national-scale survey of Shetland’s terrestrial habitats, vegetation, and soils conducted in 1974 as part of evaluating the natural environment for oil-exploration impacts and as a basis for monitoring change.
- Originators and methods: fieldwork led by R.G.H. Bunce and colleagues; used Bunce & Shaw (1973) standardized survey procedures and a field handbook; data management by C. Wood, C. Hallam, and D. Caffrey.

## Dataset scope and purpose

- Geographic coverage: Shetland Islands, Scotland.
- Time period: 1974 (baseline survey; data described as part of a larger project to monitor habitat change since 1974).
- Objectives:
  - Assess variation in vegetation and classify habitat types.
  - Provide a structural basis for monitoring future vegetation change.
- Related outputs: Handbooks, standard procedures, and reports (e.g., Bunce & Shaw 1973; Milner 1975; Bunce & Bassett 2015 on land classification).

## Survey design and sampling

- Stratified sampling across the entire area, using 16 strata (site-level classes) based on geographic features with 150 attributes per 1 km2.
- Within each stratum: five 1 km2 quadrats were selected (total across strata); each 1 km2 was subdivided into 16 sub-squares.
- Plot design within sub-squares: a 200 m2 plot randomly selected from each sub-square; if allocation fell in water, sub-square omitted.
- Total plots targeted: 927; plots actually surveyed: 911 (some inaccessible or in crop fields).
- Plot layout: each 1 km2 area surveyed yielded between 1 and 16 plots, resulting in 911 terrestrial plots.

## Data collected and structure

- Vegetation data (within 200 m2 plots):
  - Nested quadrat sampling: recorded vegetation at 4 m2, 25 m2, 50 m2, 100 m2, and the full 200 m2 quadrat.
  - Species recorded: vascular plants, bryophytes, macro-lichens; percentage cover estimated in bands.
  - Appendix II provides a full species list.
- Soil data:
  - Horizon depths and descriptive categories; top 10 cm sampled for pH analysis.
  - Field measurements of horizon properties and soil pH (pH measured in the field).
- Habitat data:
  - Within-plot and within-50 m surrounding plot; habitat categories defined and recorded with slope and aspect.
- Data files (three main CSVs):
  - SHETLAND_SURVEY_PLOT_DATA.csv: Descriptions for soil, plot habitat, and habitats within 50 m of each plot.
  - SHETLAND_SURVEY_PLOT_INFO.csv: Slope, aspect, soil horizons, pH, and related depth measurements.
  - SHETLAND_SURVEY_GROUND_FLORA.csv: Species list per nest (plot) with cover percentages and species metadata.
- Data codes and terminology (e.g., STRATA, PLOT, CODE, DESCRIPTION) enable cross-referencing between vegetation, soil, and habitat datasets.

## Methods and data quality

- Vegetation sampling: hierarchical quadrats (4 m2 to 200 m2) to capture species presence and cover across scales.
- Soil sampling: centre-plot pits and augers; horizon-based classifications; pH from topsoil; standardised categories defined in the field handbook.
- Habitat and slope: documented inside plots and within 50 m, with slope from a clinometer and aspect from a compass.
- Provenance and documentation: dataset compiled from field sheets and later documentation; references include Bunce & Shaw (1973), Bunce (1974), Milner (1975), and Bunce & Bassett (2015) for land classification of Shetland 1974.
- Privacy and access considerations: CEH holds precise locations confidential to protect landowner privacy; squares are representative of Land Classes; location data may be accessed via linked datasets (e.g., Bunce & Bassett 2015) for contextual classification.

## Appendices and species data

- Appendix I: Plot codes (strata, site codes, plot identifiers) and cross-references for plotting and data coding.
- Appendix II: Full species list (extensive compilation of vascular plants, bryophytes, and lichens observed during the survey), with nomenclature references (Clapham et al. 1962; Warburg; Paton; James; etc.).
- The dataset includes both field-collected data and derived metadata, with ongoing references to related surveys (e.g., Shetland Freshwater Survey 1974; Shetland Coastal Survey 1974).

## Data access, use cases, and caveats

- Data accessibility: three main CSV files plus the published species list; exact plot locations are withheld to protect privacy, but data are structured to enable analysis at the stratum and plot levels.
- Potential analytical opportunities for analysts:
  - Correlate vegetation composition (vascular plants, bryophytes, lichens) with soil horizons and pH.
  - Examine habitat type distributions inside plots and within 50 m margins across strata.
  - Model relationships between slope/aspect and vegetation/habitat categories.
  - Track changes by comparing 1974 baseline with later monitoring efforts (e.g., Bunce & Bassett 2015 Land Classification) to assess habitat change over time.
- Limitations for analysis:
  - Access to precise coordinates is restricted; analysis relies on stratified strata and generalized site codes.
  - Some plots were inaccessible or crop-field-occupied, potentially introducing gaps.
  - Taxonomic updates may be needed to align with modern nomenclature; the Appendix II provides the 1974 species list with historical names.

## How this fits the Analysts archetype

- Provides multi-layered data across vegetation, soils, and habitats suitable for uncovering correlations, building predictive models, and informing environmental decision-making.
- Combines standardized field methods with a robust sampling design enabling cross-dataset integration and reproducible analyses (strata, plot codes, habitat categories, soil horizons, and species data).
- Supports monitoring and impact assessment needs by supplying a rigorous baseline for change detection, with metadata and references to methodological standards and related datasets.