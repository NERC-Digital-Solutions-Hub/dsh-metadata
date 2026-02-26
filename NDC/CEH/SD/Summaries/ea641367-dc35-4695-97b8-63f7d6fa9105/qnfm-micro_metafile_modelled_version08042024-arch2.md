# Metafile for the QNFM-MICRO dataset ' Modelled dynamic response characteristics of selected micro-basins in the UK '

## Purpose and context
- Part of the NERC-funded programme on the effectiveness of Natural Flood Management (NFM) and the Defra £15M NFM interventions programme.
- Installed over twenty 430 litre trapezoidal flumes within the Cumbrian mountains (the C-NFM network) to monitor continuous discharge from ~1 km² micro-basins.
- Aim to quantify rainfall–runoff characteristics and assess how different landscape types respond during flood events, informing the design and deployment of NFM features.
- Hypothesis: micro-basins with different landscape types in the same region can exhibit distinct rainfall–runoff behaviour, necessitating different NFM features for peak reduction.

## Data structure and variables
- Micro-basin scope: basins ranging from 0.0071 to 2.7329 km², largely in Cumbria.
- Modelling approach: rainfall–discharge dynamics modelled with the Refined Instrumental Variable (RIV) algorithm of the CAPTAIN Toolbox, yielding transfer-function-based dynamic response characteristics.
- Output dataset: event-by-event characteristics per micro-basin.
- Data file: QNFM-MICRO_datafile_version08042024.csv with columns A–K; primary variables include:
  - Micro_Basin_#: micro-basin number
  - Micro_Basin_Name
  - Micro_Basin_Area (sq m)
  - Peak_Streamflow (mm/15min per unit micro-basin area)
  - Antecdent_Flow (discharge per unit area at the start of the hydrograph, mm/15min)
  - Rainfall_Intensity (mm/hour; rainfall from event start to peak divided by time to peak)
  - Total_Rainfall (mm/event)
  - Response_Time (Time Constant of the transfer function; hours)
  - Simulated_Runoff_Coefficient (Steady State Gain; event discharge as a proportion of event rainfall)
  - Time_Delay (Pure Time Delay; hours)
  - Event_Start_Date_for_Columns_D_to_J (date)

- Data collection notes: rainfall measured with a single raingauge within each micro-basin; discharge time-series derived from FRPB flume calibrations; continuous measurements central to the flume.
- Model structure: RIVSID (Refined Instrumental Variable System Identification) algorithms within CAPTAIN Toolbox to estimate discrete-time transfer-function dynamics.

## Collection, processing, and quality control
- Observed discharge per unit area (mm/15min) modelled from rainfall data obtained from a single within-basin raingauge.
- Simulated discharge time-series (mm/15min) generated using RIVSID transfer-function representations.
- Outputs per event include Time Constant, Steady State Gain, and Pure Time Delay (Dynamical characteristics of rainfall–discharge response).
- Processing environment: Matlab; final outputs exported to CSV format.
- Methodological references and context provided in Mindham et al. (2023) and related literature for RIVSID application and transfer-function interpretation.

## Outputs, interpretation, and usage
- Results enable comparison of rainfall–runoff response across diverse upland micro-basins and landscape types.
- Supports quantification of nonlinearity in storm response and identification of differential response characteristics among basins.
- Datasets are intended for standardised storage and publication in appropriate data portals, facilitating reuse and scrutiny by environmental analysts and policy evaluators.

## References and further context
- Mindham, D., Beven, K., & Chappell, N. A. (2023). Rainfall–streamflow response times for diverse upland UK micro-basins: quantifying hydrographs to identify the nonlinearity of storm response. Hydrology Research, 54(2), 233–244.
- Chappell et al. (various years) on parsimonious modelling of rainfall–runoff and transfer-function approaches.
- Box, Jenkins, Reinsel (Time Series Analysis) and CAPTAIN Toolbox documentation for RIVSID methodology.