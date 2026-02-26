# Dataset Summary

- A survey of terrestrial habitats and vegetation in marginal uplands of Cumbria, conducted in 1978.
- 262 plots of 200 m2 were sampled across Cumbria using a stratified framework to inform environmental classification and monitoring of agricultural impact.
- Data focus on vegetation (vascular plants, bryophytes, macro-lichens) and habitat characteristics (within-plot and whole-square classifications, slope, aspect); soils data were collected but not documented or available as of 2017.
- The dataset supports understanding of data availability, quality, and gaps to enable prediction and monitoring over time.

## Dataset contents

- Vegetation data:
  - Presence/absence of vascular plants, bryophytes, and macro-lichens in 200 m2 plots.
  - Nested quadrat sampling with species recorded at 4 m2, 25 m2, 50 m2, 100 m2, and 200 m2 scales.
- Habitat data:
  - Habitat categories recorded for both the 200 m2 plots and the encompassing 1 km square.
  - Slope (measured with a clinometer) and aspect (bearing down the slope).
- Data files (CSV) included:
  - CMUP_1978_SITE_DESCS.csv: habitat descriptions for entire 1 km square sites.
  - CMUP_1978_SITE_DESCS_RELATED.csv: related habitat descriptions, including woody species.
  - CMUP_1978_PLOTS.csv: plot-level data (plot number, slope, aspect, and 10 km grid references).
  - CMUP_1978_PLOT_DESCS.csv: habitat descriptions for each plot within 1 km square sites.
  - CMUP_1978_GROUND_FLORA.csv: presence of vascular plants, bryophytes, and lichens by plot, plus survey date, species codes, and growth forms.
  - Appendix 1 (within CMUP_GROUND_FLORA) provides a full species list recorded during the survey.
- Site privacy note: exact site locations are not provided to protect landowner privacy; most sites were in private ownership.

## Survey design and methods

- Original purpose: classify the environment of Cumbria (ecological classification project) and monitor changes in marginal uplands where agricultural practices affect vegetation, fauna, and soils.
- Sampling design:
  - Cumbria stratified into 16 strata (based on a 1 km2 attribute map), with marginal areas represented by specific strata numbers.
  - 52 one-kilometre squares selected as survey sites, each containing five 200 m2 vegetation plots.
- Vegetation methodology:
  - Nested quadrat sampling within each 200 m2 plot (4 m2 → 25 m2 → 50 m2 → 100 m2 → 200 m2); new species recorded as quadrats increase in size.
  - Data collected by 262 plots across 1 km squares; plots distributed randomly within each 1 km square.
- Habitat methodology:
  - Habitat types recorded both within the 200 m2 plot and for the entire 1 km square.
  - Slope and aspect recorded as described above.
- Parameters captured:
  - Ground flora by species and quadrat, habitat types (within plot and within square), slope, and aspect.
- Related references and standards:
  - Bunce & Shaw (1973) standardized survey methods.
  - Bunce, Smith, and colleagues (1978, 2015) related to the UK Ecological Survey and land classification.
  - Full methodological context documented in UK ecological survey field methods handbooks.

## Data management and provenance

- Originators: C.B. Benefield and J.K. Adamson (Institute of Terrestrial Ecology – Merlewood).
- Field surveyors: C.B. Benefield, J.K. Adamson, W. Elfyn Hughes.
- Data management: C. Wood (Centre for Ecology & Hydrology, Lancaster).
- Related publications and datasets:
  - Bunce, R.G.H.; Shaw, M.W. (1973). A Standardised Procedure for Ecological Survey.
  - Bunce, R.G.H.; Smith, R.S.; Hill, M.O. (2015). Land Classification of Cumbria 1975.
  - Bunce, R.G.H.; Smith, R.S.; Booy, M.; Wood, C.M. (2017). Terrestrial habitat, vegetation and soil data from Cumbria, England, 1975.
  - Bunce, R.G.H.; Smith, R.S. (2015) and related UK Ecological Survey materials (handbooks, field methods).
- Data documentation:
  - Comprehensive metadata is provided via multiple CSV files (site descriptions, plot descriptions, ground flora, etc.), including a full species appendix.

## Privacy, access, and limitations

- Location data are intentionally withheld at the site level to protect landowner privacy.
- Soil data were collected but are not documented or available in this dataset (as of 12/9/2017).
- The dataset provides a robust framework and metadata, but access to exact coordinates is restricted; high-level site descriptions and 1 km square identifiers are available.

## Related datasets and publications

- Related Cumbria ecological datasets and historical classifications:
  - Bunce, R.G.H.; Smith, R.S.; Booy, M.; Wood, C.M. (2017). Terrestrial habitat, vegetation and soil data from Cumbria, England, 1975. NERC Environmental Information Data Centre. DOI: https://doi.org/10.5285/e96b909d-d52e-4b36-bc51-905ece420794
  - Bunce, R.G.H.; Smith, R.S.; Hill, M.O. (2015). Land Classification of Cumbria 1975. NERC Environmental Information Data Centre. DOI: https://doi.org/10.5285/0ac6249c-a6f2-4147-8ae9-50d576e85fc5
- Foundational methods:
  - Bunce, R.G.H.; Shaw, M.W. (1973). A Standardized Procedure for Ecological Survey. Journal of Environmental Management.
  - Bunce, R.G.H.; Smith, R.S.; 1978. UK Ecological Survey: Handbook of Field Methods. Institute of Terrestrial Ecology.

## Key takeaways for data leadership

- The dataset exemplifies a well-documented, methodologically standardized ecological survey with clear provenance and governance (originators, surveyors, and data management roles).
- It highlights the importance of comprehensive metadata and standardized methods for enabling data discovery, reuse, and integration with other datasets.
- Privacy considerations are explicitly addressed by withholding precise site locations while preserving meaningful regional descriptors.
- Availability of multiple related CSV files and a full species appendix supports robust data discovery, lineage tracing, and potential integration with broader Cumbria environment datasets.