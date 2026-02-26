# Soil physico-chemical properties 1978 [Countryside Survey], Great Britain

- Overview
  - Dataset from Countryside Survey 1978 detailing soil physico-chemical properties (pH and loss on ignition, LOI) from up to 256 1km squares across Great Britain.
  - LOI measurements come from 1197 plots, taken from the top 15 cm of soil.
  - Includes both raw measurements and derived soil carbon metrics.

- Data scope and structure
  - Coverage: 256 1km squares and 1197 plots across England, Scotland, and Wales.
  - Year of survey: 1978.
  - Key columns:
    - SQUARE: 1km square sampling site code
    - PLOT: Plot identifier (one of 5 plots within each 1km square)
    - YEAR: Year of survey
    - PH: Soil pH
    - LOI: Percentage loss on ignition
    - C_CONC_LOI: Carbon concentration (g/kg) calculated as 0.55 × LOI
    - C_STOCK_LOI: Carbon stock (t/ha) calculated as 0.55 × LOI
    - LC07: ITE Land Class 2007 (text)
    - LC07_NUM: Land Class numeric code
    - COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
    - COUNTY07: County or Council
    - EZ_DESC_07: Countryside Survey Environmental Zone description

- Derived variables and calculations
  - C_CONC_LOI = 0.55 × LOI (g/kg)
  - C_STOCK_LOI = 0.55 × LOI (t/ha)
  - Note: The conversion factor for soil carbon concentration evolved from 0.5 (earlier) to 0.55 (adopted for CS estimates from 1998 and 2007 data).

- Measurement methods
  - Loss-on-ignition (LOI) methods
    - Sample: 10 g soil, sieved to 2 mm, from the top 15 cm.
    - Procedure: Dry at 375°C for 16 hours; combust a 1 g sub-sample at 550°C for 3 hours; measure weight loss to determine LOI (%).
    - LOI values computed from weight loss.
  - Soil pH methods
    - Method: pH in water for a suspension.
    - Procedure: 10 g field-moist soil with 25 ml de-ionised water (soil:water ratio 1:2.5 by weight); stir, stand 30 minutes, measure pH after a further 30 seconds.

- Data usage and attribution
  - Acknowledgement required: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
  - Copyright: “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
  - Acknowledgement and copyright text should appear on all copies, publications, and presentations.

- References and publications
  - Key publications and sources related to the dataset and methodologies, including:
    - Emmett et al. 2010, Countryside Survey: Soils Report from 2007
    - Bunce et al. (1996, 1981, 2007) on the ITE Land Classification of Great Britain
    - Avery & Bascomb (1974) soil survey laboratory methods
    - Carey et al. 2008, Countryside Survey: UK Results from 2007
  - Links and DOIs provided for several references and datasets (e.g., CEH/NERC data centres).