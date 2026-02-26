# Metadata and methods for the dataset: Hydrometric data and stable isotope data for streamflow and rainfall in the Marolaona catchment, Madagascar, 2015-2016

## Overview
- Datasets describe hydrometric measurements and stable isotopes in the Marolaona catchment, Madagascar, spanning February 3, 2015 to March 3, 2016.
- Measurements cover rainfall, streamflow, perched groundwater, soil moisture, soil temperature, and isotopic signatures (δ18O, δ2H, deuterium excess) to support rainfall–runoff and hydrological investigations.

## Study Area
- 31.7 ha catchment within the Ankeniheny Zahamena Corridor on the Eastern escarpment of Madagascar (approx. 18.970°S, 48.422°E).
- Measurements at two rainfall gauges, multiple weirs, perched water tables at several sites, and soil moisture/temperature at three hillslope plots.
- Isotope sampling includes streamflow (upstream of weirs) and overland flow from plots TF2, EUC, and TSF.

## Data Collection Timeline and Variables
- Timeframe: 2015-2016 with 5-minute resolution data for the entire period.
- Hydrometric data components:
  - Rainfall: two tipping-bucket gauges (downstream and upstream); some data loss at upstream gauge July 1–Aug 17, 2015 due to battery failure.
  - Streamflow: two weirs (outlet 31.7 ha; upper catchment 7.11 ha); limited data due to sensor failures; rating curves established using salt-dilution methods.
  - Perched groundwater: measurements at several sites (TF1, TF2, EUC, TSF) with depths to the low-permeability layer.
  - Soil moisture and temperature: three plots (TF2, EUC, TSF) at depths 5, 15, 30 cm; high-frequency measurements (minute-level, aggregated to 5-minute).
- Data completeness: missing values denoted NaN; some periods have limited streamflow data due to equipment issues.

## Measurement Methods and Instruments
- Rainfall: Rain Collector II tipping-bucket gauges (0.2 mm per tip; ±4%–5% accuracy depending on intensity), connected to HOBO loggers; gauges installed about 1.2 m above soil.
- Streamflow: Weirs measured water level at 5-minute intervals; upper catchment weir modified to a 90° V-notch; rating curves based on weir theory and salt-dilution slug injections; data supplemented by bucket checks.
- Soil moisture and temperature: Decagon ECHO-EC-TM sensors (5 cm and 15 cm depths) and ECHO-TM-5 sensors (30 cm); accuracy ≈ ±3%, 0.1% resolution; sensors installed upslope from measurement boundaries.
- Perched groundwater: fully screened wells at 0.30 m depth; water levels measured with Decagon CTD-10 or Keller DCX-18 sensors; data logged at 5-minute or 1-minute intervals depending on site.
- Isotope sampling and analysis: water samples from streamflow and overland flow; rainfall samples collected with daily bulk sampling and a sequential rainfall sampler; δ18O and δ2H measured by Cavity Ring-Down Spectroscopy (CRDS, L2130-i, Picarro) at Freiburg; results referenced to VSMOW with stated precisions (δ18O ±0.16‰, δ2H ±0.6‰); deuterium-excess (DEx) calculated.

## Data Files and Structure
- HydrometricData_Marolaona.csv
  - 5-minute interval records for Feb 3, 2015–Mar 3, 2016.
  - Columns include: Datetime; downstream/upstream rainfall amounts and intensities (P_down_a, P_down_i, P_up_a, P_up_i); downstream/upstream discharge metrics (Q_down_q, Q_down_i, Q_up_q, Q_up_i); perched water table measurements (PWT_* for TF2, EUC, TSF, TF1); soil moisture contents and temperatures at TF2, EUC, TSF (5/15/30 cm); and corresponding water table depths/ depths-related fields.
- IsotopeData_Marolaona.csv
  - Records of isotopic samples with columns: Location, Water_type (rainfall, streamflow, plot runoff/overland flow), DateTime, Delta18O, Delta2H, DEx.

- Table references in the document describe the exact column contents and units for both HydrometricData and IsotopeData files.

## Isotope Data Details
- Sampling scope:
  - Rainfall: 39 samples (26 sequential sampler, 13 bulk).
  - Streamflow: 209 samples (173 at downstream catchment outlet, 36 at upper sub-catchment).
  - Overland flow: 31 samples (TF1, TF2, TSF, EUC across plots).
- Analysis: isotopes measured with CRDS; results reported relative to Vienna Standard Mean Ocean Water (VSMOW); precision: δ18O ±0.16‰; δ2H ±0.6‰; DEx derived from δ18O and δ2H.
- Sample timing: during and after rainfall events, with daily rainfall samples during January–February 2016 (wet season) at plot TF2.

## Data Quality, Gaps, and Considerations for Analysts
- Data gaps due to equipment/battery failures (notably upstream rainfall data missing July–August 2015; limited streamflow data periods due to sensor issues).
- Measurements provide high-temporal-resolution insight into rainfall–runoff processes, groundwater dynamics, soil moisture kinetics, and isotopic tracing.
- Scale considerations: perched water tables and soils measured at selected plots; isotopic data enable hydrograph separation and source attribution, but spatial extrapolation should consider plot locations and catchment heterogeneity.
- Referenced context and methods are expanded in Zwartendijk et al. (2020, 2023) and related supplementary materials for rating curves and methodological details.

## References
- Zwartendijk et al. 2020; Zwartendijk et al. 2023; and supporting methodological sources cited within the document for rating curves, salt-dilution gauging, and isotope analysis.