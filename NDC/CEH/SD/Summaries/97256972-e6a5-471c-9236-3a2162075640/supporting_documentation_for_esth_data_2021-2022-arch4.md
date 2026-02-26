# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2021 -2022

## What is this dataset?
- Part of an ongoing long-term monitoring effort at Esthwaite Tarn, Cumbria, England.
- Fortnightly sampling from January 2021 to end of 2022.
- Data downloadable include: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), phytoplankton chlorophyll a (TOCA, µg per L).

## Data collection and sampling regime
- Water samples integrated from 0 to 5 m depth.
- Measurements taken from a boat at the buoy located at the deepest part of the lake; if not possible, samples from the shore were collected.
- When sampling could not access buoy, samples taken from shore; some occasions did not include 0–5 m integration (Flag 2).

## Temporal and location details
- Timeframe: January 2021 – end of 2022.
- Location: Esthwaite Tarn, Cumbria, England.

## Data structure and format
- Delivered as comma separated values (CSV).
- Columns include:
  - Date
  - Variable (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value
  - Sign(if<LOD): indicates values below detection limit (uses a “<” symbol)
  - Flag: 1 = sample collected at buoy; 2 = shore sample

## Quality control and limitations
- Data are raw and not yet quality controlled or calibrated.
- Double entered and visually checked.
- Missing data attributed to weather, lake access restrictions, COVID-19 restrictions, or staff shortages.
- Users should account for detection limits (Sign<LOD) and forthcoming calibration/quality control steps.

## Metadata, provenance, and funding
- Part of long-term Esthwaite Tarn monitoring program.
- Data collection funded by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE) as part of National Capability.
- Data validation funded by NERC award NE/Y006208/1 (ACCESS-UK) as part of National Capability.

## Implications for data strategy and stewardship (for Data Leaders)
- Demonstrates a structured, multi-parameter aquatic dataset with clear variable definitions and units, suitable for trend analyses once QC is applied.
- Key data governance needs include completing quality control/calibration, documenting detection limits, and maintaining metadata for discoverability.
- Data gaps exist due to access and external factors; plan for gap handling and transparent provenance.
- Consider establishing standardized QC workflows, versioning, and metadata enrichment (sampling location, depth, method notes) to enhance reuse across networks and partners.