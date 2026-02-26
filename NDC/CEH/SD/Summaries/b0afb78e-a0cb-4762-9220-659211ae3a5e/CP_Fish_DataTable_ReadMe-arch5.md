# CP_Fish_DataTable_readme.txt

## Overview
- Provides an annual time series of fish abundance, densities, and covariate data for English river sites from the Environment Agencies NFPD dataset, covering 1975–2017.
- Covariates include habitat quality indicators (HABSCORE), climatic variables (Gulf Stream Index, NAOI), and water temperature indicators (Degree Days).
- Data organized by region: Anglian, Midlands, North East, North West, Thames, Southern, South West; separate region files for Site and Data; a single Species table references species codes.

## Dataset Content and Structure
- File List:
  - CP_Fish_DataTable_Region.csv: NFPD fish abundance and covariates, including density estimates, NAOI, GSI, HABSCORE, and Degree Days.
- Data Linkage:
  - Fish_SiteID in Region files matches Fish_SiteID in DataTable files, Hydrology files, and chemical determinand files.
- Data Tables:
  - Site table and Data table are regional files; Species table is a single file indicating species for Fish_SpeciesCode.
- Regional Structure:
  - Data structure is consistent across regions; 19 variables per region.

## Versions and Updates
- Multiple versions exist; notable update:
  - 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire HABSCORE
    - Reasons: correction of start/end dates for some juvenile sites; addition of covariate data to data tables; removal of juvenile sites from NFPD data and site tables; removal of some covariate data from the sitetable.
    - When: 13 June 2022
- Acknowledges ongoing versioning and updates.

## Provenance and Data Sources
- Primary provenance from Environment Agency’s National Fisheries Population Datasets (NFPD) including Freshwater Fish Counts and site/survey data.
- HABSCORE data contributed by Environment Agency and University of Hull (various files listed).
- Climate covariates:
  - Gulf Stream Index (GSI) sourced from Gulf Stream data.
  - North Atlantic Oscillation Index (NAOI) from NCAR Climate Data Guide.
  - Degree Days derived from water temperature data; base data from EA archive and CEH CHESS-MET dataset; model-based temperature estimates via GAMM in R.
- Data processing and transformations performed to derive densities from counts, including handling of semi-quantitative vs quantitative surveys.

## Methodology
- Data collection and selection:
  - NFPD fish data downloaded from EA portal; included sites surveyed at least 10 times.
  - Density calculations convert raw counts to densities per unit area to standardize sampling effort.
  - Handling of survey types:
    - Use RUN1 (first catch) for quantitative surveys where applicable.
    - Replace missing standard counts with estimated abundances following EU FAME/EFI+ conventions.
    - Manage special cases with suffixes like [Best Run], [Survey], and when surveys had no area data.
- Data processing:
  - Taxa without Chempop codes removed; densities aggregated where needed.
  - HABSCORE, GSI, NAOI, and Degree_Days appended as covariates; Degree_Days computed from water temperature data.
- Software and tools:
  - Python 3 (Jupyter) for air temperature, degree days, and related computations.
  - R (R Studio) for Degree Days calculation, GAMM-based water temperature modeling, and model validation.
- Quality assurance:
  - Data checked by Andy Nunn (14 July 2022).
  - GAMM model performance assessed using RMSE, normalised RMSE, and Scatter Index.

## Data Schema and Variables
- Regional files share a common structure with 19 variables per region.
- Key variables:
  - Fish_SiteID, Fish_SurveyID, Fish_Easting, Fish_Northing, Fish_SurveyDate
  - Fish_SpeciesCode, Fish_Densities
  - HQS_Bt_Small, HQS_Bt_Med, HQS_Bt_Large
  - HQS_Sal_Small, HQS_Sal_Large
  - GSI, NAOI, Degree_Days
- Additional notes:
  - Some NFPD sites may also contain HIFI data in metadata.
  - Potential coordinate mismatches between SiteTable and DataTable for survey locations.
  - SurveyID values starting with -9999 indicate UoH data corresponding to NFPD sites.

## Caveats and Considerations for Data Stewards
- Data integrity considerations due to multiple data sources and version updates, especially around juvenile site handling and covariate inclusion/removal.
- Interoperability requires careful alignment of regional files and the central Species table via Fish_SpeciesCode.
- Users should reference the appropriate version notes (e.g., 20220505 update) to account for juvenile removals and covariate changes.
- Attention needed for possible coordinate discrepancies between site and data tables and for -9999 survey identifiers.

## Governance and Access Implications
- Clear provenance and processing logs enable auditability and reproducibility for governance and data-sharing purposes.
- Versioned releases with documented changes support traceability and appropriate data reuse in governance frameworks.
- The dataset supports discovery and reuse across organisations managing large datasets, aligning with data stewardship aims to ensure standards, up-to-date information, and usable, well-documented data products.