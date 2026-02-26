# Fish abundance, habitat, water quality, flow and climate in English rivers 1975-2017

## Aims and scope
- Compile a long-term, open dataset to investigate whether chemical releases affect freshwater wildlife and how chemical effects compare with other drivers.
- Link demographic and community changes in fish populations to predicted chemical exposure, enabling regulator and industry assessment and informing future monitoring decisions.
- Assemble open data from multiple sources (fish, habitat, water quality, hydrology, climate) for use in modelling and environmental data analyses within the ChemPop project (NERC-funded).

## Data sources and provenance
- Fish data: Environment Agency’s National Fish Population Database (NFPD) and University of Hull (UoH) fish population data.
- Habitat data: River Habitat Survey (RHS) and HABSCORE (habitat quality measures for salmonids and trout).
- Water quality data: UK Environment Agency Water Quality Archive (Water Quality Data Archive, Beta) and 41 chemical determinands (WIMS determinands).
- Hydrology and flow: National River Flow Archive (NRFA) and LF2000-WQX model for effluent dilution/ wastewater impact.
- Temperature and climate: water temperature gauging stations, CHESS-MET daily air temperature, Gulf Stream Index (GSI), North Atlantic Oscillation Index (NAOI).
- Land cover and terrain: Land Cover Map 2015 (LCM2015) and Integrated Hydrological Digital Terrain Model (IHDTM).
- Temporal coverage: fish data 1975–2017; chemical determinands 1960–2017; climatic and hydrological covariates spanning the study period.

## Data integration and methodology
- Spatial and temporal alignment across diverse data sources to a common set of riverine fish survey sites.
- Three-stage integration workflow:
  - Spatially match survey locations along the river network.
  - Integrate model-generated and observed covariates (e.g., wastewater, land cover).
  - Temporally match environmental observations to survey dates.
- Nearest-neighbor and river-network path methods used to link RHS, HABSCORE, RHS/HQA/HMS data, water quality sites, river flow gauges, land cover, and EDF data to fish sites.
- Data completeness reflects data availability and temporal overlap; some covariates have full coverage while others have gaps due to dataset timing and spatial constraints.

## Key data components and structure
- Data are organized into five types of files:
  - Species table: CP_Fish_SpeciesTable.csv (unique fish species codes, Latin names, common names, and EA codes).
  - Site variables by region: CP_Fish_SiteVariables_region.csv (location, habitat scores, elevation, land-cover metrics, BFI, EDF metrics).
  - Data tables by region: CP_Fish_DataTable_region.csv (survey-level fish densities, habitat scores by species, climate covariates, and location metadata).
  - Hydrology statistics by region: CP_Fish_HydrologyStats_Region.csv (flow metrics at NRFA stations and derived flow descriptors for survey periods).
  - Water quality determinands by region: Region_FISHWIMSStats_DET.csv and larger spreadsheets (Region and DET identifiers; WIMS and LOQ/LOQ handling statistics; 329 data tables for determinands).
- Data types include counts converted to densities, habitat scores (HQA, HMS, HABSCORE), land-cover percentages/areas, EDF estimates, water temperature (degree-days), river flow statistics, and 41 chemical determinand statistics.
- Data for each region include seasonal and multi-year covariates linked to survey dates, with results stored in region-specific files to preserve regional structure.

## Variables and covariates
- Fish abundance: species-specific densities (per 100 m^2) derived from Environment Agency NFPD counts (excluding juveniles and qualitative-only surveys; handling of abundance categories and special suffixes).
- Habitat variables: RHS HMS, RHS HQA (including adjustments for 1994 data to enable cross-year comparability); HABSCORE habitat quality metrics for salmon and trout.
- Land cover: four macro-categories (Woodlands, Arable, Seminatural, Urban) upstream of each survey; areas and percentages derived from Land Cover Map 2015 and IHDTM; raster-to-polygon processing approach described.
- Water temperature: cumulative degree days ≥12°C prior to survey; modeled using GAMMs across 0.3–0.99 increments of Base Flow Index (BFI); integration of in-situ gauged data and CHESS-MET-derived air temperature.
- River flow: daily NRFA data linked to nearest NRFA station along the river network; extraction of mean, median, SD, CV, quantiles (Q5, Q95) and threshold-based metrics for 3-, 6-, and 12-month windows prior to surveys; additional 3/6/12-month metrics to capture extreme events and patch lengths.
- Effluent Dilution Factor (EDF): modeled wastewater contribution along the river network using LF2000-WQX (percentage wastewater at modelled WWTWs responsible for 95% of DWF); outputs include EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95.
- Water quality determinands: 41 chemicals with data from Water Quality Archive; matching fish sites to up to three nearby water-quality determinand sites; data extraction includes statistical summaries (min, max, median, mean, SD) under alternative LOQ handling schemes (LoQ as LOQ, 0, or LOQ/2) for the preceding 12 months.
- Altitude/elevation: two IHDTM-derived elevation values per site; one site assigned 0 m (estuary context).
- Climate indices: Gulf Stream Index (GSI) and North Atlantic Oscillation Index (NAOI) as marks of broader climatic regime affecting hydrology and ecosystem productivity.
- Data gaps and exclusions: 33 fish sites lacking water quality data due to licensing restrictions; some determinants may be missing due to non-overlapping timeframes or licensing constraints.

## Data quality, completeness, and limitations
- Data completeness varies by covariate and region; some covariates show near-complete coverage, while others exhibit gaps due to sampling design, spatial reach, or licensing constraints.
- Metadata sufficiency is highlighted as a barrier in some instances; notable challenges include data standardization across sources, varying sampling efforts, and the need to publicly share underlying data.
- The dataset acknowledges gaps (noData) and notes careful treatment of uncertain or conflicting records (e.g., LOQ handling for chemical data, exclusion of non-identifiable species).
- Some data are restricted by licensing and are not publicly available for certain sites (water quality data exclusions).

## Data access, sharing, and governance
- Open data orientation: designed as an open data product to support broad analyses and modelling.
- Clear documentation of data sources, provenance, and processing steps to enable reproducibility and governance.
- Acknowledgments emphasize funding (NERC) and data contributions from Environment Agency and partner institutions; data usage respects licensing and data rights.

## Practical considerations for monitoring framework authors
- Data harmonization: integrating heterogeneous data requires careful spatial-temporal alignment along river networks and consistent species coding.
- Metadata and provenance: maintain thorough metadata for each data source, including collection methods, temporal coverage, and transformation steps to enable reproducibility.
- Data completeness strategies: plan for data gaps by incorporating model-based covariates (e.g., EDF, modeled water temperature) and clearly document gaps and their potential impact on analyses.
- Transparency in data processing: document specifically how semi-quantitative counts were converted to densities and how LOQ handling affects summary statistics.
- Governance and sharing constraints: anticipate licensing limitations (e.g., water quality data restrictions) and design monitoring frameworks that allow safe data sharing while preserving data rights.

## References and acknowledgments (high-level)
- ChemPop project and related data sources described (NFPD, RHS/HABSCORE, WQ Archive, EDF modelling, CHESS-MET, NRFA, GSI, NAOI, IHDTM, LCM2015).
- Key methodological references cited throughout the dataset documentation (Nunn et al., Mann, Cowx, Williams et al., Rowland et al., Morris & Flavin, etc.).
- Acknowledgments to NERC, Environment Agency, and contributing researchers.