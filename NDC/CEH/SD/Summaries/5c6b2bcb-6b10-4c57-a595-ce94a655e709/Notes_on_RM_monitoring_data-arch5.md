# Supporting Documentation

- This document describes a lake-water quality and hydrology dataset collected from Rostherne Mere and surrounding inflows/outflows between January 2016 and February 2017.
- Aims align with routine environmental monitoring: capturing flow, water quality, phytoplankton, and nutrient data to enable discovery, reuse, and governance of the dataset.

## Data collection scope and locations

- Sampling locations:
  - Rostherne Brook (main inflow, 250 m upstream from the lake)
  - Harper's Bank Spring (groundwater inflow)
  - Blackburn's Brook (outflow, 350 m downstream from the lake)
  - Central lake location (surface and depth samples)
- Sampling period: January 2016 to February 2017; central lake depth sampling added from September 2016.
- Sample types and preservation:
  - Two 250 ml PTFE sealable bottles per site every ~3 weeks
  - An 8 m integrated water-column sample from the central lake location collected into two 500 ml opaque bottles (with two 2 ml Lugol’s iodine preservative for phytoplankton) and two 250 ml opaque bottles
  - One 250 ml sample per site frozen on collection day; the other filtered (GF/F, 0.45 μm) and then frozen
  - Samples transported in a cool box to Loughborough University
- In-situ measurements: Secchi depth recorded at the central lake location during each visit

## Sample handling and preservation

- On collection day: one sample per site frozen; one sample filtered and frozen
- Lugol’s iodine used to preserve phytoplankton in selected bottles
- Transport: samples placed in a cool box; later analyses performed by an external lab for certain nutrients

## Analyses and methods

- Chlorophyll and pigments:
  - Chlorophyll a/b/c and total chlorophyll calculated via standard spectrophotometric methods
  - Pigments extracted with 80% acetone, centrifuged, and measured spectrophotometrically
- Phytoplankton:
  - Concentrated 1 L sample to 50 mL using settling procedures
  - Sub-sample prepared on a Sedgwick-Rafter cell and counted under 400x inverted microscope
  - Taxa including filaments of Aphanizomenon spp. and colonies of Microcystis spp. recorded
- Nutrients:
  - Periodic external laboratory analysis for orthophosphate (SRP), DIN (oxidised nitrogen), and total phosphorus (TP)
- Discharge and hydrology:
  - Inflow and outflow discharge estimated via cross-sectional profiles and velocities across multiple stage heights
  - Continuous stage height readings collected with a Van Essen mini-diver data logger (every 5 minutes) and corrected for air pressure using a barometer

## Data products and structure

- Three CSV data files:
  - RMFlowData: minutely flow data for inflow and outflow
  - RMLake: lake water quality and phytoplankton data
  - RMWaterChem: water chemistry nutrients by location
- RMFlowData columns:
  - InflowDate, InflowWaterHead_m, InflowTemperature_C, InflowFlow_m3s-1
  - OutflowDate, OutflowWaterHead_m, OutflowTemperature_C, OutflowFlow_m3s-1
- RMLake columns:
  - Date, SecchiDepth (m)
  - Chl-aµgL-1, Chl-bµgL-1, Chl-cµgL-1, SumChl
  - CarotenoidµSPU, TotalAlgaePer1L
  - Phytoplankton species counts (columns H to Z) and related tallies
- RMWaterChem columns:
  - ItemLocation (inflow, outflow, groundwater spring, lake)
  - Date
  - NitriteasN, NitrogenTotalOxidisedasN, OrthophosphatereactiveasP, SilicatereactivasSiO2, NitrateasN, TPmgL
- Units:
  - Flow: m^3 s^-1
  - SecchiDepth: m
  - Chl-a/b/c, SumChl: μg L^-1
  - Phytoplankton: cells L^-1
  - Nutrients: mg L^-1 (N, SRP, Si, TP)
- References for methods:
  - Lund, J. W. G. et al. 1958. Inverted microscope method for estimating algal numbers
  - Sartory, D. P. & Grobbelaar, J. U. 1984. Chlorophyll extraction from freshwater phytoplankton

## Data quality, provenance, and quality assurance

- Data collection cadence combines regular (~3-week) sampling with higher-frequency hydrological measurements (every 5 minutes for stage/flow)
- Preservation and handling steps documented to ensure comparability across samples and time
- External laboratory analyses for key nutrients (SRP, DIN, TP) provide standardized nutrient measurements
- Phytoplankton counts and pigment analyses follow established microscopy and spectrophotometric protocols
- Documentation includes cross-referencing standard methods to support reproducibility and reuse

## Governance and stewardship considerations

- Clear data ownership and custody: samples and data curated with transfer to a university repository; external analyses linked to internal records
- Metadata requirements to ensure discoverability and interoperability:
  - Locations, dates/times, depths, sample IDs, preservation methods, units, and instrument details
- Standardized data formats (three CSV files) to ease integration with other datasets
- Update and versioning approach for new data additions or re-analyses
- Data sharing considerations: external lab contributions and preserved phytoplankton samples may require licensing or access controls

## Notes for future reuse

- Ensure unit consistency when combining datasets (e.g., mg L^-1 vs. μg L^-1)
- Maintain consistent naming conventions for locations and sample types
- Verify completeness of time series (minutely flow data alongside periodic lake and water-chemistry measurements)
- Consider incorporating QA/QC flags for data points sourced from external laboratories
- Document any deviations or amendments to methods over time to preserve historical comparability