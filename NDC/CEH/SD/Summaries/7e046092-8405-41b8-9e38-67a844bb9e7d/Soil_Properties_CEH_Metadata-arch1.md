# Dataset Description (Soil_Properties_CEH)

- The dataset describes soil physical and chemical properties across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
- Collected March–April 2015 as part of the NERC-funded BALI project; analyzed at the Centre for Ecology & Hydrology (CEH), Lancaster, UK.

## Sampling design and data collection

- 9 one-hectare plots across 3 sites representing the land-use types: Danum Valley Conservation Area (unlogged), Maliau Basin Conservation Area (logged), and SAFE project area (oil palm).
- Stratified sampling: each 1-ha plot subdivided into 25 subplots (20 m x 20 m); 5 subplots randomly sampled per plot.
- For each sampled subplot, 5 samples were collected using a gouge augur; organic layer depth measured and separated from underlying mineral soil.
- A separate bulk density sample was collected using a bulk density ring.
- Soil moisture determined gravimetrically; pH measured on fresh soil with a calibrated Hanna pH meter.
- Total carbon (C) and total nitrogen (N) measured on oven-dried, ground soil using a LECO Truspec Micro Elemental Analyzer.
- Inorganic phosphorus (P) extracted with Bray No. 1 extractant and analyzed with a SEAL AutoAnalyser.
- Sampling yielded 100 samples for each forest type group and 25 samples from oil palm plots.

## Variables and metadata

- The CSV (Soil_Properties_CEH.csv) includes 15 columns:
  - Identifier, Site, Land_Use, Plot_Name, Subplot, Horizon
  - Soil_Moisture, Horizon_Depth, Bulk_Density, Soil_pH
  - total_C, total_N, Inorganic_P, C:N, C:P
- Metadata fields describe units/format and descriptions (e.g., Soil_Moisture as gravimetric moisture; Horizon as soil horizon; Horizon_Depth in cm; Bulk_Density in g/cm3; Inorganic_P in µg/g; C:N and C:P as numeric ratios; C_total and N_total as percentages).

## Data quality, missing data, and scope

- Missing data: 3 missing samples from oil palm plots.
- Temporal scope: data represent a single time window (March–April 2015); no longitudinal data described.
- Spatial scope: 9 plots across 3 sites in Sabah, Malaysia; comparisons across three land-use types.

## Site context and land use

- Land-use categories: Unlogged tropical forest, Logged tropical forest, Oil palm plantation.
- Sites: DVCA (unlogged), MBCA (logged), SAFE project site (oil palm).

## Measurement methods and instruments

- Organic layer depth and soil horizons identified; gravimetric soil moisture measured.
- pH measured on fresh soil with a Hanna pH meter.
- Total C and N measured with LECO Truspec Micro Analyzer.
- Inorganic P measured after Bray No. 1 extraction; analyzed with SEAL AutoAnalyser.
- Bulk density determined from samples dried at 105°C.

## References

- Bray, R.H. and Kurtz, L.T. 1945. Determination of total organic and available forms of phosphorus in soils.
- Emmett, B.A. et al. 2010. Countryside Survey: Soils Report (Technical Report No. 9/07).
- Riutta, T. et al. 2018. Logging disturbance shifts net primary productivity in Bornean tropical forests (Global Change Biology).

## Potential analytical uses and considerations for Analysts

- Enables comparison of soil physical/chemical properties across unlogged, logged, and oil palm landscapes.
- Suitable for exploring correlations between C, N, P metrics and soil moisture, bulk density, pH, and horizon depth.
- Design is unbalanced (100 samples for each forest type vs. 25 for oil palm), which should be accounted for in analyses (e.g., weighting or stratified models).
- Data are at plot/subplot scale with explicit metadata, aiding data integration with other datasets and reproducibility.
- Single-timepoint data limit inference about temporal dynamics; consider site-specific factors (location, management history) when generalizing.