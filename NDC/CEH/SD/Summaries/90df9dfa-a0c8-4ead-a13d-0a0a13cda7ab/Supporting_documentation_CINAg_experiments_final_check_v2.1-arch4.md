# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- A multinational research program (CINAg) aims to optimise farm practices and soil management to improve nitrogen use efficiency (NUE) and reduce environmental Nr losses, with UK-China collaboration.
- Four work packages (WP1–WP4) structure the program: 
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange
- Partnerships span multiple UK institutions and farms, plus cross-UK field platforms and a wider network for soil and crop assessment.

## Aims and data-centric perspective for Data Leaders

- Develop novel indicators of NUE and integrate physical/chemical soil metrics to produce holistic soil health and quality metrics that inform farming practices.
- Test and scale indicators and knowledge in on-field experiments and farm platforms to enable sustainable intensification.
- Translate developments to Chinese farmers via the Science and Technology Backyard program.
- Emphasis on data systems that support understanding of the whole data cycle: collection, processing, analysis, feedback, and dissemination.

## Project structure and data landscape

- Data are generated across four UK farm platforms (NW, HA, HF, EB) and expanded to nine UK sites in 2018 for broader soil and biomass sampling.
- Locations:
  - NW (North Wyke), HA (Harpenden), HF (Henfaes Farm), EB (Easter Bush)
- 2018 cross-UK sampling includes diverse land uses to capture variability in soil and vegetation responses.
- The project web page and published outputs provide access to processed results and methods.

## Data types and measurements

- Agronomic and yield data:
  - Grass yields (dry matter), yield quality metrics (crude protein, ME, NDF, ADF, etc.), biomass measurements.
  - Wheat (winter wheat) yield components when applicable (grain and straw dry weights).
- Plant N metrics:
  - Grass N content, N offtake, nitrogen use efficiency (NUEc, NUEg).
- Soil nitrogen metrics (WP2/WP1 focus):
  - NH4+, NO3-, amino acids, peptides, mineralizable N
  - DOC and TDN; DON estimates
  - Soil microbial biomass C and N (MBC/MBN)
  - Aggregate size distribution, soil texture (sand/silt/clay)
  - Soil moisture and organic matter (SOM)
  - pH and electrical conductivity (EC)
  - Base cations (Na, K, Ca, Mg)
  - Total soil C and N; total P
  - POXC (permanganate oxidisable carbon)
  - Citric acid extractable P, acetic acid extractable P, Olsen-P
- Soil biogeochemistry and molecular data:
  - DNA extraction, qPCR targets for nitrogen cycling genes (nifH, amoA AOA/AOB, nirK/nirS, nosZ clades I & II, ureC)
  - OTUs and microbial diversity indices (Shannon, richness)
  - Amplicon sequencing (16S rRNA and ITS regions) with rarefaction and diversity analyses
- Gas flux measurements:
  - Ammonia (NH3) volatilization (wind tunnels, passive samplers, dispersion modeling)
  - Nitrous oxide (N2O) emissions (static chambers, manual and automatic chambers, isotopic analysis)
- Physical and hydrological data:
  - Soil infiltration rates and soil water release curves
  - Meteorological data (temperature, rainfall) at multiple platforms
- Data collection scope:
  - Experiments conducted in 2016 (inorganic fertiliser on grass), 2017 (digestate on winter wheat and additional grass trials), and 2018 UK-wide sampling
- Data outputs are designed to feed into NUE indicators, real-time soil health metrics, and knowledge exchange.

## Experimental design and platforms

- Inorganic fertiliser trials (grass, 2016) across NW, HF, EB with four treatments (Urea, Urea+inhibitor IU, AN, Control) in a randomized block design; plots subdivided for NH3, N2O, biomass, and harvesting.
- Digestate experiment (winter wheat, 2017) at NW and HF with five digestate treatments plus controls; randomized block design; harvest and sampling subplots defined for yield and soil measurements.
- UK-wide sampling (2018) across multiple land uses and soil types to capture broader system responses.
- Pre-treatment standardization (soil preparation, liming, P/K/Mg inputs) to ensure consistent baseline conditions where feasible.

## Protocols, data processing, and QA/QC

- Clear separation of data collection protocols for WP1 (soil metrics, baseline and end-of-cycle sampling) and WP2 (process measurements, treatments, and repeated sampling post-application).
- Yields and quality analyses performed by partner labs with standardized lab methods; NUE calculations based on total plant N content and N applied.
- Gas measurements:
  - NH3: wind tunnel measurements, acid traps, and colorimetric analysis; cumulative NH3 emissions calculated using area-under-curve methods.
  - N2O: manual and automatic chamber measurements; both hourly flux calculations and cumulative flux via Bayesian/lognormal modeling (MCMC with JAGS) to accommodate spatial and temporal variability.
- Soil sampling and analyses:
  - Topsoil cores (0-15 cm) and deeper samples (as appropriate) with standardized extraction and analysis for NH4+, NO3-, amino acids, DON, DOC/TDN, MBC/MBN, POXC, P fractions, and total C/N.
  - Aggregate size distribution via laser diffraction; texture by laser and traditional methods; LOI for SOM; pH/EC with standard protocols; base cations via ammonium acetate extraction and ICP-OES.
- DNA/RNA and microbial analyses:
  - DNA extraction, qPCR for nitrogen-cycle genes, and amplicon sequencing for bacteria and fungi; diversity indices calculated with standard bioinformatics pipelines; QA/QC includes controls, standards, triplicates, and rarefaction thresholds.
- Data governance and storage:
  - Use of LIMS and Excel-based datasets across labs; QA/QC checks, standard references, and cross-lab calibration.
  - Reproducibility supported by detailed protocols, samples, and timing, with dates and site metadata recorded for traceability.
- Data processing tools:
  - R used for statistical analyses and curve fitting (cumtrapz, MCMC workflows).
  - Publication-ready datasets and supporting documentation generated from the experimental outputs.

## Data management implications for Data Leaders

- Data heterogeneity across sites, platforms, and years necessitates a central, standardized metadata schema to enable discovery, integration, and reuse.
- The programme demonstrates end-to-end data flows from field measurement through laboratory analyses to statistical modeling (e.g., NUE calculations, N2O/NH3 flux modeling) and dissemination.
- QA/QC processes are embedded at multiple levels (laboratory standards, QA samples, replication, and cross-lab checks), illustrating robust data governance practices.
- The combination of traditional laboratory measures, advanced molecular data, and process-based emissions models calls for interoperable data schemas and clear data provenance.
- Outputs include both quantified agronomic indicators (NUE, yields) and process-level metrics (GHG fluxes, soil nutrient pools, microbial community structure), enabling comprehensive data products for policy colleagues and researchers.
- Data sharing and knowledge translation are explicit objectives, with outputs aimed at both scientific audiences and end-user farming communities (via Science and Technology Backyard).

## Challenges and opportunities highlighted for Data Leaders

- Data are dispersed across numerous sites, years, and measurement modalities, posing challenges for data standardization and integration.
- Gaps in data granularity and completeness (e.g., differential sampling frequencies across WP1/WP2 and sites) require careful harmonization and documentation.
- Access and discoverability depend on the availability of project webpages, LIMS, and potentially publications; ensure open, well-documented data access policies where possible.
- Coordination across sector partners and labs is essential to minimize duplication and maximize the value of cross-site datasets.
- Metadata richness (site characteristics, soil types, management history, sampling dates) is critical for secondary analyses and transferability to other contexts.

## Endnotes and outputs

- The document references project webpage and two key publications detailing benefits, wider costs, and advanced processing of digestate data.
- Appendices detail site-specific fertiliser rates, harvests, and pre-treatment information, underscoring the need for precise data lineage.
- The work sits within a broader ecosystem of soil–N research, with contributions to NUE metrics and soil health indicators that can inform policy and practice.