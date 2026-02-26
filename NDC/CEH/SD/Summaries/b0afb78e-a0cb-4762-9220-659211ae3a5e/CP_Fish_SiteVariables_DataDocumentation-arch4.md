# Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017

- Overview
  - A combined dataset describing fish abundance, habitat, water quality, flow and climate data for English rivers, spanning 1975–2017.
  - Compiled under the Chempop project with funding from NERC (Chempop grant NE/S000100/2) and authored by R.F. Ainsworth et al.
  - Data collection date range for the compiled dataset approximately 2019/04/03–2022/07/26.
  - Geographic scope: England.

- Data scope and content
  - Core themes: fish abundance (NFPD juvenile and adult datasets), habitat quality and modification (RHS HQA/HMS), land use, altitude, baseflow index (BFI), and effluent dilution factors (EDF) related to wastewater influence.
  - Data sources include: Environment Agency river habitat surveys (RHS/HQA/HMS), NFPD freshwater fish surveys, CEH land cover (LCM2015), CEH IHDTM elevation, UK National Flow Archive (BFI), and the LF2000-WQX wastewater model.
  - Data are organized regionally (Anglian, Midlands, North East, North West, Thames, Southern, South West) with a separate Species table and region-specific SiteVariables and DataTables.
  - Key metadata: dataset DOI provided; licensing notes indicate open access (NFPD data and RHS are open).

- Data structure and relationships
  - Files and relationships:
    - CP_Fish_SiteVariables_region.csv: region-specific site covariates (18 variables), linked to Fish_SiteID.
    - Data is partitioned into region-based DataTable files; a single CP_Fish_SpeciesTable.csv links with Fish_SpeciesCode in DataTable files.
  - Core relationship: Fish_SiteID in SiteVariables matches Fish_SiteID in DataTable, Hydrology, and chemical determinand files.
  - ED_SITE_ID and EDF-derived metrics (EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95) provide wastewater influence covariates.

- Provenance and data sources
  - Primary data contributors: Ainsworth, Nunn, Bachiller-Jareno, Rizzo, Scarlett, Antoniou, and colleagues (Chempop/NERC EDS IOD).
  - Derived/ancillary data:
    - RHS/HQA/HMS from RHS surveys; sites matched to fish sites within 5 km along the river.
    - Land use upstream of each fish site derived from CEH LCM2015 and IHDTM using GIS tools.
    - Altitude from CEH IHDTM (50 m resolution) with center-cell and bilinear-interpolated values.
    - EDF model based on LF2000-WQX to estimate wastewater influence.
    - BFI values from CEH National Flow Archive.
  - Data curation and transformation performed with ArcGIS, DataLabs, GRASS GIS, and Python 3.

- Data processing and methods
  - Collection/generation:
    - HQA/HMS (RHS habitat quality and modification scores) linked to nearest fish site via 5 km rule; 1994 HQA data differ from later years; protocols updated for year-to-year comparability.
    - Land use: 21 land cover categories aggregated into four macro-categories (Woodland, Arable, Sem-natural, Urban) with upstream catchment calculations for each fish site.
    - Altitude: two calculations (IHDTM cell center value and bilinear interpolated average); NoData treated as zero where applicable.
    - EDF: wastewater percentage estimated per site using LF2000-WQX; significant WWTWs defined as contributing to 90% of dry weather flow or 95% of catchment total; outputs include mean, SD, Q90, Q95.
  - Processing details:
    - HQA/HMS values are used as-is for RHS-based covariates; some sites may not match RHS data.
    - Land use processed via ArcGIS GRASS tools; DataLabs used to extract area/percentage upstream for fish sites; macro-categories validated for sum consistency (~99.96–100.04%).
    - EDF data linked to the closest river network reach; discrepancies flagged result in missing data for that site.
    - Altitude handled with IHDTM data; nodata cells mapped to estuarine/low-elevation areas appropriately.

- Quality assurance and validation
  - QA checks performed by researchers (e.g., A. Nunn, 14/07/2022).
  - Spatial matching distances checked (≤1 km between fish sites and RHS points).
  - Land-use sum consistency verified (aggregations close to 100%).
  - EDF handling includes provisions for network gaps leading to missing data.
  - Documentation notes any data gaps or non-matches.

- Access, licensing, and usage
  - Licensing: NFPD data and RHS are open; Crown copyright and database rights; use for lawful purposes.
  - Public data links:
    - NFPD fish data: data.gov.uk dataset page
    - Land cover map (LCM2015): CEH catalogue
    - Elevation (IHDTM): CEH data portal
    - EDF/lowFlowsWQX references and related publications
  - Required software/tools:
    - Land cover/altitude: ArcGIS 10.7+ or ArcGIS Pro
    - Land use: DataLabs (CEH Catchment Tool)
    - EDF: Python 3; 1:50,000 river network from Ordnance Survey
    - General: Python 3 for data processing; GRASS GIS for land-use processing
  - Publication/acknowledgments: Dataset cited with DOI; formal citation provided in the readme.

- File-level details and key variables
  - CP_Fish_SiteVariables_region.csv
    - Variables: 18 total, including Fish_SiteID, Fish_Name, Fish_River, Fish_Catchment, coordinates (Easting/Northing), HQA_Score, HMS_Score, Fish_Altitude, and land-use metrics (LC_Woodland_Per, LC_Arable_Per, LC_Seminatural_Per, LC_Urban_Per, LC_Woodland_Area, LC_Arable_Area, LC_Seminatural_Area, LC_Urban_Area), BFI, EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95, and EDF_Site_ID.
  - DataTable and SpeciesTable
    - Relationship: Fish_SiteID links site covariates to time-varying data such as fish counts, habitat scores, and other covariates across regions.
  - Data updates and versions
    - Version updates include 20211116_HIFI_JuvenileFish_England_SiteTable; reason: removal of certain covariates (HQA/HMS land use and BFI) from the main data table and split into regional files.
    - Update history: 2022-05-31 and 2022-08-12 (split and reorganized regional files).

- Version history and governance
  - Multiple data versions exist; regional file split and covariate adjustments implemented to streamline regional analyses.
  - Documentation and QA notes indicate ongoing maintenance and data provenance tracking.

- How this supports data-leader aims
  - Demonstrates end-to-end data integration across biological, habitat, hydrological, land-use, and wastewater domains.
  - Provides clear provenance, regional structuring, and linking keys (Fish_SiteID) enabling cross-team collaboration and reuse across networks.
  - Includes robust metadata, quality assurance steps, and explicit data processing workflows, supporting governance, discoverability, and trust.
  - Highlights both data assets (site covariates, regional tables) and derived analytics (EDF, land-use aggregates) essential for data strategy and impactful data products.

- Caveats and considerations for use
  - Some RHS-period comparability issues noted (1994 HQA data differences); cross-year comparisons should account for updated protocols.
  - Data gaps may occur where RHS matching fails or network links have missing segments, resulting in blank EDF values.
  - Specialized software and GIS workflows are required to reproduce land-use and EDF calculations; ensure appropriate tooling and licenses are available.