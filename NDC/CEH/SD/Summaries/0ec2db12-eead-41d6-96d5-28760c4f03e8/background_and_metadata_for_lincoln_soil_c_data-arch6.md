# Data sets Lincoln_Miscanthus_Soil_C_Data Lincoln_Miscanthus_ESM_Soil_C_Data

## Overview
- Two datasets from a commercial Miscanthus x giganteus plantation near Lincolnshire, UK, with arable controls.
- 2011 sampling (0–30 cm) across fields; 2016 sampling extended to 1 m depth at selected locations.
- Lincoln_Miscanthus_Soil_C_Data contains raw soil carbon data per core increment.
- Lincoln_Miscanthus_ESM_Soil_C_Data contains soil carbon stock calculated on an equivalent soil mass (ESM) basis for comparison across land uses.

## Datasets at a glance
- Lincoln_Miscanthus_Soil_C_Data
  - Raw soil carbon data by core increments; depths 0–30 cm (2011) and up to 1 m (2016).
  - Includes paired arable control and a paired un-tilled Miscanthus field; Miscanthus fields Mis A and Mis B.
  - For each core increment, records include land management, date, depth, wet core weight, stone/root mass and volume, soil moisture, carbon concentration, bulk density, and derived carbon stock.

- Lincoln_Miscanthus_ESM_Soil_C_Data
  - Calculated soil carbon stocks based on equivalent soil mass (ESM) for 0–30 cm and 0–70 cm depths.
  - Provides reference masses (4,000 Mg ha-1 for 0–30 cm; 10,390 Mg ha-1 for 0–70 cm) and corresponding ESMapplied stocks (ESM_30 and ESM_70) along with fixed-depth equivalents (FD_30, FD_70).
  - Keeps core-level and location-level context with fields describing land management and sampling details.

## Site context
- Location: site near Lincoln, UK; precise coordinates withheld to protect privacy.
- Land use: 11 ha Miscanthus fields; adjacent arable field (winter wheat and oilseed rape) at 7.5 ha.
- Soil: Stagnogley over mudstone/chalk till; texture ~49% sand, 36% silt, 15% clay; pH 6.8–7.3; bulk density ~1.46–1.53 g cm-3.
- Climate: mean annual temperature ~9.8°C; mean annual precipitation ~614 mm.

## Sampling and measurement methods
- 2011: five random sampling plots per field; three soil cores per plot; depth to 30 cm.
- 2016: three locations extended to 1 m; five sampling plots per field; cores sectioned into increments (0–30 cm and 0–1 m with 10 cm increments).
- Core processing: oven-dried mass, moisture content, stone/root mass and volume; carbon content via ball-milled subsample analyzed by elemental analyzer after inorganic C removal with HCl.
- Quality control: use of standards and drift correction; data include calibration procedures and pseudo-replication notes for pH.

## Data structure and formats
- File format: CSV for both datasets.
- Key fields (examples): Land_management, Field_id, Date_sampled, Plot, Core, Depth_Range, Depth_Code, Wet Core wt, Stone_and_Root Vol., Moisture content, Carbon conc (%), Bulk density, Core_Soil_dry_weight, Carbon (t C ha-1), Soil oven-dried mass (t ha-1), pH.
- ESM dataset includes: ESM_30_Mg C ha-1, FD_30, ESM_70_Mg C ha-1, FD_70, with corresponding field descriptions.

## Provenance, calibration, and data quality
- Primary sources: Rowe et al. (2020, 2023), Morrison et al. (2019), Reynolds et al. (2013), Roberson et al. (2017), Drewer et al. (2012).
- Data steward: Rebecca Rowe; field sites described in associated publications.
- Important caveats:
  - Lincoln_Miscanthus_Soil_C_Data should not be used directly for comparing soil C stocks across land uses due to bulk-density changes.
  - ES M_Soil_C_Data is specifically designed for land-use comparison, using standardized reference masses.
  - Gaps exist in the data; some fields have pseudo-replication for pH; analysis should use data summarized by sampling location where appropriate.

## Usage guidance
- Best for developing models or methods that account for bulk density changes in soil C stock assessment.
- Use Lincoln_Miscanthus_ESM_Soil_C_Data for cross-field land-use comparisons and carbon-stock budgeting where equivalent soil mass is required.
- The dataset descriptions provide depth definitions for upper/lower sections (e.g., 0–10 cm + 10–20 cm as upper for 0–30 cm; 20–30 cm as lower; for 0–70 cm, upper is 0–60 cm, lower is 60–70 cm).

## Related metadata and references
- References to field studies and data products underpinning the datasets (Rowe et al., 2020; Rowe et al., 2023; Morrison et al., 2019; Drewer et al., 2012; Reynolds et al., 2013; Robertson et al., 2017).

## What’s included ( Field descriptions and variables)
- Land management status (Arable, Mis A, Mis B; pre-/post-tillage, none tilled).
- Spatial and temporal identifiers (Field_id, Plot, Date sampled).
- Core-level measurements (Depth_Range, Core, Wet Core wt, Core_Soil_dry_weight, Carbon conc, Bulk density, Moisture content, Stone and Root Vol., Core volume).
- Stock calculations (Carbon stock in t C ha-1) and lab metrics (Soil oven-dried mass, pH).
- For ESM data: ESM and FD values for 30 cm and 70 cm depths.