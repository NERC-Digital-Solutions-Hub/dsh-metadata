# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 1990 to 2013.

## Overview
- Long-term fortnightly monitoring dataset from Derwent Water, Cumbria, England, covering August 1990 to the end of 2013.
- Measured variables (with units): 
  - TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3 per L), pH (PH), NH4N (µg N per L), NO3N (µg N per L), PO4P (µg P per L), TOTP (µg P per L), SIO2 (µg per L), TOCA (µg per L).
- Water samples integrated from 0 to 5 m; collected from a boat at a buoy (deepest part) or from shore if the buoy was inaccessible.
- Data format provided for download as CSV with clearly described columns.

## Sampling regime and collection methods
- Fortnightly sampling regime.
- Location and method:
  - Primary: boat-based sampling at the buoy (deepest part of the lake).
  - Secondary: shore sampling when buoy access was not possible.
  - Integrated depth: 0–5 m.
- Data fields include Date, Variable (with description), Value (measurement), Sign_if_LT_LOD (below detection limit indicator), and Flag (1 = buoy sample, 2 = shore sample).

## Quality control and limitations
- Data are raw and not yet quality controlled or fully calibrated (except double entries from 2005 onwards); visually checked.
- Missing periods:
  - March–June 2001: foot-and-mouth disease restricted lake access.
  - 2009: weather-related data gaps.
- Detection-limit issues noted via Sign_if_LT_LOD indicators.

## Data structure and access
- File format: comma-separated values (CSV).
- Columns (descriptions): Date; Variable; Description (variable description); Value; Description (value description); Sign_if_LT_LOD; Description (LOD flag); Flag; Description (sample location flag).
- Variables and units listed above; data include indicators for measurements below detection limits and sample origin flags.

## Notable publications using the dataset
- George et al. (2007). The impact of climate change on the physical characteristics of the larger lakes in the English Lake District. Freshwater Biology.
- Maberly et al. (2013). Catchment productivity controls CO2 emissions from lakes. Nature Climate Change.
- Winfield et al. (multiple works, 2006–2017). Fisheries, vendace, and lake ecology in the English Lake District.
- Woolway et al. (2016). Lake surface temperatures (State of the Climate in 2015). Bulletin of the American Meteorological Society.

## Potential uses for analysis
- Analyze long-term trends and correlations among physical, chemical, and biological markers (temperature, oxygen, pH, nutrients, and chlorophyll a).
- Assess responses to climatic events or changes in catchment productivity.
- Model relationships between nutrient status and phytoplankton (TOCA) while accounting for sampling method and detection limits.
- Consider data gaps and raw-data limitations when building predictive models or conducting local-scale assessments.