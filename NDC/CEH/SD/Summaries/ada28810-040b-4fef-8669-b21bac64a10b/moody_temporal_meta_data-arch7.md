# Spatial and temporal variations in aquatic organic matter composition in UK surface waters

## Overview
- A multi-site UK study (2018–2021) examining how aquatic organic matter (DOM) composition varies in space and time across four locations in England and Scotland.
- Samples were taken from diverse water bodies (reservoirs, streams, lakes, peat-influenced systems) within multiple catchments.
- Data are organized into three linked datasets capturing site metadata, DOM composition metrics, and water chemistry/environmental variables.

## Study design and sampling
- Fieldwork conducted between 2018 and 2021 at four locations in the UK.
- Water samples collected from various water body types with peat or organic soils, including pools, headwaters, streams, reservoirs, lakes, and inlets/outlets.
- Multiple sampling sites per catchment; sampling visits range from 1 to 24 per site.
- Site and catchment context recorded, with locations anonymized due to access restrictions.

## Field measurements and sample processing
- In situ measurements at each site: pH, conductivity, dissolved oxygen, water temperature; concurrent air temperature, pressure, and humidity.
- Grab water samples filtered on-site (0.45 µm) and stored cold for laboratory analysis.
- Organic matter processing:
  - Particulate organic matter (POM) collected by filtering large volumes and concentrating residuals.
  - DOM extracted from filtered water via rotary evaporation and oven-drying to isolate colloidal/dissolved fractions.
- Laboratory analyses:
  - Elemental composition (C, H, N, O) using Elementar Vario MICRO cube after acid treatment.
  - Subset analyzed by negative-mode FT-ICR MS.
- QA: 10% replicate analyses; instrument calibration before runs; data cross-checks; re-analysis if replicates differ beyond tolerance.

## Analytical methods and QA
- DOM characteristics quantified through a suite of metrics (elemental composition, oxidation state, aromaticity indices, bond-equivalence metrics, and compound class percentages).
- FT-ICR MS used for detailed molecular composition in a subset.
- Quality assurance includes replicate agreement thresholds, calibration checks, and derived-metric constraints based on physical properties.

## Datasets and schemas
- UK_Sites: metadata per sampling site and visit.
  - Key fields: ID, Visit, Month, Year, Group, PEAT_AREA, Elevation, Type_4 (water body type), LAND_USE, VEG_COVER, POSITION, CATCHMENT_AREA, HOSTPEAT, DISTANCE_SEA, plus location-agnostic notes due to access constraints.
- UK_DOM: composition metrics derived from DOM (per site/visit).
  - Key fields include DOM_PROP_C, DOM_COX, DOM_OR, DOM_DBEC, DOM_C_N, DOM_H_C, DOM_O_C, Assigned_formula, Mean_mz, Std_mz, Mean_ai, Simpson, Shannon, PERC_LIPID, PERC_CARBO, PERC_AMINO, PERC_PEPTI, PERC_OXYAR, MS_DBEC, etc.
- UK_Water: environmental variables and water chemistry per sample.
  - Key fields include pH, CONDUCTIVITY, DISS_O2, WATER_TEMP, AIR_TEMP, HUMIDITY, AIR_PRES, BANK_TEMP, DOC, major ions (Cl, SO4, Ca, K, Mg, Na, Al, Mn, Fe, Pb, Cd, Co, Cu, Ni, Zn, Li), carbon/nitrogen/phosphorus pools (DOP, DIP, DON, DIN), and related ratios/indices (e.g., SUVA254, E4E6).

## Data use for GIS and mapping
- Enables spatial visualization of DOM composition and water chemistry across sites and through time.
- Suitable for creating time-enabled maps showing spatial trends in DOM metrics, oxidation state, diversity indices, and lipid/carbohydrate/peptide composition.
- Can be integrated with GIS layers such as land cover, peatland extent, catchment boundaries, elevation, and proximity to the sea to explore drivers of DOM variation.
- Anonymized site locations constrain precise GIS mapping; spatial analyses should account for limited geographic precision at the site level.
- Valuable for policy and public-facing mapping of water quality and organic matter characteristics in UK surface waters.

## Data access considerations
- Site locations are anonymized due to access permissions from water companies; spatial analyses should respect confidentiality while enabling regional assessments and trend analyses.

## Reference
- Moody, Catherine S.; Bell, N.G.A.; Mackay, C.L.; Kitson, E.; 2025. Spatial and temporal variations in aquatic organic matter composition in UK surface waters. Environmental Science and Technology Water, in press.