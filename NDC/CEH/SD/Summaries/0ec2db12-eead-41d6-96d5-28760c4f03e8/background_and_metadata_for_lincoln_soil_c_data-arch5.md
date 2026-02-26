# Data sets Lincoln_Miscanthus_Soil_C_Data and Lincoln_Miscanthus_ESM_Soil_C_Data

## Purpose and scope
- Two related datasets from a commercial Miscanthus plantation near Lincoln, UK.
- Lincoln_Miscanthus_Soil_C_Data: raw soil carbon stock data from cores at multiple depths and years (2011 0-30 cm; 2016 up to 1 m), including paired arable control and un-tilled Miscanthus field.
- Lincoln_Miscanthus_ESM_Soil_C_Data: soil carbon stock calculated on an equivalent soil mass (ESM) basis for 0-30 cm and 0-70 cm depths, enabling fair comparison across land uses with changing bulk density.

## Location and site context
- Site: private farm about 10 km north of Lincoln; exact coordinates embargoed to protect landowner privacy.
- Fields: two Miscanthus fields (Mis A tilled in 2013; Mis B never tilled) and a paired arable field (winter wheat/oilseed rape).
- Soils: Stagnogley with sand/silt/clay mix; pH 6.8–7.3; bulk density around 1.46–1.53 g cm-3.
- Climate: temperate maritime; mean annual temperature ~9.8°C; mean annual precipitation ~614 mm.

## Temporal coverage and sampling design
- 2011: sampling across five randomly selected plots per field; three cores per plot to 30 cm (total 15 samples per field).
- 2016: same protocol with depth extension at three locations to 1 m; five plots per field; cores sectioned into increments (0-10, 10-20, 20-30 cm or up to 1 m in some locations).
- Two paired comparisons included: Miscanthus vs arable control; tilled vs untilled Miscanthus fields.

## Provenance and data quality
- Field methods: split-tube sampler for 0-30 cm (2011); window sampler to 1 m at three locations (2016); standard GB Countryside Survey processing for soil mass, moisture, roots, stones.
- Laboratory methods: oven-dry mass, moisture content, root/stone mass; carbon content measured by elemental analysis after acid treatment to remove inorganic C; calibration and drift correction with standards.
- Data quality notes: standard procedures and metadata describe calibration, quality checks, and data processing; gaps indicated in the data; pH values are pseudo-replicated for processing ease.
- Data lineage: detailed metadata provided, including staff responsible (Rebecca Rowe) and references to underpinning methods.

## Dataset contents and structure
- Lincoln_Miscanthus_Soil_C_Data:
  - For every core increment: land management, date, depth, soil dry mass, moisture, root/stone mass and volume, bulk density, carbon concentration and total carbon stock (t C ha-1), soil oven-dried mass (t ha-1), pH, core volume metrics, and related fields.
  - CSV format; includes dataset field definitions and descriptions.
- Lincoln_Miscanthus_ESM_Soil_C_Data:
  - Calculated soil C stocks based on equivalent soil mass for 0-30 cm and 0-70 cm depths (ESM_30 and ESM_70).
  - Includes reference masses (4,000 Mg ha-1 for 0-30 cm; 10,390 Mg ha-1 for 0-70 cm) and the SCESM equation.
  - Also includes fixed-depth equivalents (FD_30, FD_70) for comparison, with notes that FD data are not recommended for cross-land-use comparisons.
  - CSV format; includes dataset field descriptions and metadata on ESM calculations.

## How this supports data stewardship and governance
- Standardized data formats and rich metadata to facilitate discoverability and reuse (CSV files with explicit field definitions, units, and processing steps).
- Clear provenance and methodological transparency (sampling design, lab procedures, calibration, and references).
- Governance considerations:
  - Location privacy: exact coordinates embargoed.
  - Embargoed site details alongside published methods enable responsible data sharing while protecting privacy.
  - Documentation distinguishes raw (0-30 cm) data from processed, comparable (ESM) data, guiding appropriate use.
- Data sharing and reuse guidance:
  - Use Lincoln_Miscanthus_ESM_Soil_C_Data for comparing soil carbon stocks across land uses due to bulk density adjustments.
  - Use Lincoln_Miscanthus_Soil_C_Data for model development or alternative calculations that account for bulk density changes.
- Data quality and limitations:
  - Acknowledgement of gaps in data; pseudo-replication for pH; data should be used with metadata describing processing and limitations.
  - Methods align with published standards (GB Countryside Survey; Gifford & Roderick 2003; Rowe et al. references).

## Related literature and references
- Drewer et al. 2012; Morrison et al. 2019; Reynolds et al. 2013; Robertson et al. 2017; Rowe et al. 2020/2023; additional context in Rowe et al. (2016).

## Access and contact
- Staff responsible: Rebecca Rowe.
- Data formats: CSV.
- Site privacy considerations and reliance on published methods for reproducibility and cross-study comparability.