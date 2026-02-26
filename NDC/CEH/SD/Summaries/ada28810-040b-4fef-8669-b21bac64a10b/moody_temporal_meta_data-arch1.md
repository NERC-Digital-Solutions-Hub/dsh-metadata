# Spatial and temporal variations in aquatic organic matter composition in UK surface waters

## Overview
- Aims to characterize how aquatic organic matter (DOM) composition varies spatially and temporally in UK surface waters.
- Data collected between 2018 and 2021 from four locations in England and Scotland, focusing on water bodies influenced by peat or organic soils.
- Samples taken from multiple locations within each catchment across diverse water body types (pools, headwaters, streams, reservoir inlets/outlets, lakes).

## Field sampling and site characteristics
- In situ measurements: pH, conductivity, dissolved oxygen, and water temperature; also recorded air temperature, pressure, and humidity using a multi-parameter probe.
- Sample collection: Grab water samples of 50 mL at each site, filtered on site through 0.45 µm membranes, kept cold in the field, transported in a cool box, and stored at 4 °C for laboratory analysis.
- Site metadata: locations anonymized for reservoirs; dataset UK_Sites includes site IDs, visits (1–24), sampling month and year, location-based groupings, peatland area, elevation, water body type, land use, vegetation cover, catchment area, peat catchment fraction, and distance to sea.

## DOM extraction and analysis
- Organic matter processing: large-volume water samples filtered to remove particulate matter, then concentrated by rotary evaporation to about 100 mL; residual material represents colloidal and dissolved organic matter (DOM).
- DOM characterization:
  - Elemental composition (C, H, N, O) determined with a CHNO analyzer after removal of inorganic carbonates (acid treatment).
  - A subset analyzed by negative-mode electrospray FT-ICR Mass Spectrometry (FT-ICR MS) for detailed molecular composition.
- Housekeeping and quality control: routine QA steps ensure accuracy of laboratory measurements (instrument calibration, replicate analyses).

## Datasets and contents
- UK_Sites: metadata per site and visit (IDs, visit numbers, months, years, groupings) plus descriptive site variables such as:
  - Peat area, elevation, water body type (e.g., reservoir headwater, inlet, surface water, lake, peat pool, stream)
  - Land use, vegetation cover, catchment area, peat coverage, distance to sea
  - Spatial anonymization of site locations
- UK_DOM: DOM composition metrics derived from CHNO data and FT-ICR MS analyses, including:
  - Proportions and oxidation-related metrics (DOM_PROP_C, DOM_COX, DOM_OR, DOM_DBEC, DOM_C_N, DOM_H_C, DOM_O_C)
  - Structural and diversity indicators (Assigned_formula, Mean_mz, Std_mz, Mean_ai, Mean_nosc, Simpson, Shannon)
  - Functional group proportions (PERC_LIPID, PERC_CARBO, PERC_AMINO, PERC_PEPTI, PERC_OXYAR)
  - Mass-spectrometry related metric (MS_DBEC)
- UK_Water: per-sample environmental and chemical measurements, including:
  - Basic water quality: pH, conductivity, dissolved oxygen, water temperature
  - Atmospheric conditions: air temperature, humidity, pressure
  - DOM-related and nutrient chemistry: DOC, DON, DIN, DOP, DIP
  - Anions and cations: chloride, sulfate, calcium, potassium, magnesium, sodium, aluminium, iron, manganese, zinc, copper, etc.
  - Other chemical indicators: SUVA254, E4E6, and related absorbance indices
  - Bank temperature and other site-specific measurements
- Data structure: each dataset uses IDs and visit numbers to link samples across sites and times.

## Data quality and governance
- Quality assurance:
  - 10% of samples analyzed in replicate; instrument calibration and ongoing checks during runs.
  - Replicate data compared; if within 95% agreement, an average value is used; if not, samples are re-analyzed.
  - Derived metrics restricted based on physical-property plausibility.
- Anonymity and access:
  - Site locations are withheld to preserve confidentiality; reservoirs’ access was granted under conditions of anonymity.
  - Datasets are prepared with metadata and are intended to be discoverable and usable through data portals.

## Reference context
- Moody, Catherine S.; Bell, N.G.A.; Mackay, C.L.; Kitson, E.; 2025. Spatial and temporal variations in aquatic organic matter composition in UK surface waters. Environmental Science and Technology Water, in press.
- Related methodological foundation: Moody, 2020, A comparison of methods for the extraction of dissolved organic matter from freshwaters. Water Research.