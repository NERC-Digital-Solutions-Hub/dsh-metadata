# Tree, vegetation and soil information from an ecological survey of semi- natural woodlands in the English Lake District, 1969

## Overview
- A comprehensive ecological survey of 48 semi-natural woodlands in the English Lake District conducted in June–August 1969.
- Nearly 300 plots were sampled across sites in the north west of England using standardized methods.
- Data encompass vegetation (vascular plants and bryophytes), trees, shrubs, soil chemistry, and site attributes (slope and aspect).
- Aimed at enabling site classification, monitoring of environmental health, and informing broader woodland surveys and policy decisions.

## Data scope and coverage
- Geographic: Lake District, England; sites across northwest England.
- Time period: June–August 1969.
- Datasets include:
  - Ground flora (vascular plants and bryophytes)
  - Trees and shrubs (species, heights, DBH)
  - Soil properties (pH, loss on ignition)
  - Site-level attributes (slope, aspect)
- 48 woodland sites with six randomly placed 20 m × 20 m plots per site (occasionally 8 plots).

## Sampling design and methods
- Plot design: 6 (occasionally 8) plots per site, each 20 m × 20 m.
- Within-plot sampling:
  - Trees: species, DBH, height of tallest trees within the plot.
  - Shrubs: species, DBH categories, heights of tallest shrubs.
  - Ground flora: presence/absence recorded at 10 random 25 cm × 25 cm nests per plot; bryophyte presence recorded for the whole plot.
  - Soil: samples from 5 points per plot (top 10 cm) analyzed for pH (lab, 1:1 soil to water) and loss on ignition (LOI) after ashing at 550°C.
- Sampling framework and data collection notes:
  - Date, weather, aspect, and site angle recorded for each plot.
  - Detailed plotting and nest layout visualized as 20 m × 20 m plots divided into a 4 × 4 grid; nests distributed across the grid for vegetation sampling and nutrient analysis.

## Data management, metadata, and access
- Originator: Woodland Ecology Section, Nature Conservancy – Merlewood (Grange-over-Sands, Cumbria).
- Key context: Informed by the Merlewood conference and prior woodland classification work (Woodland Cards, Steele 1968) to identify representative site groups.
- Analysis lineage: Presence/absence data used for association analysis; 6 random plots per site used to derive practical classifications; procedures informed planning of the National Woodland Surveys (1971).
- Core references: Bunce & Shaw (1973); Williams & Lambert (1959); Allen (1974); Steele (1968); Wood et al. (2015, 2016) and related lineage.
- Data management credit: Wood, C.
- Data structure: Separate datasets with linked keys:
  - LAKEDISTRICTWOODS_1969_SITES (site_id, name, coordinates)
  - LAKEDISTRICTWOODS_1969_PLOTS (site_id, plot, date, weather, aspect, angle, coordinates)
  - LAKEDISTRICTWOODS_1969_GROUND_FLORA (species-level presence/absence across nests 1–10, bryophyte flag, NEST1–NEST10 fields, QUAD_COUNT)
  - LAKEDISTRICTWOODS_1969_SoilPH (top-10 cm pH by nest per plot)
  - TREE/SHRUB data table (TREE_ID, SITE_ID, PLOT, SPECIES, DBH_CM, HT_M, D_CODE, TYPE, etc.)
- Metadata considerations:
  - Latin names for species updated to current nomenclature (BRC_NAME).
  - Missing data encoded (e.g., 999 for no sample).
  - Geographic references include OS grid coordinates for site plots.
  - Data sharing is implemented through public availability of underlying data, though some metadata completeness and data governance considerations apply.

## Data contents and structure highlights
- Ground flora data: presence/absence for 10 inner nests per plot; bryophyte data for whole plot; species coded with updated Latin names.
- Soil data: pH values from top 10 cm at nests 2, 4, 6, 8, and 10; LOI data per plot; quality notes (QC).
- Tree and shrub data: species, DBH, heights; dead stems indicated by D_CODE; fraction or count of stems per clump (SHRUB data).
- Plot and site metadata: precise location via OS grid references; weather and site attributes captured during sampling.

## Related resources and references
- Related datasets and presentations:
  - LAKEDISTRICTWOODS_1969_SITES
  - LAKEDISTRICTWOODS_1969_PLOTS
  - LAKEDISTRICTWOODS_1969_GROUND_FLORA
  - LAKEDISTRICTWOODS_1969_SoilPH
  - TREE/SHRUB data table
- Related publications and baseline methods:
  - Bunce, R.G.H. & Shaw, M.W. (1973). Standardized ecological survey procedures.
  - Williams, W. & Lambert, J.M. (1959). Multivariate methods in plant ecology.
  - Allen, S.E. (1974). Chemical analysis of ecological materials.
  - Steele, R.C. (1968). National survey of woodlands.
  - Wood, C.M., Bunce, R.G.H., et al. (2015–2016). Woodland Survey of Great Britain (1971–2001) and related datasets.

## Practical considerations for monitoring frameworks
- Demonstrates robust multi-taxa data collection across trees, shrubs, ground flora, bryophytes, and soils within a standardized, repeatable plot design.
- Emphasizes the importance of:
  - Randomized sampling within sites to obtain representative classifications.
  - Clear documentation of methods, plot geometry, and nest/grid layout to support reproducibility.
  - Metadata completeness and data governance to enable re-use, including data provenance and versioning of species nomenclature.
  - Linking site-level classification with multi-taxa data to inform policy and monitoring decisions.

## Limitations and governance considerations
- Temporal relevance: data are from 1969; applicability to current monitoring requires noting potential ecological changes over time.
- Data accessibility and metadata quality: while datasets are structured and linked, ongoing governance is needed to maintain metadata standards, update species nomenclature, and ensure timely data sharing.
- Data transformation needs: some fields require interpretation (e.g., 999 as missing; unit consistency for DBH, height).
- Potential data silos: the data are distributed across multiple tables within a single project; integration with other datasets may require careful cross-referencing by site_ID and PLOT.