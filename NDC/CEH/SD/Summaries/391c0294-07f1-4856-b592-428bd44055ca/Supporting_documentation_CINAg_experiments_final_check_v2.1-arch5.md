# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview

- International CINAg project aims to optimise farm practices and soil management to use nitrogen more efficiently and reduce Nr losses to the environment.
- Project objectives:
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange
- Scope includes cross-UK farm platforms and cross-UK sites (2016–2018) and translation to Chinese farming through a Science and Technology Backyard programme.
- Datasets span agronomic yields, nitrogen content and use efficiency, soil nitrogen metrics, soil chemistry, microbial community metrics, greenhouse gas measurements, and environmental context data.

## Data landscape and scope

- Experimental platforms and sites:
  - Four UK farm platforms: North Wyke (NW), Harpenden (HA), Henfaes (HF), Easter Bush (EB).
  - 2018: nine UK sites for soil and biomass sampling across Scotland, Wales, and England.
- Data types and variables:
  - Yields and biomass: dry matter yields, yield components, quality metrics (CP, ME, NDF, etc.), metabolisable energy, digestibility.
  - N metrics: herbage N content, N offtake, nitrogen use efficiency (NUEc, NUEg); grain and straw N analyses.
  - Greenhouse gases: ammonia (NH3) and nitrous oxide (N2O) fluxes; concentration measurements; dispersion and flux modeling.
  - Soil metrics: inorganic N (NH4+, NO3-), amino acids/peptides, mineralisable N; DOC/TDN; microbial biomass (MBC/MBN); aggregate size distribution; texture; moisture; SOM; pH and EC; base cations; total C and N; total P; POXC; extractable P pools (CE, Olsen, acetic acid extractable P).
  - DNA/RNA and microbial diversity: DNA extractions, qPCR targets for nitrogen cycling genes (nifH, amoA, nirK, nirS, nosZ, ureC) and 16S/ITS amplicon sequencing; OTUs and diversity indices; Shannon, richness.
  - Physical/soil properties: soil infiltration (infiltration rate), soil water release curves (HYPRO), hydraulic parameters.
  - Meteorology: site-specific weather data (rainfall, temperature), soil temperatures, water-filled pore space (WFPS).
- Temporal coverage:
  - 2016: inorganic fertilizer grass trials (NW, HF, EB).
  - 2017: digestate trials on winter wheat (NW, HF) plus grass trials at EB/HA.
  - 2018: UK-wide soil and biomass sampling (land-use comparisons).
- Governance and provenance elements:
  - Data contributed by multiple institutions (CEH, Rothamsted Research, Bangor University, etc.).
  - Public project webpage and listed publications for data access and reporting.

## Experimental design and data collection

- Experimental designs:
  - 2016 inorganic fertilizer grass trials: complete randomized block design at NW, HF; four fertilizer treatments (Urea, Urea + inhibitor IU, AN, Control) with P, K, S; three subplots per plot for NH3, N2O, and harvest measurements.
  - EB 2016: four control plots and four replicates per treatment; 2 m × 8 m plots.
  - 2017 digestate trial (NW, HF): complete randomized block design; five control plots and five replicates per digestate treatment (Digestate, Digestate + DMPP, Acidified Digestate, Acidified Digestate + DMPP, Control); harvest and sampling subplots.
  - 2017 UK-wide grass/digestate sampling: targeted across multiple sites with various land uses.
- Measurements and protocols:
  - Yields and biomass: multiple harvests; subsampling for quality metrics; NIR analysis for forage quality; crop mass and moisture assessments; grain/straw separation for wheat.
  - NUE and N content: calculation of total N content from crude protein where needed; NUEc and NUEg calculated from crop N offtake and N applied.
  - Gas sampling:
    - NH3: wind-tunnel measurements, acid traps, colorimetric analysis; cumulative NH3 flux computed via area under the curve.
    - N2O: manual and automated static chambers; gas chromatography and isotopic analyses; cumulative flux calculated with area-under-curve and Bayesian/time-analysis approaches.
- Soil sampling regimes:
  - WP1 (2016–2018): topsoil cores (0–15 cm) and deeper depths as per site; sampling before treatment, after key events, and post-harvest.
  - WP2 (digestate and follow-up): intense sampling after digestate application with high temporal resolution; 0–15 cm depth; 8 cores per plot pooled.
  - EB site N2O-related soil cores near flux measurement areas; storage and extraction protocols for Nr.
- UK-wide sampling (2018): land-use contrasts; biomass measurements; grazing/exclusion cages employed where applicable.

## Data processing, QA/QC and analysis

- Processing tools and methods:
  - R used for statistical analyses including N2O flux modeling and area-under-curve computations.
  - Bayesian modeling (MCMC via JAGS) for N2O cumulative flux estimation.
  - Standard analytical methods for soil chemistry (colorimetric assays, ion chromatography, spectrophotometry) and molecular analyses (qPCR, amplicon sequencing).
- QA/QC measures:
  - Laboratory standards and random replicates; cross-lab QA (Bangor, CEH, Rothamsted, etc.); calibration checks with reference soils and standard solutions.
  - Duplicates, blanks, and cross-validation with established reference methods and protocols.
  - Data validation steps by multiple personnel prior to release.
- Data processing outputs:
  - Tables and appendices detailing fertilizer application rates, harvest dates, and site-specific parameters (A1–A3).
  - Derived metrics such as NUE, N content, N off-take, and various soil/microbial indices.
- Data integration notes:
  - Data generated across WP1 and WP2 with differing sampling protocols but aligned by site and treatment; final outputs combine yields, soil chemistry, microbial data, gas fluxes, and environmental context.

## Metadata, standards and interoperability

- Site and protocol metadata:
  - Precise site coordinates, soil types, textures, MAT and MAP where available.
  - Experimental layout details, plot dimensions, replications, and treatment mappings.
- Variable definitions and units:
  - Clearly defined units for all measurements (e.g., N content, NUE percentages, mg N kg-1 soil, g kg-1, mg L-1, etc.).
  - For molecular data, gene targets, copy numbers per gram dry soil, and sequencing-derived diversity metrics.
- Documentation and references:
  - Appendices with detailed tables of treatments, harvests, and protocols.
  - References to standard methods and datasets underpinning analytic approaches.

## Data access, sharing and governance

- Access and dissemination:
  - Project webpage hosting information and links to related publications.
  - Datasets associated with linked publications and Supporting Documentation.
- Governance considerations for Data Stewards:
  - Ensure metadata completeness for cross-site harmonization (sites, depths, units, sampling dates, methods).
  - Maintain provenance: track instrument methods, labs, and analysts for each measurement type.
  - Standardize data formats and create a central repository or LIMS-compatible schema to consolidate WP1 and WP2 datasets.
  - Include data dictionaries and variable definitions to facilitate reuse by other researchers and governance bodies.
  - Version control and clear licensing/disclaimers for data reuse.

## Key data products and outputs

- Multi-dimensional dataset encompassing:
  - Agronomic outcomes: yields, biomass, grain vs. forage metrics, quality parameters, NUE calculations.
  - Soil N metrics: NH4+, NO3-, mineral N pools, amino acids/peptides, mineralisable N.
  - Organic/inorganic soil carbon metrics: DOC, TDN, DON, MBC, MBN, POXC, total C and N, soil P pools (CE, Olsen, acetic-extractable P).
  - Soil physical properties: texture, moisture content, SOM, pH, EC, base cations.
  - Microbial and functional data: DNA extractions, qPCR for nitrogen-cycling genes, OTU richness and composition, Shannon index, ITS/fungal data.
  - Gas emissions: NH3 and N2O fluxes, time-series data, model-derived cumulative flux estimates.
  - Meteorological and site context: temperature, rainfall, soil temperature, WFPS, long-term station data.
- Appendices with site lists, treatment schemes, and dates (A1–A3).

## Particular data stewardship considerations and challenges

- Complexity from multi-site, multi-year design across WP1 and WP2 requires careful harmonization of metadata, units, and sampling schemes.
- Data heterogeneity across laboratories and measurement techniques necessitates robust QA/QC documentation and cross-lab calibration records.
- Temporal variability (e.g., harvest timing shifts in 2018 due to drought) impacts comparability and requires explicit documentation of adjusted protocols.
- Large, diverse datasets (gas fluxes, molecular data, soil chemistry, and physical properties) demand a scalable data infrastructure with clear provenance and version control.
- The document provides explicit protocols and methodologies, enabling reproducibility but requires consolidated data dictionaries and standardized data schemas for long-term stewardship.

## Appendices and references

- Appendix materials include experimental design diagrams, site-level layouts, and detailed tables of fertilizer and digestate treatments, harvest dates, and measurements.
- References cover foundational methods for soil chemistry, gas flux calculations, molecular analyses, and statistical approaches used in data interpretation.
- Project webpage and listed publications provide avenues for data access and dissemination of findings.