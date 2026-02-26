# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2021 to 2022

## Overview
- Long-term monitoring dataset for surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Fortnightly sampling at Blelham Tarn, Cumbria, England.
- Timeframe: January 2021 to end of 2022.
- Data intended for download; raw and not yet fully quality controlled.

## Sampling regime and data collection methods
- Water samples integrated from 0 to 5 meters; measurements taken from a boat at the buoy located at the deepest lake point.
- When buoy access was unavailable, samples collected from shore alongside surface temperature and oxygen measurements.
- Measurements and units:
  - TEMP: temperature in °C
  - OXYG: oxygen saturation in % air-saturation
  - SECC: Secchi depth in metres
  - ALKA: alkalinity in µg CaCO3 per litre
  - pH: pH
  - NH4N: ammonium in µg N per litre
  - NO3N: nitrate in µg N per litre
  - PO4P: soluble reactive phosphate in µg P per litre
  - TOTP: total phosphorus in µg P per litre
  - SIO2: dissolved reactive silicon in µg per litre
  - TOCA: phytoplankton chlorophyll a in µg per litre

## Data quality and validation
- Data are raw and not yet quality controlled or calibrated.
- Double entered and visually checked; missing data attributed to weather, COVID-19 restrictions, or staff shortages.

## Data structure and metadata
- Format: comma-separated values (CSV).
- Key columns:
  - Date: measurement date
  - Variable, Description: variable name and description (e.g., TEMP, TEMP description)
  - Value, Description: measurement value and descriptor
  - Sign(if<LOD), Description: indicates if value is below detection limit (a "<" sign)
  - Flag, Description: 1 = sample taken at buoy location; 2 = sample taken from shore when buoy access was not possible

## Access, usage and applicability for data strategy
- Data are available for download (raw form; not yet QC’ed), enabling early integration into data systems and pipelines.
- Critical for understanding data provenance, lineage, and limitations (raw status, detection limits, sampling regime).
- Highlights need for downstream steps: formal quality control/calibration, metadata enrichment, and standardization to improve discoverability and interoperability.

## Funding and ownership
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE, delivering National Capability).
- Data validation supported by NERC award NE/Y006208/1 (ACCESS-UK, delivering National Capability).