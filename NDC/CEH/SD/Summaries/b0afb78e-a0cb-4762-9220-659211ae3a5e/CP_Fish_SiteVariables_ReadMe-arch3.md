# CP_Fish_SiteVariables_readme.txt

## Overview and purpose
- WP/task: Compile NFPD site variable data for English river fish sites (1975–2017).
- Dataset captures site-invariant covariates (habitat quality indicators and physical site characteristics) to support environmental health monitoring, policy scrutiny, and decision-making.
- Covariates include habitat quality indicators (HQS, HMS) and physical site features (altitude, upstream land use, wastewater influence via Base Flow Index and EDF).

## Data authors
- Ainsworth, R.F.; Nunn, A.D.; Bachiller-Jareno, N.; Rizzo, C.; Scarlett, P.; Antoniou, V.

## Dataset and file structure
- Site tables and data tables are stored as regional files (Anglian, Midlands, North East, North West, Thames, Southern, South West); a single Species table maps species referenced by Fish_SpeciesCode.
- Primary file: CP_Fish_SiteVariables_Region.csv contains information on individual fish sites (names, location, land use, habitat variables).
- Relationship: Fish_SiteID links the Region-specific SiteVariables to corresponding DataTable, Hydrology, and chemical determinand files.
- Multiple versions exist; an update introduced 20211116_HIFI_JuvenileFish_England_SiteTable.
- Reasons for update: removal of HMS, HQS land use, and BFI from the data table file; regional file split to improve data organization.
- Update timeline: 2022/05/31 and 2022/08/12.

## Provenance and data sources
- HQA and HMS (habitat quality indicators) derived from River Habitat Survey (RHS); RHS sites linked to the nearest fish site within 5 km in ArcGIS (IRN extension).
- Altitude: CEH Integrated Hydrological Digital Terrain Model (IHDTM) elevation data (50 m resolution).
- Land use: CEH Land Cover Map 2015 (LCM2015); 21 land cover categories collapsed into four macro-categories (Woodland, Arable, Semi-natural, Urban) for upstream catchments.
- BFI (Base Flow Index): derived from CEH National Flow Archive (upstream of fish site).
- EDF (Effluent Dilution Factor): modeled with LowFlows2000-WQX to estimate percent wastewater influence from wastewater treatment works; results expressed as mean and percentiles (Mn, SD, Q90, Q95).

## Methodology
- Data collection and linkage:
  - HQA/HMS: RHS-derived scores; closest RHS site matched to each fish site; non-mappable sites exist.
  - Land use: upstream catchment composition calculated from LCM2015; 21 categories aggregated into four macro-categories; aggregation and consistency checks performed.
  - Altitude: extraction from IHDTM; two approaches used, with the cell-centre value adopted.
  - EDF: mapping fish sites to the nearest reach on the LF2000-WQX river network; EDF statistics computed from the modeled distribution.
- Data processing and transformations:
  - RHS-derived HQA/HMS remained largely untransformed (one sample per site; some sites unmatched).
  - Land use calculations performed in ArcGIS and DataLabs (Python) to derive percentage and area upstream from each fish site.
  - NFPD data filtered to sites surveyed at least 10 times; juvenile fry sites removed; nearest RHS-derived values attached where possible.
  - EDF data linked via Python to the LF2000-WQX network; outputs include Mn, SD, Q90, Q95 per site.
- Software and tools:
  - ArcGIS (10.6.1+; later requirements include ArcGIS 10.7+ or ArcGIS Pro for land cover/altitude interpretation).
  - GRASS GIS (r.accumulate) for land-use accumulation rasters.
  - DataLabs (for land-use area/percentage extraction).
  - Python (for linking EDF data to sites).
- Quality assurance:
  - Spatial matching quality checked (distance < 1 km deemed acceptable).
  - Macro-category sums checked to be near 100% (99.96–100.04%).
  - EDF data flagged if river network segments were omitted (no data where applicable).
  - NoData cells in elevation treated as 0 m where appropriate (estuarine/lowland areas).
  
## Data specifics for CP_Fish_SiteVariables_Region.csv
- Size: region-dependent rows/columns; 18 variables (per region) described.
- Key variables include:
  - Fish_SiteID, Fish_Name, Fish_River, Fish_Catchment, Fish_Easting, Fish_Northing.
  - HQA_Score, HMS_Score (habitat quality covariates).
  - Fish_Altitude (site elevation).
  - Land-use components by upstream catchment (LC_Woodland_Per, LC_Arable_Per, LC_Seminatural_Per, LC_Urban_Per) and corresponding areas (LC_Woodland_Area, LC_Arable_Area, LC_Seminatural_Area, LC_Urban_Area).
  - BFI (Base Flow Index).
  - EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95 (effluent dilution factors).
  - ED_SITE_ID (effluent dilution factor site identifiers).

## Data interpretation and guidance for users
- Instrument/software requirements: ArcGIS 10.7+ or ArcGIS Pro for land cover and altitude interpretation; GRASS GIS for land-use processing; DataLabs; Python for EDF linkage.
- Metadata and data governance: linking across multiple regional files and legacy RHS data; note potential data-sharing barriers discussed in governance considerations (public sharing of underlying data; data provenance and versioning are explicit).
- Data completeness and caveats:
  - HQA/HMS may be missing for some sites due to non-mappable RHS data.
  - EDF data may be blank where network segments were omitted; some NoData cases exist for estuarine or low-lying areas.
  - 1994 HQA data differ from later years; cross-year comparability addressed via updated protocols.

## Version history and references
- Versions exist; noted update file 20211116_HIFI_JuvenileFish_England_SiteTable.
- References for data sources and methods include:
  - Dawson, F.H., Hornby, D.D., Hilton, J. (2002) on automated extraction of environmental variables.
  - Gustard, A., Bullock, A., Dixon, J.M. (1992) on Low Flow estimation.
  - Young, A.R., Grew, R., Holmes, M.G.R. (2003) Low Flows 2000 study.
  - Williams, R.J. et al. (2009) LF2000-WQX model for wastewater distributions.
  - CEH LCM2015 and IHDTM sources; NFPD/RHS linkage methodology.