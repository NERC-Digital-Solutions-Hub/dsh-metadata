# Metafile for the QNFM-MICRO dataset ' Modelled dynamic response characteristics of selected micro-basins in the UK '

## Purpose and Context
- Part of NERC-funded research on the effectiveness of Natural Flood Management (NFM) and Defra’s £15M NFM interventions.
- Installed over twenty 430 litre trapezoidal flumes in the C-NFM network to continuously monitor discharge from areas of ~1 sq km (micro-basins).
- Aim to quantify how different landscape types at the micro-basin scale influence rainfall-runoff during flood events, informing the need for varied NFM features.

## Data Content and Structure
- Study area: micro-basins largely in Cumbria (UK), with areas ranging from 0.0071 to 2.7329 sq km.
- Modeling approach: rainfall-runoff response modeled with the Refined Instrumental Variable (RIV) algorithm of the CAPTAIN Toolbox, using Single-Input-Single-Output (SISO) transfer functions.
- Output: event-by-event model characteristics of rainfall-discharge dynamics (Dynamic Response Characteristics, DRCs): Time Constant, Steady State Gain (Simulated Runoff Coefficient), Pure Time Delay.
- Main data file: QNFM-MICRO_datafile_version08042024.csv with columns A–K:
  - A: Micro_Basin_#, B: Micro_Basin_Name, C: Micro_Basin_Area (sq m)
  - D: Peak_Streamflow (mm/15min), E: Antecdent_Flow (mm/15min)
  - F: Rainfall_Intensity (mm/hour) (derived to peak)
  - G: Total_Rainfall (mm/event)
  - H: Response_Time (Time Constant, hours)
  - I: Simulated_Runoff_Coefficient (Steady State Gain)
  - J: Time_Delay (hours)
  - K: Event_Start_Date_for_Columns_D_to_J

- Rainfall data: recorded with a single Onset S-RGB-M002 raingauge mounted 2 m above ground; telemetry via Onset RX3000 device.
- Discharge data: derived from FRPB flume calibrations; modeled per micro-basin event.

## Methods and Quality Control
- Observed discharge data (per unit micro-basin area) were modeled from rainfall data using CAPTAIN Toolbox RIVSID algorithms to produce transfer-function-based dynamics.
- Each hydrograph event was modeled separately; outputs exported to CSV from Matlab.
- Key references for methods: Mindham et al. (2023) and related literature on transfer-function modeling (Chappell et al., Box et al., Taylor et al.).
- Full methodological details available in Mindham et al. 2023 (Hydrology Research) and CAPTAIN Toolbox documentation.

## Data Management, Provenance, and Reuse
- Explicit definitions of variables and units to support understanding, reuse, and cross-basin comparisons.
- Metadata includes instrument details, event-based modeling, and the data’s provenance (RIVSID CAPTAIN toolbox workflow; MATLAB-based export).
- Suitable for informing NFM design evaluations, comparative analyses across micro-basins, and integration into larger datasets on rainfall-runoff response.

## References
- Mindham, D., Beven, K., Chappell, N. A. 2023. Rainfall-streamflow response times for diverse upland UK microbasins: quantifying hydrographs to identify the nonlinearity of storm response. Hydrology Research.
- Chappell et al. (1999, 2006, 2012), Box, Jenkins & Reinsel (Time Series Analysis, 2008), Cheng et al. (2023), Taylor et al. (2007) and CAPTAIN Toolbox resources.