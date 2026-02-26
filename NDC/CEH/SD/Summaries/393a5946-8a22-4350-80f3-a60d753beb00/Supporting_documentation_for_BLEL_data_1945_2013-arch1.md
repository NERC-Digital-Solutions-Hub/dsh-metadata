# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 1945 to 2013. Maberly, S.C., Brierley, B., Carter, H.T., Clarke, M.A., De Ville, M.M., Fletcher, J.M., James, J.B., Keenan, P., Kelly, J.L., Mackay, E.B., Parker, J.E., Patel, M., Pereira, M.G., Rhodes, G., Tanna, B., Thackeray, S.J., Vincent, C., Feuchtmayr, H. (2017)

## Overview
- Long-term monitoring dataset for multiple variables at Blelham Tarn, Cumbria, England.
- Variables include surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Sampling frequency ranges from weekly to fortnightly; data span from April 1945 to the end of 2013.
- Original collection by the Freshwater Biological Association; since 1989 by CEH and its predecessors.

## Sampling regime and collection methods
- Water samples are based on a 0–5 m integrated depth.
- Measurements taken from a boat at the deepest part of the lake (buoy location).
- If visiting the buoy was not possible, samples were taken from the shore (not integrated), flagged as Flag 2.
- Core variables and units:
  - TEMP: surface temperature in degrees Celsius
  - OXYG: surface oxygen saturation in % air-saturation
  - SECC: Secchi depth in metres
  - ALKA: alkalinity in µg CaCO3 per litre
  - PH: pH
  - NH4N: ammonium in µg N per litre
  - NO3N: nitrate in µg N per litre
  - PO4P: soluble reactive phosphate in µg P per litre
  - TOTP: total phosphorus in µg P per litre
  - SIO2: dissolved reactive silicon in µg per litre
  - TOCA: phytoplankton chlorophyll a in µg per litre

## Data structure and access
- Data delivered as a comma-separated values (CSV) file.
- Key columns:
  - sdate: date of measurement
  - variable/Description: name and description of the measured variable
  - value: measured value for each variable
  - sign_if_LT_LOD: indicates if value is below detection limit (a < sign)
  - flag: sampling location indicator (1 = buoy; 2 = shore)
- All data cover April 1945 to end of 2013.
- Measurements are raw and not quality controlled (except duplicate entries from 2005 onward); visual checks performed.

## Quality control, limitations, and caveats
- Data are raw and not fully calibrated or quality controlled.
- Visual checks were performed; formal QC/calibration is not indicated.
- Missing data occurred between March and July 2001 due to foot-and-mouth disease restricting access.
- Some samples were not integrated (shore samples) when buoy visits were not possible; flagged accordingly.
- Detection-limit signs and data gaps should be accounted for in analyses; data from shore versus buoy may introduce differences in integration when interpreting hydrological depth.

## Use for analysis
- Suitable for exploring long-term trends, correlations between physical, chemical, and biological parameters, and potential predictive modelling of lake responses to environmental drivers.
- Important to:
  - Handle <LOD values using sign_if_LT_LOD information.
  - Distinguish buoy-based integrated samples from shore-based non-integrated samples (Flag 1 vs Flag 2).
  - Consider the historical gap in 2001 and the raw nature of the data when interpreting results.
  - Be mindful of unit consistency across variables when integrating with other datasets.

## Related publications and context
- Recent example publications utilizing this dataset include:
  - Bernhardt, Elliott, & Jones (2008) – modelling phytoplankton responses to changing mixed depth and extinction coefficients in English lakes.
  - Feuchtmayr et al. (2012) – spring phytoplankton phenology across lakes in the same region.
  - Foley et al. (2012) – long-term oxygen depletion trends in temperate lakes related to climate change and eutrophication.
  - Maberly et al. (2013) – catchment productivity controls on lake CO2 emissions.
  - Wang et al. (2016) – coupling of carbon and silicon cycles in rivers and lakes.
  - Woolway et al. (2016) – Lake surface temperatures in State of the Climate reports.