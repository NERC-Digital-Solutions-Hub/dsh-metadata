# Supporting Documentation

- Purpose and scope
  - Document describes a long-term nutrient, chlorophyll, phytoplankton, and hydrology dataset for Rostherne Mere collected between Jan 2016 and Feb 2017.
  - Data support environmental monitoring and assessment of lake health and nutrient dynamics.

- Sampling locations and design
  - Inflow sites: Rostherne Brook (main inflow, 250 m upstream from the lake) and Harper's Bank Spring (groundwater inflow).
  - Outflow site: Blackburn's Brook (outflow, 350 m downstream from the lake).
  - Central lake: surface water sampling with additional depth-specific samples (6 m, 12 m, 18 m, 24 m); an 8 m integrated water-column sample collected into two opaque 500 mL bottles and two opaque 250 mL bottles.
  - 250 mL bottles used for immediate sampling; 500 mL bottles preserved with Lugol's iodine for phytoplankton.

- Sampling schedule and depth sampling
  - Approximately every 3 weeks for each site from January 2016 to February 2017.
  - Additional depth-integrated sampling commenced from September 2016.
  - On sampling days, one 250 mL sample per site was frozen; the other filtered through GF/F filter (0.45 μm) and then frozen.
  - Secchi depth measured at the central lake location during each visit.

- Sample handling and transport
  - Samples sealed and placed in a cool box for transport to Loughborough University.
  - Periodic shipment (roughly every 2 months) to an external certified laboratory (National Laboratory Service, UK) for nutrient analyses.

- Analyses and methods
  - Nutrients: orthophosphate (SRP), dissolved inorganic nitrogen (DIN), and total phosphorus (TP).
  - Chlorophyll: standard spectrophotometer method; pigments extracted with 80% acetone; readings at 750, 665, 645, and 630 nm.
  - Phytoplankton: concentration of a 1 L sample reduced to 50 mL, then settled, mixed, and a 1 mL subsample counted under a 400x inverted microscope (Sedgwick-Rafter chamber) to determine absolute abundance; identification and counts for algae present.
  - Notable taxa observed: filaments of Aphanizomenon spp. and colonies of Microcystis spp.
  - Phytoplankton preservation for identification: Lugol’s iodine used for 500 mL samples.

- Discharge estimation and hydrology
  - Inflow and outflow discharge estimated from cross-sectional profiles and velocities across multiple stage heights.
  - Stage-discharge relationships derived and applied to continuous stage height records from Jan 2016 to Feb 2017 using a Van Essen mini-diver data logger (5-minute intervals), with air pressure corrections from a barometer.

- Data recorded and units
  - Five-minute inflow and outflow flow data (m^3 s^-1).
  - Lake Secchi depth (m).
  - Lake chlorophyll (µg L^-1) including Chl-a, Chl-b, Chl-c and total Chl.
  - Phytoplankton counts (cells L^-1) by species.
  - Water chemistry: nitrite (as N), oxidised nitrogen (as N), orthophosphate reactive (SRP as P), biogenic silica (SiO2 as SiO2), nitrate (as N), total phosphorus (TP) in mg L^-1.
  - Additional lake depth/nutrient/chlorophyll metrics summarized in the dataset.

- Data structure and files
  - Three csv files: RMFlowData, RMLake, RMWaterChem.
  - RMFlowData: eight columns
    - InflowDate, InflowWaterHead_m, InflowTemperature_C, InflowFlow_m3s-1, OutflowDate, OutflowWaterHead_m, OutflowTemperature_C, OutflowFlow_m3s-1
  - RMLake: 27 columns
    - Date, SecchiDepth, Chl-aµgL-1, Chl-bµgL-1, Chl-cµgL-1, SumChl, CarotenoidµSPU, plus phytoplankton species counts (per L) and TotalAlgaePer1L
  - RMWaterChem: eight columns
    - ItemLocation, Date, NitriteasN, NitrogenTotalOxidisedasN, OrthophosphatereactiveasP, SilicatereactivasSiO2, NitrateasN, TPmgL
  - Methods and conventions cited for analyses (in-lab and spectrophotometric/eyed references).

- References and methodology notes
  - Microbiological and phytoplankton methodology references:
    - Lund, Kipling & Le Cren (1958) for inverted microscope counting method.
    - Sartory & Grobbelaar (1984) for chlorophyll extraction from freshwater phytoplankton.
  - Data collection and standardisation align with environmental monitoring practices to enable inter-study comparability and long-term trend analysis.

- Quality, storage, and accessibility
  - Standardised data handling, verification, and quality assurance routines described.
  - Data stored and uploaded to appropriate portals to facilitate access and reuse by analysts and stakeholders.
  - The design supports combining these datasets with other environmental data sources and enables broader access to underlying measurements.