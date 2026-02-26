# Metafile for the QNFM-MICRO dataset ' Modelled dynamic response characteristics of selected micro-basins in the UK '

## Overview
- Part of NERC/NFM and Defra-funded initiatives to assess Natural Flood Management (NFM) effectiveness.
- Involves over twenty 430 litre trapezoidal flumes installed in the C‑NFM network to monitor discharge from approx. 1 km² micro-basins.
- Aims to quantify rainfall–runoff characteristics across diverse micro-basin landscapes and evaluate the need for different NFM features.

## Data structure and contents
- Study area: micro-basins largely in Cumbria, UK, sizes ranging from 0.0071 to 2.7329 km².
- Modelling approach: single-input–single-output (SISO) transfer functions used to derive rainfall–discharge dynamics.
- Data file: QNFM-MICRO_datafile_version08042024.csv (columns A–K) containing event-by-event model outputs:
  - A: Micro_Basin_# (micro-basin number)
  - B: Micro_Basin_Name
  - C: Micro_Basin_Area (sq m)
  - D: Peak_Streamflow (mm/15min per unit area)
  - E: Antecedent_Flow (mm/15min per unit area at event start)
  - F: Rainfall_Intensity (mm/hour; sum rainfall from event start to peak divided by time to peak)
  - G: Total_Rainfall (mm/event)
  - H: Response_Time (Time Constant; hours)
  - I: Simulated_Runoff_Coefficient (Steady State Gain; event runoff as proportion of event rainfall)
  - J: Time_Delay (hours; pure time delay from rainfall input to first discharge response)
  - K: Event_Start_Date_for_Columns_D_to_J (start date of the event)

## Data collection and quality control
- Observed discharge data per micro-basin derived from a single interior flume, scaled by micro-basin area.
- Rainfall measured by a single raingauge (Onset S-RGB-M002) located 2 m above ground, with data transmitted via Onset RX3000 telemetry.
- Discharge time series modelled to discharge per unit area using CAPTAIN Toolbox’s RIVSID algorithms (Refined Instrumental Variable System Identification).
- Outputs are transfer-function characteristics: Time Constant, Steady State Gain (Simulated_Runoff_Coefficient), and Pure Time Delay.
- All model outputs exported from MATLAB to CSV.

## Modelling approach and outputs
- Transfer function framework: models rainfall–runoff dynamics for each event separately.
- Key characteristics (DRCs):
  - Time Constant (Response_Time)
  - Steady State Gain (Simulated_Runoff_Coefficient)
  - Pure Time Delay (Time_Delay)
- Documentation and detailed methodology referenced from Mindham et al. (2023) and foundational transfer-function literature.

## Metadata and provenance
- File provides explicit variable definitions and units (e.g., mm/15min, hours, mm/event).
- Event-based modelling approach supports comparative analyses across micro-basins with different rainfall–runoff responses.
- Full methodological context and validation described in associated publications:
  - Mindham, Beven, Chappell (2023) Hydrology Research
  - Box, Jenkins, Reinsel (Time Series Analysis) for transfer-function theory
  - Related CAPTAIN toolbox documentation and usage guides

## Reuse considerations and governance
- Data governance considerations for Data Stewards:
  - Single rainfall gauge per micro-basin may limit representativeness; document potential measurement bias.
  - Event-by-event modelling introduces variability; users should consider the transfer-function nonlinearity and calibration context.
  - Clear unit definitions and column mappings facilitate interoperability and metadata quality.
  - Data are suitable for evaluating rainfall–runoff response across diverse micro-basin types but may require bespoke handling for non-interoperable legacy systems.
- Data availability and sharing:
  - Dataset is clearly structured for discoverability with explicit event-based outputs and core metadata.
  - Model-derived outputs accompany observed data, enabling reproducibility of the DRC estimates.

## References and further reading
- Mindham, D., Beven, K., Chappell, N. A. (2023). Rainfall–streamflow response times for diverse upland UK micro-basins: quantifying hydrographs to identify the nonlinearity of storm response. Hydrology Research.
- Chappell, N. A. et al. (various) on parsimonious and transfer-function modelling approaches.
- Box, G.E.P., Jenkins, G.M., Reinsel, G.C. (Time Series Analysis) for transfer-function concepts.
- Taylor, C.J. et al. (CAPTAIN toolbox) for environmental time series analysis and RIVSID methods.