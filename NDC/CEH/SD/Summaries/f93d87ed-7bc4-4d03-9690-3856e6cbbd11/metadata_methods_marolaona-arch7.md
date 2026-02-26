# Metadata and methods for the dataset: Hydrometric data and stable isotope data for streamflow and rainfall in the Marolaona catchment, Madagascar, 2015-2016

## Overview
- Dataset from the 31.7 ha Marolaona catchment in Madagascar (Ankeniheny Zahamena Corridor, Eastern escarpment).
- Time period: February 3, 2015 to March 3, 2016.
- Data types: hydrometric measurements (rainfall, streamflow, perched groundwater levels, soil moisture) and stable isotope data (δ18O, δ2H, and deuterium excess) for streamflow and overland flow.
- Data primarily intended for GIS-based analysis and map-based visualization of hydrological processes.

## Data Files and Content
- HydrometricData_Marolaona.csv
  - Measurements at 5-minute intervals over the study period.
  - Variables include:
    - Rainfall: P_down_a, P_down_i (downstream/upstream gauges) and P_up_a, P_up_i
    - Streamflow: Q_down_q, Q_down_i (downstream weir), Q_up_q, Q_up_i (upstream weir)
    - Perched water tables: PWT_TF2, PWT_EUC_down/mid/up, PWT_TSF_down/mid/up, PWT_TF1_down/mid/up
    - Soil moisture and temperature at TF2, EUC, TSF ranges (SMC and Temp at 5 cm, 15 cm, 30 cm)
  - Units: standard SI (e.g., mm, L s^-1, °C) with detailed explanations in Table 1.
  - Notes:
    - Missing data denoted as NaN.
    - Rainfall data gaps due to battery failure at the upstream gauge between 01 Jul and 17 Aug 2015.

- IsotopeData_Marolaona.csv
  - Stable isotope samples from streamflow and overland flow, plus rainfall samples during the wet season.
  - Variables include:
    - Location, Water_type (rainfall, streamflow, plot runoff/overland flow)
    - DateTime
    - Delta18O, Delta2H, DEx
  - Precision: δ18O ±0.16‰; δ2H ±0.6‰.
  - Notes:
    - Samples analyzed by CRDS (L2130-i, Picarro) at University of Freiburg.
    - Data described with Table 2 in the source document.

- Location and plotting context
  - Measurement sites and catchment features are described and mapped (Fig. 1 in the document), including downstream/upstream weirs, measurement plots (TF2, EUC, TSF), streams, and 10 m contours from a 12 m DEM.

## Data Collection and Methods
- Rainfall
  - Two tipping-bucket gauges (Rain Collector II) at ~1.2 m above soil to reduce splash effects.
  - Gauges located downstream: 18.9678°S, 48.4258°E; upstream: 18.971°S, 48.4212°E.
  - Data converted to 5-minute intervals; potential data loss due to battery failures (upstream gauge: Jul 1 – Aug 17, 2015).

- Streamflow
  - Weirs at the catchment outlet (31.7 ha) and upper catchment (7.11 ha) to measure flow.
  - Weirs reconstructed/updated in the 1960s; 90° V-notch used at upper catchment.
  - Water levels logged at 5-minute intervals; two measurement periods with different sensors (Decagon CTD-10, EM50 logger; or STS DL/N 70 sensor).
  - Rating curves established via salt-dilution-slug injection method; upper catchment using truncated-triangular sharp-crested weir equations.
  - Calibration and validation described in the supplementary materials of Zwartendijk et al. (2023).

- Soil moisture
  - Measurements at three hillslopes (TF2, EUC, TSF) using Decagon sensors (SMC and Temp at 5 cm, 15 cm, 30 cm depths).
  - Sensor placements upslope from plot boundaries; data logged at 1-minute intervals with 5-minute averages stored.

- Perched groundwater
  - Fully screened wells at TF1, TF2, EUC, TSF locations (0.30 m depth) with different arrangements.
  - Water levels logged: TF1, EUC, TSF every minute; EUC and TSF upslope/downstream wells at 5-minute intervals.
  - Data corrected for atmospheric pressure; stored in 5-minute averages.

- Isotope sampling
  - Rainfall samples collected daily during wet season at TF2; additional samples triggered by rainfall events using a sequential sampler near the downstream rain gauge.
  - Streamflow samples: upstream and downstream of weirs; overland flow samples from TF1, TF2, TSF, EUC plots.
  - Sampling periods cover pre-event, event, and post-event phases.
  - Isotope analysis via CRDS; results reported as δ18O, δ2H, and DEx relative to VSMOW.

## Data Quality and Limitations
- Missing data indicated as NaN in hydrometric measurements; occasional sensor/fault-related gaps (e.g., upstream rainfall gauge battery failure).
- Isotope data quality controlled via established laboratory protocols; reported precisions noted above.
- Rating curves and measurement techniques are documented, with supplementary materials referenced for detailed validation.

## Spatial and Temporal Coverage
- Spatial scope: Marolaona catchment area with key measurement locations mapped and described; includes downstream and upstream weirs, overland flow plots, and soil moisture stations.
- Temporal scope: February 2015 to March 2016, with continuous near real-time 5-minute hydrometric data and isotope samples collected across the study period, including wet-season events in 2016.

## Data Use and Linkages
- Primary CSV files: HydrometricData_Marolaona.csv and IsotopeData_Marolaona.csv.
- Tables 1 and 2 in the source document detail column names, units, and explanations for the two datasets.
- Background and methodology contextualized in Zwartendijk et al. (2020, 2023) and related references.
- Spatial context and base mapping supported by DEM and land-cover sources cited (TanDEM-X DEM, SPOT6 imagery).

## References and Further Information
- Key methodological and background references include:
  - Zwartendijk et al. (2020, 2023) on soil water dynamics and rainfall–runoff responses.
  - Moore (2004, 2005) on salt-dilution gauging for streamflow measurement.
  - Bos (1989) on discharge measurement structures.
  - TanDEM-X DEM sources and high-resolution land cover classifications for CAZ Madagascar.
- Supplementary materials and figures (e.g., Figure 1 and Tables 1–2) provide additional context for dataset integration.