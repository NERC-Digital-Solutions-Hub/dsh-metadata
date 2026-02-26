# SOURHOPE FIELD DATA HANDBOOK 2003

## Overview
- The NERC Soil Biodiversity Thematic Programme (established 1999) focused on understanding soil biodiversity and functional roles of soil organisms through 24 projects at the Sourhope field site (Scott et al., 2003).
- Primary measurements cover above-ground biomass production and vegetation nutrient composition.
- Site location: Sourhope farm, Macaulay/LURIs (now James Hutton Institute), Scottish Borders (Grid NT8545019630).

## Data Content and Purpose
- Two CSV data files are provided:
  - Biomass values, 1999-2001: P2109_VEG_BIOMASS_1999_2002.csv
  - Mineral nutrient analysis, 1999: P2109_BASELINE_99_VEG_MIN_ANAL.csv
- Purpose: to document and enable analysis of biomass production and vegetation nutrient content, suitable for GIS-based visualization and map-like data products.
- Normalisation: biomass results are suggested to be normalised against a baseline (C1) within each year due to year-to-year variation (noting a 2001 biomass increase likely due to staffing and equipment changes).

## Data Files (Structure)

- Biomass values, 1999-2001 (P2109_VEG_BIOMASS_1999_2002.csv)
  - MEASID: Project sample code
  - BLOCK: Block number (1-5)
  - MAIN_PLOT: Main plot letter (A-F)
  - SUB_PLOT: Sub-plot identifier
  - CELL_X, CELL_Y: Cell grid coordinates (within plots)
  - TREATMENT: Soil treatment applied
  - MEAS_DATE: Approximate date of measurement
  - BIOMASS: Dry weight of grass per 50 x 50 cm cell (grams)

- Mineral nutrient analysis, 1999 (P2109_BASELINE_99_VEG_MIN_ANAL.csv)
  - VEG_ID: Project sample code
  - CUT_DATE: Date of grass cut
  - TREATMENT: Soil treatment
  - BLOCK, MAIN_PLOT: Plot metadata
  - NITROGEN (N), CALCIUM (Ca), POTASSIUM (K), MAGNESIUM (Mg), PHOSPHORUS (P), ALUMINIUM (Al): Vegetation content (% or g/100g as specified)
  - Each nutrient includes associated method and detection limit data
  - N, Ca, K, Mg, P, Al detection limits provided (e.g., 0.15, 0.4, etc.)

## Site Context and Measurement Methods
- Sampling: Grass cut from 50 x 50 cm cells within each of the 4 main sub-plots in each main plot; vegetation sorted by species, dried at 80°C, weighed.
- Timing: Measurements taken across five occasions in each of 1999-2002 growing seasons; peak biomass in July/August.
- 2001 changes: Increase in biomass likely due to personnel changes and switch from manual cutting to mechanical shears.
- Baseline nutrient analyses conducted in July 1999; laboratory work by Macaulay/LURIs with specified acid-digest methods (B021, B032, D021).

## Data Quality and Limitations
- Quality control: numeric range checks, formatting conformity, and logical integrity checks; laboratories followed internal MLURI QA procedures.
- Legal/accuracy caveats: NERC cannot warrant the data’s accuracy or fitness for a particular use; no liability for losses or damages from data use.
- Data usability caveats: cross-year and cross-plot comparisons may be affected by personnel changes and equipment differences; normalization against year-specific baselines is recommended.

## Relevance for GIS Specialists
- Grid-based spatial data: CELL_X and CELL_Y enable spatial visualization of biomass across the Sourhope plots.
- Rich metadata: includes BLOCK, MAIN_PLOT, SUB_PLOT, and TREATMENT for spatial analysis of treatment effects on productivity and nutrient status.
- Supports map-based data products and spatial analyses of vegetation biomass and nutrient composition within experimental plots.

## References
- Scott, R.; Bell, J.; Kenny, C.; Jeffers, J.; Buckland, S.; Burt-Smith, G. (2003) SOURHOPE FIELD DATA HANDBOOK 2003. Available via the EIDC catalogue: https://catalogue.ceh.ac.uk/documents/766ffc31-9d38-4c8f-980b-6cd13edab3a8