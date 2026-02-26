# Metafile for the QNFM-MICRO dataset ' Modelled dynamic response characteristics of selected micro-basins in the UK '

## Overview
- Part of the NERC-funded programme on Natural Flood Management (NFM) and Defra NFM interventions.
- Micro-basins (approximately 0.0071 to 2.7329 sq km) equipped with 430 L trapezoidal flumes in the C-NFM network, mainly in Cumbria.
- Aim: quantify rainfall-runoff characteristics at micro-basin scale to assess how different landscapes respond to rainfall and inform the design of NFM features to reduce flood peaks.
- Hypothesis: micro-basins with similar regional characteristics may show different rainfall-runoff behavior, requiring different feature types/sizes for peak reduction.

## Data structure and recorded values
- Data file: QNFM-MICRO_datafile_version08042024.csv (columns A–K).
- Columns and descriptors:
  - Micro_Basin_#: micro-basin number.
  - Micro_Basin_Name: micro-basin name.
  - Micro_Basin_Area: area in square meters.
  - Peak_Streamflow: peak discharge per unit area (mm/15 min).
  - Antecedent_Flow: discharge per unit area at the start of the selected hydrograph (mm/15 min).
  - Rainfall_Intensity: rainfall rate to peak (mm/hour); derived from rainfall from event start to peak, divided by time to peak.
  - Total_Rainfall: total rainfall per event (mm).
  - Response_Time: time constant of the identified transfer function for the event (hours).
  - Simulated_Runoff_Coefficient: event runoff as proportion of event rainfall (steady-state gain of the transfer function).
  - Time_Delay: pure time delay between rainfall input and discharge response (hours).
  - Event_Start_Date_for_Columns_D_to_J: date the event started.
- All discharge time-series are per unit micro-basin area and reported in mm/15 min.
- Rainfall data sourced from a single raingauge within the micro-basin (mm/15 min).

## Modelling and data generation methods
- Observed discharge (per unit area) derived from continuous level measurements in the flume; rainfall measured at a single 2 m-raingauge.
- Discharge time-series modelled using the Refined Instrumental Variable (RIV) approach within the CAPTAIN Toolbox (RIVSID algorithms) to represent dynamics as Transfer Functions.
- For each hydrograph event, a separate discharge model is estimated; outputs are exported to CSV from Matlab.
- Dynamic response characteristics (Time Constant, Steady State Gain, Pure Time Delay) are derived per event.

## Transfer function concepts and definitions
- Time Constant: transfer time of flood-wave propagation through the catchment.
- Steady State Gain: simulated runoff coefficient; ratio of event discharge to event rainfall for the transfer function.
- Pure Time Delay: time between unit rainfall input and unit discharge response.

## Data quality, provenance, and references
- Methodology and application described in Mindham, Beven, and Chappell (2023) for rainfall–streamflow response times and nonlinearity assessment.
- Additional methodological references provided for transfer function concepts (Box, Jenkins, Reinsel; Chappell et al.; Cheng et al.).
- The dataset and modelling approach are documented for replication and interpretation within the CAPTAIN toolbox framework.

## File access and output
- The dataset is organized with clearly defined event-based columns and is intended for analysis of rainfall–discharge dynamics and comparisons across micro-basins.
- Output values were generated in Matlab and exported to CSV format for dissemination.

## Applications for analysts
- Identify correlations between micro-basin characteristics (area, landscape type) and dynamic response metrics (Time Constant, Delay, Runoff Coefficient).
- Build predictive models of rainfall-runoff response at micro-basin scale to inform NFM feature design and flood risk assessment.
- Compare hydrological responses across different micro-basins under varying rainfall events to understand nonlinearity and responsiveness.