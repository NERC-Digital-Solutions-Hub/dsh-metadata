# CP_Fish_SiteVariables_readme.txt

## Overview
- WP/task: NFPD site variable data for fish sites in English rivers 1975-2017.
- Dataset: Site variables that do not change over time; covariates include habitat quality indicators (HQS and HMS) and physical site characteristics (altitude, land use, wastewater and BFI).
- Data authors: Ainsworth, R.F.; Nunn, A.D.; Bachiller-Jareno, N.; Rizzo, C.; Scarlett, P.; Antoniou, V.
- Structure: Site tables and Data tables are regional (Anglian, Midlands, North East, North West, Thames, Southern and South West); Species table is a single file for species referenced in Fish_SpeciesCode.

## Data contents and structure
- File CP_Fish_SiteVariables_Region.csv: information for individual NFPD fish sites (names, location, land use, habitat variables).
- Relationship: Fish_SiteID in region file matches Fish_SiteID in DataTable, Hydrology, and chemical determinand files.
- Versions: multiple versions exist; updated 20211116_HIFI_JuvenileFish_England_SiteTable.
- Update details: HMS, HQS land use and BFI removed from the data table; file split into regional files. Updates occurred 2022-05-31 and 2022-08-12.
- Region-specific organization: regional files accompany a single Species table indicating referenced species.

## Provenance and data sources
- Derived from: RHS habitat quality indicators HQA and HMS (habitat quality) and HQA/HMS data linked to the nearest fish site via RHS surveys.
- Altitude: CEH Integrated Hydrological Digital Terrain Model (IHDTM), 50 m resolution.
- Land use: CEH Land Cover Map 2015 (LCM2015); categories pooled into four macro groups.
- BFI: Base Flow Index from CEH National Flow Archive.
- EDF (Effluent Dilution Factor): modeled from LF2000-WQX to estimate wastewater contribution from significant wastewater treatment works (WWTWs).
- Data sources cited and linked to external datasets and models.

## Methodology and processing
- Data collection:
  - HQA/HMS: RHS survey scores matched to closest fish site within 5 km using ArcGIS IRN extension; earlier HQA data (1994) differs and has been standardized for comparability.
- Land use processing:
  - 21 land cover categories derived from LCM2015; aggregated to four macro-categories: Woodland, Arable, Sem-natural, Urban.
  - Upstream catchment areas computed with 25 m and 50 m rasters; proportions/areas calculated per fish site.
- Altitude processing:
  - Elevation values derived from IHDTM; two values computed, selected the cell-centre value for the dataset.
- EDF processing:
  - LF2000-WQX model used to estimate percentage wastewater; sites matched to nearest reach on the 1:50,000 river network; outputs include mean, SD, Q90, Q95.
- Data processing notes:
  - Distances between fish points and RHS reference points checked (≤1 km acceptable).
  - Land-use sums checked to near 100%.
  - EDF data may be blank if model network omitted; nodata cells treated as 0 m elevation for estuarine/low areas.
- Instrument/software:
  - ArcGIS (10.6.1+; or ArcGIS Pro), GRASS GIS (r.accumulate), DataLabs (Python), and LF2000-WQX tools.
- Quality assurance:
  - Spatial matching accuracy checks; macro-category sums validated; handling of missing data and potential mismatches documented.

## Data products and variable details
- Number of rows/columns: region-dependent (in CP_Fish_SiteVariables_Region.csv).
- Number of variables: 18.
- Key variables:
  - Fish_SiteID, Fish_Name, Fish_River, Fish_Catchment, Fish_Easting, Fish_Northing
  - HQA_Score, HMS_Score
  - Fish_Altitude
  - LC_Woodland_Per, LC_Arable_Per, LC_Seminatural_Per, LC_Urban_Per
  - LC_Woodland_Area, LC_Arable_Area, LC_Seminatural_Area, LC_Urban_Area
  - BFI
  - EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95
  - ED_SITE_ID

## Usage for monitoring and analysis
- Provides standardized, time-invariant covariates for fish sites to support environmental health assessments and policy performance monitoring over time.
- Enables cross-regional comparisons by harmonizing habitat, land-use, and hydrological covariates.
- Facilitates integration with other datasets (e.g., hydrology, chemical determinands) via the Fish_SiteID linkage.
- Useful for modelling habitat quality, land-use impacts, wastewater influence, and downstream ecological assessments.

## Quality and reliability
- Robust QA steps documented (spatial matching checks, category sum checks, handling of missing data).
- Some HQA data differences across years require standardized protocols for comparability.
- Data gaps (EDF) noted where the modeled river network excluded the site.
- Precautions regarding nodata and elevation zeroing in estuarine or below-sea-level contexts.

## Access and interoperability
- Data organized regionally; standard GIS tools required for interpretation and analysis (ArcGIS, GRASS GIS, DataLabs, Python).
- Data sharing includes provenance and references to external datasets and models for traceability and reproducibility.

## References
- Dawson, F. H., Hornby, D. D., Hilton, J. (2002). Automated extraction of environmental variables to help river classification. Aquatic Conservation.
- Gustard, A., Bullock, A., Dixon, J. M. (1992). Low flow estimation in the United Kingdom.
- CEH Land Cover Map 2015 (LCM2015).
- Young, A.R., Grew, R., Holmes, M.G.R. (2003). Low Flows 2000.
- Williams, R.J. et al. (2009). LowFlows2000-WQX and related environmental assessments.