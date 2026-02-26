# Lincoln_Miscanthus_Soil_C_Data

## Overview
- Two datasets described: Lincoln_Miscanthus_Soil_C_Data (soil core analysis) and Lincoln_Miscanthus_ESM_Soil_C_Data (equivalent soil mass–based soil carbon stocks).
- Measurements per core/increment: soil carbon, soil moisture, root and stone mass/volume, and bulk density.
- Temporal coverage: samples from 2011 (pre-tillage) and 2016 (post-remedial tillage conducted in 2013); includes a paired arable control (2011) and a paired un-tilled Miscanthus field (2016).
- Depth coverage: 2011 surface soil (0–30 cm); 2016 extended to 1 m; ES_M dataset covers 0–30 cm and 0–70 cm depths.

## Site context
- Location: commercial Miscanthus plantation near Lincolnshire, UK; precise location withheld to protect landowner privacy.
- Fields: two 11 ha Miscanthus fields; one 7.5 ha arable field (winter wheat and oilseed rape).
- Soil: Stagnogley over mudstone/chalk till; texture ~49% sand, 36% silt, 15% clay; pH 6.8–7.3; bulk density ~1.46–1.53 g cm-3.
- Climate: mean annual temperature ~9.8°C; mean annual precipitation ~614 mm.
- Management history: Miscanthus established 2006; Mis A tilled 2013; Mis B largely tilled/not tilled; arable field continuously cultivated.

## Data collection and processing (Provenance & quality)
- Sampling design:
  - 2011: five random plots per field; three soil cores per plot to 30 cm (total ~15 samples/field).
  - 2016: same sampling framework plus extension to 1 m depth at three locations; five sampling plots per field; cores sectioned into increments (up to 1 m; 0–30 cm data collected at most locations).
- Laboratory processing:
  - Core sections dried; moisture loss, volume, stone and root volume recorded.
  - Oven-dry soil mass determined; carbon content measured on ball-milled subsamples using an elemental analyzer after acid treatment to remove inorganic C (HCl).
  - pH measured on bulked samples.
- Calibration and quality control:
  - Calibration standards included; drift corrections applied; data gaps noted.
- Important caveat:
  - Due to bulk density changes across land uses and over time, Lincoln_Miscanthus_Soil_C_Data should not be used directly to compare land-use/land-management impacts on soil C stocks. For comparisons, Lincoln_Miscanthus_ESM_Soil_C_Data should be used.

## Data structure and formats
- Data formats: CSV files for both datasets.
- Lincoln_Miscanthus_Soil_C_Data: per-core/increment fields include Land_management, Field_id (Arable, Mis A, Mis B), Date sampled, Depth_Range, Wet Core weight, Stone and Root weight/volume, Moisture content, Carbon concentration, Core volume, Bulk density, Carbon stock (t C ha-1), Soil oven-dried mass (t ha-1), Soil pH, and related core descriptors (Core, Sample Plot, etc.).
- Lincoln_Miscanthus_ESM_Soil_C_Data: calculated soil C stock based on equivalent soil mass (ESM) for 0–30 cm and 0–70 cm:
  - ES_M values: ESM_30_Mg C ha-1, ESM_70_Mg C ha-1
  - Fixed-depth references: FD_30, FD_70
  - Upper/lower section definitions for ESM calculations (0–10 cm + 10–20 cm as upper; 20–30 cm as lower for 0–30 cm; 0–60 cm upper; 60–70 cm lower for 0–70 cm)
  - Reference dry soil masses: 4,000 Mg ha-1 (0–30 cm) and 10,390 Mg ha-1 (0–70 cm)
  - Equation used: SCESM = SC_upper + (ConcLower × (Mref − Mupper))
- Metadata and field descriptions included; data are organized to support model development and alternative ES_M calculations.

## How to use the data (analytical guidance)
- For cross-field comparisons of soil C stocks under different management, prefer Lincoln_Miscanthus_ESM_Soil_C_Data due to bulk density adjustments.
- Lincoln_Miscanthus_Soil_C_Data provides rich site-specific measurements (carbon concentration, moisture, roots, stones, bulk density) across depths and time, suitable for process understanding and model calibration.
- The ES_M dataset enables robust comparisons by normalizing soil mass, with explicit reference masses and depth definitions, suitable for assessing land-use impacts.

## Related information and references
- Key publications and datasets cited for context and methods, including:
  - Drewer et al. (2012)
  - Morrison et al. (2019)
  - Reynolds et al. (2013)
  - Robertson et al. (2017)
  - Rowe et al. (2020, 2016, 2023)
- Dataset provenance and management are tied to Rowe et al. (2023) and related methodological sources.