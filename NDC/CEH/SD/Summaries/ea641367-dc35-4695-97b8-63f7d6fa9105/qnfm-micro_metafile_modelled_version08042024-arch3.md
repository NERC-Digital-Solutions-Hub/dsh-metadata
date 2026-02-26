# Metafile for the QNFM-MICRO dataset ' Modelled dynamic response characteristics of selected micro-basins in the UK '

## Overview
- Part of the NERC-funded programme assessing Natural Flood Management (NFM) effectiveness and the Defra £15M NFM interventions.
- >20 instrumented 430 litre trapezoidal flumes installed mainly in the Cumbrian mountains (the C-NFM network) to monitor discharge from approximately 1 sq. km landscape units (micro-basins).
- Key hypothesis: different landscape types at the micro-basin scale can exhibit distinct rainfall–runoff behaviours during flood events, potentially requiring different NFM features to minimise peak flows.
- Approach: quantify rainfall–runoff characteristics for micro-basins using Single-Input-Single-Output (SISO) transfer functions to derive rainfall–runoff characteristics for event-scale hydrology (Mindham et al., 2023).

## Data structure and content
- Basin coverage: micro-basins range from 0.0071 to 2.7329 sq km.
- Modelling framework: rainfall–discharge response modelled with the Refined Instrumental Variable (RIV) algorithm within the CAPTAIN Toolbox (RIVSID), providing transfer-function-based dynamics.
- Output characteristics (per event): Time Constant, Simulated Runoff Coefficient (steady-state gain), and Pure Time Delay.
- Data file: QNFM-MICRO_datafile_version08042024.csv with columns A–K:
  - A: Micro_Basin_# (micro-basin identifier)
  - B: Micro_Basin_Name
  - C: Micro_Basin_Area (sq m)
  - D: Peak_Streamflow (mm/15min per micro-basin area)
  - E: Antecedent_Flow (discharge per unit area at event start, mm/15min)
  - F: Rainfall_Intensity (mm/hour up to peak, divided by time to peak)
  - G: Total_Rainfall (mm/event)
  - H: Response_Time (Time Constant of the transfer function; hours)
  - I: Simulated_Runoff_Coefficient (event discharge as a proportion of event rainfall)
  - J: Time_Delay (Pure Time Delay, hours)
  - K: Event_Start_Date_for_Columns_D_to_J (date)

## Methods and quality control
- Data collection: observed discharges per unit micro-basin area derived from rainfall data for a single raingauge within each micro-basin.
- Modelling: simulated discharge time-series (mm/15min) generated using the RIVSID algorithms of the CAPTAIN Toolbox; these represent the dynamics via transfer-function models.
- Event-level processing: each discharge hydrograph event modelled separately; resulting characteristics (Time Constant, Time Delay, Runoff Coefficient) are exported to CSV from Matlab.
- Documentation and definitions:
  - Time Constant: transfer time of flood-wave propagation through the catchment.
  - Simulated Runoff Coefficient: steady-state gain of the rainfall–runoff system (simulated discharge as a function of rainfall).
  - Pure Time Delay: lag between unit rainfall input and first unit discharge response.
- References and tooling:
  - Mindham, Beven, and Chappell (2023) for rainfall–streamflow response times and nonlinearity in diverse upland UK micro-basins.
  - CAPTAIN Toolbox and RIVSID methodology (Taylor et al., 2007).
  - Foundational hydrology/time-series references (Box, Jenkins, Reinsel, 2008; Chappell et al., 1999, 2006, 2012).

## How to use and interpret
- Objective: provide quantitative measures of micro-basin hydrological response to inform evaluation of NFM interventions and landscape-scale flood management strategies.
- Key metrics enable:
  - Cross-basin comparison of response characteristics under similar rainfall events.
  - Assessment of how landscape type and scale influence rainfall–runoff dynamics.
  - Informing design choices for NFM features based on quantified dynamic responses.
- Metadata clarity: explicit variable names, descriptors, units, and event-based structure to support data verification, reproducibility, and governance.

## References and related work
- Mindham, D., Beven, K., Chappell, N. A. (2023). Rainfall–streamflow response times for diverse upland UK micro-basins: quantifying hydrographs to identify the nonlinearity of storm response. Hydrology Research, 54(2), 233-244.
- Chappell et al. (various) on parsimonious and transfer-function hydrological modelling.
- Box, G.E.P., Jenkins, G.M., Reinsel, G.C. (2008). Time Series Analysis. John Wiley & Sons.
- Taylor, C.J., Pedregal, D.J., Young, P.C., & Tych, W. (2007). CAPTAIN toolbox and environment time series analysis. Environmental Modelling & Software.