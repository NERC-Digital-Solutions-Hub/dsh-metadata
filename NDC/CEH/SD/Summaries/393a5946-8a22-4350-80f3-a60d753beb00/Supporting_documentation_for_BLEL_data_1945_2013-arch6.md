# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 1945 to 2013

## Overview
- Long-term monitoring dataset from Blelham Tarn, Cumbria, England, with weekly to fortnightly sampling.
- Variables cover physical, chemical, and biological water properties: surface temperature (TEMP, °C); surface oxygen saturation (OXYG, % air-saturation); Secchi depth (SECC, m); alkalinity (ALKA, µg CaCO3 per L); pH (PH); ammonium (NH4N, µg N/L); nitrate (NO3N, µg N/L); soluble reactive phosphate (PO4P, µg P/L); total phosphorus (TOTP, µg P/L); dissolved reactive silicon (SIO2, µg/L); phytoplankton chlorophyll a (TOCA, µg/L).
- Data originally collected by the Freshwater Biological Association; CEH and predecessors have maintained since 1989.
- Data span: 1945–2013 (some variables began earlier; all data available up to end of 2013).

## Sampling regime and collection methods
- Sampling frequency: weekly to fortnightly.
- Water samples are integrated from 0 to 5 m; measurements taken from a boat at the deepest part of the lake (buoy location).
- If buoy sampling was not possible, samples were taken from the shore (Flag 2).
- Sampling location and methods documented for each record; some shore samples reflect unintegrated water when buoy access was not possible.

## Quality control and data limitations
- Data provided as raw, not yet quality controlled or calibrated (except double entries from 2005 onward).
- Visual checks performed; no formal calibration described.
- Data gaps: March–July 2001 with missing data due to foot-and-mouth disease restricting access.
- Values below detection limits are indicated with a < sign in sign_if_LT_LOD.

## Data structure and field definitions
- Data delivered as a comma separated values (CSV) file with columns:
  - sdate: date of measurement
  - variable: what is measured (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - value: measured value
  - sign_if_LT_LOD: indicates if the value is below detection limit (<)
  - flag: 1 = buoy location, 2 = shore sample (when buoy sampling was not possible)

## Using the data (data products and support)
- For analysis, treat as raw data: clean and calibrate if needed, handle < detections, and account for shore vs buoy sampling flags.
- Potential outputs include time-series graphs, dashboards, pivot-style summaries, and data extracts for end users to explore.
- Data can be integrated with related datasets or used to reproduce long-term trends in limnology, phytoplankton dynamics, and nutrient cycling.

## Publications using this dataset
- Bernhardt, J., Elliott, J.A. & Jones, I.D. (2008). Modelling the effects on phytoplankton communities of changing mixed depth and background extinction coefficient on three contrasting lakes in the English Lake District. Freshwater Biology, 53, 2573-2586.
- Feuchtmayr, H., Thackeray, S.J., Jones, I.D., De Ville, M., Fletcher, J., James, J.B. & Kelly, J. (2012). Spring phytoplankton phenology - are patterns and drivers of change consistent among lakes in the same climatological region? Freshwater Biology, 57, 331-344.
- Foley, B., Jones, I.D., Maberly, S.C. & Rippey, B. (2012). Long-term changes in oxygen depletion in a small temperate lake: effects of climate change and eutrophication. Freshwater Biology, 57, 278-289.
- Maberly, S.C., Barker, P.A., Stott, A.W. & De Ville, M.M. (2013). Catchment productivity controls CO2 emissions from lakes. Nature Climate Change, 3, 391-394.
- Wang, B., Liu, C.-Q., Maberly, S.C., Wang, F. & Hartmann, J. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports, 6, 35832.
- Woolway, R.I., Cinque, K., de Eyto, E., DeGasperi, C.L., Dokulil, M.T., Korhonen, J., Maberly, S.C., Marszelewski, W., May, L., Merchant, C.J., Paterson, A.M., Riffler, M., Rimmer, A., Rusak, J.A., Schladow, S.G., Schmid, M., Teubner, K., Verburg, P., Vigneswaran, B., Watanabe, S., & Weyhenmeyer, G.A. (2016). Lake surface temperatures [in 'State of the Climate in 2015']. Bulletin of the American Meteorological Society, 97(8), S17-S18.