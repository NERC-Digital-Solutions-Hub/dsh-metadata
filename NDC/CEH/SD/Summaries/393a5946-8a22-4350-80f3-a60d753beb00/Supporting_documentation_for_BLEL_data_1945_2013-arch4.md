# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 1945 to 2013

## Overview
- Long-term monitoring dataset covering surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH (PH), ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA) from 1945 to 2013.
- Weekly to fortnightly sampling regime; some variables begin earlier than others.
- Data primarily collected by the Freshwater Biological Association and, since 1989, CEH and its predecessor Institute of Freshwater Ecology.

## Sampling regime and collection methods
- Sampling location: from a boat at a marked buoy at the deepest part of Blelham Tarn; when unavailable, shore samples were taken (Flag 2).
- Water samples: integrated from 0 to 5 m when possible; otherwise not integrated if buoy sampling was not feasible.
- Variables and units available for download: TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3 per L), PH, NH4N (µg N per L), NO3N (µg N per L), PO4P (µg P per L), TOTP (µg P per L), SIO2 (µg SiO2 per L), TOCA (µg per L).

## Quality control and data status
- Data are raw and have not been quality controlled or calibrated (except for double entries from 2005 onward).
- Visual checks have been performed; data quality varies.
- Notable gap: March–July 2001 missing due to an outbreak of foot-and-mouth disease restricting lake access.

## Data structure and metadata
- Data format: comma-separated values (CSV) file.
- Key columns:
  - sdate: Date of measurement.
  - variable: Description of the measured parameter (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - value: Measured value for each variable.
  - sign_if_LT_LOD: Indicator if value is below detection limit (a "<" sign).
  - flag: Sampling location indicator (1 = buoy, 2 = shore when buoy sampling was not possible).
- Water chemistry values are reported as concentrations in their respective units; samples are typically from 0–5 m depth.

## Notable publications using the dataset
- Bernhardt J., Elliott, J.A. & Jones, I.D. (2008). Modelling the effects on phytoplankton communities of changing mixed depth and background extinction coefficient on three contrasting lakes in the English Lake District. Freshwater Biology 53, 2573-2586.
- Feuchtmayr, H., et al. (2012). Spring phytoplankton phenology - are patterns and drivers of change consistent among lakes in the same climatological region? Freshwater Biology 57, 331-344.
- Foley, B., et al. (2012). Long-term changes in oxygen depletion in a small temperate lake: effects of climate change and eutrophication. Freshwater Biology 57, 278-289.
- Maberly, S.C., et al. (2013). Catchment productivity controls CO2 emissions from lakes. Nature Climate Change 3, 391-394.
- Wang, B., et al. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports 6, 35832.
- Woolway, R.I., et al. (2016). Lake surface temperatures [in State of the Climate in 2015]. Bulletin of the American Meteorological Society 97(8), S17-S18.

## Implications for data leadership and management
- Data provenance and stewardship: dataset has a long establishment history with CEH; clear custodianship and evolution over time.
- Data quality management: raw status necessitates development of QC/calibration pipelines and metadata improvements to enable robust downstream analyses.
- Metadata and accessibility: documentation of detection limits (LOD) and flag meanings supports interpretability; ensure discoverability and user guidance for data re-use.
- Gap and limitation awareness: acknowledged data gaps (e.g., 2001 hiatus) and non-integrated samples require careful handling in analyses and trend assessments.
- Interoperability potential: uniform structure and clear variable definitions facilitate integration with other lake datasets and cross-site studies for broader ecological and climate research.