# Supporting Documentation

- Timeframe and purpose
  - Describes a nutrient-focused monitoring program for Rostherne Mere and adjacent inflows/outflows from Jan 2016 to Feb 2017.
  - Goals include characterizing hydrology, nutrient status, chlorophyll, and phytoplankton to inform environmental health monitoring and policy decisions.

- Sampling design and locations
  - Inflow: Rostherne Brook (main inflow, ~250 m upstream from lake)
  - Groundwater inflow: Harper's Bank Spring
  - Outflow: Blackburn's Brook (~350 m downstream from lake)
  - Lake sampling: central lake location with surface water samples and multi-depth (6 m, 12 m, 18 m, 24 m) profiles; an 8 m integrated water column sample
  - Preservation: Lugol's iodine added to 500 ml samples for phytoplankton; other samples kept in cool conditions

- Sampling frequency and handling
  - Water samples collected ~every 3 weeks; two 250 ml samples per site
  - On collection day: one 250 ml sample frozen, the other filtered (GF/F 0.45 μm) and frozen
  - Nutrient analyses (SRP, DIN, TP) conducted by an external certified lab roughly every 2 months
  - Chlorophyll analysis via standard spectrophotometry; pigments extracted with 80% acetone
  - Phytoplankton analysis: concentration from concentrated sample, settled, counted under inverted microscope (400x) using Sedgwick-Rafter cell
  - Discharge estimation: cross-sectional profiles and velocities for multiple stage heights; stage-discharge relationship applied to continuous stage data collected every 5 minutes with a Van Essen mini-diver; pressure corrected using a co-located barometer

- Measured variables and units
  - Hydrology: inflow and outflow water head (m), temperature (°C), and flow rate (m3 s-1) with five-minute resolution
  - Lake water quality: Secchi depth (m); chlorophyll a/b/c and total chlorophyll (µg L-1); carotenoids (µSPU); total algae per litre; phytoplankton species counts (cells L-1)
  - Nutrients: nitrite (as N), oxidised nitrogen (as N), orthophosphate (as P), silicate (as SiO2), nitrate (as N), total phosphorus (TP mg L-1)
  - Location markers: inflow, outflow, groundwater spring, lake surface, and lake depth samples

- Data structure and formats
  - Three CSV files: RMFlowData, RMLake, RMWaterChem
  - RMFlowData: InflowDate, InflowWaterHead_m, InflowTemperature_C, InflowFlow_m3s-1, OutflowDate, OutflowWaterHead_m, OutflowTemperature_C, OutflowFlow_m3s-1
  - RMLake: Date, SecchiDepth, Chl-aµgL-1, Chl-bµgL-1, Chl-cµgL-1, SumChl, CarotenoidµSPU, phytoplankton species counts (per L), TotalAlgaePer1L
  - RMWaterChem: ItemLocation, Date, NitriteasN, NitrogenTotalOxidisedasN, OrthophosphatereactiveasP, SilicatereactivasSiO2, NitrateasN, TPmgL

- Analytical methods and references
  - Phytoplankton counts: Lund, Kipling & Le Cren (1958) inverted microscope method
  - Chlorophyll extraction: Sartory & Grobbelaar (1984) acetone extraction protocol

- Data quality, sharing, and governance considerations
  - Combines in-house measurements with externally analyzed nutrient data; clear documentation of data structure and units supports transparency and reuse
  - Use of standard methods aids comparability and QA/QC across datasets
  - Data sharing is facilitated by explicit metadata and accessible CSV formats, though the document notes broader data governance considerations (e.g., provenance and storage) implicitly through method transparency

- Relevance for monitoring frameworks and policy
  - Provides a multi-matrix, time-series basis for assessing lake health, nutrient loading, and bloom risk
  - Demonstrates practical integration of hydrology, chemistry, and biology to inform management decisions
  - Highlights the importance of metadata, standardized units, and clear data structures to enable policy-relevant analyses and inter-agency data use