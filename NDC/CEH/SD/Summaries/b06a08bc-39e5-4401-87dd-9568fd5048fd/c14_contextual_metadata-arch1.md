# Radiocarbon dating of charcoal pieces collected from soil in the Amazon Basin

## Data overview
- Macrocharcoal pieces (≥1 mm) from soil in Guyana, Peru, and Brazil within Amazon forest plots.
- Terra firme, non-seasonally flooded sites; part of the RAINFOR network.
- Total of 60 charcoal samples dated; collected in field campaigns 2015, 2017, 2018, and 2019.
- Funding: NERC grant NE/N011570/1 and CAPES Brazil (PVE177-2012).
- Related publications:
  - Feldpausch et al. (2022) Frontiers in Forests and Global Change
  - Goulart et al. (2017) Quaternary Geochronology
- Data file: C14.csv with radiocarbon ages and associated metadata.

## Collection methods
- Charcoal collected from soil profiles at each site using three replicate pits separated by 100 m, located just outside 1 ha plots.
- Macrocharcoal sampling: soil excavated in 1 cm depth increments from pit wall down to 70 cm.
- For each pit: select 4 charcoal pieces for dating based on:
  - (i) sample nearest the surface, and
  - (ii) splitting the profile into 5 cm depth increments and selecting the next three samples from deeper intervals.
- Northern Peru site includes an additional date at 46 cm depth to balance sample size.
- Samples processed by removing soil surface charcoal, air-drying, and storing properly for analysis.

## Laboratory analysis and dating
- Pre-treatment: acid-base-acid method (0.5 M HCl at 80°C, 2 h; 0.5 M KOH at 80°C, 2 h; 0.5 M HCl at 80°C, 2 h).
- Graphite target preparation via Fe/Zn reduction (Slota et al., 1987).
- 14C dating by Accelerator Mass Spectrometry (AMS) at:
  - NERC Radiocarbon Facility, UK, and
  - Physics Institute, Universidade Federal Fluminense, Brazil.
- Result units: 14C age in years before present (BP).

## Data fields and structure
- File: C14.csv
- Columns:
  - Location (region)
  - Plot (RAINFOR plot code)
  - Latitude
  - Longitude
  - Soil_Pit (pit identifier)
  - Depth (cm depth of sampled charcoal)
  - C-14_age_yr_BP (14C age, years BP)
  - C-14_age_Uncertainty (uncertainty in age)
  - Lab_ID (laboratory identifier)
- Missing data indicated as NA; some field details may be unavailable.
- Depth range: 0–70 cm; sampling includes surface sample and deeper 5 cm increments.
- Note: Northern Peru site includes an extra 46 cm depth sample.

## Quality control
- Only converged and successful runs are included; failed runs were discarded.
- Data quality relies on standardized pre-treatment, AMS dating, and lab provenance (two laboratories).

## Data context and use
- Enables reconstruction of forest fire history and carbon dynamics in Amazonia through charcoal deposition events.
- Suitable for cross-site comparisons and temporal analysis of fire occurrence.
- Data provenance and metadata support reproducibility and potential integration with other datasets (e.g., broader RAINFOR data).
- Closely linked to published research on Amazonian charcoal chronology and fire history.

## References
- Slota, P. J., Jull, A. T., Linick, T. W., and Toolin, L. J. (1987). Preparation of small samples for 14C accelerator targets by catalytic reduction of CO. Radiocarbon, 29, 303-306.
- Feldpausch, T. R., Carvalho, L., Macario, K. D., Ascough, P. L., Flores, C. F., Coronado, E. N. H., Kalamandeen, M., Phillips, O. L., & Staff, R. A. (2022). Forest Fire History in Amazonia Inferred From Intensive Soil Charcoal Sampling and Radiocarbon Dating. Frontiers in Forests and Global Change, 5.
- Goulart, A. C., Macario, K. D., Scheel-Ybert, R., Alves, E. Q., Bachelet, C., Pereira, B. B., Levis, C., Marimon Junior, B. H., Marimon, B. S., Quesada, C. A., & Feldpausch, T. R. (2017). Charcoal chronology of the Amazon forest: A record of biodiversity preserved by ancient fires. Quaternary Geochronology, 41, 180-186.