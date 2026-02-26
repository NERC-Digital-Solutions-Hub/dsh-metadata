# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Purpose and aims
- International CINAg project to optimise farm practices and soil management for improved nitrogen use and reduced Nr losses to the environment.
- Develop novel indicators of nitrogen use efficiency (NUE) and holistic soil health metrics; integrate real-time physical and chemical indicators to inform practice.
- Test on-field practices across UK and China; translate developments to Chinese farmers via the Science and Technology Backyard programme.
- Work planned through four WPs:
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## Project structure and key activities
- Four UK-based farm platforms for controlled experiments: North Wyke (NW), Harpenden (HA), Henfaes (HF), Easter Bush (EB).
- UK-wide soil and biomass sampling in 2018 across nine sites with multiple land uses.
- Experimental programs:
  - 2016: Inorganic fertiliser trials on grassland across NW, HF, EB (three-cut silage system).
  - 2017: Digestate experiment on winter wheat at NW and HF; additional grass trials at EB and HA.
  - 2018: UK-wide soil sampling and aboveground biomass measurements across various land uses.
- Cross-cutting emphasis on data collection, site- and period-specific protocols, and integration of results for NUE and soil health.

## Experimental sites, layouts, and meteorology
- Four UK farm platforms:
  - NW (North Wyke, Devon) and HA (Harpenden, Herefordshire) operated by Rothamsted Research
  - HF (Henfaes Farm, North Wales) operated by Bangor University
  - EB (Easter Bush, Edinburgh) operated by CEH
- Site characteristics include soil types (e.g., Cambisols, Luvisols, etc.), textures, mean annual temperatures, and rainfall.
- 2018 sampling included nine sites across Scotland, Wales, and England with at least two land-use types per site.
- Meteorological data collected via on-site weather stations and instruments (rainfall, temperature, soil temperature, soil moisture at various depths); long-term data at Easter Bush measurement station.

## Data types and measurements
- Agronomic and biomass data
  - Yields: dry matter yields (tonnes per hectare); biomass quality metrics (crude protein, metabolisable energy, N-content, N-use efficiency).
  - For grass trials (2016): three silage cuts; sub-sampling for quality analyses.
  - For wheat trials (2017): grain and straw yields; thousand-grain weight; moisture.
- Nitrogen metrics
  - Herbage and crop N-content; N offtake; NUEc (crop NUE) and NUEg (grain NUE).
  - Soil nitrogen metrics: NH4+, NO3-, amino acids, peptides, mineralisable N; dissolved organic C (DOC) and total dissolved N (TDN); DON.
- Microbial and DNA data
  - Soil microbial biomass C and N (MBC/MBN); aggregate size distribution; DNA-based analyses for microbial diversity and nitrogen cycling genes (nifH, amoA for AOB/AOA, nirK/nirS, nosZ, ureC); qPCR data for gene copies.
  - Amplicon sequencing for bacteria (16S rRNA) and fungi (ITS) with analysis pipelines (GreenGenes, UNITE); diversity indices (Shannon, richness) and OTUs.
- Soil physical and chemical properties
  - Soil texture (sand/silt/clay), soil moisture, soil organic matter (LOI), pH, electrical conductivity (EC), base cations (Na, K, Ca, Mg), total C and N, total P.
  - Phosphorus forms: Olsen-P, citric acid extractable P (CEH Bangor), acetic acid extractable P (WP2).
  - Permanganate oxidisable carbon (POXC) as a soil quality indicator.
- Soil function and infiltration
  - Soil water infiltration (mini-disk infiltrometer) and soil water release curves (hyprop, WP4) for hydraulic parameters.
- Ammonia and nitrous oxide fluxes
  - NH3 volatilisation measured with wind tunnels and passive samplers; flux calculations using concentration differentials and tunnel geometry; cumulative NH3 emissions via area-under-curve methods.
  - N2O fluxes measured with static chambers (manual and automated) and, at some sites, isotopic analyses; cumulative fluxes modeled with Bayesian approaches and lognormal distributions.
- Aboveground biomass and land-use data
  - Biomass estimates from cages or cutting within plots; stratified sampling for competition with land-use types; grazing exclusion where applicable.

## Protocols and data processing (WP-specific)
- Data collection cadence tailored to WP1 (soil metrics, DNA/microbial indices) and WP2 (ecosystem gas fluxes and yields); sampling days aligned within sites but varied by weather and growth stage.
- Yields and quality data processing
  - Grass: multiple cuts; fresh weight and dry matter; NIRS-based quality analyses; conversion to per-area metrics.
  - Wheat: harvest-area estimates; grain and straw moisture corrections; total N analyses; NUE calculations.
- NUE calculations
  - NUEc and NUEg formulas comparing crop N offtake to N applied (including digestate or inorganic fertilisers) relative to controls.
- Gas sampling and analysis
  - NH3: flux calculation from inlet/outlet NH3-N concentrations and air flow; cumulative NH3 via area-under-curve.
  - N2O: flux calculations from chamber data; cumulative flux via area-under-curve or Bayesian time-upscaling (with MCMC in JAGS).
- Soil sampling and analyses
  - 0–15 cm topsoil cores with 0–30 cm deeper samples; KCl extractions for Nr; colorimetric, spectrophotometric, and LC methods for N species; DOC/TDN via AnalytikJena Multi N/C; POXC via permanganate oxidation; P forms via citrate/acetic extractions and colorimetric detection.
  - Soil texture by laser diffraction; LOI for SOM; pH and EC via standard methods; base cations by ammonium acetate extraction and ICP-OES.
  - Total soil C and N by elemental analysis (CN analyzer) or elemental combustion methods; total P via digestion and colorimetry.
- DNA and microbial data
  - DNA extractions, qPCR for nitrogen cycling genes; amplicon sequencing with Illumina MiSeq; data processing with standard pipelines; QA/QC with standards, controls, and read depth thresholds.
- Soil physical properties
  - Aggregate size distribution via sieving and laser diffraction; infiltration curves analyzed with HYPRO-FIT and related models; hydraulic parameters derived from bimodal soil water retention models.

## Data governance, QA/QC, and outputs
- QA/QC implemented across laboratories with reference standards (BS1, BS3), replicates, and cross-lab checks.
- Data stored and managed through common lab information management systems (LIMS) and Excel-based data compilations; outputs linked to project publications.
- Analytical methods and models documented (e.g., Bonferroni-like corrections not specified; Bayesian MCMC in JAGS; area-under-curve calculations; standard gas-chromatography and colorimetric procedures).
- Project webpage and publications provide access to datasets and results:
  - Project page: www.rothamsted.ac.uk/international/china/cinag
  - Publications (examples): "Assessing the benefits and wider costs of different N fertilisers for grassland agriculture" and "Advanced processing of food waste based digestate for mitigating nitrogen losses in a winter wheat crop."

## Appendices and data resources
- 8.1 Inorganic fertiliser experiment (2016): detailed fertiliser rates, dates, and harvests for HF, NW; 3 N-fertiliser treatments plus controls.
- 8.2 Digestate experiment (2017): pre-treatment crop establishment details; plot designs; digestate treatment layouts; sampling plans for WP1 and WP2.
- 5.4.15–5.4.16: Additional Protocols for soil infiltration and water release curves.

## Publications and related work
- Carswell et al. 2018: Assessing the benefits and wider costs of different N fertilisers for grassland agriculture.
- Sánchez-Rodríguez et al. 2018: Advanced processing of food waste based digestate for mitigating nitrogen losses in a winter wheat crop.
- Supporting datasets and related methodological references provided throughout (e.g., Keeney 1982; de Klein & Harvey 2012; Loubet et al. 2018; Levy et al. 2017).

## Key considerations for data leaders
- Data system scope: multi-site, multi-year, multi-method datasets spanning agronomy, soil science, microbiology, and atmospheric chemistry.
- Data interoperability and discoverability: standardized metrics, units, sampling times, and metadata across WP1 and WP2; alignment with LIMS and QA/QC standards.
- User needs and governance: datasets designed to support NUE indicators and soil health metrics; potential for cross-network collaboration and knowledge exchange.
- Gaps and challenges: scattered data sources across platforms; ensuring consistent metadata and access; coordinating cross-site protocols and data sharing.