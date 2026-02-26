# CP_Fish_SiteVariables_readme.txt

## Overview
- WP/task: NFPD site variable data for fish sites in English rivers 1975-2017.
- Dataset: Site variables that do not change over time; covariates include habitat quality indicators (HQS and HMS) and physical site characteristics (altitude, land use, wastewater and BFI).
- Data authors: Ainsworth, R.F.; Nunn, A.D.; Bachiller-Jareno, N.; Rizzo, C.; Scarlett, P.; Antoniou, V.
- Data structure: Site tables and data tables are regional (Anglian, Midlands, North East, North West, Thames, Southern, South West); a single Species table denotes species referenced by Fish_SpeciesCode.

## Data & File Overview
- File list:
  - CP_Fish_SiteVariables_Region.csv: Information for individual NFPD fish sites including names, location, land use and habitat variables.
- Relationship: Fish_SiteID links to Fish_SiteID in DataTable files, Hydrology files, and chemical determinand files.
- Versions: There are multiple versions. Notably, 20211116_HIFI_JuvenileFish_England_SiteTable was updated (HMS, HQS land use, and BFI removed from the data table; file split into regional files). Updates occurred 2022/05/31 and 2022/08/12.
- Additional related data not in package: n/a
- Species data: Species table is a separate file indicating species referred to in Fish_SpeciesCode.

## Provenance
- Derived from:
  - HQA/HMS (RHS habitat quality data) from River Habitat Survey (RHS) sites, linked to the nearest fish site (within 5 km) via ArcGIS.
  - Altitude: CEH Integrated Hydrological Digital Terrain Model (IHDTM) elevation data.
  - Land use: CEH Land Cover Map 2015 (LCM2015), processed to 21 categories and aggregated upstream of each fish site.
  - BFI: Base Flow Index from CEH National Flow Archive.
  - EDF: Effluent Dilution Factor modeled from LowFlows2000-WQX to estimate wastewater influence.
- Data sources and references provided (with URLs and citations).

## Methodological Information
- Data collection and generation:
  - HQA/HMS: RHS-derived scores matched to the nearest fish site (within 5 km) using IRN extension for ArcGIS; HQA data from RHS portal. HQA data from 1994 differ from later years; adjustments made to enable year-to-year comparison.
  - Land use: Upstream catchment land cover (21 categories) derived from LCM2015, aligned to IHDTM 50 m; annual categories collapsed into four macro-categories (Woodland, Arable, Semi-natural, Urban). Percentages and areas computed for each site upstream catchment.
  - Altitude: IHDTM elevation values extracted for each site; two values computed (cell center value and bilinear-interpolated average); final value used documented.
  - EDF: LF2000-WQX model used to estimate percentage wastewater contribution at each site; significant WWTWs selected (top contributors). Outputs include mean, standard deviation, 90th and 95th percentiles.
- Data processing:
  - NFPD data filtered to sites surveyed at least 10 times; removed juvenile fry sites; nearest RHS site’s HQA/HMS values extracted.
  - Land use processing involved ArcGIS GRASS tools (r.accumulate) and DataLabs with Python to compute upstream land use percentages and areas.
  - EDF data linked to the closest river network reach on the 1:50,000 network; used to assign EDF values to sites or flagged as missing if mismatches occurred.
- Software and technical requirements:
  - ArcGIS (10.6.1 or later) or ArcGIS Pro; GRASS GIS; DataLabs; Python; 1:50,000 river network; LF2000-WQX model.

## Quality Assurance
- Spatial checks:
  - Distances between fish observation points and nearest RHS points checked; distances <1 km considered acceptable; all sites passed.
- Data consistency:
  - Sum of macro-categories for land use checked to be ~99.96–100.04%, indicating precise aggregation.
- EDF handling:
  - If a river network stretch was omitted in the model, corresponding EDF values left as no data.
- Elevation handling:
  - Nodes with NoData treated as estuarine or land below sea level and set to 0 m elevation.

## Data-Specific Information for CP_Fish_SiteVariables_Region.csv
- Rows/columns: variable depending on region; 18 variables.
- Key variables:
  - Fish_SiteID, Fish_Name, Fish_River, Fish_Catchment, Fish_Easting, Fish_Northing
  - HQA_Score, HMS_Score
  - Fish_Altitude
  - LC_Woodland_Per, LC_Arable_Per, LC_Seminatural_Per, LC_Urban_Per
  - LC_Woodland_Area, LC_Arable_Area, LC_Seminatural_Area, LC_Urban_Area
  - BFI
  - EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95
  - ED_SITE_ID (site-specific EDF identifiers)

## Technical Details and Interpretation Notes
- Instrument/software requirements:
  - Land cover/altitude data require ArcGIS 10.7+ or ArcGIS Pro; Land Cover 2015 with GRASS GIS; DataLabs Python scripts for land-use extraction; EDF requires Python and the 1:50,000 river network and LF2000-WQX model.
- Data interpretation:
  - HQA/HMS reflect RHS habitat quality; nearest RHS site matching may exclude some sites.
  - Land-use metrics represent upstream catchment characteristics for each fish site.
  - EDF provides a modeled estimate of wastewater influence on river reaches around each site, not a direct measurement.

## References
- Dawson, F.H., Hornby, D.D., Hilton, J. (2002). Automated extraction of environmental variables. Aquatic Conservation.
- Gustard, A., Bullock, A., Dixon, J.M. (1992). Low flow estimation in the United Kingdom.
- UKCEH Land Cover Map 2015 (LCM2015).
- Young, A.R., Grew, R., Holmes, M.G.R. (2003). Low Flows 2000: national water resources assessment.
- Williams, R.J. et al. (2009). LowFlows2000-WQX model; EDF methodology.
- Additional references for methods and data sources as listed in the document.