# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017.

## Overview
- Dataset describing covariates (habitat quality, land use, altitude, flow characteristics, and wastewater influence) associated with fish site observations in English rivers.
- Aims aligned with analysts’ interest in identifying correlations and informing predictions about how habitat, water quality, flow, and climate relate to fish abundance over time.

## Scope and provenance
- Geographic coverage: England.
- Timeframe: Fish site data span 1975-2017; associated covariates collected or derived around 2019/2020–2022.
- Data authors: Ainsworth, R.F.; Nunn, A.D.; Bachiller-Jareno, N.; Rizzo, C.; Scarlett, P.; Antoniou, V., et al.
- Funding: NERC Chempop grant NE/S000100/2.
- Purpose: To link fish site observations with habitat, land use, water quality, flow, and climate covariates for analytical use.

## Access and licensing
- Licenses: NFPD data and RHS are open; Crown copyright and database rights (EMOU206) apply; altitude data, land use maps, and LF2000-WQX EDF model are licensed by UKCEH.
- Access points: NFPD fish data; CEH Land Cover Map 2015; CEH IHDTM elevation; EDF LF2000-WQX model.
- Licensing notes: Data can be used for lawful purposes; some components have specific license terms.
- Data citation: Ainsworth et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI: 10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e.

## Data organization and files
- File structure: Site table files are region-specific (Anglian, Midlands, North East, North West, Thames, Southern, South West); a single Species table applies to both NFPD fish and juvenile datasets.
- Primary data file for covariates: CP_Fish_SiteVariables_region.csv containing 18 variables per fish site (regionalized).
- Relationship: Fish_SiteID links CP_Fish_SiteVariables_region.csv to DataTable files, Hydrology files, and chemical determinand files.
- Version history: Updated 2021-11-16; reasons include removal of certain covariates (HQA/HMS land use and BFI) from the DataTable and splitting into regional files; updates occurred 2022-05-31 and 2022-08-12.
- Data completeness: Missing data code -9999 used in datasets.

## Covariates and data sources (methods)
- Habitat quality and modification (HQA, HMS) via River Habitat Survey (RHS) scores; RHS sites linked to nearest fish site within 5 km along the river.
- Land use upstream catchment (upstream of fish sites) derived from CEH Land Cover Map 2015 (LCM2015); 21 land cover categories were collapsed into four macro-categories: Woodland (Woodland), Arable, Semi-natural, Urban. Calculated as percentage and area (km²) upstream from each site.
- Altitude: Elevation from CEH Integrated Hydrological Digital Terrain Model (IHDTM, 50 m resolution). Two calculations: elevation at cell centre, and bilinear-interpolated average of adjacent valid cells; the centre value used.
- Base Flow Index (BFI): Computed from CEH National Flow Archive daily mean flows upstream of fish sites.
- Effluent Dilution Factor (EDF): Modeled wastewater influence using LF2000-WQX, providing distributions of wastewater percentages across reaches. Outputs include EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95.
- Software and standards:
  - GIS: ArcGIS 10.7+ or ArcGIS Pro for elevation and land-use extraction.
  - Land use processing: GRASS GIS (r.accumulate) and DataLabs (Python) for extraction of land-use percentages and areas.
  - EDF processing: LF2000-WQX model with Python to link fish sites to river network.
  - Python 3 required for land use and EDF data processing.
- Data integration: Fish site coordinates matched to RHS/land-use/edf layers; associated uncertainties acknowledged (e.g., RHS year differences).

## Data processing and quality assurance
- Data processing:
  - RHS data (HQA/HMS) used directly when matched; some sites could not be matched.
  - Land use: 21-category land cover maps converted to four macro-categories; upstream catchment metrics derived via GRASS r.accumulate and DataLabs extraction; consistency checks performed.
  - EDF: fish sites matched to closest river network reach; wastewater percentages derived from LF2000-WQX are long-term representative.
  - Altitude: IHDTM-based extractions for all sites; nodata cells handled as estuarine/sea-level where appropriate.
- Quality checks:
  - Distances from fish sites to RHS matchpoints checked; <1 km considered acceptable.
  - Sum of macro-category percentages near 100% (99.96–100.04%) to confirm aggregation integrity.
  - EDF missing data flagged when river network segments were omitted; such sites are treated as no data.
  - Nodata handling for altitude to reflect estuarine/sea-level areas.
- Documentation of data provenance and QA: Data checked by Nunn, A. on 14 July 2022; comprehensive variable definitions and processing steps documented.

## Data-specific information for CP_Fish_SiteVariables_region.csv
- Content: 18 variables describing each fish site covariate (regional file).
- Key variables include:
  - Fish_SiteID, Fish_Name, Fish_River, Fish_Catchment, Fish_Easting, Fish_Northing
  - HQA_Score, HMS_Score (habitat quality/ modification)
  - Fish_Altitude
  - Land-use covariates: LC_Woodland_Per, LC_Arable_Per, LC_Seminatural_Per, LC_Urban_Per
  - Land-use areas: LC_Woodland_Area, LC_Arable_Area, LC_Seminatural_Area, LC_Urban_Area
  - BFI (Base Flow Index)
  - EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95
  - ED_SITE_ID (EFF site identifiers)
- Data handling: -9999 used for missing values.
- Interpretation: Covariates prepared to support correlation analyses between habitat, land use, flow, wastewater influence, and fish metrics.

## Usage notes and caveats
- The dataset provides covariates intended for correlation and predictive analyses with fish abundance data; users should account for potential mismatches in RHS year and fish sampling year, and apply consistent regional alignment when combining files.
- Some covariates were split or removed in later versions; ensure the correct regional CP_Fish_SiteVariables file is used for your analyses.
- Readers should reference the linked datasets (NFPD, Land Cover Map 2015, IHDTM elevation, LF2000-WQX) for complete methodological context and to reproduce covariate derivations.

## References and related materials
- Methodological references for data sources and models:
  - Dawson, F.H., Hornby, D.D., Hilton, J. (2002). Automated extraction of environmental variables to help river classification.
  - Gustard, A., Bullock, A., Dixon, J.M. (1992). Low flow estimation in the UK.
  - Young, A.R., Grew, R., Holmes, M.G.R. (2003). Low Flows 2000: national water resources assessment.
  - Williams, R.J., et al. (2009). LF2000-WQX model for wastewater distribution.
- Dataset citation: Ainsworth, R.F. et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI: 10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e.