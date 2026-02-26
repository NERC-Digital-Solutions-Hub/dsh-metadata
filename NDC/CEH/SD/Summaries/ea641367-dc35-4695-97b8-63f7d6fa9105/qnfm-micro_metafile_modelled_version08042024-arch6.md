# Metafile for the QNFM-MICRO dataset ' Modelled dynamic response characteristics of selected micro-basins in the UK '

## Overview and context
- Part of the NERC-funded programme on Natural Flood Management (NFM) effectiveness and Defra's NFM interventions.
- >20 430 L trapezoidal flumes installed mainly in the Cumbrian mountains (the C-NFM network) to continuously monitor discharge from ~1 km2 micro-basins.
- Aim: quantify rainfall-runoff characteristics across diverse micro-basin types to assess different landscape responses and guide NFM feature design.
- Approach: use Single-Input-Single-Output (SISO) transfer functions to derive rainfall-runoff characteristics for micro-basin behaviour (referenced in Mindham et al., 2023).

## Data structure and content
- Study area and data scope:
  - Micro-basins in Cumbria, UK, sizes from 0.0071 to 2.7329 km2.
  - Rainfall–discharge response modeled with the Refined Instrumental Variable (RIV) algorithm of the CAPTAIN Toolbox.
- Model outputs (event-based) are the Dynamic Response Characteristics (DRCs) of rainfall–discharge:
  - Time Constant (Response_Time): transfer time of flood wave through the catchment.
  - Simulated Runoff Coefficient (Simulated_Runoff_Coefficient): steady-state gain (discharge as a fraction of rainfall).
  - Pure Time Delay (Time_Delay): delay between rainfall input and first discharge response.
- Data file:
  - QNFM-MICRO_datafile_version08042024.csv with columns A to K defined as below.

## Data file columns and definitions
- Column A: Micro_Basin_# — micro-basin identifier.
- Column B: Micro_Basin_Name — name of the micro-basin.
- Column C: Micro_Basin_Area — area in square meters.
- Column D: Peak_Streamflow — peak discharge per unit micro-basin area (mm/15min).
- Column E: Antecedent_Flow — discharge per unit area at the start of the hydrograph (mm/15min).
- Column F: Rainfall_Intensity — rainfall intensity (mm/hour) calculated as rainfall from event start to peak divided by time to peak.
- Column G: Total_Rainfall — total rainfall per event (mm).
- Column H: Response_Time — Time Constant of the transfer function for the event (hours).
- Column I: Simulated_Runoff_Coefficient — simulated runoff coefficient for the event (unitless; steady-state gain).
- Column J: Time_Delay — pure time delay between rainfall input and discharge response (hours).
- Column K: Event_Start_Date_for_Columns_D_to_J — date the event started.

## Collection, processing, and quality control
- Data sources:
  - Observed discharge per unit area derived from measured rainfall using a single raingauge within each micro-basin; discharge time-series derived via standard FRPB flume calibration.
- Modeling approach:
  - Each hydrograph event modeled separately using RIVSID algorithms in the CAPTAIN Toolbox to produce transfer-function characteristics.
  - Outputs (DRCs) exported to CSV from Matlab.
- References and methodology:
  - CAPTAIN toolbox and RIVSID methods as detailed in Mindham, Beven, and Chappell (2023) and related literature (Box et al., 2008; Chappell et al., 1999, 2006, 2012; Taylor et al., 2007; Cheng et al., 2023).
- Purpose of the data:
  - Enable understanding of rainfall–runoff dynamics across diverse upland micro-basins and support comparisons to inform the design of NFM interventions.

## Applications and potential uses for data support
- Cross-basin comparison of rainfall–discharge dynamics to identify nonlinearity or region-specific responses.
- Calibration or validation of hydrological models for micro-scale catchments.
- Development of data products (dashboards, pivot tables) enabling end-users to explore event-based DRCs and associated rainfall characteristics.
- Support for communicating interpretations of micro-basin flood response behavior to policy-makers and stakeholders.

## References
- Mindham, D., Beven, K., and Chappell, N. (2023). Rainfall-streamflow response times for diverse upland UK micro-basins: quantifying hydrographs to identify the nonlinearity of storm response. Hydrology Research, 54(2): 233-244.
- Chappell, N.A., et al. (various years). Parsimonious modelling and transfer-function approaches in catchment hydrology.
- Box, G.E.P., Jenkins, G.M., Reinsel, G.C. (2008). Time Series Analysis. John Wiley and Sons.
- Taylor, C.J., et al. (2007). CAPTAIN toolbox and environmental time series analysis. Environmental Modeling & Software.