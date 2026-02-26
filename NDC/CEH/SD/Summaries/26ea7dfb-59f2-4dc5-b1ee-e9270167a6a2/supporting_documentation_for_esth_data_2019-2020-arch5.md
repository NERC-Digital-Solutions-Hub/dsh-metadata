# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2019  2020.

## Overview
- Long-term monitoring dataset from Esthwaite Tarn (Cumbria, England) with fortnightly sampling.
- Includes surface temperature, surface oxygen saturation, Secchi depth, water chemistry (alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon) and phytoplankton chlorophyll a.
- Data cover January 2019 to end of 2020.

## Sampling regime and collection methods
- Measurements taken from a boat at the buoy location (Latitude 54.364, Longitude -2.988) at the deepest part of the lake; when not possible, samples collected from the shore.
- Water samples are integrated from 0 to 5 meters.
- Sampling frequency: fortnightly.
- When buoy sampling was not feasible, shore sampling is indicated (Flag 2).
- Variables and approximate units (as described in the dataset): TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg/L as CaCO3), pH, NH4N (µg/L), NO3N (µg/L), PO4P (µg/L), TOTP (µg/L), SIO2 (µg/L), TOCA (µg/L). Below detection limits are marked with a < sign.

## Quality control and data provenance
- Data presented are raw and have not undergone full quality control or calibration yet.
- Data have been double entered and visually checked.
- Missing data largely due to weather, lake access restrictions, COVID-19 restrictions, or staff shortages.

## Data structure and metadata
- Data are provided in a CSV file with columns including Date, Variable, Description, Value, Sign (for <LOD), and Flag (1 = buoy sampling, 2 = shore sampling).
- Variables explicitly include surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon, and phytoplankton chlorophyll a.
- Integrated from 0–5 m; sampling location and method are recorded via flags for transparency and reproducibility.

## Availability and reuse considerations for data stewards
- The dataset is prepared for sharing but requires standardization and QC before release into production data portals.
- Documentation notes the need to respect sampling method differences (buoy vs shore) and detection-limit indicators (<LOD).
- Metadata should capture sampling regime, location coordinates, depth integration, units, and data quality status.

## Funding and governance
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of UK-SCAPE National Capability.
- Data validation supported by NERC award NE/Y006208/1 as part of the ACCESS-UK programme delivering National Capability.