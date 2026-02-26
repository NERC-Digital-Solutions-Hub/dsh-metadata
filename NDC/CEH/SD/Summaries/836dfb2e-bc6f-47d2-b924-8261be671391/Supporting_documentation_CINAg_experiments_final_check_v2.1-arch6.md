# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- A multi-country project (CINAg) aiming to optimise farm practices and soil management to improve nitrogen use efficiency (NUE) and reduce environmental Nr losses, with translation to Chinese farmers via the Science and Technology Backyard programme.
- Objectives include developing novel NUE indicators, holistic soil-health metrics, field-testing on farm platforms, and knowledge exchange.

## Aims and scope

- Develop indicators and real-time metrics to inform farm practices and soil management for better agronomic NUE and sustainable crop production.
- Test and develop on-field experiments and farm platforms to support sustainable intensification.
- Translate developments to Chinese farmers through established CAU/CAAS programmes.

## Project structure (work packages)

- WP1: Improved fundamental understanding of N cycling
- WP2: Harnessing novel N technologies
- WP3: Improved agronomic practices
- WP4: Predictive capacity and knowledge exchange

## Study sites and platforms

- Four UK farm platforms: North Wyke (NW), Harpenden (HA), Henfaes (HF), Easter Bush (EB).
- 2016–2017 experiments: inorganic fertilizer grass trials (NW, HF, EB) and digestate trials on winter wheat (NW, HF); additional grass trials at EB and HA in 2017.
- 2018 UK-wide soil sampling across nine sites with at least two land uses per site (Scotland, Wales, England).
- Site details include soil types, textures, mean annual temperature (MAT) and precipitation (MAP); locations and coordinates provided in tables and figures.

## Experimental design and timeline

- 2016: Inorganic fertilizer experiments on grassland (NW, HF, EB) with total N application ~240 kg N ha-1; randomized blocks; treatments: Urea (U), Urea + urease inhibitor (IU), Ammonium-nitrate (AN), and Controls; plots subdivided for NH3, N2O, and biomass/yield measurements.
- 2017: Digestate experiments on winter wheat (NW, HF) with five replicates per digestate treatment (digestate only, digestate + DMPP inhibitor, acidified digestate, acidified digestate + DMPP, control); harvest/subplot layout; target N rate ~190 kg N ha-1 as digestate.
- 2018: UK-wide sampling across diverse land uses and soils; includes previously involved UGRASS sites and additional fields; biomass measurements across seasons.
- Pre-treatment and plot layouts documented; digestate trials included precise timing of application dates and biomass harvests.

## Data collection and measurements

- Yields and biomass
  - Dry matter yields (t ha-1), forage quality metrics (crude protein, ME, NDF, ADF, etc.), and digestibility estimates.
  - Harvest methods varied by site; central harvest strips and subplots used for sampling; harvest equipment included small plot harvesters and Sampo combine in different sites.
- Wheat N content, N offtake and NUE
  - Total crop N content derived from crude protein or direct analyses; N offtake calculated from grain/straw yields and N content; NUEc and NUEg calculated relative to N applied.
- Greenhouse gases
  - Ammonia (NH3) and nitrous oxide (N2O) measurements using wind tunnels, static manual/automatic chambers, and passive samplers.
  - NH3 concentration measured via citric acid traps with colorimetric analysis; NH3 fluxes computed from concentration differences, wind speed, and tunnel volume; cumulative NH3 emissions estimated via area under the curve.
  - N2O fluxes measured with static chambers (manual and automatic); data processed to derive hourly fluxes and cumulative emissions, with different replication schemes per site.
  - For EB grass trial, N2O fluxes derived with static chambers and a dispersion model; cumulative fluxes modeled using Bayesian (MCMC) approaches.
- Soil sampling and metric suite (WP1 and WP2)
  - Topsoil cores (0–15 cm) and deeper samples (up to 30 cm) collected across sites and dates; T0/T1/T2 timing in 2016–2017; five samples per topsoil per site in 2018.
  - Nitrogen metrics: NH4+, NO3-, amino acids, peptides, mineralisable N; DOC and TDN; DON derived.
  - Microbial and biological metrics: soil microbial biomass C and N (MBC/MBN); DNA extraction and qPCR for nitrogen-cycle genes (nifH, amoA AOA/AOB, nirK, nirS, nosZ I/II, ureC); amplicon sequencing (16S rRNA and ITS) for diversity indices.
  - Physical-chemical soil properties: aggregate size distribution, texture (sand/silt/clay), moisture, soil organic matter (LOI), pH, electrical conductivity (EC), base cations (Na, K, Ca, Mg), total C and N, total P; POXC; extractable P pools (CE, Olsen, acetic acid extractable P); CDOC/TDN.
  - Infiltration and water retention: soil water infiltration with Mini Disk Infiltrometer; water release curves with hyprop and WP4, modeling with HYPRO-FIT and bimodal retention models.
- Plant and soil biodiversity
  - DNA extractions and qPCR data for nitrogen-cycling genes; amplicon sequencing data processed with standard pipelines; diversity metrics (Shannon, Richness) and community composition.
- Metadata, QA/QC
  - Protocols clearly separated for WP1 vs WP2; sampling days aligned within sites; QA/QC with standards, blanks, replicates; instrument calibration and cross-site data checks.
- Data processing and analytics
  - NUE calculations, N content conversions (e.g., CP-to-N using a 6.25 factor for grass in early years); N2O cumulative flux estimation via area under the curve; N2O dynamics modeled with lognormal distributions and Bayesian inference (JAGS) for cumulative emissions; use of R for computations (lm, cumtrapz, etc).

## Data management, standards and accessibility

- Data collection and processing workflows are described in detail, with consistent protocols across sites and years.
- References to LIMS-based data handling, data quality checks, and QC procedures.
- Project outputs include peer-reviewed publications and public project webpage, with links to datasets and datasets’ DOIs where applicable.

## Outputs and publications

- Publications derived from these datasets include:
  - Carswell et al., 2018. Assessing the benefits and wider costs of different N fertilisers for grassland agriculture.
  - Sánchez-Rodríguez et al., 2018. Advanced processing of food waste-based digestate for mitigating nitrogen losses in winter wheat.
- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Datasets underpinning these publications are described and can be requested or accessed through project channels.

## Appendices and protocols

- Detailed appendices (A1–A3) document fertiliser application rates, harvest dates, and digestate pre-treatment layouts.
- Site layouts and experimental designs included to enable data re-use and replication.
- Pre-treatment information for digestate experiments and fully randomized plot designs with treatment labeling.

This summary highlights how the project generates, manages, and analyzes multi-site, multi-year data to support data-driven insights into nitrogen use, soil health, and environmental outcomes, providing data products, standardized protocols, and QA/QC frameworks suitable for data-support workflows.