# Dataset Description (Soil_Properties_CEH)

- Purpose and scope
  - Describes soil physical and chemical properties across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
  - Collected as part of the NERC-funded BALI project (March–April 2015) and analysed at the Centre for Ecology & Hydrology, Lancaster, UK.
  - Provides a structured basis for monitoring soil health and ecosystem function to inform environmental policy and decision-making.

- Dataset content and structure
  - File: Soil_Properties_CEH.csv with 15 columns.
  - Columns (with description in metadata): Identifier, Site, Land_Use, Plot_Name, Subplot, Horizon, Soil_Moisture, Horizon_Depth, Bulk_Density, Soil_pH, total_C, total_N, Inorganic_P, C:N, C:P.
  - Metadata defines units/formats for each field (e.g., Soil_Moisture: gravimetric or percentage; Horizon_Depth: cm; Bulk_Density: g/cm3; etc.).

- Sampling design and methods
  - 9 one-hectare plots across 3 sites representing each land-use category.
  - Stratified sampling: each 1 ha plot subdivided into 25 subplots (20 x 20 m); 5 subplots sampled per plot.
  - For each sampled subplot, 5 soil samples collected using a gouge auger; organic layer depth recorded and soils separated into organic and mineral layers.
  - A bulk density sample collected with a ring; moisture measured gravimetrically; pH measured on fresh soil with a calibrated pH meter.
  - Total carbon and nitrogen measured on oven-dried soil using a LECO analyser; inorganic phosphorus extracted with Bray No. 1 and analysed with a SEAL AutoAnalyser.
  - Sampling yield: approximately 100 samples per forest type (unlogged or logged) and 25 samples from oil palm; plus an additional bulk density sample per sampling event.

- Data quality, provenance, and metadata
  - Metadata provides unique sample identifiers and descriptive fields (Site, Land_Use, Plot_Name, Subplot, Horizon) to support traceability and reproducibility.
  - Units and formats for each variable are specified in metadata to enable consistent interpretation and cross-study comparability.
  - Missing data: 3 missing data points from oil palm samples (no data for those entries).

- Data governance and usability considerations for monitoring frameworks
  - Clear documentation of sampling design and laboratory analyses supports evaluation of data quality and comparability across sites and land-use types.
  - Availability of complete metadata and measurement methods facilitates integration into monitoring dashboards, trend analyses, and policy assessments.
  - Potential data governance considerations include ensuring ongoing data sharing and metadata completeness to maintain transparency and usefulness for long-term monitoring.

- References
  - Bray, R.H. and Kurtz, L.T. 1945. Determination of total organic and available forms of phosphorus in soils. Soil Science 59, 39-45.
  - Emmett, B.A. et al. 2010. Countryside Survey: Soils Report from 2007. Technical Report No. 9/07 NERC/CEH.
  - Riutta, T. et al. 2018. Logging disturbance shifts net primary productivity and its allocation in Bornean tropical forests. Global Change Biology.