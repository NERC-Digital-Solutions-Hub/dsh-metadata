# Supporting Documentation

## Overview
- A nutrient and phytoplankton monitoring dataset for Rostherne Mere area collected from January 2016 to February 2017.
- Sampling locations: Rostherne Brook inflow (main inflow, 250 m upstream from the lake), Harper's Bank Spring (groundwater inflow), Blackburn's Brook outflow (350 m downstream), and a central lake location with surface and depth samples.
- Sampling cadence: approximately every three weeks, with multi-depth sampling (6 m, 12 m, 18 m, 24 m) added from September 2016; 8 m integrated lake column sample also taken.

## Sampling and sample handling
- Water samples collected in new PTFE sealable bottles; one 250 ml sample frozen on collection day, the other filtered (GF/F 0.45 μm) and frozen.
- Phytoplankton preserved with Lugol's iodine in two opaque 500 ml bottles for preservation, plus two opaque 250 ml bottles.
- Secchi depth recorded at the central lake site during each visit.
- On sampling days, some samples shipped to an external certified lab (National Laboratory Service, UK) about every two months for orthophosphate (SRP), dissolved inorganic nitrogen (DIN), and total phosphorus (TP) analyses.
- Chlorophyll analysis and pigment extraction performed via standard spectrophotometric methods; pigments extracted with 80% acetone and analyzed spectrophotometrically.
- Phytoplankton analysis: concentrate 1 L sample to 50 mL, settle, homogenize, and count under inverted microscope (Sedgwick-Rafter cell, 400x) for absolute abundance; notable focus on filaments of Aphanizomenon spp. and colonies of Microcystis spp.

## Discharge and flow measurements
- Discharge estimates derived from cross-sectional profiles and velocities for a range of stage heights at both inflow and outflow locations.
- Continuous stage height data (inflow, outflow) collected Jan 2016–Feb 2017 using a Van Essen mini-diver data logger recording water pressure every 5 minutes; data corrected for air pressure using a local barometer.

## Data structure and files
- Three CSV files: RMFlowData, RMLake, RMWaterChem.

- RMFlowData (8 columns):
  - InflowDate, InflowWaterHead_m, InflowTemperature_C, InflowFlow_m3s-1
  - OutflowDate, OutflowWaterHead_m, OutflowTemperature_C, OutflowFlow_m3s-1

- RMLake (27 columns):
  - Date, SecchiDepth (m)
  - Chl-aµgL-1, Chl-bµgL-1, Chl-cµgL-1, SumChl, CarotenoidµSPU
  - Phytoplankton species counts (columns H to Z; all counts in cells L-1)
  - TotalAlgaePer1L
  - Additional fields as part of the 27-column structure

- RMWaterChem (8 columns):
  - ItemLocation (inflow, outflow, groundwater spring, lake surface, lake depth)
  - Date
  - NitriteasN, NitrogenTotalOxidisedasN
  - OrthophosphatereactiveasP (SRP)
  - SilicatereactivasSiO2
  - NitrateasN, TPmgL

## Units and measurement references
- Flow: m3 s-1
- Secchi depth: m
- Chlorophyll: µg L-1
- Phytoplankton counts: cells L-1
- Nutrients: mg L-1 (N species, SRP, SiO2, TP)
- Annotations reference standard methods:
  - Inverted microscope counting (Lund, Kipling & LeCren, 1958)
  - Chlorophyll extraction (Sartory & Grobbelaar, 1984)

## Data quality, provenance, and workflow
- Analyses include lab-confirmed measurements (external lab for SRP, DIN, TP) and standardized phytoplankton and chlorophyll methods.
- Multiple data streams combined: hydrology (flow and stage), limnology (Secchi, chlorophyll, pigments), biology (phytoplankton counts), and water chemistry (nutrients).
- Temporal resolution varies: high-frequency flow data (5-minute intervals) and periodic chemical/phytoplankton analyses, enabling multi-resolution GIS integration.
- Data packaging uses CSV with clearly defined fields and headers; depth-related sampling enables vertical profiling analyses.

## GIS-oriented considerations
- Suitable for mapping spatial dynamics of inflow/outflow hydraulics and their relationship with lake health indicators (Secchi depth, chlorophyll, phytoplankton counts, nutrient concentrations).
- Time-series support for trend analyses across the hydrological network and lake column, with alignment to sampling locations and depth strata.
- Potential for integrating with other GIS layers (topography, bathymetry, land use) to assess nutrient transport and phytoplankton blooms.

## References
- Lund, J. W. G., Kipling, C. & Le Cren, E. D. 1958. The inverted microscope method of estimating algal numbers and the statistical basis of estimations by counting. Hydrobiologia, 11, 143-170.
- Sartory, D. P. & Grobbelaar, J. U. 1984. Extraction of chlorophyll a from freshwater phytoplankton for spectrophotometric analysis. Hydrobiologia, 114, 177-187.