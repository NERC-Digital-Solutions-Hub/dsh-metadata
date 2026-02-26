# Supporting Documentation

## Overview
- A nutrient analysis dataset from Rostherne Mere, collected Jan 2016 – Feb 2017.
- Sampling at multiple locations: Rostherne Brook inflow, Harper's Bank Spring (groundwater inflow), Blackburn's Brook outflow, and central lake surface with depth-integrated samples.
- Additional depth samples added from Sept 2016 (6 m, 12 m, 18 m, 24 m) and an 8 m integrated column sample.
- Preservation and storage: Lugol's iodine added to two 500 ml bottles for phytoplankton; samples sealed and kept in a cool box; on collection day, one 250 ml sample frozen, the other filtered and frozen.
- Analyses include nutrients (SRP, DIN, TP), chlorophyll measurements, phytoplankton counts, and pigments; discharge and hydrology data collected to relate flows to lake conditions.

## Sampling Design and Handling
- Sampling frequency: approximately every 3 weeks per site.
- Sampling locations and roles:
  - Inflow: Rostherne Brook (main inflow, 250 m upstream of lake)
  - Inflow groundwater: Harper's Bank Spring
  - Outflow: Blackburn's Brook (350 m downstream of lake)
  - Central lake location: surface water samples with multiple depth profiles
- Sample preservation:
  - 500 ml bottles: two bottles per site with Lugol's iodine for phytoplankton preservation (2 ml added to each 500 ml bottle)
  - 250 ml bottle: one preserved as collected (frozen later), the other filtered (0.45 μm GF/F) and stored frozen
- Transport and storage: samples placed in a cool box for transport to Loughborough University; periodic shipping to an external certified lab (~every 2 months) for SRP, DIN, TP analyses.
- Secchi depth: measured at the central lake location during each visit.

## Analyses and Measurements
- Nutrient analyses:
  - Orthophosphate reactive (soluble reactive phosphorus, SRP)
  - Nitrogen species (nitrate, nitrite, oxidised nitrogen)
  - Total phosphorus (TP)
  - Units: SRP, DIN, TP reported in mg L-1
- Chlorophyll and pigments:
  - Chlorophyll a, b, c; total chlorophyll; carotenoids
  - Methods: spectrophotometric analysis; pigment extraction with 80% acetone; wavelengths recorded at 750, 665, 645, 630 nm
- Phytoplankton analysis:
  - Concentration from 1 L samples concentrated to 50 mL, settled, mixed, and sub-sampled (1 mL) on Sedgwick-Rafter cells
  - Identification and counting under 400x magnification
  - Outputs include counts of phytoplankton species per liter; specific attention to filamentous Aphanizomenon spp. and colonies of Microcystis spp.
- Hydrology and discharge:
  - Discharge estimates for inflow (Rostherne Brook) and outflow (Blackburn's Brook) via cross-sectional profiles and velocities at multiple stage heights
  - Application of stage-discharge relationships to continuous stage data from a Van Essen mini-diver data logger, recording every 5 minutes
  - Data corrected for atmospheric pressure using a barometer

## Data Structure and Variables
- RMFlowData (8 columns):
  - InflowDate, InflowWaterHead_m, InflowTemperature_C, InflowFlow_m3s-1
  - OutflowDate, OutflowWaterHead_m, OutflowTemperature_C, OutflowFlow_m3s-1
- RMLake (27 columns):
  - Date; SecchiDepth (m)
  - Chl-aµgL-1, Chl-bµgL-1, Chl-cµgL-1, SumChl (total chlorophyll)
  - CarotenoidµSPU (carotenoids)
  - Phytoplankton species counts (header labels are species names; values: cells L-1)
  - TotalAlgaePer1L
- RMWaterChem (8 columns):
  - ItemLocation (inflow, outflow, groundwater spring, lake surface/depth)
  - Date
  - NitriteasN, NitrogenTotalOxidisedasN, OrthophosphatereactiveasP, SilicatereactivasSiO2, NitrateasN, TPmgL
- Units:
  - Flow: m3 s-1
  - SecchiDepth: m
  - Chl-a/b/c and SumChl: µg L-1
  - Phytoplankton: cells L-1
  - Nutrients: mg L-1

## Data Provenance and References
- Phytoplankton counting methodology references:
  - Lund, Kipling & Le Cren (1958) for inverted microscope counting method
  - Sartory & Grobbelaar (1984) for chlorophyll extraction from freshwater phytoplankton
- Sampling and analyses conducted through established laboratory procedures with periodic external laboratory analysis for key nutrients.

## Governance, Quality, and Usage Considerations
- Ensures sample integrity through immediate preservation, cold-chain storage, and documentation of sample handling.
- Data are organized into three structured CSV files with clear column definitions to support integration into wider data systems and cross-site analyses.
- Metadata covers locations, sample timing, and processing methods to facilitate data auditing, reproducibility, and appropriate use in nutrient dynamics and phytoplankton studies.