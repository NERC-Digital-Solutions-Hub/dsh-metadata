# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview
- A multi-site UK-China project (CINAg) aimed at optimizing farm practices and soil management to improve nitrogen use efficiency (NUE) and reduce environmental Nr losses.
- Seeks holistic soil health metrics by integrating novel indicators with real-time physical and chemical data.
- Aims to translate findings to Chinese farmers via the Science and Technology Backyard programme.

## Aims and scope
- Develop novel NUE indicators and combine them with real-time metrics to deliver holistic soil health assessments that inform farming practices.
- Test and develop on-field experiments and farm platforms to enable sustainable intensification.
- Translate developments to farmers in China to support poverty reduction and community enrichment.
- Structured into four Work Packages (WPs):
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## Experimental design and locations
- Four UK farm platforms (2016–2017):
  - North Wyke (NW), Harpenden (HA), Henfaes Farm (HF), Easter Bush (EB)
- 2018 UK-wide soil sampling across nine sites with at least two land uses per site
- Site information includes soil types, textures, mean annual temperature, and precipitation
- Cross-platform and cross-UK sampling to capture variability in soils, climates, and management

## Data types and indicators (key measures)
- Plant/biomass outcomes
  - Yields (dry matter), forage quality metrics (crude protein, metabolisable energy, fibre components, digestibility)
  - Aboveground biomass across grass and wheat trials
- Nitrogen metrics
  - NUE at crop and whole-crop levels (N content, N offtake, NUEc, NUEg)
  - Nitrogen input-output balance for different fertiliser regimes (inorganic fertilisers, digestate)
- Greenhouse gas measurements
  - Ammonia (NH3) emissions (fluxes measured with wind tunnels and dispersion models)
  - Nitrous oxide (N2O) emissions (static chambers, automated chambers, or dispersion-based approaches)
- Soil nitrogen metrics (topsoil 0–15 cm or targeted depths)
  - Ammonium (NH4+), nitrate (NO3-), amino acids, peptides, mineralisable N
  - DOC and TDN (dissolved organic carbon and nitrogen)
  - Microbial biomass C and N (MBC, MBN)
  - Aggregate size distribution, soil texture, soil moisture and soil organic matter (SOM)
  - pH, electrical conductivity (EC)
  - Base cations (Na, K, Ca, Mg)
  - Total soil C and N, total P
  - Permanganate oxidisable carbon (POXC)
  - Phosphorus pools: citric acid extractable P, acetic acid extractable P, Olsen-P
- Soil biogeochemistry and biology
  - DNA, nitrogen-cycling genes (nifH, amoA AOA/AOB, nirK/nirS, nosZ, ureC)
  - Microbial diversity indices (Shannon, richness) and OTUs
  - Bacterial and fungal community composition (16S rRNA and ITS amplicon sequencing)
- Hydrology and soil physics
  - Soil water infiltration, soil water release curves (HYPRO-FIT modelling)
- Measurements and sampling cadence
  - WP1: soil cores at multiple depths; sampling dates aligned with fertiliser events
  - WP2: intensive soil sampling following N applications, then weekly to monthly
  - 2018 UK-wide sampling aligned with land uses and biomass measurements
- Outputs
  - Reports, charts, dashboards, and scientific publications
  - Public availability of datasets in line with data provenance and governance

## Protocols and data processing
- Clear separation of WP1 and WP2 protocols; sampling days harmonised within each site
- Yields and quality analysis
  - Grass: harvest regimes; DM, CP, ME, NDF, ADF, D value; NIR-based quality analysis
  - Wheat: grain and straw yields; moisture content; total N
  - NUE calculations using standard formulas comparing treated plots to controls
- Gas sampling and emissions
  - NH3: wind tunnels, acid traps, concentration measurements, and area-based flux calculations
  - N2O: manual and automated chambers; concentration time series used to compute fluxes; cumulative fluxes via area-under-curve or Bayesian approaches
- Soil sampling and analyses (WP1 and WP2)
  - NH4+, NO3−, amino acids, DON/DON; mineralisable N via anaerobic incubation
  - DOC/TDN, MBC/MBN, aggregate distribution, texture, moisture, SOM (LOI), pH, EC
  - Base cations via ammonium acetate extraction and ICP-OES
  - Total C and N via elemental analysers
  - Total P via acid digestion and colorimetry; Olsen-P and CE-P through standard extraction and colorimetric methods
  - POXC as a soil quality metric
- Advanced molecular analyses
  - DNA extraction, qPCR for nitrogen-cycling genes, amplicon sequencing for bacteria and fungi
  - Diversity metrics and OTU-level analyses; bioinformatic pipelines for 16S and ITS data
- Data processing and modelling
  - Statistical analyses in R; Bayesian MCMC (JAGS) for N2O cumulative flux with lognormal models
  - Inverse dispersion modelling for NH3 fluxes (EB grassland data)
  - QA/QC protocols with standards, replicates, and laboratory controls
- Data management and provenance
  - Data are collected across multiple labs and platforms with harmonised protocols
  - References to project website and publications for data access
  - Emphasis on sharing underlying data and ensuring data quality and traceability

## Data governance, metadata and sharing considerations
- Acknowledges the need to overcome barriers to data sharing (metadata gaps, data ownership, openness)
- Emphasises data quality assurance, data cleaning, transformations, and clear presentation of findings
- Highlights the importance of publicly sharing underlying data and establishing governance processes
- Project outputs include disseminated outputs (reports, dashboards) and public-facing publications
- Provides a pathway for policy-relevant monitoring by translating complex measurements into actionable NUE and soil-health indicators

## Challenges and considerations for monitoring frameworks
- Data availability and quality
  - Gaps in data and metadata; access constraints; need for timely data
- Inter-organisational silos
  - Cross-site coordination and data harmonisation challenges
- Data sharing barriers
  - Public sharing requirements for datasets; maintaining up-to-date data
- Metadata and data transformation
  - Inadequate metadata; transformation of diverse datasets into usable formats
- Communicating complex findings
  - Translating technical results into clear, policy-relevant messages
- Data governance and stewardship
  - Implementing robust governance to ensure datasets meet standards and remain accessible

## Key takeaways for policy and decision-makers (monitoring framework perspective)
- The CINAg project demonstrates how to build a multi-site monitoring framework to evaluate NUE and environmental nitrogen losses
- It integrates agronomic, environmental, and molecular data to form comprehensive indicators of soil health and nutrient use efficiency
- It provides a structured approach to data collection, processing, and sharing across platforms, with explicit QA/QC and statistical modelling
- The framework supports evidence-based decisions for improved fertiliser practices, soil management, and dissemination to farmers, aligned with policy goals on sustainable agriculture and environmental protection
- It highlights the importance of governance, metadata, and stakeholder engagement to ensure data transparency and utility for monitoring and policy evaluation