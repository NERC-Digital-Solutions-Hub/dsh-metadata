# Metadata and methods for the dataset: Hydrometric data and stable isotope data for streamflow and rainfall in the Marolaona catchment, Madagascar, 2015-2016

## Overview
- Provides hydrometric data and stable isotope measurements for the Marolaona catchment in Madagascar (2015–2016).
- Data cover rainfall, streamflow, perched groundwater, soil moisture, and stable isotopes (δ18O, δ2H, and deuterium excess) from multiple plots and locations.
- Two main CSV datasets: HydrometricData_Marolaona.csv and IsotopeData_Marolaona.csv, with accompanying methodological details and references.

## Study area and period
- Location: Marolaona catchment, 31.7 ha, Ankeniheny Zahamena Corridor, Eastern Madagascar (approx. 18.970°S, 48.422°E).
- Measurement period: February 3, 2015 to March 3, 2016 (rainfall and hydrometric data; isotopes sampled during the same overall period with multiple campaigns).

## Data collected
- Hydrometric data
  - Rainfall: two tipping-bucket gauges (downstream and upstream) with HOBO loggers; data at 5-minute intervals; one upstream period data gap due to battery failure (July 1–Aug 17, 2015).
  - Streamflow: water levels behind two weirs (downstream catchment 31.7 ha; upper sub-catchment 7.11 ha); rating curves established; data for two measurement periods affected by sensor failures.
  - Soil moisture: volumetric soil moisture at three hillslopes (TF2, EUC, TSF) at depths 5 cm, 15 cm, and 30 cm with Decagon sensors; data logged at 1-minute intervals and averaged to 5-minute values.
  - Perched groundwater: fully screened wells at multiple sites (TF1, TF2, EUC, TSF) at ~0.30 m depth; water levels recorded at 1-minute or 5-minute intervals depending on site and sensor.
- Isotope data
  - Water samples from streamflow (upstream of weirs) and overland flow (TF2, EUC, TSF plots); samples collected before, during, and after rainfall events.
  - Rainfall samples collected in Jan–Feb 2016; daily bulk samples and event-based sequential samples.
  - Isotopes analyzed for δ18O and δ2H using a CRDS (Picarro L2130-i); precision: ±0.16‰ for δ18O, ±0.6‰ for δ2H; results expressed relative to Vienna Standard Mean Ocean Water (VSMOW).

## Measurement methods and instruments
- Rainfall: tipping-bucket rain gauges (Rain Collector II, Davis) with HOBO loggers; data converted to 5-minute intervals; ground-splash avoidance via installation height.
- Streamflow: weirs with water level sensors (Decagon CTD-10, STS DL/N 70, or STS DL/N 70 sensors) and salt-dilution slug-injection method for rating curves.
- Soil moisture: Decagon ECHO-EC-TM and ECHO-TM-5 sensors; measurements at multiple depths; hourly to 1-minute logging with 5-minute averages.
- Perched groundwater: fully screened wells with CTD-10 sensors or Keller DCX-18 sensors; data logged at 1-minute or 5-minute intervals.
- Isotopes: water samples analyzed by CRDS (L2130-i, Picarro) at Freiburg; delta notation (δ18O, δ2H); DEx computed from isotope ratios.

## Data structure and formats
- HydrometricData_Marolaona.csv
  - Columns include: Datetime; rainfall at downstream and upstream gauges (P down_a, P down_i, P up_a, P up_i); streamflow at downstream and upstream weirs (Q down_q, Q down_i, Q up_q, Q up_i); perched water tables (PWT_...) for TF2, EUC, TSF, and soil moisture plus temperature at 5 cm, 15 cm, and 30 cm depths for TF2, EUC, TSF; and similar PWT and SMC/Temp columns for TF1.
  - Temporal resolution: 5-minute intervals; missing data indicated as NaN.
- IsotopeData_Marolaona.csv
  - Columns: Location; Water_type (rainfall, streamflow, or plot runoff/overland flow); DateTime; Delta18O; Delta2H; DEx.
  - Date/time in local time; isotope values in ‰ relative to VSMOW.

## Data quality, gaps and governance
- Data quality considerations
  - High-frequency measurements (5-minute to minute-scale) enabling detailed hydrological analysis.
  - Clear documentation of measurement methods, instrument types, depths, and locations.
  - Isotopic data with explicit precision and standardization approach (VSMOW).
- Gaps and limitations
  - Upstream rainfall data gap due to battery failure (July 1–Aug 17, 2015).
  - Stream level data limited to two periods due to sensor failure; rating curves established under certain conditions.
  - Perched groundwater and soil moisture data constrained by site selection and deployment specifics.
- Data governance and sharing
  - Metadata emphasizes data provenance, measurement standards, and the need to ensure openness and data management at the source.
  - Underlying data are publicly described and referenced to prior work (Zwartendijk et al. 2020, 2023); data sharing may require attention to metadata completeness and data stewardship standards.

## References
- Zwartendijk et al. (2020). Soil water- and overland flow dynamics in a tropical catchment subject to long-term slash-and-burn agriculture. Journal of Hydrology.
- Zwartendijk et al. (2023). Rainfall-Runoff Responses and Hillslope Moisture Thresholds for an Upland Tropical Catchment in Eastern Madagascar Subject to Long-Term Slash-and-Burn Practices. Hydrological Processes.
- Background methods and calibration references for rainfall, weirs, salt-dilution, soil moisture sensors, isotopic analysis, and DEM/topographic data cited in the document.