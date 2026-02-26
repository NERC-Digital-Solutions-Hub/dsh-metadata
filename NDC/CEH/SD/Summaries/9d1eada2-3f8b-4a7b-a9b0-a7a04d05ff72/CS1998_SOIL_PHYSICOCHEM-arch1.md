# Soil physico-chemical properties 1998 [Countryside Survey], Great Britain

## Overview
- Dataset CS1998_SOIL_PHYSICOCHEM.csv contains soil physico-chemical properties from up to 256 1km squares across Great Britain, surveyed in 1998/1999.
- propertiesInclude pH, loss on ignition (LOI), carbon concentration and stock, total nitrogen, Olsen phosphorus; linked to location and land classification data.

## Data structure and fields
- SQUARE: 1km square sampling site code
- PLOT: Plot identifier (one of 5 per square)
- YEAR: Year of survey
- PH: Soil pH
- LOI: Percentage loss on ignition
- C_CONC_LOI: Carbon concentration (g/kg) calculated from LOI
- C_STOCK_LOI: Carbon stock (t/ha) calculated from LOI
- N_PERCENT: Percentage nitrogen
- PO4_OLSEN: Olsen phosphorus (mg/kg)
- LC07: ITE Land Classification 2007 (text)
- LC07_NUM: Land Classification code (numeric)
- COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
- COUNTY07: County or council area
- EZ_DESC_07: Countryside Survey Environmental Zone description

## Measurement scope and units
- LOI: percentage
- C_CONC_LOI: g/kg (carbon concentration)
- C_STOCK_LOI: t/ha (carbon stock)
- N_PERCENT: percentage nitrogen
- PO4_OLSEN: mg/kg (Olsen phosphorus)

## Methods and data processing
- Loss-on-ignition (LOI) methods
  - Samples: top 15 cm soil, up to 256 1km squares
  - Procedure: 10 g soil, dried, combusted (550°C, 3 h) after 375°C drying; LOI% calculated
  - Carbon conversion: used conversion factor 0.55x LOI to estimate soil carbon concentration; previously 0.50 used, now 0.55 for CS estimates

- Soil pH methods
  - Measured in deionised water suspension
  - Soil-to-water ratio: 1:2 (by weight; 50 ml soil to 25 ml water)
  - Procedure: mix, stand 30 minutes, read pH after 30 seconds
  - Location: ITE Merlewood

- Total nitrogen methods
  - Up to 1280 samples
  - Instrument: Elementar Vario-EL elemental analyser
  - Principle: oxidative combustion with detection of CO2 and N2
  - Sample weights: typically 15 mg for peat, 15–60 mg for mineral soils
  - Quality control: two in-house reference materials per batch

- Olsen phosphorus methods
  - Up to 1280 cores
  - Extraction: 5 g air-dried, sieved soil with 100 ml 0.5 M NaHCO3 (pH 8.5)
  - Detection: colorimetric molybdenum blue at 880 nm with dialysis step
  - Instrument: Skalar continuous flow analyser
  - Quality control: two in-house reference materials per batch

## Classification and metadata
- LC07 and LC07_NUM provide ITE Land Classification 2007
- COUNTRY, COUNTY07, EZ_DESC_07 provide geographic and environmental zoning context

## Usage rights and acknowledgments
- All use of Countryside Survey data must be acknowledged
- Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
- Copyright: Countryside Survey © NERC Centre for Ecology & Hydrology

## References and related publications
- Key sources and links for methodologies and context, including:
  - Allen (1989) soil pH method reference
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Bunce et al. (1996, 1981, 2007) ITE Land Classification of Great Britain
  - MASQ and related soil quality studies
  - Countryside Survey project website and associated documentation