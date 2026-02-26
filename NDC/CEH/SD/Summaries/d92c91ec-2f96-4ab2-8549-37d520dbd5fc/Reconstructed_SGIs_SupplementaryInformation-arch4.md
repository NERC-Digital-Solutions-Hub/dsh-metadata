# Historic Standardized Groundwater level Index (SGI) for 54 UK boreholes (1891-2015)

## Project context and aim
- Historic Droughts project (2014–2018; £1.5m) funded by UK Research Councils to build cross-disciplinary understanding of past UK droughts and develop tools for future drought management.
- Emphasizes the interaction between hydrometeorological factors and social/regulatory drivers in drought and water scarcity (DWS).
- Goal: characterise and quantify drought history since the late 19th century using a range of sector information (hydrometeorological, environmental, agricultural, regulatory, social, cultural).

## Inventory and outputs
- Eight UK institutions contributed: British Geological Survey (BGS), Centre for Ecology & Hydrology, Cranfield University, University of Exeter, HR Wallingford, Lancaster University, Met Office, University of Oxford.
- Historic Droughts Inventory (HDI): a knowledge base with two main elements:
  - hydro-meteorological timelines (rainfall, river flows, groundwater) + consistent drought indicators.
  - references to past droughts (newspapers, legislation, agricultural media, oral histories) to understand drivers, impacts, and responses.
- Major output: Standardised Groundwater level Index (SGI) dataset, part of the HDI’s groundwater data collections (with reconstructed groundwater levels and other groundwater datasets).

## Description of the SGI dataset
- SGI series: monthly, standardized groundwater levels for 54 UK boreholes across Principal Aquifers (predominantly Chalk; many sites in southern/eastern England).
- Standardisation method: non-parametric normal scores transform applied per calendar month; includes probability estimates for SGI being below 0, -1, -1.5, and -2.
- Time coverage: 1891–2015.
- Purpose: enable direct comparison of groundwater drought status with meteorological drought indices (e.g., SPI) and hydrological drought indices (e.g., SSI).

## Data sources and standardisation method
- Data source: reconstructed groundwater level time series (Bloomfield et al., 2018) prepared for the Historic Droughts Inventory.
- Standardisation approach:
  - rank-based normal scores transform for each month.
  - apply inverse normal CDF to ranks to produce SGI values.
- Uncertainty quantification:
  - Generalised Likelihood Uncertainty Estimation (GLUE) methodology.
  - Behavioural parameter sets (Nash-Sutcliffe Efficiency > 0.5) converted to SGI series to compute monthly exceedance probabilities (Prob0, Prob1, Prob15, Prob2).

## Format and contents of the datasets
- Per-site CSV files: one file per borehole site with headers:
  - Date (YYYY-MM-DD; first day of each month)
  - SGI (standardised groundwater level)
  - Prob0, Prob1, Prob15, Prob2 (probabilities of SGI being below 0, -1, -1.5, -2)
- File naming: [Project] [Model Identifier] [Run of the model] [Input or Output] [Time] [Variable] [Catchment/Borehole ID] [Version] (e.g., HistoricDroughts_BGSAquiMod_Output_Feb2018_SGI_Rockleyver1)
- Metadata file: Metadata_forGWLandSGI_reconstructions.csv with:
  - Site_name, Easting, Northing, BGS_WellMaster_ID, Full_BGS_site_name, Aquifer, MORECS_ID, and related site details
- Documentation: Acknowledgements credit NERC funding; references include key methodological and background sources.

## Implications for data governance and reuse
- Data lineage: SGI derived from reconstructed groundwater levels; standardised across sites to enable comparability with other drought indicators.
- Interoperability: SGI aligned with meteorological drought indices (SPI) and hydrological drought indices (SSI) for integrated drought assessment.
- Metadata richness: site coordinates, aquifer type, and WELLMASTER identifiers support spatial analyses and data discovery.
- Data availability and provenance: historical reconstructions and GLUE-based uncertainty are explicitly documented, enabling informed use and interpretation.

## Practical considerations for data leaders
- Use cases: drought history analysis, coherence checks between groundwater and meteorological drought signals, planning references for water utilities.
- Data quality and gaps: stronger representation in Chalk and southern/eastern England; sparse records prior to 1890s and limited pre-1960s observations for some sites; uncertainties quantified via GLUE.
- How to apply: leverage Prob0/Prob1/Prob15/Prob2 to assess likelihoods of groundwater drought conditions and compare with SPI/SSI benchmarks.
- Governance takeaways: well-documented data provenance, standardized methodology, and explicit uncertainty underpin trustworthy cross-site analyses and cross-domain collaborations.

## Acknowledgments and references
- Funded by the Natural Environment Research Council (Historic Droughts project; NE/L010151/1).
- Key methodological references: GLUE methodology (Beven & Freer, 2001); standardised drought indices (McKee et al., 1993; WMO, 2012); groundwater drought framework (Bloomfield & Marchant, 2013; Bloomfield et al., 2018).