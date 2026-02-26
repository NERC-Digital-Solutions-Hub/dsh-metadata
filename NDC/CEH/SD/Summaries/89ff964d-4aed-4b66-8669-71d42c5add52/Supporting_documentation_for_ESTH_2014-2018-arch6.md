# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 2014 to 2018. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., James, J.B., Mackay, E.B., Pereira, M.G., Rhodes, G., Thackeray, S.J., Maberly, S.C. (2021)

## Overview
- Long-term, fortnightly monitoring dataset from Esthwaite Water, Cumbria, England (2014–2018).
- Variables recorded: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 L⁻¹), pH, ammonium (NH4N, µg N L⁻¹), nitrate (NO3N, µg N L⁻¹), soluble reactive phosphate (PO4P, µg P L⁻¹), total phosphorus (TOTP, µg P L⁻¹), dissolved reactive silicon (SIO2, µg L⁻¹), and phytoplankton chlorophyll a (TOCA, µg L⁻¹).
- Water samples integrated from 0–5 m; measurements from the lake’s deepest buoy location. If buoy access is not possible, samples taken near shore along with surface temperature and oxygen.
- Data span January 2014–end of 2018.

## Sampling regime and collection methods
- Part of a long-term monitoring effort; sampling frequency is fortnightly.
- Sampling method: boat-based at a marked buoy location; when unavailable, shore-based sampling used.
- Variables and units are explicitly defined in the data description.

## Quality control and data status
- Data are raw and have not been quality controlled or calibrated.
- Double entered and visually checked.
- Missing data largely due to weather conditions or staff shortages.

## Data structure and format
- Data delivered as a comma-separated values (CSV) file.
- Columns include:
  - Date: measurement date.
  - Variable: one of TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA.
  - Value: measured value for each variable.
  - Sign (if<LOD): indicates values below detection limit with a < sign.
  - Flag: 1 if sample taken at buoy location; 2 if sample taken near shore (no buoy access).

## Variables and measurement details
- TEMP: surface temperature (°C)
- OXYG: surface oxygen saturation (% air-saturation)
- SECC: Secchi depth (m)
- ALKA: alkalinity (µg CaCO3 L⁻¹)
- pH: acidity/alkalinity indicator
- NH4N: ammonium (µg N L⁻¹)
- NO3N: nitrate (µg N L⁻¹)
- PO4P: soluble reactive phosphate (µg P L⁻¹)
- TOTP: total phosphorus (µg P L⁻¹)
- SIO2: dissolved reactive silicon (µg L⁻¹)
- TOCA: phytoplankton chlorophyll a (µg L⁻¹)

## Availability and examples of use
- Funded and maintained as part of a broader research program.
- Recent publications using the dataset include:
  - Pilotto et al. (2020) Nature Communications – meta-analysis of multidecadal biodiversity trends in Europe.
  - Wang et al. (2016) Scientific Reports – coupling of carbon and silicon geochemical cycles in rivers and lakes.
  - Woolway et al. (2016) Bulletin of the American Meteorological Society – lake surface temperatures (state of the climate in 2015).
- An overview reference: Maberly et al. (2017) on long-term ecological research in the English Lake District.

## Funding and governance
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.

## Relevance for data support and usage
- Provides a multi-parameter, time-series dataset suitable for dashboards, self-serve analysis, and cross-variable exploration.
- Clear guidance on data provenance, sampling methods, and limitations aiding quality assurance, data cleaning, and integration with other datasets.
- Useful for developing data products (e.g., dashboards, reports) and for promoting data reuse and broader dissemination to end users.
- Considerations for data support work:
  - Address raw data status by planning quality control and calibration steps.
  - Manage two sampling contexts (buoy vs shore) via the Flag variable for geolocation context.
  - Handle detection-limit indicators (<LOD) in analysis and reporting.