# Metafile for the QNFM-MICRO dataset ' Modelled dynamic response characteristics of selected micro-basins in the UK '

- Purpose and context
  - Part of NERC-funded research on Natural Flood Management (NFM) effectiveness and Defra NFM interventions.
  - Over twenty 430-litre trapezoidal flumes installed primarily in the Cumbrian mountains (the C-NFM network) to monitor discharge from ~1 km² micro-basins.
  - Goal: quantify rainfall–runoff characteristics across different micro-basin types to identify appropriate NFM features for varying catchments.
  - Uses Single-Input-Single-Output (SISO) transfer functions to derive rainfall–runoff characteristics at the micro-basin scale (Mindham et al. 2023).

- Data structure and content
  - Dataset: QNFM-MICRO_datafile_version08042024.csv (event-based model output per micro-basin).
  - Columns and meanings (A–K):
    - Micro_Basin_#: micro-basin number
    - Micro_Basin_Name: micro-basin name
    - Micro_Basin_Area: area in square metres
    - Peak_Streamflow: peak discharge per unit area (mm/15min)
    - Antecedent_Flow: discharge per unit area at start of hydrograph (mm/15min)
    - Rainfall_Intensity: rainfall intensity to peak (mm/hour)
    - Total_Rainfall: total rainfall per event (mm)
    - Response_Time: time constant of the transfer function (hours)
    - Simulated_Runoff_Coefficient: event runoff as proportion of rainfall (Steady State Gain)
    - Time_Delay: pure time delay between rainfall input and discharge response (hours)
    - Event_Start_Date_for_Columns_D_to_J: event start date
  - Coverage: micro-basins range from 0.0071 to 2.7329 km².
  - Data are derived per event from modeled discharge time series (mm/15min) using rainfall data from a single raingauge within each micro-basin.

- Collection, processing, and quality control
  - Observed rainfall (mm/15min) from a single Onset raingauge within each micro-basin; discharge modeled per unit area.
  - Modeling approach: Refined Instrumental Variable System Identification (RIVSID) via the CAPTAIN Toolbox to generate transfer-function-based dynamics (Time Constant, Steady State Gain, Pure Time Delay).
  - Output: modeled discharge hydrographs per event, converted to CSV from MATLAB.
  - Methodology detailed in Mindham, Beven, and Chappell (2023); definitions and data-processing steps align with CAPTAIN toolbox guidance (Taylor et al. 2007).

- Model concepts and interpretation
  - Transfer Function concepts:
    - Time Constant: propagation time of the flood wave through the catchment (hydraulic response speed).
    - Steady State Gain: simulated runoff coefficient (event discharge / event rainfall).
    - Pure Time Delay: lag between rainfall input and first discharge response.
  - Application: per-event characterization of rainfall–runoff response across diverse upland micro-basins to identify nonlinearity and variability in storm response (Mindham et al. 2023).

- Technical and provenance notes
  - Data and methods cited and contextualized by:
    - Box, Jenkins, Reinsel (Time Series Analysis)
    - Chappell et al. (various publications on rainfall–runoff modelling)
    - Mindham, Beven, Chappell (2023) on rainfall–streamflow response times
    - CAPTAIN Toolbox documentation (Taylor et al. 2007)
  - Full application details for RIVSID in Mindham et al. (2023) and CAPTAIN toolbox materials.

- Usage and GIS relevance
  - Provides event-based dynamic characteristics for micro-basins suitable for GIS-based visualization and comparison across basins.
  - Enables map-based exploration of spatial patterns in rainfall–runoff response (e.g., comparing Time Constant, Runoff Coefficient, and Time Delay across basins).
  - Useful for researchers and practitioners assessing NFM feature design and targeting across landscapes with different rainfall–runoff behaviours.

- References
  - Mindham, D., Beven, K. and Chappell, N. (2023). Hydrology Research.
  - Chappell, N.A. et al. (various, 1999–2012). Hydrology and related methods.
  - Box, G.E.P., Jenkins, G.M. and Reinsel, G.C. (2008). Time Series Analysis.
  - Taylor, C.J. et al. (2007). CAPTAIN toolbox documentation.