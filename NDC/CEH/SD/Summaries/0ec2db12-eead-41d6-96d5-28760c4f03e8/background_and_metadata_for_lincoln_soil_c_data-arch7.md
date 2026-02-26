# Lincoln_Miscanthus_Soil_C_Data

- Datasets describe soil core analyses from a commercial Miscanthus bioenergy plantation near Lincolnshire, UK, with measurements up to 1 m depth and increments (0–30 cm for 2011; 0–1 m for 2016).
- Core per-field measurements include soil carbon, soil moisture, root and stone mass/volume, and bulk density.
- Sampling events: pre-tillage in 2011 and post-tillage in 2016 (remedial tillage conducted in 2013). Includes a paired arable control field (sampled in 2011) and a paired unretilled Miscanthus field (sampled in 2016).
- Data supports model development and alternative soil carbon stock calculations, with explicit guidance on when not to use raw data for land-use comparisons due to bulk density changes.

## What the dataset contains

- For every core increment: land management, date sampled, depth range, core identifiers, physical weights (wet and oven-dried), stone and root volumes, moisture content, bulk density, carbon concentration, core volume, and derived carbon stock metrics.
- Primary outputs: carbon stock (t C ha-1), oven-dried soil mass (t ha-1), soil pH; CSV format for interoperability with GIS workflows.
- Metadata fields describe dataset naming, field IDs (Arable, Mis A, Mis B), sampling plots, depth ranges, and core-specific measurements.

## Site context and provenance

- Location: approximately 10 km north of the City of Lincoln, Eastern England; exact location embargoed to protect landowner privacy.
- Site details: commercial farm with Miscanthus and other crops; climate: mean annual temperature ~9.8°C, precipitation ~614 mm; soil type: Stagnogley over clay-till with texture ~49% sand, 36% silt, 15% clay; bulk density ~1.46–1.53 g cm-3.
- Management history: Miscanthus fields (11 ha each) established around 2006; one Miscanthus field tilled in 2013 to address crop gaps, the other left untilled; an adjacent arable field used for winter wheat/oilseed rape.

## Sampling and laboratory methods

- 2011: five random plots per field; three cores per plot to 30 cm (15 samples per field).
- 2016: sampling extended to 1 m at three locations; remaining locations sampled to 30 cm; consistent protocol with 2011 but expanded depth.
- Laboratory processing followed GB Countryside Survey methods: oven-dried mass, moisture, root/stone mass, HCl treatment to remove inorganic C, CN analysis; standards and drift corrections applied.
- Data quality notes: 2011 and 2016 sampling followed published protocols; data gaps indicate missing data.

## Lincoln_Miscanthus_ESM_Soil_C_Data (Equivalent Soil Mass)

- Contains soil carbon stock calculations based on an equivalent soil mass (ESM) approach for tilled/untilled Miscanthus fields and paired arable field.
- Depths: 0–30 cm and 0–70 cm (with corresponding reference masses of 4,000 Mg ha-1 and 10,390 Mg ha-1).
- Calculation: SCESM = SCupper + (ConcLower × (Mref − Mupper)); upper/lower sections defined per depth (e.g., 0–10 and 10–20 cm upper, 20–30 cm lower; for 0–70 cm, upper is 0–60 cm, lower 60–70 cm).
- Purpose: enable robust comparisons of soil carbon stock across land uses by correcting for bulk density changes.
- Data includes fields for ESM values (30 cm and 70 cm), fixed-depth comparisons, and related metadata.

## Data formats and access

- File formats: CSV for both Lincoln_Miscanthus_Soil_C_Data and Lincoln_Miscanthus_ESM_Soil_C_Data.
- Dataset fields include: land_management, field_id (Arable, Mis A, Mis B), date sampled, plot, core number, depth ranges, core measurements (wet weight, stone/root weight and volume, moisture content, bulk density, carbon concentration, core volume), soil carbon stock (t C ha-1), soil oven-dried mass (t ha-1), soil pH, and derived ES.M. metrics (ESM 30/70 Mg C ha-1; FD 30/70).
- Metadata notes emphasize data provenance, processing steps, calibration, and quality control.

## How this data supports GIS analysis

- Provides depth-resolved soil carbon and related properties suitable for creating GIS layers of soil carbon stocks by depth.
- Enables spatial comparisons between land uses (Miscanthus vs arable) and assessment of tillage effects when using appropriate ES.M. adjustments.
- Depth-structured core data allows interpolation or aggregation to form map-ready soil carbon surfaces at varying depths.
- Rich ancillary fields (bulk density, pH, moisture, stone/root content) support more accurate carbon stock calculations and soil property mapping.

## Cautions and recommended usage

- For land-use impact comparisons, prefer Lincoln_Miscanthus_ESM_Soil_C_Data over raw Lincoln_Miscanthus_Soil_C_Data due to bulk density changes over time.
- ES.M. calculations rely on reference soil masses; ensure consistent application of the equation SCESM = SCupper + (ConcLower × (Mref − Mupper)).
- Data are site-specific with embargoed precise location; use provided descriptive location and climate context for spatial modeling.
- Gaps in data exist; treat missing values accordingly in GIS analyses.

## Related references

- Drewer et al. (2012); Morrison et al. (2019); Reynolds et al. (2013); Robertson et al. (2017); Rowe et al. (2020, 2023) for methods and context.
- Used to inform soil carbon stock modeling, baselining for Miscanthus plantations, and comparisons with arable controls.