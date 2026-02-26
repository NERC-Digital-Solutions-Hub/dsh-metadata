Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview
- Documentation for the CINAg project, a China-UK collaboration to optimise farm practices and soil management to improve nitrogen use efficiency (NUE) and reduce environmental Nr losses.
- Project structure includes four work packages: WP1 (N cycling), WP2 (novel N technologies), WP3 (improved agronomic practices), WP4 (predictive capacity and knowledge exchange).
- Extensive, multi-site data collection across four farm platforms in the UK (North Wyke, Harpenden, Henfaes, Easter Bush) and nine additional UK sites for 2018 sampling; aims to translate findings to Chinese farmers.

## Project and aims
- Develop novel indicators of NUE and holistic soil health metrics to inform farm management.
- Test and develop on-field experiments and farm platforms for sustainable intensification.
- Translate developments to Chinese farmers via the Science and Technology Backyard programme.

## Data architecture and datasets
- Datasets span agronomic yields, plant N content and N offtake, NUE metrics, soil inorganic N (NH4+, NO3−), amino acids and peptides, mineralisable N, DOC and TDN, microbial biomass C and N, DNA-based nitrogen cycling genes, OTUs and diversity indices, soil texture, moisture, pH, EC, base cations, total C and N, total P, POXC, various P fractions (CEH Bangor Olsen-P, citric/acetic extractable P), and root/aboveground biomass data.
- Gaseous emissions datasets include ammonia (NH3) fluxes and nitrous oxide (N2O) fluxes, with multiple measurement approaches (wind tunnels, static/manual and automated chambers, Isotopic N2O analyser) and modelling outputs (FIDES inverse dispersion, lognormal flux modelling).
- Meta-data and processing outputs are tied to: sampling dates, sites, land uses, plot layouts, treatment codes, and laboratory methods.
- Data processing pipelines involve R (glm, cumtrapz, MCMC with JAGS), Excel data compilations, LIMS integration, and standard QA/QC procedures.

## Study sites, platforms, and sampling scope
- Four farm platforms (UK): North Wyke (NW), Harpenden (HA), Henfaes Farm (HF), Easter Bush (EB). Cross-UK sampling across nine additional sites in 2018.
- Site details:
  - NW, HF, EB host inorganic fertiliser grass trials (2016) and digestate trials on winter wheat (2017); multiple plots and subplots for different measurements.
  - HA site used for additional grass trials in 2017.
  - EB site hosted grass trials (2016) and related measurements; 2017 digestate sampling included.
- 2018 UK-wide sampling encompassed diverse land uses and soil types (Table 3 references), with biomass and soil measurements across multiple sites (e.g., Silwood, Parsonage Down, Kirkton, etc.).

## Experimental design and treatments
- 2016 Inorganic fertiliser experiments (grass trials):
  - Locations: NW, HF, EB.
  - Complete randomized block design; four fertiliser treatments plus controls: 
    1) Urea (46% N), 2) Urea + urease inhibitor (IU), 3) Ammonium nitrate (AN, ~36% N), 4) Control.
  - Sub-plotting to accommodate NH3 emission measurements, soil sampling/N2O measurements, and biomass harvest.
  - Total N application around 240 kg N ha−1; P, K, S added per guidelines.
- 2017 Digestate experiment (winter wheat):
  - Locations: NW and HF; complete randomized block with five digestate treatments (digestate alone, digestate + nitrification inhibitor DMPP, acidified digestate, acidified digestate + DMPP, control).
  - Target N application: 190 kg N ha−1 as digestate (rates varied by plot).
  - Harvest/subplot design for biomass and grain/straw separation.
- 2018 UK-wide sampling:
  - Soil and aboveground biomass measurements across nine sites with at least two land uses per site.
  - Some sites re-visited from the UGRASS dataset.

## Protocols and data processing (WP1 vs WP2)
- Protocols are separated by WP1 (process and soil N metrics) and WP2 (functional N technologies and treatments); plot-level sampling occurred on the same day within a site, with dates adjusted for weather and crop phenology.
- Measurements include:
  - Yields and biomass: dry matter yield, crude protein, ME, N content, fibre fractions, digestibility, etc.; harvest methods varied by site, with subplots dedicated to yields and quality.
  - N content, N offtake, NUEc and NUEg: calculated from measured N in biomass or grain/straw and yields; treatment means compared to controls.
  - Greenhouse gases: NH3 volatilization via wind tunnels and NH3 traps; N2O via manual and automated chambers; flux calculations use standard equations, with cumulative emissions analysed via area under the curve or Bayesian approaches (MCMC in JAGS).
  - Soil sampling (WP1 and WP2): topsoils 0–15 cm (and deeper as needed); timepoints T0, T1, T2 for 2016; T1/T2 for 2017; 0–15 cm sampling across land uses in 2018; extractions (KCl for Nr, cations; CaCl2 for nitrification; standard colorimetric methods for NH4+/NO3−; amino acids via OPA-MET; mineralisable N via anaerobic incubation).
  - DOC and TDN from K2SO4 extracts; MBC/MBN via chloroform-killing assay; aggregate size distribution by laser diffraction; soil texture via laser diffraction; SOM by LOI; pH and EC; base cations via ammonium acetate extraction; total C and N by combustion methods; total P via peroxide/sulfuric digestion; POXC via permanganate oxidation.
  - Phosphorus fractions: CEH Bangor CE (citric acid extractable P) and Olsen-P (CEH Lancaster); acetic acid extractable P used as proxy for plant-available P in WP2.
  - DNA and microbial analyses: DNA extractions; qPCR for nitrogen cycling genes (nifH, amoA for AOB/AOA, nirK/nirS, nosZ I/II, ureC); 16S and ITS amplicon sequencing for bacterial/fungal communities; diversity metrics (Shannon, richness, OTUs); sequencing on Illumina MiSeq with standard pipelines and QC checks.
  - Microbial diversity indices: processed with Vegan in R; rarefaction and QC checks included.
  - Soil physical properties: infiltration (Mini Disk Infiltrometer), water release curves (HYPRO and HYPRO-FIT), and bimodal hydraulic models for retention.
- Data handling and QA/QC
  - Analytical labs used standard protocols with QA/QC standards (BS1, BS3) and replicate checks; calibrations and instrument checks performed regularly.
  - Use of LIMS for data capture; cross-lab coordination across NW, HF, EB, HA, CEH teams.
  - Data are often compiled in Excel files; unit standardization and moisture corrections applied; careful documentation of sampling dates and methods to support reproducibility.
  - Data processing scripts and statistical analyses (R, JAGS) documented; transparency around model structures (e.g., N2O flux modelling) and priors.

## Data management, governance, and accessibility
- Multi-institution collaboration with consistent data capture across sites; clear delineation of WP responsibilities for data types.
- Data provenance includes explicit sampling dates, site coordinates, plot names, fertiliser treatments, and measurement methods.
- Public-facing references include a project webpage and peer-reviewed publications (with DOIs).
- Appendices and supplementary materials (Appendix A: detailed tables for fertiliser/digestate experiments; 8. Appendices 8.1–8.2) provide granular, site-level metadata and experimental layouts.
- Data stewardship considerations embedded in the document:
  - Harmonisation of methods and units across sites and years.
  - Documentation of data processing steps and code (R, JAGS) for reproducibility.
  - Plans for updates and versioning via UK partners and the LIMS-based workflow.
  - Emphasis on metadata richness to enable reuse (site, land use, soil type, meteorology, treatment, sampling scheme).

## Appendices and references
- Appendices detail specific fertiliser and digestate treatments, dates, and plots (A1–A3).
- Comprehensive references support methods and models used (e.g., for NUE calculations, NH3/N2O measurement techniques, soil analyses, qPCR, sequencing pipelines, and soil physics models).
- Project webpage and selected publications provide data access points and examples of dataset usage.