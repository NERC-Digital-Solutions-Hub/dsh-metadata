# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview
- International CINAg project aims to optimise farm practices and soil management to improve nitrogen use efficiency (NUE) and reduce nitrogen losses to the environment.
- Collaboration across China and the UK with multiple research institutions.
- Structure centered on four work packages (WP1–WP4) to advance understanding, technologies, practices, and predictive capacity, with knowledge exchange to farming communities.

## Aims and structure
- WP1: Improve fundamental understanding of nitrogen cycling.
- WP2: Harness novel nitrogen technologies.
- WP3: Improve agronomic practices.
- WP4: Predictive capacity and knowledge exchange.
- Translational goal: apply findings with CAU/CAAS programs to Chinese farmers through established Science and Technology Backyard initiatives.

## Field locations, experimental platforms, and sampling
- Four UK farm platforms (NW North Wyke, HA Harpenden, HF Henfaes, EB Easter Bush) used for inorganic fertiliser experiments (2016) and a digestate experiment on winter wheat (2017); additional grassland trials conducted at EB and HA in 2017; cross-UK soil sampling in 2018 at nine sites with diverse land uses.
- Site data include soil type, texture, mean annual temperature (MAT), mean annual precipitation (MAP), and coordinates.
- Meteorological data collected via on-site weather stations (NW, HF, EB) with daily rainfall and temperature; soil moisture via SDI-12 sensors at depth; EB included long-term meteorological data from a dedicated measurement station.

## Experimental design and treatments
- Inorganic fertiliser experiments (2016): complete randomized blocks at NW, HF, EB with four treatments:
  - Urea (46% N)
  - Urea with urease inhibitor (IU)
  - Ammonium nitrate (AN, ~36% N)
  - Control
- Total N applied: 240 kg N/ha; plots divided into subplots for NH3 emission measurements, N2O emission measurements, and biomass/yield measurements.
- Digestate experiment (2017): complete randomized block design at NW and HF with five digestate-related treatments:
  - Digestate only
  - Digestate + nitrification inhibitor (DMPP)
  - Acidified digestate
  - Acidified digestate + DMPP
  - Control
- Target N input as digestate: ~190 kg N/ha (rates varied in the field); plots split into harvest and sampling subplots.
- 2018 UK-wide sampling: nine sites with at least two land uses per site to capture variability across soils and management.

## Data collection and measurements (WP focus)
- Yields and quality (grass and wheat):
  - Dry matter yields, crude protein, metabolisable energy, fibre metrics, and digestibility indicators.
  - Harvest methods varied by site; standardised to convert to yield per hectare where possible.
- Nitrogen content and use efficiency:
  - Grass N content (kg N ha^-1) derived from crude protein; N offtake (kg N ha^-1); NUEc (crop NUE) and NUEg (grain NUE) calculated from N offtake, controls, and N inputs.
- Greenhouse gas measurements (NH3 and N2O):
  - Ammonia: wind tunnel measurements and acid trap analysis; cumulative NH3 emissions calculated per plot.
  - N2O: manual and/or automatic static chambers; gas analyses via chromatography or isotopic analyses; cumulative fluxes computed using area-under-curve methods and Bayesian/MCMC approaches for time-series data.
- Soil sampling and analyses (WP1 and WP2):
  - Depths: 0–15 cm and deeper where applicable; frequent sampling after fertiliser/digestate applications (e.g., first weeks post-application, then weekly/monthly).
  - Nitrogen metrics: NH4+, NO3-, amino acids, peptides, mineralisable N.
  - Dissolved organics: DOC and total dissolved N (TDN); DON via difference.
  - Microbial biomass: MBC and MBN via chloroform fumigation technique.
  - Physical-chemical soil properties: aggregate size distribution, texture (sand/silt/clay), soil moisture, soil organic matter, pH, EC, base cations (Na, K, Ca, Mg), total C and N, total P.
  - Phosphorus pools: POXC, citric acid extractable P, acetic acid extractable P, Olsen-P.
  - DNA-based analyses: gene targets for nitrogen cycling (nifH, amoA qPCR for AOB/AOA, nirK, nirS, nosZ, ureC); microbial diversity indices; OTUs via 16S rRNA (bacteria/archaea) and ITS (fungi).
  - Infiltration and water-release: soil infiltration (mini-disk infiltrometer) and soil water retention curves (HYPRO-FIT and related methods).
- UK-wide soil and biomass data (2018):
  - Aboveground biomass via exclusion cages where applicable; adjusted for field conditions; species composition considered in some sites.
  - Land-use and site variability documented (nine sites across Scotland, Wales, and England).

## Protocols and data processing
- Sampling timing varied by WP (WP1 vs WP2) but within-site sampling occurred on the same day; crops harvested to peak biomass.
- Data handling:
  - Yields and quality data compiled by partner institutions; NUE calculations using standard ratios of N content and fertilizer input.
  - NH3/N2O data processed with site-specific protocols; NH3 fluxes converted to cumulative emissions; N2O fluxes calculated per chamber and aggregated over time with Bayesian methods.
  - Soil data processed with multiple labs and QA/QC checks; data stored in LIMS and Excel; inter-lab QA included reference standards and duplicate measures.
  - Molecular data: qPCR efficiency and specificity checked; standard curves generated; amplicon sequencing data processed with established pipelines (GreenGenes for bacteria, UNITE for fungi); diversity analyses performed in R.
- Data management and quality control:
  - Two-tier QA/QC across laboratories; random replicates; calibration with standards; documentation of sampling dates and methods.
  - Data and metadata captured to enable cross-site comparability; some data stored in project-specific repositories and published with related outputs.

## Outputs, dissemination, and data access
- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Publications arising from the datasets (example titles provided) detailing benefits and costs of different N fertilisers, and advances in processing of digestate for mitigating nitrogen losses.
- Data produced across multiple domains (soil chemistry, gas fluxes, crop yields, microbial genetics) intended for integration into policy-relevant insights and knowledge exchange.

## Appendices and references
- Appendices include detailed fertiliser and digestate treatment schemes, plot layouts, and site-specific harvesting dates.
- Comprehensive references cover methods for soil analyses, gas flux measurements, statistical modelling (MCMC, lognormal flux modelling), and molecular techniques.

## Relevance to Monitoring Frameworks (key takeaways)
- Rich, multi-site dataset spanning agronomic practices, soil health indicators, and environmental emissions, suitable for monitoring policy impacts on NUE and Nr losses.
- Clear delineation of data types, collection protocols, and QA/QC procedures supports data quality, transparency, and reproducibility.
- Integration of physical, chemical, and biological indicators enables holistic assessment of soil health and agronomic performance, aligning with the aim to develop holistic metrics for informing farm management decisions.
- The structure anticipates data governance considerations (data provenance, metadata, sharing through LIMS/excel pipelines; cross-institution collaboration) while highlighting typical barriers such as data heterogeneity, access, and maintenance of up-to-date metadata.