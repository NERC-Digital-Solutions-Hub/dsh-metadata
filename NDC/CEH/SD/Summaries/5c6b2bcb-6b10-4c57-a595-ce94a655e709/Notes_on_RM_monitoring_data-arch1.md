# Supporting Documentation

- Overview
  - Two 250 ml water samples per site for nutrient analysis collected roughly every 3 weeks from January 2016 to February 2017.
  - Sampling locations: Rostherne Brook (main inflow, 250 m upstream from the lake), Harper's Bank Spring (groundwater inflow), Blackburn's Brook (outflow, 350 m downstream), and a central lake surface location with multiple depth samples (6 m, 12 m, 18 m, 24 m) added from September 2016.
  - An 8 m integrated water column sample from the central lake location collected into two opaque 500 ml bottles and two opaque 250 ml bottles; 2 ml Lugol's iodine added to each 500 ml bottle to preserve phytoplankton.

- Sample handling and transport
  - All samples sealed and kept in a cool box for transport to Loughborough University.
  - On collection day: one 250 ml sample per site frozen; the other filtered through GF/F filter paper (0.45 μm) and then frozen.
  - Periodic shipments (~2 month intervals) to an external certified laboratory (National Laboratory Service, UK) for orthophosphate (SRP), dissolved inorganic nitrogen (DIN), and total phosphorus (TP).
  - Chlorophyll analysis followed standard spectrophotometer methods.
  - Pigments extracted from filtered samples using 80% acetone, then analyzed spectrophotometrically at 750, 665, 645, and 630 nm.

- Phytoplankton analysis
  - Phytoplankton analyzed by concentrating a 1 L sample to 50 ml using settling procedures.
  - The concentrate is well mixed; a 1 ml sub-sample is examined on a Sedgwick-Rafter cell under a 400x inverted microscope to count algae present per litre.
  - Notable mentions: identification/counts include filaments of Aphanizomenon spp. and colonies of Microcystis spp.

- Discharge, flow, and stage measurement
  - Inflow (Rostherne Brook) and outflow (Blackburn's Brook) discharge estimated by measuring cross-sectional profiles and sectional velocities at multiple stage heights.
  - Discharge/stage relationships applied to continuous stage height recordings from January 2016 to February 2017 using a Van Essen mini-diver data logger (records water pressure every 5 minutes; corrected for air pressure using a barometer in the boathouse).

- Data recorded and units
  - Five-minute flow data for inflow and outflow (m^3 s^-1).
  - Lake Secchi depth (m).
  - Lake chlorophyll (Chl-a) in μg L^-1.
  - Phytoplankton species counts in cells L^-1.
  - Nutrient concentrations (in mg L^-1) for inflow, outflow, groundwater spring, and lake (surface and depth) samples.

- Data structure and contents
  - Three CSV files: RMFlowData, RMLake, RMWaterChem.
  - RMFlowData columns: InflowDate, InflowWaterHead_m, InflowTemperature_C, InflowFlow_m3s-1, OutflowDate, OutflowWaterHead_m, OutflowTemperature_C, OutflowFlow_m3s-1.
  - RMLake columns: Date, SecchiDepth, Chl-aµgL-1, Chl-bµgL-1, Chl-cµgL-1, SumChl, CarotenoidµSPU, plus phytoplankton species counts (header labels as species names) and TotalAlgaePer1L.
  - RMWaterChem columns: ItemLocation, Date, NitriteasN, NitrogenTotalOxidisedasN, OrthophosphatereactiveasP, SilicatereactivasSiO2, NitrateasN, TPmgL.
  
- Method references
  - Inverted microscope method for estimating algal numbers (Lund, Kipling & Le Cren, 1958).
  - Chlorophyll a extraction from freshwater phytoplankton for spectrophotometric analysis (Sartory & Grobbelaar, 1984).