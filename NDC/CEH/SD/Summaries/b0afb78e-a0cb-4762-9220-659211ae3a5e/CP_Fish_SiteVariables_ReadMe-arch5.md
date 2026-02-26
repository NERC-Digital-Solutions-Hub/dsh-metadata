# CP_Fish_SiteVariables_readme.txt

## Overview
- WP/task: NFPD site variable data for fish sites in English rivers 1975-2017
- Dataset: Site variables that do not change over time, including habitat quality indicators (HQS, HMS) and physical site characteristics (altitude, land use, wastewater, Base Flow Index)
- Data authors: Ainsworth, Nunn, Bachiller-Jareno, Rizzo, Scarlett, Antoniou

## Data structure and contents
- File organization: Site tables and Data tables are split into regional files (Anglian, Midlands, North East, North West, Thames, Southern, South West). A separate Species table indicates species referred to in Fish_SpeciesCode within the data tables.
- Primary file: CP_Fish_SiteVariables_Region.csv contains information for individual fish sites (names, location, land use, habitat variables).
- Relationships: Fish_SiteID in site variables file matches Fish_SiteID in DataTable, Hydrology, and chemical determinand files.
- Versions: Multiple versions exist. Notable updates include:
  - 20211116_HIFI_JuvenileFish_England_SiteTable (file updated)
  - 2022/05/31 and 2022/08/12 updates involved removing HMS/HQS from data table files and splitting into regional files

## Provenance and data sources
- Derived from River Habitat Survey (RHS) data for habitat scores:
  - HQA (Habitat Quality Assessment) and HMS (Habitat Modification Score)
  - RHS site linkage to nearest fish site within 5 km along the river
  - 1994 HQA data differs from later years; protocols updated for comparability
- Land use: CEH Land Cover Map 2015 (LCM2015), aggregated to four macro-categories:
  - Woodland, Arable, Semi-natural, Urban
- Altitude: CEH Integrated Hydrological Digital Terrain Model (IHDTM), 50 m resolution
- Base Flow Index (BFI): CEH NRFA-derived data
- Effluent Dilution Factor (EDF): Modelled wastewater fraction using LowFlows2000-WQX; significant WWTWs retained; EDF metrics provided (Mean, SD, Q90, Q95)

## Methods: data collection and processing
- Data collection and linkage:
  - RHS scores linked to nearest fish site using IRN extension for ArcGIS; closest match within 5 km
  - HQS/HMS values extracted from RHS data portal; HQA data from 1994 updated to enable year-to-year comparability
- Land use processing:
  - 21 land use categories derived from LCM2015; categories aggregated into four macro-categories
  - Upstream catchment calculations performed with GRASS GIS r.accumulate; DataLabs used to extract area and percentage upstream
- Altitude processing:
  - IHDTM elevation extracted for fish sites; two values computed (cell-centre value and bilinear-interpolated average); NoData ignored unless all adjacent cells are NoData
- EDF processing:
  - LF2000-WQX model used to estimate wastewater distribution; Python associates fish sites with closest reach on 1:50,000 river network
  - Outputs include mean, standard deviation, 90th and 95th percentiles
- Data handling and validation:
  - Distances between fish sites and RHS points checked; ≤1 km deemed acceptable
  - Sum of macro-categories checked to be 99.96–100.04% (precision check)
  - EDF data blanks flagged where river network omissions occurred
  - NoData cells assigned 0 m elevation if estuarine or land below sea level
- Tools and software required:
  - ArcGIS (10.6.1 or later) for elevation and land-use extraction
  - ArcGIS Pro for newer workflows
  - GRASS GIS for land-use accumulation
  - DataLabs and Python for extraction and processing
  - Access to CEH catchment tool and LF2000-WQX model

## Data-specific information
- File: CP_Fish_SiteVariables_Region.csv
  - Rows/columns: Region-dependent
  - Variables: 18 columns
  - Key variables:
    - Fish_SiteID, Fish_Name, Fish_River, Fish_Catchment
    - Fish_Easting, Fish_Northing
    - HQA_Score, HMS_Score
    - Fish_Altitude
    - LC_Woodland_Per, LC_Arable_Per, LC_Seminatural_Per, LC_Urban_Per
    - LC_Woodland_Area, LC_Arable_Area, LC_Seminatural_Area, LC_Urban_Area
    - BFI
    - EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95
    - ED_SITE_ID

## Quality assurance and data governance
- QA checks:
  - Spatial matching distances validated (<1 km acceptable)
  - Macro-category aggregation sums near exactly 100%
  - EDF values checked against network coverage; blanks used when data not available
  - Handling of NoData documented (elevation and network caveats)
- Data governance considerations:
  - Data is regionally partitioned; maintaining versioned files ensures traceable updates
  - Clear provenance links to original sources (RHS, LCM2015, IHDTM, NRFA, LF2000-WQX)
  - Metadata indicates methods, software, and data sources to support reproducibility and reuse

## Notes for data stewards
- When using or sharing these data, ensure alignment with the region-specific files and the central site-variable linkage via Fish_SiteID
- Be aware of version history: updates in 2022 removed HQS/HMS from the data table and split into regional files
- Record source references for provenance: RHS for habitat scores, LCM2015 for land use, IHDTM for altitude, BFIs from NRFA, and EDF from LF2000-WQX
- Monitor for any missing data in EDF or unmatched sites and document any gaps in downstream analyses

## References
- Dawson et al. (2002) on automated extraction of environmental variables
- Gustard et al. (1992) Low flow estimation
- Young et al. (2003); Williams et al. (2009) on Low Flows and wastewater modelling
- UKCEH LCM2015 and CEH IHDTM data resources