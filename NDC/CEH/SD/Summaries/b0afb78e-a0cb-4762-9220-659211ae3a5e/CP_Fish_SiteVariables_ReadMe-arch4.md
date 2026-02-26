# CP_Fish_SiteVariables_readme.txt

## Overview
- Describes the NFPD site variable data for fish sites in English rivers (1975–2017), including covariates such as habitat quality indicators (HQS/HMS) and physical site characteristics (altitude, land use, wastewater indicators, BFI).
- Data structure spans regional site tables and a single species table; multiple versions exist with updates noted.

## Data Structure and Content
- Site tables and Data tables are formatted as separate regional files (Anglian, Midlands, North East, North West, Thames, Southern, South West). A single Species table references species in the Fish_SpeciesCode column in the data tables.
- File List:
  - CP_Fish_SiteVariables_Region.csv: information on individual NFPD fish sites (names, location, land use, habitat variables).
- Relationship:
  - Fish_SiteID links across CP_Fish_SiteVariables_Region.csv and DataTable, Hydrology, and chemical determinand files.
- Multiple versions exist; updated file noted as 20211116_HIFI_JuvenileFish_England_SiteTable (changes include removal of HMS, HQS, and BFI covariates from the data table and splitting into regional files).

## Provenance and Data Sources
- Data derived from:
  - HQA and HMS: River Habitat Survey (RHS) habitat quality indicators; matched to closest fish site using a 5 km rule.
  - Land use: CEH Land Cover Map 2015 (LCM2015); categories collapsed into four macro-classes (Woodland, Arable, Semiinatural, Urban).
  - Altitude: CEH IHDTM elevation data (50 m resolution).
  - BFI: Base Flow Index from CEH National Flow Archive.
  - EDF: Effluent Dilution Factor modeled from LF2000-WQX to estimate wastewater influence.
- References and data sources for methods and models are provided (Dawson et al., Gustard et al., Young et al., Williams et al., etc.).

## Data Processing and Methods
- HQA/HMS: RHS survey-derived scores; matched to the nearest fish site; some sites could not be matched.
- Land use: Upstream catchment land cover calculated from LCM2015; 21 categories aggregated into four macro-categories; processed with ArcGIS GRASS and DataLab Python to obtain percentage and area upstream from each fish site.
- Altitude: Elevation values extracted from IHDTM for each site; two values computed (cell-centre value and bilinear-interpolated average); NoData values ignored except when all adjacent cells are NoData.
- EDF: Wastewater percentage modeled with LF2000-WQX; significant WWTWs retained; Python used to map fish sites to the river network and extract EDF values; results include mean, SD, Q90, Q95.
- Data filtering: NFPD data filtered to sites surveyed at least 10 times from 1975–2017; juvenile fry sites removed; RHS data used to fill HQA/HMS; EDF values mapped to the closest river network reach.

## Software and Tools Required
- Land cover/altitude analyses require ArcGIS (10.7+ or ArcGIS Pro) and CEH IHDTM/LCM2015 data; GRASS GIS for land use aggregation; DataLabs for land cover extraction.
- EDF processing uses Python and the 1:50,000 river network from OS Panorama; LF2000-WQX model for wastewater distributions.

## Quality Assurance and Data Checks
- Spatial validation: distances from fish points to nearest RHS points checked; distances <1 km considered acceptable.
- Consistency check: sum of macro-category land use percentages ~ 100% (99.96–100.04%).
- EDF validation: discrepancies flagged omitted stretches from the model; missing EDF values treated as no data.
- Elevation handling: NoData cells may correspond to estuarine or below-sea-level areas and are treated appropriately.

## Data Dictionary (CP_Fish_SiteVariables_Region.csv)
- Fish_SiteID: unique fish site code (Chempop project)
- Fish_Name: site name
- Fish_River: river/location
- Fish_Catchment: catchment/basin
- Fish_Easting: easting coordinate
- Fish_Northing: northing coordinate
- HQA_Score: Habitat Quality Assessment score
- HMS_Score: Habitat Modification Score
- Fish_Altitude: altitude (m above sea level)
- LC_Woodland_Per: upstream woodland percentage
- LC_Arable_Per: upstream arable percentage
- LC_Seminatural_Per: upstream semi-natural percentage
- LC_Urban_Per: upstream urban percentage
- LC_Woodland_Area: upstream woodland area (km2)
- LC_Arable_Area: upstream arable area (km2)
- LC_Seminatural_Area: upstream semi-natural area (km2)
- LC_Urban_Area: upstream urban area (km2)
- BFI: Base Flow Index
- EDF_Mean: mean effluent dilution factor
- EDF_SD: standard deviation of effluent dilution factor
- EDF_Q90: 90th percentile of effluent dilution factor
- EDF_Q95: 95th percentile of effluent dilution factor
- ED_SITE_ID: unique EDF site identifier

Note: The dataset contains 18 variables per region file, with regional and species tables forming the complete dataset.

## Access, Versioning, and Updates
- The dataset exists in multiple versions; explicit updates include:
  - 20211116_HIFI_JuvenileFish_England_SiteTable updated (removal of HMS/HQS/BFI from data table and regional split) with subsequent update dates 2022-05-31 and 2022-08-12.
- The data are organized regionally for site-level analyses and are linked to a single species table.

## References
- Dawson, F. H., Hornby, D. D., Hilton, J. (2002). Automated extraction of environmental variables for river classification.
- Gustard, A., Bullock, A., Dixon, J. M. (1992). Low flow estimation in the United Kingdom.
- CEH Land Cover Map 2015 (LCM2015).
- Young, A.R., Grew, R., Holmes, M.G.R. (2003). Low Flows 2000: national water resources assessment.
- Williams, R.J. et al. (2009). LF2000-WQX and wastewater distribution.
- Additional citations for datasets and methods as listed in the readme.

## Authors and Contact
- Ainsworth, R.F.; Nunn, A.D.; Bachiller-Jareno, N.; Rizzo, C.; Scarlett, P.; Antoniou, V.