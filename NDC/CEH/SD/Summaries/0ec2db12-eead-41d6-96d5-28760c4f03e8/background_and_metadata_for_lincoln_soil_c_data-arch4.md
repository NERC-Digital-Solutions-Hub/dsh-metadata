# Lincoln_Miscanthus_Soil_C_Data and Lincoln_Miscanthus_ESM_Soil_C_Data

- Overview
  - Two related datasets from a commercial Miscanthus plantation near Lincolnshire, UK.
  - 2011 data for surface soil (0-30 cm); 2016 data for surface to 1 m depth (0-1 m) with five plots per field in 2011 and expanded sampling in 2016.
  - Fields include two Miscanthus fields (Mis A tilled in 2013; Mis B not tilled) and a paired arable control field (winter wheat/oilseed rape).
  - Measurements per core increment up to 1 m include soil carbon, soil moisture, root and stone mass/volume, and bulk density.
  - Data intended for assessing soil carbon under different land uses; 2011 data are not directly comparable across land uses due to bulk density changes; 2016 updates address this with an equivalent soil mass (ESM) approach.

- Datasets and their purpose
  - Lincoln_Miscanthus_Soil_C_Data
    - Primary soil carbon data with depth- and location-specific measurements.
    - Not recommended for direct cross-land-use comparisons of soil carbon stocks because bulk density changes affect stock calculations.
  - Lincoln_Miscanthus_ESM_Soil_C_Data
    - Soil carbon stocks calculated on an equivalent soil mass (ESM) basis to enable fair cross-land-use comparisons.
    - Provides data for 0-30 cm and 0-70 cm depths using reference dry soil masses (4,000 Mg ha-1 and 10,390 Mg ha-1) and the SCESM equation.
    - Includes both tilled and untilled scenarios and the arable control, aligned to support land-management impact analyses.

- Site details
  - Location: approximately 10 km north of Lincoln, UK; exact site location embargoed to protect landowner privacy.
  - Field sizes: Miscanthus fields ~11 ha each; arable field ~7.5 ha.
  - Soils: Stagnogley over mudstone/chalk till; texture 49% sand, 36% silt, 15% clay; pH 6.8–7.3; bulk density ~1.46–1.53 g cm-3.
  - Climate: mean annual temperature ~9.8°C; mean annual precipitation ~614 mm.
  - Management history: Miscanthus established around 2006; Mis A tilled in spring 2013 to fix crop gaps; Mis B remained untilled; arable field under winter wheat/oilseed rape.

- Provenance and data collection
  - Field sampling
    - 2011: five randomly selected plots per field; three cores per plot to 30 cm (total 15 samples per field).
    - 2016: same five locations for Mis A; three new plots for Mis B (tilled vs tilled history); depth extended to 1 m at three locations, others 0-30 cm; cores divided into 10 cm increments.
  - Laboratory processing
    - Oven-dried mass, moisture content, root and stone mass/volume determined; cores dried and ground; inorganic C removed with hydrochloric acid (HCl); carbon concentration measured with elemental analyzer (CN).
    - Calibration with standards; drift correction as per established methods.
  - Data structure and fields
    - For each core increment: land management, date, stone/root weight and volume, soil moisture, carbon concentration, bulk density, oven-dried soil mass, pH, core volume, and derived carbon stocks (t C ha-1).
    - File formats are CSV; metadata describes field IDs, plot IDs, depth ranges, core numbers, and sampling years.
  - Quality and gaps
    - Data quality notes reference standard procedures and indicate that some fields contain gaps (no data).
    - Pseudo-replication noted for soil pH values in the ES dataset; analysis should be performed on summarized data by sampling location.

- Equivalent Soil Mass (ESM) methodology (Lincoln_Miscanthus_ESM_Soil_C_Data)
  - Purpose: to enable fair comparisons of soil carbon stocks across land uses by normalizing for changes in soil mass.
  - Key concepts
    - SCESM = SC upper + (ConcLower × (Mref − Mupper))
    - Upper and lower sections defined by depth (0-10/10-20 cm as upper; 20-30 cm as lower for 0-30 cm; 0-60 cm upper and 60-70 cm lower for 0-70 cm).
    - References: Mref = 4,000 Mg ha-1 (0-30 cm) and 10,390 Mg ha-1 (0-70 cm), based on median soil mass (Gifford & Roderick, 2003).
  - Application
    - Provides ESM-based carbon stock values for model development and cross-field comparison.
    - Also includes fixed-depth (FD) baselines for comparison, though use for land-use comparisons is not recommended in the FD datasets.

- Data usage guidance for Data Leaders
  - Use the ESM dataset for cross-field, land-management impact assessments of soil carbon, ensuring comparisons account for bulk-density changes.
  - Use the primary S_C_Data to support model development and to understand raw, increment-level soil carbon, moisture, roots, stones, and density data.
  - Leverage metadata and standardized lab methods to ensure reproducibility, including the HCl treatment to remove inorganic C and the CN analyzer measurements.
  - Be mindful of privacy-related access restrictions and the embargo on exact locations; plan analyses around available fields and aggregated summaries.
  - Consider the two timepoints (pre-2013 tillage and post-tillage 2016) to evaluate management interventions on soil carbon dynamics in a commercial setting.
  - When communicating findings, distinguish between raw stock estimates (S_C_Data) and equivalent-mass-adjusted stocks (ESM_Data) to avoid misinterpretation.

- Related references
  - Several publications cited for methods and context (e.g., Rowe et al. 2020; Morrison et al. 2019; Drewer et al. 2012; Robertson et al. 2017; Rowe et al. 2023).

- Limitations and considerations
  - Location privacy leads to embargoed coordinates; access may be restricted.
  - 2011 vs 2016 sampling design differences (depths and number of locations) require careful handling during longitudinal analyses.
  - Pseudo-replication in pH data; analysis should rely on location- or plot-level summaries.