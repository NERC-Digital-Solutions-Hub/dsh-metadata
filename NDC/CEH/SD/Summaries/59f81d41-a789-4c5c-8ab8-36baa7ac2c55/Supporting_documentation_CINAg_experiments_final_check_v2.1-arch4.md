# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview and Aims
- International CINAg project to optimise farm practices and soil management for better use of nitrogen sources and reduction of Nr losses to the environment.
- Objectives include developing novel indicators of nitrogen use efficiency (NUE) and holistic soil health metrics, testing on-field practices and farm systems for sustainable intensification, and translating developments to Chinese farmers via the Science and Technology Backyard programme.
- Structure includes four work packages: WP1 (N cycling fundamentals), WP2 (novel N technologies), WP3 (improved agronomic practices), WP4 (predictive capacity and knowledge exchange).

## Data Assets and Sources
- Multi-site data across the UK: four farm platforms (North Wyke NW, Harpenden HA, Henfaes HF, Easter Bush EB) and nine additional UK sites for 2018 sampling.
- Experimental data types (examples):
  - Treatments and yields: inorganic fertiliser trials (grass), digestate trials (winter wheat), and 2018 UK-wide surveys.
  - Plant metrics: herbage N content, N offtake, NUEc and NUEg, dry matter yields, forage quality (CP, ME, NDF, ADF, etc.).
  - Greenhouse gas measurements: ammonia (NH3) emissions and nitrous oxide (N2O) fluxes.
  - Soil metrics: NH4+/NO3-, amino acids/peptides, mineralisable N, DOC/TDN, microbial biomass C/N, aggregate size distribution, texture, moisture, SOM, pH, EC, base cations, total C and N, total P, POXC, P fractions (CE, Olsen, acetic acid extractable P).
  - Biological data: DNA extractions, qPCR targets (nifH, amoA, nirK, nirS, nosZ, ureC), OTUs, microbial diversity indices.
  - Physical and hydrological data: soil infiltration, water release curves, soil moisture, rainfall and temperature (meteorological data at multiple sites).
- Documentation and dissemination: project webpage and publications derived from the datasets.

## Experimental Design and Data Generation
- 2016 Inorganic fertiliser experiments (grass trials) conducted at NW, HF, EB with three-cut silage system; treatments include Urea, Urea with urease inhibitor (IU), Ammonium-nitrate (AN), and Controls; all plots received P, K, S per guidelines.
- 2017 Digestate experiments (winter wheat) at NW and HF; five digestate-related treatments (digestate only, digestate + nitrification inhibitor, acidified digestate, acidified digestate + NI, control) in a complete randomized block design.
- 2018 UK-wide sampling: soils and above-ground biomass across nine sites with at least two land uses per site; included grazing exclusion cages at actively grazed fields for biomass estimation; moss meshes at Plynlimon to assess moss growth.
- Layout and site metadata: four main farm platforms with coordinates, soil types, textures, mean annual temperature (MAT) and precipitation (MAP); nine UK sites with diverse land uses (Table summaries and site figures referenced).

## Protocols, Processing and QA/QC
- Distinction between WP1 (in-season soil and plant metrics) and WP2 (on-farm processing and technologies); sample dates and protocols adjusted to site conditions, but standardized within WP.
- Yield and biomass protocols: harvest methods customized per site; sub-sampling for quality analyses; NIR-based quality metrics; conversion to per-hectare basis.
- NUE calculations: based on total crop N uptake (grain and straw) minus controls, divided by N applied; specific equations provided for different sites.
- Greenhouse gases: NH3 fluxes measured with wind tunnels and air samplers; N2O fluxes measured via manual and automatic chambers; cumulative fluxes calculated using area under the curve or Bayesian models depending on method and site.
- Soil sampling protocols: 0–15 cm topsoil cores and deeper cores; KCl extractions for Nr (NH4+/NO3-); DON/N forms; DOC/TDN measurements; soil microbial and biochemical assays; QA/QC includes blanks, reference soils, replicates, and instrument calibration.
- DNA and microbial analyses: MoBio DNA extraction; qPCR for nitrogen-cycle genes; amplicon sequencing (16S rRNA, ITS) with data processing pipelines; diversity metrics computed with standard R packages.
- Soil physical and chemical characterisation: texture by laser diffraction; pH and EC; exchangeable bases; total C and N by combustion or CN analyzer; POXC; various P metrics; QA/QC embedded throughout (standards, replicates, and cross-lab checks).
- Data processing tools: R (lm, cumtrapz, Bayesian analyses with JAGS), LIMS for data capture, Microsoft Excel-based data compilation, and specialized software for spectroscopy and sequencing data.

## Data Management and Access
- Data captured across institutions with standardised protocols; key datasets stored in LIMS and associated Excel files; QA/QC procedures built into each batch.
- Publications and datasets produced from the CINAg program:
  - Examples include assessments of different N fertilisers for grassland systems and processing of digestate for mitigating nitrogen losses.
- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Data outputs linked to collaborative publications and data papers; data sharing primarily through project publications and data releases associated with CINAg.

## Challenges and Risks for Data Leaders
- Cross-site heterogeneity: multiple sites, farms, and countries with differing soils, climates, and management practices; potential inconsistencies in measurements and sampling schedules.
- Data gaps and fragmentation: scattered datasets across WP1 and WP2, with variations in timing, depth, and methods; some sites faced operational issues (e.g., cages movement, drought effects on 2018 biomass sampling).
- Metadata completeness and standardization: ensuring consistent metadata across sites, experiments, and years to enable integrative analyses.
- Measurement complexity and QA: diverse measurement techniques for NH3, N2O, soil N metrics, and molecular data requiring rigorous QA/QC and traceability.
- Reproducibility and data integration: combining agronomic, soil, gaseous emission, and genomic data into holistic NUE and soil-health indicators; ensuring transparent data processing pipelines (R, JAGS) and documentation for reuse.
- Access and governance: coordinating data sharing among multiple institutions while preserving data provenance and enabling knowledge exchange with external partners (including Chinese collaborators).

## Key Takeaways for Data Leaders
- Build a cohesive data strategy that unifies multi-site agronomic, soil, gas-emission, and molecular datasets under common metadata standards to enable holistic NUE and soil-health indicators.
- Invest in robust data governance: centralized data management (LIMS), consistent sampling timelines, clear documentation, and open workflows (R/JAGS) to support reproducibility.
- Prioritize data discoverability and accessibility for user-need alignment: identify data consumers (policy colleagues, farmers, researchers) and co-ownership opportunities for data products and dashboards.
- Emphasize interoperability across WP1 and WP2 to translate experimental findings into practical farming recommendations and scalable knowledge transfer to partners like CAU/CAAS.
- Plan for uncertainty and variability inherent in multi-site data by applying Bayesian approaches and transparent uncertainty quantification in key outputs (e.g., cumulative N2O fluxes, NUE), and by documenting assumptions and priors.