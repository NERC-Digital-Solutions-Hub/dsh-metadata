# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 1750 - 2018

- The dataset provides annual total atmospheric deposition (heavy metals, nitrogen, and sulphur) over the UK for 1750–2018, generated with the EMEP4UK model rv4.36 and the WRF model v4.2.2.
- Outputs cover surface concentrations and dry/wet deposition, including cadmium, copper, nickel, lead, zinc, oxidised/reduced nitrogen, oxidised sulphur, and rainfall.

## Purpose and scope

- Purpose: to support environmental health monitoring, policy scrutiny, and informing future decisions by providing long-term deposition estimates.
- Coverage: 1750–2018 with outputs for decadal intervals from 1750–1990, every 5 years around 2005–2010, and the year 2018; UK domain at high resolution nested within a European domain.
- Uses: suitable for assessing trends, informing emission control strategies, and evaluating policy impacts on environmental health indicators.

## Modeling framework and inputs

- Atmospheric chemistry transport model: EMEP4UK rv4.36, derived from EMEP MSC-W rv4.36; simulates hourly to annual deposition for multiple pollutants.
- Meteorology: 3D fields from the Weather Research and Forecasting (WRF) model v4.2.2 with data assimilation of NCEP/NCAR reanalysis.
- Domain and resolution: EU domain at 27 × 27 km2 with a nested UK domain at 3 × 3 km2.
- Emissions inputs:
  - UK anthropogenic emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOCs) from 2019 National Atmospheric Emission Inventory (NAEI), rescaled to 2018.
  - Non-UK emissions from CEIP 0.1° × 0.1° data; UK total used for 2018.
  - Historical heavy metal emissions (1750–1960) from literature; contemporary emissions (1970–2018) from UK emissions inventory.
  - Projections (2040, 2070, 2100) use UK-specific SSPs.
- References and provenance: emissions and model descriptions are linked to multiple cited studies (e.g., Tomlinson 2023; Vieno et al. 2016a,b; Ge et al. 2021).

## Data products and variables

- NetCDF data files: 30 files named EMEP4UK_met2018_emisYYYY.nc, where YYYY denotes the year; output year coverage matches the described temporal scheme.
- Spatial-temporal structure:
  - Grid: longitude-latitude grid (240 × 240 in each file; supports 0.1° resolution for non-UK emissions, with UK-specific finer resolution).
  - Time: time dimension (currently 1 per file; model outputs aligned to mid-year for the meteorological year).
  - Vertical: lev and ilev dimensions indicating model levels (volumetric deposition are area-weighted).
- Reported variables (examples):
  - Dry deposition: oxidised sulphur (DDEP_SOX_m2Grid), oxidised nitrogen (DDEP_OXN_m2Grid), reduced nitrogen (DDEP_RDN_m2Grid), cadmium (DDEP_CD_m2Grid), copper (DDEP_CU_m2Grid), nickel (DDEP_NI_m2Grid), lead (DDEP_PB_m2Grid), zinc (DDEP_ZN_m2Grid).
  - Wet deposition: oxidised sulphur (WDEP_SOX), oxidised nitrogen (WDEP_OXN), reduced nitrogen (WDEP_RDN), cadmium (WDEP_CD), copper (WDEP_CU), nickel (WDEP_NI), lead (WDEP_PB), zinc (WDEP_ZN).
  - Rainfall (WDEP_PREC).
  - Area grid: Grid area (Area_Grid_km2).
- Units and post-processing:
  - Units provided per variable in NetCDF files; post-processing includes extraction of target variables.
  - NetCDF conforming structure with explicit variable naming conventions for deposition components.

## Data quality and governance

- Quality assurance: full QA/QC performed for 2018; visual QA for historical and future runs. QA/QC reports available on request.
- Documentation and risk: the dataset carries a note that use is at the user’s risk; no warranty of error-free content.
- Metadata and sharing: underlying data sharing and metadata practices are acknowledged as potential barriers in monitoring contexts; underlying data availability is subject to governance and data-sharing constraints as noted in related methodological guidance.

## Access, structure, and usage notes

- Data access: 30 NetCDF files containing annual outputs; model outputs are organized for each year with the specified naming convention.
- Data structure: global and UK-specific deposition fields regridded to the model’s grid; explicit variable naming allows traceability from deposition component to pollutant.
- Documentation references: technical descriptions and model evaluations cited in the associated bibliography (e.g., Ge et al. 2021; Jalkanen et al. 2016; Simpson et al. 2012).
- Typical user considerations for monitoring frameworks:
  - Long-term, policy-relevant deposition trends across 1750–2018 enable evaluation of historic and prospective policy impacts.
  - The combination of dry and wet deposition, plus metal species and nitrogen/sulphur forms, supports comprehensive environmental health assessments.
  - Potential barriers include metadata completeness, data governance constraints, and the need to access QA reports and original data sources for full reproducibility.

## Implications for monitoring and policy evaluation

- Provides a robust historical baseline and scenarios for UK deposition of heavy metals, nitrogen, and sulphur, aiding policy appraisal and decision-making.
- Supports crosswalks between emissions inventories, atmospheric transport models, and deposition outcomes for environmental health indicators.
- Highlights governance considerations (data sharing, metadata, timeliness) relevant to monitoring framework authors aiming to improve data usefulness and accessibility.