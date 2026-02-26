# Data sets

## Lincoln_Miscanthus_Soil_C_Data
- Description: Results from analysis of soil cores from a commercial Miscanthus bioenergy plantation near Lincolnshire, with measurements for each core (and increments to 1 m depth) including soil carbon, soil moisture, root and stone volume, and bulk density. Samples taken pre-tillage (2011) and post-tillage (2016; tilled 2013). Includes samples from a paired arable control field (2011) and a paired un-tilled Miscanthus field (2016). Surface soil data (0-30 cm) for 2011 and full profile (0-1 m) for 2016.
- Site details: Commercial private farm ~10 km north of Lincoln, UK; exact location embargoed. Miscanthus fields 11 ha each; arable field 7.5 ha. Stagnogley soil, with pH 6.8–7.3, bulk density ~1.46–1.53 g cm-3, and a temperate maritime climate (mean annual temp ~9.8°C, precip ~614 mm).
- Sampling design: 
  - 2011: five randomly selected plots per field; three soil cores per plot to 30 cm (total 15 samples per field).
  - 2016: same protocol but depth extended to 1 m at three sampling locations using a window sampler; sampling yielded 15 cores per field (nine from 1 m and six from 0-30 cm); increments sampled in 10–cm or 15–cm ranges as described.
- Measurements and processing:
  - Field: core sections measured for soil moisture, stone and root mass/volume; bulk density (fine earth density) calculated from core volumes.
  - Lab: oven-dry soil mass, carbon concentration (via elemental analyzer after acid treatment to remove inorganic C with HCl), moisture loss, and stone/root volumes recorded.
  - QA/metadata: standard GB Countryside Survey methods referenced; data formatted as CSV; extensive dataset descriptions and field metadata included.
- Important caveat: Lincoln_Miscanthus_Soil_C_Data should not be used directly to compare soil carbon stocks across land-use types due to bulk density changes between uses and over time. For cross-management comparisons, use Lincoln_Miscanthus_ESM_Soil_C_Data.
- File formats and fields: Includes detailed field descriptions, land management categories (Arable, None tilled Miscanthus, post tillage Miscanthus, pre tillage Miscanthus), field IDs (Arable, Mis A, Mis B), sampling year, plot, core, depth ranges, core measurements (wet weight, stone/root mass, moisture, carbon concentration, dry weight), core volume, bulk density, carbon stock per core, and aggregated totals. Data gaps noted where data are missing.
- Related information: Metadata and dataset descriptions reference Rowe et al. (2023) and other linked publications for site history and methods.

## Lincoln_Miscanthus_ESM_Soil_C_Data
- Purpose: Soil carbon stocks calculated on an equivalent soil mass (ESM) basis for tilled and untilled Miscanthus fields and the paired arable control, enabling fair comparisons of soil carbon across land-management scenarios.
- ESM approach: Uses equation SCESM = SCupper + (ConcLower × (Mref − Mupper)) to convert C stocks to an equivalent soil mass. Upper and lower sections defined as:
  - 0-30 cm: upper 0-20 cm (0-10 cm + 10-20 cm) and lower 20-30 cm.
  - 0-70 cm: upper 0-60 cm and lower 60-70 cm.
  - Reference soil masses: 4,000 Mg ha-1 (0-30 cm) and 10,390 Mg ha-1 (0-70 cm), based on median core masses.
- Depths and data: C stock calculations provided for 0-30 cm and 0-70 cm depths for each core; 0-70 cm data only available for 2016 cores. Includes both ESM-derived values (ESM_30_Mg C ha-1, ESM_70_Mg C ha-1) and fixed-depth equivalents (FD_30, FD_70) with cautions on use for cross-land-use comparisons.
- Site and samples: Derived from the Lincoln_Miscanthus_Soil_C_Data framework, with the same field layout (Mis A, Mis B, Arable) and sampling design across years as described above.
- Data fields: Includes land management, field ID, sampling year, plot, core, and ES M calculations (ESM_30_Mg C ha-1, ESM_70_Mg C ha-1) and fixed-depth equivalents (FD_30, FD_70), along with standard metadata fields (calibration notes, data formats, and quality indicators).
- File formats and quality: CSV format; data gaps acknowledged; designed to support model development and alternative C stock calculations that account for variable soil mass.
- References and context: Describes the ES M method from Gifford & Roderick (2003) and provides linked references for site history and prior studies (e.g., Rowe et al., 2016; Morrison et al., 2019).