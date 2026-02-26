# Supporting Documentation

## Overview
- Describes a nutrient, pigment, phytoplankton, and flow dataset collected from Rostherne Mere and nearby inflow/outflow points between January 2016 and February 2017.
- Sampling produced three CSV data files: RMFlowData, RMLake, and RMWaterChem.
- Includes high-resolution (minutely) discharge data, lake Secchi depth, chlorophyll, phytoplankton counts, and nutrient concentrations.
- Methods cover sample collection, preservation, laboratory analyses, and field discharge estimation.

## Sampling and Sample Handling
- Locations:
  - Rostherne Brook (main inflow, 250 m upstream from the lake)
  - Harper's Bank Spring (groundwater inflow)
  - Blackburn's Brook (outflow, 350 m downstream)
  - Central lake surface water (plus multiple depth samples)
- Depth sampling added from September 2016 (6 m, 12 m, 18 m, 24 m); an 8 m integrated sample from the central lake collected into two 500 mL bottles and two 250 mL bottles.
- Preservation:
  - 2 mL Lugol's iodine added to each 500 mL bottle for phytoplankton preservation.
- Handling:
  - On collection day, one 250 mL sample per site frozen; the other filtered (GF/F filter, 0.45 μm) and frozen.
  - Periodic shipments (~every ~2 months) to an external certified lab for orthophosphate (SRP), DIN, and total phosphorus (TP).
  - Chlorophyll pigments analyzed spectrophotometrically; pigments extracted with 80% acetone, centrifuged, and analysed at specific wavelengths.
  - Phytoplankton analyzed by concentrating 1 L to 50 mL, settling, and counting algae under a 400× microscope (Sedgwick-Rafter cell); notable taxa included Aphanizomenon spp. and Microcystis spp. colonies.
- Discharge estimation:
  - Inflow and outflow discharge estimated from cross-sectional profiles and velocity for multiple stage heights.
  - These relations applied to continuous stage height records (5-minute intervals) from a Van Essen mini-diver data logger, corrected for air pressure.

## Measurements and Units
- Five-minute discharge data for inflow and outflow: cubic meters per second (m3 s-1).
- Lake Secchi depth: meters (m).
- Lake chlorophyll: micrograms per liter (µg L-1).
- Phytoplankton: cells per liter (cells L-1).
- Nutrients: milligrams per liter (mg L-1) for N species (nitrite, oxidised nitrogen, nitrate), phosphate (SRP), silicate (SiO2), and total phosphorus (TP).

## Data Structure and Files
- RMFlowData (8 columns):
  - InflowDate, InflowWaterHead_m, InflowTemperature_C, InflowFlow_m3s-1
  - OutflowDate, OutflowWaterHead_m, OutflowTemperature_C, OutflowFlow_m3s-1
- RMLake (27 columns):
  - Date, SecchiDepth (m)
  - Chl-aµgL-1, Chl-bµgL-1, Chl-cµgL-1, SumChl, CarotenoidµSPU
  - Phytoplankton species counts (columns H to Z): cells L-1
  - TotalAlgaePer1L
- RMWaterChem (8 columns):
  - ItemLocation, Date
  - NitriteasN, NitrogenTotalOxidisedasN, OrthophosphatereactiveasP, SilicatereactivasSiO2, NitrateasN, TPmgL

## Data Processing and Analysis Methods
- Discharge: derived from stage-height–velocity relationships using multiple stage heights and continuous logger records, with air-pressure corrections.
- Chlorophyll: standard spectrophotometric method following extraction with acetone.
- Phytoplankton: concentration and enumeration via Sedgwick-Rafter method; identification and counting of algae under 400×.
- Data provenance and citations:
  - Lund, J. W. G., Kipling, C., & Le Cre,n, E. D. 1958. Inverted microscope method for algal counts.
  - Sartory, D. P. & Grobbelaar, J. U. 1984. Chlorophyll extraction from freshwater phytoplankton.

## Location, Timeframe, and Scope
- Timeframe: January 2016 – February 2017.
- Sampling included inflows (Rostherne Brook, groundwater spring) and outflow (Blackburn’s Brook), plus central-lake surface and depth samples.
- Depth-integrated sampling initiated from September 2016.
- Multiple sample types collected and processed as described above, with periodic external lab analyses for key nutrients.

## How to Use / Potential Data Products
- Self-serve dashboards for:
  - Temporal trends in flow, Secchi depth, chlorophyll, and phytoplankton counts.
  - Nutrient concentrations (N species, SRP, SiO2, TP) over time and across locations.
  - Lake health indicators by depth and location, linked to discharge data.
- Data fusion opportunities:
  - Correlate phytoplankton abundance and community composition with nutrient loads and hydrological conditions.
  - Compare surface and depth-sampled nutrient/chlorophyll data to assess vertical gradients.
- Data quality considerations:
  - Sparse and variable sampling frequency across locations; depth sampling began mid-study.
  - Multiple formats and preservation steps; time-aligned merging of flow and water-chemistry data requires careful handling.

## Data Sources and References
- Lund, J. W. G., Kipling, C., & Le Cren, E. D. (1958). The inverted microscope method of estimating algal numbers and the statistical basis of estimations by counting.
- Sartory, D. P., & Grobbelaar, J. U. (1984). Extraction of chlorophyll a from freshwater phytoplankton for spectrophotometric analysis.