# Tree, vegetation and soil information from an ecological survey of semi-natural woodlands in the English Lake District, 1969

- A survey of 48 semi-natural woodlands in the English Lake District conducted in June–August 1969.
- Within each woodland, six randomly placed 20 m x 20 m plots were sampled to collect:
  - Tree and shrub data (species, heights, diameters at breast height DBH).
  - Ground flora (vascular plants and bryophytes) presence/absence across nested sampling areas.
  - Soil properties, including pH and loss on ignition (LOI), from top 10 cm.
- Vegetation data include both qualitative (presence/absence) and quantitative (DBH, height) measurements.
- Data are organized into multiple related datasets with site- and plot-level identifiers, enabling multi-level analysis.

## Data Scope and Coverage

- Geographic scope: Lake District, England.
- Time frame: June–August 1969.
- Sampled content:
  - Vascular plants and bryophytes (ground flora).
  - Trees and shrubs: species, heights, DBH; growth metrics.
  - Soil: pH values and LOI; site attributes (slope, aspect).
  - Plot-level context: weather, date, site and plot identifiers, geographic coordinates.
- Site list: 48 woodland sites (with OS grid references and descriptive names); two sites included as outliers.

## Sampling Design and Methods

- Study design:
  - 48 woodlands sampled (including two outliers).
  - In each woodland: 6 plots (occasionally 8) of 20 x 20 meters.
  - Each plot subdivided into a grid; sampling at 10 random intersections (nests) for ground flora.
- Tree and shrub measurements:
  - DBH measured for trees in the plot; tallest tree heights recorded.
  - Shrubs measured across DBH categories with heights documented.
- Ground flora sampling:
  - 10 nests per plot, each 25 cm x 25 cm, recording presence/absence of species.
  - Bryophytes recorded for the whole plot.
- Soil sampling:
  - 5 soil samples per plot, from nests, top 10 cm for pH (measured with glass electrode) and LOI (ashed at 550°C).
  - Fresh soil pH values noted; 999 indicates no sample taken.
- Plot documentation:
  - Date, weather, aspect, slope angle, and site observations recorded for each plot.

## Data Structure and Key Datasets

- LAKEDISTRICTWOODS_1969_SITES
  - Location of each woodland site; site IDs, names, and grid coordinates (OSGB grid/point references).
- LAKEDISTRICTWOODS_1969_PLOTS
  - Plot-level metadata for each site (SITE_ID, SITE, PLOT, DATE, WEATHER, ASPECT, ANGLE_PC, EASTING/NORTHING, etc.).
- LAKEDISTRICTWOODS_1969_GROUND_FLORA
  - Ground flora data: ROW_ID, SITE_ID, SITE, PLOT, SPECIES (updated to accepted Latin name BRC_NAME), BRYO (bryophyte flag), NEST1–NEST10 presence/absence indicators, QUAD_COUNT.
  - Includes a taxonomic standardization field (BRC_NAME) and references to external species libraries.
- LAKEDISTRICTWOODS_1969_SoilPH
  - Soil pH values by nest; includes SITE_ID, SITE, PLOT, NEST2/NEST4/NEST6/NEST8/NEST10 pH values, and a QC note.
- TREE recording data (template described)
  - TREE_ID, SITE_ID, SITE, PLOT, SPECIES, DESCRIPTION (latinate name), DBH_CM, HT_M/HT_FT, STEM_COUNT (shrubs only), D_CODE (dead stems), TYPE (TREE or SHRUB).
- Related data and metadata
  - Plot location description, sampling plots (LAKEDISTRICTWOODS_1969_PLOTS), authorship and data management notes (e.g., Wood, C.).

## Background and Methodological Context

- Rationale for site classification and standardized woodland surveys established in the late 1960s (Merlewood programme).
- Data collected to support objective classification of woodland sites and to enable cross-site comparisons.
- Preliminary analyses indicated presence/absence data captured meaningful quantitative vegetation features (e.g., similar dominants) across site groups identified by association analysis.
- The project contributed to planning for subsequent National Woodland Surveys (1971).

## Data Quality, Standardization, and Documentation

- Taxonomic names updated to current references where feasible (BRC_NAME with links to plant trait libraries).
- Data include both presence/absence and quantitative measurements, enabling diverse analytical approaches.
- Documentation provides detailed field protocols, data fields, and data management notes to support reuse and reproducibility.
- Recognizes potential data limitations such as missing soil pH values (coded as 999) and inclusion of two outlier sites.

## Related Datasets and Publications

- Wood, Bunce and colleagues’ work on standardized ecological survey methods (e.g., Bunce & Shaw 1973; Steele 1968).
- Related datasets: Woodland Survey of Great Britain, 1971 (Wood et al., 2015; 2016).
- Key references for analysis approaches include Williams & Lambert (1959) on multivariate association analysis and subsequent ecological data assimilation efforts.

## Potential Uses for Data Analysts

- Explore correlations between species composition (ground flora, trees, bryophytes) and site attributes (slope, aspect) and soil chemistry (pH, LOI).
- Build predictive models linking environmental variables to vegetation structure and species presence.
- Validate and extend association analyses by comparing presence/absence patterns with quantitative measures (DBH, height, stand structure).
- Cross-site comparisons across 48 woodlands to identify robust patterns of woodland classification and vegetation gradients.
- Integrate with related datasets (e.g., 1971 Great Britain woodland surveys) for broader temporal and spatial context.

## Considerations for Reuse

- Historical data collected in 1969; note potential changes in woodland composition over time.
- Data are structured to allow multi-level (plot-site-woodland) analyses but require careful handling of nested design.
- Some fields require standardization or mapping to current taxonomies and geographic references.
- Missing data indicators (e.g., 999 for pH) should be accounted for in analyses.