# Radiocarbon dating of charcoal pieces collected from soil in the Amazon Basin

## Data overview
- Dataset: C14.csv containing radiocarbon dating of macrocharcoal pieces (≥1 mm) from soil in Guyana, Peru, and Brazil within Amazon forest plots that are terra-firme and not seasonally flooded; part of the RAINFOR network.
- Sample size: 60 macrocharcoal pieces dated.
- Field campaigns: 2015, 2017, 2018, 2019.
- Funding: NERC grant NE/N011570/1 and CAPES Brazil (PVE177-2012).
- Related publications: 
  - Feldpausch et al. 2022, Frontiers in Forests and Global Change.
  - Goulart et al. 2017, Quaternary Geochronology.
- Data structure and provenance: data collected through fieldwork, prepared and dated across multiple laboratories, with open reporting of dating results and uncertainties.

## Collection methods
- Sampling design: charcoal fragments collected at each site from soil profiles in three replicate pits spaced 100 m apart, located just outside the boundary of 1 ha permanent plots.
- Sampling protocol: macrocharcoal soil sampling performed by excavating 1 cm depth increments from the pit wall to 70 cm depth; charcoal separated from soil, air-dried, stored in containers.
- Selection criteria: for each pit, 4 charcoal pieces chosen for dating using (i) the sample nearest the surface from each pit, and (ii) four samples from 5 cm depth increments spanning progressively deeper layers; the Northern Peru site includes an extra date at 46 cm for alignment with other sites.

## Data analysis
- Pre-treatment and preparation: soil-charcoal surface cleaned; standard acid-base-acid method (0.5 M HCl at 80°C for 2 h, then 0.5 M KOH at 80°C for 2 h, then 0.5 M HCl at 80°C for 2 h).
- CO2 production and dating: samples combusted to CO2 in sealed quartz tubes, purified cryogenically, and reduced to graphite using Fe/Zn reduction; AMS dating conducted at the NERC Radiocarbon Facility (UK) and AMS at the Physics Institute of Universidade Federal Fluminense (Brazil).

## Nature and units of recorded values
- Data expressed as 14C age in years before present (BP).

## Quality control
- Unsatisfactory runs (failed or non-convergent) were discarded and not included in the dataset.

## Details of data structure
- CSV file: c14.csv with columns:
  - Location, Plot, Latitude, Longitude, Soil_Pit, Depth, C-14_age_yr_BP, C-14_age_Uncertainty, Lab_ID.
- Missing data: indicated as 'NA' when not recorded during fieldwork or no longer accessible.

## References
- Slota, Jull, Linick, and Toolin (1987). Radiocarbon 29, 303-306. Preparation of small samples for 14C accelerator targets by catalytic reduction of CO.