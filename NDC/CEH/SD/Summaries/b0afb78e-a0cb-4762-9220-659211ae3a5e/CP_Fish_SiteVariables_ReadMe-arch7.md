# CP_Fish_SiteVariables_readme.txt

## Aim and scope
- Dataset documenting site variables (invariable covariates) for NFPD fish sites in English rivers (1975–2017).
- Covariates include habitat quality indicators (HQS, HMS) and physical site characteristics (altitude, land use, wastewater influence, and Base Flow Index).

## Data structure and files
- Data organized as regional files by region: Anglian, Midlands, North East, North West, Thames, Southern, and South West.
- A single Species table exists to indicate species referred to in Fish_SpeciesCode.
- Primary data file: CP_Fish_SiteVariables_Region.csv (region-specific) containing 18 variables for each site.
- Relationship: Fish_SiteID links to corresponding entries in DataTable files, Hydrology files, and chemical determinand files.
- Versions: dataset has multiple versions; notable update 2021-11-16 (HIFI_JuvenileFish_England_SiteTable) where site covariates HMS, HQS, and certain land-use/BFI fields were removed from the data table and the file split into regional files. Updated 2022-05-31 and 2022-08-12.

## Provenance and data sources
- HQA (Habitat Quality Assessment) and HMS (Habitat Modification Score) derived from River Habitat Survey (RHS). RHS sites linked to the nearest fish site within a 5 km river section; data extracted from RHS results portal. Early HQA data (1994) differ from later years; protocols updated to enable year-to-year comparability.
- Land use: upstream catchment land cover (21 categories) derived from CEH Land Cover Map 2015 (LCM2015), resampled to align with CEH IHDTM 50 m elevation data; categories pooled into four macro-groups:
  - Woodland
  - Arable
  - Seminatural
  - Urban
- Altitude: metres above sea level, sourced from CEH IHDTM 50 m elevation data; two values computed (cell-centre value and bilinear-averaged value); the cell-centre value used.
- BFI (Base Flow Index): derived from CEH National Flow Archive.
- EDF (Effluent Dilution Factor): wastewater influence modelled as a percentage of WW treatment works discharge using the LF2000-WQX model (LowFlows2000). Significant WWTWs retained (those contributing ~90% of dry-weather flow or within catchments contributing to 95% of each hydrometric area). Fish sites matched to the LF2000-WQX river network; site EDF values extracted.

## Data processing workflow (GIS-focused)
- HQA/HMS: RHS scores linked to the nearest fish site (within 5 km along river) via IRN extension; some sites may not be matched.
- Land use processing: 
  - Generate 21 land-use category rasters from LCM2015 aligned to IHDTM.
  - Use GRASS GIS r.accumulate to create accumulation rasters representing upstream catchment proportions per category.
  - DataLabs used to extract upstream land-use percentages and areas (km2) for each fish site.
  - Aggregate 21 categories into four macro-categories and validate that totals approximate 100%.
- EDF processing:
  - Link fish sites to the closest reach on the 1:50,000 river network and to the LF2000-WQX model output.
  - Compute EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95 per site.
- Altitude processing: use IHDTM elevation; select center-value elevation for each site.
- Data filtering and QA:
  - NFPD data filtered to sites with at least 10 surveys; juvenile fry removed.
  - Distances between fish sites and RHS reference points checked (≤1 km deemed acceptable).
  - Sum checks on macro-categories to ensure totals near 100%.
  - EDF data handling: if discrepancies arise and a river stretch is omitted, corresponding site data may be left blank.
  Nodata handling: estuarine/low-data areas treated appropriately (e.g., elevation set to 0 m where necessary).

## Software/tools and interpretive notes
- GIS and analysis tools required:
  - ArcGIS (10.7+ or ArcGIS Pro) for land use and altitude processing.
  - GRASS GIS (via r.accumulate) for land-use accumulation rasters.
  - DataLabs for CEH Catchment Tool and extracting land-use metrics.
  - Python for linking sites to LF2000-WQX network and EDF values.
- Data interpretation requires joining region CSV files with the corresponding data tables via Fish_SiteID.

## Data specifics
- CP_Fish_SiteVariables_Region.csv
  - Number of rows/columns: region-dependent
  - Number of variables: 18
  - Key variables (examples):
    - Fish_SiteID, Fish_Name, Fish_River, Fish_Catchment, Fish_Easting, Fish_Northing
    - HQA_Score, HMS_Score
    - Fish_Altitude
    - LC_Woodland_Per, LC_Arable_Per, LC_Seminatural_Per, LC_Urban_Per
    - LC_Woodland_Area, LC_Arable_Area, LC_Seminatural_Area, LC_Urban_Area
    - BFI
    - EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95
    - ED_SITE_ID

## Quality assurance
- Distances between fish sites and nearest RHS points verified; acceptable if <1 km.
- Macro-category sums consistently near 100% (99.96–100.04%).
- EDF data gaps flagged when modelled network exclusions occur; such sites are left as no data.
- Elevation nodata handled appropriately (e.g., estuarine areas or below sea level treated as 0 m).

## Usage and interpretation notes for GIS specialists
- The dataset supports regional, map-based analyses of static site covariates for fish sites.
- Ensure consistent software environments (ArcGIS Pro/ArcGIS 10.7+, GRASS GIS, DataLabs, Python) to reproduce processing steps.
- When combining region files, use Fish_SiteID as the primary key; understand the linkage with hydrology and chemical determinand files.
- Be aware of versioned updates: covariate sets may have been removed or reorganized in newer releases; verify the version date for reproducibility.

## References
- Dawson, F. H., et al. (2002). Automated extraction of environmental variables for river classification.
- Gustard, A., et al. (1992). Low flow estimation in the United Kingdom.
- Young, A.R., et al. (2003). Low Flows 2000: national resources assessment.
- Williams, R.J., et al. (2009). A national risk assessment for intersex in fish.