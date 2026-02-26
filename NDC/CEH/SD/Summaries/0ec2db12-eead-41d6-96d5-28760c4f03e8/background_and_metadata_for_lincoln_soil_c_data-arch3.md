# Lincoln_Miscanthus_Soil_C_Data

- Overview
  - Datasets from soil cores at a commercial Miscanthus bioenergy plantation near Lincolnshire, UK.
  - Measurements include soil carbon, moisture, root and stone volume/mass, and bulk density per core increment.
  - Sampling occurred pre-tillage in 2011 (0–30 cm) and post-tillage in 2016 (0–1 m) following remedial tillage in 2013; includes a paired arable control (2011) and a paired un-tilled Miscanthus field (2016).

- Datasets and purpose
  - Lincoln_Miscanthus_Soil_C_Data: raw soil carbon data with per-core measurements and lab processing details. Includes metadata fields and formats (CSV).
  - Lincoln_Miscanthus_ESM_Soil_C_Data: soil carbon stocks calculated on an equivalent soil mass (ESM) basis for comparing land management impacts; provided for 0–30 cm and 0–70 cm depths using reference masses.

- Site details
  - Location: approximately 10 km north of Lincoln, UK; exact location embargoed to protect landowner privacy.
  - Site characteristics: Stagnogley soil over mudstone/chalk till; texture ~49% sand, 36% silt, 15% clay; pH 6.8–7.3; bulk density ~1.46–1.53 g cm-3.
  - Climate: mean annual temperature ~9.8°C; mean annual precipitation ~614 mm.
  - Management history: Miscanthus fields established 2006; Mis A tilled in 2013 to rectify gaps; Mis B left unmilled; adjacent arable field used for winter wheat/OSR.

- Monitoring and sampling design
  - Sampling protocol (2011): five randomly selected plots per field; three cores per plot (total 15 cores per field) to 0–30 cm.
  - Sampling protocol (2016): same five locations for Mis A; three new locations for Mis B; three cores per location with three 1 m cores and six 0–30 cm cores; cores sectioned in 10 cm increments (0–1 m total depth for some cores; 0–30 cm for others).
  - Observations recorded per core increment: land management, date sampled, stone/root weight and volume, soil moisture, carbon concentration, bulk density, and oven-dried soil mass.

- Laboratory methods and data processing
  - Core processing: drying, sieving to 2 mm, moisture loss, stone/root volume measured; oven-dry mass calculated.
  - Carbon analysis: ball-milled subsamples analyzed for total carbon using an elemental analyzer (CN); inorganic C removed with HCl prior to analysis.
  - Calibration and quality control: standards run at start and periodically; drift corrections applied.
  - Data handling: CSV data files with detailed field descriptions; pseudo-replicated soil pH values; data gaps noted.

- Data structure and key fields
  - Core/Depth, Land_management, Field_id (Arable, Mis A, Mis B), Date sampled, Plot, Depth_Range, Wet Core wt, Core Stone Wt, Core Roots Wt, Moisture content, Carbon conc, Core volume, Bulk density, Carbon stock, Soil oven-dried mass, Soil pH.
  - ES data fields: ESM_30_Mg C ha-1, ESM_70_Mg C ha-1, FD_30, FD_70; detailed field and core-level descriptors for ES calculations.

- Provenance, quality, and caveats
  - Provenance and related work: Rowe et al. (2020); Morrison et al. (2019); Drewer et al. (2012); Reynolds et al. (2013); Robertson et al. (2017); Rowe et al. (2023).
  - Key caveat for monitoring use: Lincoln_Miscanthus_Soil_C_Data should not be used directly to compare soil C stocks across land uses due to changes in bulk density over time/land use; use Lincoln_Miscanthus_ESM_Soil_C_Data for cross-plot/land-use comparisons.
  - Privacy: exact observation location withheld; dataset notes location details and climate/soil context.

- Implications for monitoring frameworks
  - Metadata and data provenance are explicit, enabling traceability and reproducibility of stock calculations.
  - The need to use ES-based stocks for fair comparisons highlights the importance of standardising metrics (e.g., equivalent soil mass) in monitoring frameworks.
  - Data governance considerations include openness of underlying data, sharing of core datasets, and maintaining data standards at the source to support transparency.
  - Potential barriers identified: data gaps, data access/timeliness, organizational silos, and metadata shortcomings requiring clarification from originators.
  - The dataset supports model development and alternative stock calculations, with explicit depth definitions and field IDs to enable cross-site comparability if standardized.

- Related datasets and references
  - Lincoln_Miscanthus_ESM_Soil_C_Data: ES-based soil carbon stocks for 0–30 cm and 0–70 cm depths.
  - Key references: Rowe et al. (2020); Rowe et al. (2016, 2023); Morrison et al. (2019); Drewer et al. (2012); Reynolds et al. (2013); Robertson et al. (2017).