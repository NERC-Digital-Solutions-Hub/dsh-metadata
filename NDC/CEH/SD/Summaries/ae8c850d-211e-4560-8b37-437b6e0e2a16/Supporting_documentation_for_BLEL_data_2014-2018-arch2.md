# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2014 to 2018

## Summary
- Long-term fortnightly monitoring dataset (2014–2018) from Blelham Tarn, Cumbria, England, capturing surface temperature, oxygen saturation, water clarity, water chemistry, and phytoplankton chlorophyll a.
- Data serve as a standardized source for assessing environmental health and informing policy performance over time.

## What is collected
- Variables and units:
  - TEMP: surface temperature (°C)
  - OXYG: surface oxygen saturation (% air-saturation)
  - SECC: Secchi depth (m)
  - ALKA: alkalinity (µg CaCO3 per L)
  - pH: pH
  - NH4N: ammonium (µg N per L)
  - NO3N: nitrate (µg N per L)
  - PO4P: soluble reactive phosphate (µg P per L)
  - TOTP: total phosphorus (µg P per L)
  - SIO2: dissolved reactive silicon (µg SiO2 per L)
  - TOCA: phytoplankton chlorophyll a (µg per L)
- Water samples are integrated from 0–5 m; measurements taken from a buoy at the deepest lake location; shore sampling when buoy access is not possible.
- Data are provided as CSV with columns: Date, Variable/Description, Value/Description, Sign (if < LOD), Flag (sampling location indicator).

## Sampling regime
- Fortnightly sampling as part of ongoing long-term monitoring.
- Sampling period: January 2014 to end of 2018.
- Location: Blelham Tarn, Cumbria, England.

## Data structure and access
- Data format: CSV file with structured columns as described above.
- Flags:
  - Flag = 1: sample taken at the buoy location
  - Flag = 2: sample taken from the shore (buoy visit not possible)

## Quality control and limitations
- Data are raw and have not yet been quality controlled or calibrated.
- Data have been double entered and visually checked.
- Missing data arise from weather conditions or staff shortages.

## Context and usage
- The dataset supports environmental health assessments and policy performance monitoring through standardized outputs (e.g., time series, maps, charts).
- Recent publications citing the dataset:
  - Modelling lake cyanobacterial blooms: climate-driven impacts (Freshwater Biology, 2019)
  - Coupling of carbon and silicon geochemical cycles in rivers and lakes (Scientific Reports, 2016)
  - Lake surface temperatures in State of the Climate in 2015 (Bulletin of the American Meteorological Society, 2016)
- Overview reference: from Ecological Informatics to generation of ecological knowledge: long-term research in the English Lake District (Ecological Informatics, 2017)

## Funding
- Natural Environment Research Council award NE/R016429/1, part of the UK-SCaPE programme delivering National Capability.

## Relevance for analysts monitoring the environment
- Provides a standardized, time-series dataset suitable for trend analysis, quality assurance workflows, and integration with other environmental datasets.
- Supports reproducible reporting via clear data structure, explicit measurement methods, and documented limitations.
- Demonstrates practical use in informing lake ecosystem studies and broader environmental policy assessment.