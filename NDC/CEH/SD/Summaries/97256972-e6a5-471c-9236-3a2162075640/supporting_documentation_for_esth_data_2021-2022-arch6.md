# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2021 -2022.

- Overview
  - Long-term monitoring dataset from Esthwaite Tarn, Cumbria, England, with fortnightly sampling from January 2021 to the end of 2022.
  - Variables included: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N/L), nitrate (NO3N, µg N/L), soluble reactive phosphate (PO4P, µg P/L), total phosphorus (TOTP, µg P/L), dissolved reactive silicon (SIO2, µg/L), and phytoplankton chlorophyll a (TOCA, µg/L).
  - Water samples are integrated from 0 to 5 m; measurements are taken from a boat at the deepest part buoy, with shore sampling when buoy access was not possible.

- Sampling regime and collection methods
  - Fortnightly sampling as part of an ongoing long-term monitoring programme.
  - Data represent a comprehensive set of surface water properties and phytoplankton chlorophyll a over the 2021–2022 period.
  - When buoy sampling was not possible, samples were collected from the shore (Flag 2).

- Data available and structure
  - Variables and units:
    - TEMP: surface temperature, °C
    - OXYG: surface oxygen saturation, % air-saturation
    - SECC: Secchi depth, m
    - ALKA: alkalinity, µg CaCO3 per L
    - pH: pH units
    - NH4N: ammonium, µg N per L
    - NO3N: nitrate, µg N per L
    - PO4P: soluble reactive phosphate, µg P per L
    - TOTP: total phosphorus, µg P per L
    - SIO2: dissolved reactive silicon, µg per L
    - TOCA: phytoplankton chlorophyll a, µg per L
  - Data format:
    - CSV file with columns: Date, Variable, Value, Sign(if<LOD), Flag
    - Sign(if<LOD): indicates values below detection limit with a < symbol
    - Flag: 1 = sample collected at buoy location; 2 = sample collected from shore due to buoy unavailability
  - Variable descriptions and value-field descriptions are included as mappings within the dataset (Variable, Description; Value, Description; Sign(if<LOD), Description; Flag, Description).

- Data quality and caveats
  - The dataset comprises raw data that have not yet undergone quality control or calibration.
  - Data have been double-entered and visually checked.
  - Missing data reasons include weather conditions, lake access restrictions, COVID-19 restrictions, or staff shortages.

- Timeframe
  - January 2021 through the end of 2022.

- Availability and governance
  - Data are available to download as part of the ongoing monitoring effort.
  - Funding:
    - Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.
    - Data validation supported by NERC award NE/Y006208/1 as part of the ACCESS-UK programme delivering National Capability.