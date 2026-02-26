# Metadata and methods for the dataset: Hydrometric data and stable isotope data for streamflow and rainfall in the Marolaona catchment, Madagascar, 2015-2016

## Overview
- Describes hydrometric and stable isotope data collected in the Marolaona catchment (31.7 ha) on the Eastern escarpment of Madagascar during 2015–2016.
- Data are provided in two CSV files: HydrometricData_Marolaona.csv and IsotopeData_Marolaona.csv, with missing values indicated as NaN.
- Measurements cover rainfall, streamflow, perched groundwater, soil moisture, and water isotope values (δ18O, δ2H, and deuterium excess).

## Study area and timeline
- Location: Marolaona catchment, Ankeniheny Zahamena Corridor, Eastern Madagascar (approx. 18.970°S, 48.422°E).
- Catchment details: 31.7 ha main catchment; additional upper sub-catchment area of 7.11 ha.
- Monitoring period: February 3, 2015 to March 3, 2016.

## Data collection framework
- Monitoring components:
  - Rainfall at two locations (downstream and upstream gauges).
  - Streamflow at downstream and upstream weirs.
  - Perched water tables at 10 locations.
  - Soil moisture at 3 hillslope sites (5 cm, 15 cm, 30 cm depth).
  - Perched groundwater wells at several sites ( TF1, TF2, EUC, TSF).
  - Isotope samples from streamflow and overland flow; rainfall samples during the wet season.
- Data resolution: Primarily 5-minute intervals for hydrometric data; daily rainfall samples and event-based isotope sampling.

## Rainfall measurement
- Instruments: Two tipping-bucket rain gauges (Rain Collector II, Davis) connected to HOBO Pendant loggers.
- Precision: 0.2 mm per tip; accuracy ±4% up to 50 mm/hr, ±5% up to 100 mm/hr.
- Installations: Downstream and upstream gauges positioned ~1.2 m above soil to minimize ground-splash effects.
- Data characteristics: 5-minute interval aggregation; a data gap occurred from July 1 to August 17, 2015 due to battery failure.
- Data reference: Rainfall columns in HydrometricData_Marolaona.csv include P down_a, P down_i, P up_a, P up_i.

## Streamflow and water level measurements
- Weirs: Suppressed broad-crested weirs at the catchment outlet (31.7 ha) and the upper catchment (7.11 ha).
- Rating curves: Upper catchment rating curve based on a truncated-triangular sharp-crested weir; lower catchment rated via salt-dilution-slug-injection method.
- Water level monitoring: Behind weirs at 5-minute intervals using Decagon CTD-10 sensors (Feb–May 2015) and STS DL/N 70 pressure sensors (Dec 2015–Mar 2016).
- Data coverage: Two measurement periods with partial data due to sensor failures (Feb 15–May 13, 2015 and Dec 12, 2015–Mar 3, 2016).
- Streamflow representations: Q down_q, Q down_i, Q up_q, Q up_i in HydrometricData_Marolaona.csv.

## Soil moisture and perched groundwater
- Soil moisture sensors: Decagon ECHO-EC-TM sensors (5 cm and 15 cm depths) and ECHO-TM-5 sensors (30 cm) at TF2, EUC, and TSF plots.
- Installation: Sensors oriented upslope; 5-minute averages stored in EM50 datalogger.
- Depths: Measurements at 5 cm, 15 cm, and 30 cm depths (SMC_TF2_5cm, SMC_TF2_15cm, SMC_TF2_30cm, etc.).
- Temperature readings: Corresponding soil temperatures logged (Temp_TF2_5cm, etc.).

## Perched groundwater (wells)
- Wells installed at TF1, EUC, TSF (0.30 m below surface) and TF2 near soil moisture plots.
- Water level monitoring: 1-minute (TF1, EUC, TSF) with auto pressure corrections; 5-minute averages at some EUC and TSF sites using Keller DCX-18 sensors.

## Isotope sampling and analysis
- Sample types: Streamflow (upstream of weirs) and overland flow from culverts/lines at TF2, EUC, TSF plots; rainfall samples during the wet season.
- Rainfall sampling: Daily bulk samples from TF2 rain gauge; additional samples collected every ~13 mm of rainfall during field campaigns.
- Sample counts: 39 rainfall samples; 209 streamflow samples (173 from downstream outlet, 36 from upper sub-catchment); 31 overland-flow samples (distributed across TF1, TF2, TSF, EUC).
- Isotope analysis: δ18O and δ2H measured by CRDS (L2130-i, Picarro) at the University of Freiburg.
- Isotope notation and precision: Values expressed relative to Vienna Standard Mean Ocean Water (VSMOW); precision ±0.16‰ for δ18O and ±0.6‰ for δ2H; DEx (deuterium excess) also reported.
- Data file: IsotopeData_Marolaona.csv with columns Location, Water_type, DateTime, Delta18O, Delta2H, DEx.

## Data files and contents
- HydrometricData_Marolaona.csv
  - Columns include: Datetime, P down_a, P down_i, P up_a, P up_i, Q down_q, Q down_i, Q up_q, Q up_i, PWT_TF2, SMC_TF2_5cm, Temp_TF2_5cm, SMC_TF2_15cm, Temp_TF2_15cm, SMC_TF2_30cm, Temp_TF2_30cm, PWT_EUC_down, PWT_EUC_mid, PWT_EUC_up, SMC_EUC_5cm, Temp_EUC_5cm, SMC_EUC_15cm, Temp_EUC_15cm, SMC_EUC_30cm, Temp_EUC_30cm, PWT_TSF_down, PWT_TSF_mid, PWT_TSF_up, SMC_TSF_5cm, Temp_TSF_5cm, SMC_TSF_15cm, Temp_TSF_15cm, PWT_TF1_down, PWT_TF1_mid, PWT_TF1_up.
  - Notes: 5-minute resolution; NaN indicates missing data; rainfall data includes both downstream and upstream gauges; perched water tables expressed relative to a low-permeability layer at 300 mm below the surface.
- IsotopeData_Marolaona.csv
  - Columns: Location, Water_type, DateTime, Delta18O, Delta2H, DEx.
  - Notes: Sample locations and water types include rainfall, streamflow, and plot runoff/overland flow; units in per mil (‰); DateTime in local time; isotope values relative to VSMOW.

## Quality, limitations, and context
- Data gaps and sensor issues:
  - Rainfall gauge data gap due to battery failure (Jul 1–Aug 17, 2015).
  - Limited continuous streamflow data periods due to sensor failures; rating curves and salt-dilution methods used to establish discharge estimates during available windows.
- Data provenance and references:
  - Background context and measurement details linked to Zwartendijk et al. (2020, 2023).
  - Supplementary materials provide further details on rating curves and measurement protocols.

## Purpose and application
- Designed to support standardized assessment of hydrometric conditions and isotopic signatures to understand rainfall-runoff behavior, soil moisture dynamics, and groundwater interactions in a tropical catchment subject to land-use practices.
- Data are suitable for integration with other environmental datasets to enhance monitoring, analysis, and policy evaluation over time.