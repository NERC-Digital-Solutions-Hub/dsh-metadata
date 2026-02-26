# Radiocarbon dating of charcoal pieces collected from soil in the Amazon Basin

## Data overview
- Spreadsheet C14.csv contains radiocarbon dating data for macrocharcoal pieces (≥1 mm) from soil samples in plots across the Amazon basin (Guyana, Peru, Brazil) within the RAINFOR network.
- Total of 60 macrocharcoal pieces dated.
- Field campaigns conducted in 2015, 2017, 2018, and 2019.
- Research supported by NERC grant NE/N011570/1 and CAPES Brazil.
- Related publications:
  - Feldpausch et al. (2022). Forest Fire History in Amazonia Inferred From Intensive Soil Charcoal Sampling and Radiocarbon Dating. Frontiers in Forests and Global Change.
  - Goulart et al. (2017). Charcoal chronology of the Amazon forest: A record of biodiversity preserved by ancient fires. Quaternary Geochronology.

## Collection methods
- Charcoal fragments collected from soil profiles at each site in three replicate pits, 100 m apart, just outside the 1 ha permanent forest plots.
- For macrocharcoal dating: soil excavated in 1 cm depth increments from the pit wall to 70 cm depth; four pieces selected per pit:
  - one sample nearest the surface per pit, plus three samples from progressively deeper 5 cm depth increments.
- Northern Peru site includes an additional date at 46 cm depth from a fourth soil pit to maintain sample size consistency.

## Data analysis / lab methods
- Sample preparation involved scraping surface soil from charcoal and pre-treatment with standard acid-base-acid methods:
  - 0.5 M HCl at 80°C for 2 h, then 0.5 M KOH at 80°C for 2 h, then 0.5 M HCl at 80°C for 2 h.
- Samples combusted to CO2, purified cryogenically, and reduced to graphite using Fe/Zn method.
- 14C dating performed by Accelerator Mass Spectrometry (AMS) at:
  - NERC Radiocarbon Facility and at the Physics Institute of Universidade Federal Fluminense, Brazil.

## Nature and units of recorded values
- 14C ages recorded in years Before Present (BP).
- Each record includes an associated uncertainty.

## Quality control
- Failed runs or non-convergent runs were discarded and not included in the dataset.

## Details of data structure
- CSV columns:
  - Location (region), Plot (RAINFOR plot code), Latitude, Longitude, Soil_Pit, Depth, C-14_age_yr_BP, C-14_age_Uncertainty, Lab_ID.
- Missing data indicated as NA; some data may be missing due to field recording limitations or accessibility issues.

## Usage notes / potential analyses
- Useful for reconstructing fire history and carbon dynamics in Amazonia; can be combined with other RAINFOR data for cross-site comparisons.
- Enables self-serve exploration of depth-age relationships and spatial patterns of charcoal deposition across sites.
- References and methods provide a basis for dataset integration and reproducibility with similar radiocarbon datasets.

## Access and references
- Data attached as the C14.csv file.
- Methodological details and context drawn from Slota et al. (1987) regarding sample preparation for 14C AMS targets:
  - Preparation of small samples for 14C accelerator targets by catalytic reduction of CO. Radiocarbon, 29, 303-306.