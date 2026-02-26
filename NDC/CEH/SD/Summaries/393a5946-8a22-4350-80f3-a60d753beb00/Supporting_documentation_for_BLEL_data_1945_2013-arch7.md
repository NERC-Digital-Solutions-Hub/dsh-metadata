# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 1945 to 2013

## Overview
- Long-term monitoring dataset covering 1945–2013 for Blelham Tarn, Cumbria, England.
- Variables include surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Sampling frequency ranges from weekly to fortnightly; water samples are integrated from 0 to 5 m.

## Data Provenance and Scope
- Collected by the Freshwater Biological Association initially; since 1989, CEH and its predecessor Institute of Freshwater Ecology have continued collection.
- Data available to download as raw data (not yet quality controlled or calibrated), with visual checks performed.
- Covers April 1945 to end of 2013; missing data occurred March–July 2001 due to foot-and-mouth disease restrictions.

## Sampling Regime and Methods
- Water samples collected from a boat at a marked buoy location at the deepest part of the lake; when access to the buoy was not possible, samples were taken from the shore.
- Sampling location flag: Flag 1 = buoy sample; Flag 2 = shore sample.
- 0–5 m integrated water samples; sample collection details and handling follow long-term monitoring protocols.

## Data Structure and Content
- Data provided as a comma-separated values (CSV) file with the following columns:
  - sdate: date of measurement
  - variable, Description: each measured parameter (TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - value, Description: measurement values (units noted below)
  - sign_if_LT_LOD, Description: indicates if values are below detection limit (a < sign)
  - flag, Description: sampling location indicator (1 = buoy, 2 = shore)
- Variable units:
  - TEMP: degree Celsius
  - OXYG: % air-saturation
  - SECC: metres
  - ALKA: µg CaCO3 per litre
  - PH: pH
  - NH4N, NO3N, PO4P, TOTP, SIO2, TOCA: µg per litre (N or P or Si as specified)
- Water chemistry values are based on samples integrated from 0 to 5 m.

## Data Quality, Limitations, and Preparation for GIS
- Raw data are not yet quality controlled or calibrated; some validation performed visually.
- Potential data gaps and variability due to sampling method (buoy vs shore) and historical recording practices.
- Notable data gap: March–July 2001.
- For GIS use, consider linking by sdate and sampling location (buoy vs shore); may require coordinate assignment for the buoy and shore sampling points and handling below-detection-limit values.

## Access and Usage Notes for GIS Specialists
- Data are suitable for map-based data products and time-series visualisations in GIS.
- May require preprocessing:
  - Align dates and, if needed, interpolate or aggregate to consistent temporal resolution.
  - Attach spatial coordinates for buoy location and shore sampling sites.
  - Flag handling for values below detection limits (sign_if_LT_LOD) during visualization.

## References / Publications Using the Dataset
- Bernhardt, J.; Elliott, J.A.; Jones, I.D. (2008). Modelling the effects on phytoplankton communities of changing mixed depth and background extinction coefficient on three contrasting lakes in the English Lake District. Freshwater Biology 53:2573-2586.
- Feuchtmayr, H.; Thackeray, S.J.; Jones, I.D.; De Ville, M.; Fletcher, J.; James, J.B.; Kelly, J. (2012). Spring phytoplankton phenology - are patterns and drivers of change consistent among lakes in the same climatological region? Freshwater Biology 57:331-344.
- Foley, B.; Jones, I.D.; Maberly, S.C.; Rippey, B. (2012). Long-term changes in oxygen depletion in a small temperate lake: effects of climate change and eutrophication. Freshwater Biology 57:278-289.
- Maberly, S.C.; Barker, P.A.; Stott, A.W.; De Ville, M.M. (2013). Catchment productivity controls CO2 emissions from lakes. Nature Climate Change 3:391-394.
- Wang, B.; Liu, C.-Q.; Maberly, S.C.; Wang, F.; Hartmann, J. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports 6:35832.
- Woolway, R.I. et al. (2016). Lake surface temperatures [in 'State of the Climate in 2015']. Bulletin of the American Meteorological Society 97(8), S17-S18.