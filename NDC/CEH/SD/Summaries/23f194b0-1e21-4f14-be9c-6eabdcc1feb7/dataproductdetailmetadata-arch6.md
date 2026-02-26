# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

- Purpose and scope
  - Open data product combining macroinvertebrate taxonomic abundance from 1,519 English river monitoring sites (1965–2018) with 41 water quality determinands, river flow, air temperature, and static environmental site descriptors.
  - Created to enable broad environmental data analyses and modelling, supporting research on chemical exposures and wildlife populations (ChemPop project).
  - Outputs span seven Environment Agency regions; data integration across multiple national datasets to support cross-cut analyses.

- Data sources and components
  - Macroinvertebrate time series: Freshwater river macroinvertebrate surveys (Biosys) from the Environment Agency (EA).
  - Water quality chemistry: EA Water Quality Data Archive (pre-2000 data licensed separately) and additional EA sources.
  - River flow: National River Flow Archive (NRFA) gauging data (daily mean flows).
  - Air temperature: CHESS-met (Great Britain, 1961–2017).
  - Wastewater influence: EDF (effluent dilution factor) derived from LF2000-WQX model.
  - Habitat quality: River Habitat Survey (RHS) metrics (HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ).
  - Land cover: Land Cover Map 2015 (LCW, LCArable, LC Seminatural, LC Urban) upstream of each macroinvertebrate site.
  - Spatial framework: UKCEH digital river networks, IHDTM flow direction/accumulation grids, and the 1:50,000 river network.
  - Supporting site descriptors: altitude, slope, upstream catchment land cover, channel dimensions, substrate, distance from source, etc.

- Data integration and workflow (three core steps)
  - Spatial matching: pair macroinvertebrate sampling sites with nearby water quality, river flow, and RHS survey locations along the river network (closest distance along the network).
  - Spatial integration: extract values for modelled/derived variables (EDF, land cover, air temperature) at macroinvertebrate site locations.
  - Temporal matching: align time-series observations (water quality, river flow, air temperature) to the 6-month window preceding each macroinvertebrate sampling date; site descriptors (land cover, habitat indices) treated as static.

- Temporal and spatial coverage details
  - Spatial extent: 1,519 macroinvertebrate sites distributed across seven EA regions.
  - Temporal extent: macroinvertebrate surveys from 1965–2018; accompanying covariates aligned to sampling dates where possible.
  - Data gaps: final output contains missing values (NoData) for many variables due to non-overlapping spatio-temporal coverage and licensing/licensing restrictions for some water quality data.

- Output data products and file structure
  - Macroinvertebrate taxon abundance
    - CP_REGION_MInv_taxonAbundance_startDate-endDate.csv (7 region files; one per EA region)
  - Macroinvertebrate site descriptors (physical/site context)
    - CP_REGION_MInv_siteVariables.csv (7 region files; region-specific site descriptors including altitude, slope, distance from source, discharge, width, depth, substrate, and derived EDF)
  - Water quality statistics
    - CP_REGION_MInv_<determinantLabel>Stats_startDate-endDate.csv (41 determinands; 287 files total)
  - River flow statistics
    - CP_REGION_MInv_riverFlowStats_startDate-endDate.csv (7 region files)
  - Air temperature statistics
    - CP_REGION_MInv_airTempStats_startDate-endDate.csv (7 region files)
  - Site matched locations
    - CP_REGION_MInv_siteMatchedLocation.csv (7 region files)
  - Supporting files
    - SiteswithmultipleRHSsurveys.csv (sites with more than one RHS survey)
    - Appendix heatmaps (temporal coverage) and data quality notes

- Data processing and quality notes
  - FRMS macroinvertebrate data cleaned and harmonised; taxonomic names reconciled to Davies & Edwards (2011) standard; pre-2002 records semi-quantitative or log-scale, post-2002 more precise counts.
  - Water quality data: matched to macroinvertebrate sites using an ArcGIS-based approach with manual checks; data pre-2000 from EA licensed database; 41 determinands selected; LoQ handling options implemented (LoQ treated as LoQ, zero, or LoQ/2) for statistics; upper-quantile substitutions applied as reported.
  - River flow: gauging stations matched to macroinvertebrate sites by river-network distance; flow statistics computed for the period of interest (POI, 20/05/1974–29/03/2019) and for the 6-month pre-sampling window.
  - EDF modelling: LF2000-WQX model used to estimate percentage wastewater in river flow; caveats include truncation of the river network and potential 0% EDF values where headwaters are not connected to modelled WWTWs.
  - Air temperature: daily CHESS-met values extracted per macroinvertebrate site; 2017 end date means data beyond that date lacks CHESS-met values.
  - Habitat indices: RHS-derived HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ extracted for matched RHS sites; RHS provides one primary measurement per site (with some sites having multiple surveys).
  - Land cover: LCM2015 upstream catchment analysis using IHDTM flow accumulation; catchments up-stream delineation threshold set to cells with value >200; land cover categories aggregated into Woodlands, Arable, Seminatural, Urban.

- Data accessibility and usage notes for data support
  - Data available as CSV files with NA coding for missing values; users should specify data types and treat NA appropriately when loading (e.g., in Python Pandas or R).
  - Data are designed to enable self-service analyses and dashboard-style exploration across taxonomic abundance, water quality, river flow, temperature, and habitat descriptors.
  - The dataset supports cross-topic policy-relevant analyses (e.g., chemical exposures and macroinvertebrate responses) while noting data gaps and licensing limitations.
  - Documentation accompanies the data product with methodological details, variable definitions, and data source acknowledgments; data cited from EA, UKCEH, NRFA, and CHESS-met.

- Notes on data provenance and acknowledgments
  - Data product developed under the ChemPop project (ERCITE/NERC funding) with contributions from Environment Agency, UKCEH, NRFA, and partner researchers.
  - Acknowledges data providers and supporting information centers; references to standard taxonomic nomenclature and methodological sources are included in accompanying documentation.

- Practical considerations for data support and reuse
  - When linking macroinvertebrate data to covariates, expect varying degrees of data completeness by region and variable due to licensing and data coverage.
  - For modelling or dashboards, use region-specific files and carefully join taxon abundances with covariates via BIO_SITE_ID and sampling dates; pay attention to six-month aggregation windows for water quality and temperature.
  - Consider temporal limitations (CHESS-met ends in 2017; some variables are static, e.g., land cover) and the potential need for imputation or careful handling of missing values.