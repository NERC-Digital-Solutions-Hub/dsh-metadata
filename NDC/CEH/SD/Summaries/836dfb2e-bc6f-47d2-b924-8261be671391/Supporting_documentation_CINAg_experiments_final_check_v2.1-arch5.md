Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview and Aims
- International project CINAg aims to optimise farm practices and soil management to use nitrogen efficiently and reduce environmental Nr losses.
- Develop novel indicators of nitrogen use efficiency (NUE) and real-time soil health metrics to inform practice.
- Test and develop field experiments and farm platforms for sustainable intensification.
- Translate developments to Chinese farmers via the Science and Technology Backyard programme.
- Structure includes four work packages: WP1 fundamental N cycling; WP2 novel N technologies; WP3 improved agronomic practices; WP4 predictive capacity and knowledge exchange.

## Project Structure and Work Packages
- WP1: Improved fundamental understanding of N cycling.
- WP2: Harnessing novel N technologies.
- WP3: Improved agronomic practices.
- WP4: Predictive capacity and knowledge exchange.

## Data Collection: Farm Platforms and UK Sites
- Four UK farm platforms (North Wyke, Harpenden, Henfaes, Easter Bush) used for fertiliser experiments in 2016–2017; EB site added in 2016–2017.
- 2018 UK-wide sampling across nine sites with at least two land uses per site.
- Farm platform details:
  - North Wyke (NW) and Harpenden (HA): Rothamsted Research.
  - Henfaes Farm (HF): Bangor University.
  - Easter Bush (EB): Centre for Ecology & Hydrology (CEH).
- Site coordinates and soils varied; climate (mean annual temperature, precipitation) recorded to contextualise results.
- 2018 UK-wide sites included a mix of land uses (arable, grassland, pasture, biodiverse margins, etc.) across Scotland, Wales, and England.

## Meteorological Data
- NW and HF: daily rainfall and temperatures; soil moisture sensors at 2.5 cm depth for water-filled pore space (WFPS).
- EB: handheld probes for soil temperature and WFPS; long-term station data at Engineer’s Field for air/soil temperature and rainfall.
- Data collected to interpret gas fluxes, nutrient dynamics, and microbially mediated processes.

## Experimental Information and Designs
- Two multi-platform experiments (2016 and 2017); additional 2017 grass trials at EB and HA.
- 2016 inorganic fertiliser experiments (grass trials) across NW, HF, EB; complete randomized block design (EB had four control plots and four replicates per treatment).
- 2017 digestate experiment (winter wheat) at NW and HF; complete randomized block with five control plots and five replicates per digestate treatment; subplots allocated for harvest and sampling.
- 2017 EB/HA grass trials included additional setups.
- 2016–2017 treatments:
  - Inorganic fertilisers for grass: Urea (U), Urea with urease inhibitor (IU), Ammonium-nitrate (AN), Control.
  - Digestate trials for wheat: Digestate (Dig), Digestate + nitrification inhibitor (DMPP), Acidified digestate (Dig + Ac), Acidified + DMPP, Control.
- Plot layouts and harvest/sampling subplots described; field operations conducted with manual or mechanised methods depending on site.

## UK-wide Sampling and Protocols (2018)
- Sampling across land uses and soils; biomass measurement through grazing-exclusion cages or predefined harvests.
- Sampling days aligned to site schedules; full growing season harvest when advised by managers.
- Data gathered to complement WP1 and WP2 outcomes and extend across wider landscapes.

## Protocols and Data Processing
- Protocols differentiated for WP1 (soil/plant measurements around fertiliser events) and WP2 (detailed processing of treatments and soil/biogeochemical metrics).
- Sampling performed on all treatment plots on the same day per site; harvests timed to reach peak biomass when possible.

### 5.1 Yields (Herbage Production and Quality) and Biomass
- Measurement of dry matter yields, fibre and protein content, metabolisable energy, digestibility, and related quality metrics.
- Grass trials (2016): three silage cuts; biomass harvested and sub-sampled for quality analyses (NIR-based) and conversion to plot-based yields.
- EB 2016: 1 m2 subplots harvested; composition analyses performed.
- EB 2017: harvest with larger plots and on-board weighing; grain and straw analyses for wheat.
- 2018 UK-wide sampling: aboveground biomass assessed within cages (where applicable) with dry biomass quantified.

### 5.2 Wheat N Content, N Offtake and NUE
- N content in harvested plant material (grass or grain) used to compute N content, N offtake, and NUE (NUEc and NUEg).
- Calculations based on N content, yields, and treatment differences relative to controls.

### 5.3 Sampling of Greenhouse Gases: Ammonia and Nitrous Oxide
- Ammonia (NH3) measured using wind tunnels and passive samplers; cumulative NH3 flux calculated per plot by integrating concentration differences and wind volume.
- Nitrous oxide (N2O) measured with manual and automated chambers; fluxes converted to standard units; cumulative fluxes estimated via area-under-curve methods.
- 2016 inorganic fertiliser: NH3 measured across selected treatments; 2017 digestate: NH3 sampling intensified post-application.
- 2017 N2O measurements used manual and automated chambers with isotopic analysis at HF; movement between treatments adjusted over time.
- EB site used static chambers with GC analysis for N2O; Bayesian methods applied to derive cumulative flux estimates.

### 5.4 Soil Sampling and Associated Metrics
- WP1: topsoil cores (0–15 cm) across treatments; multiple depths (0–30 cm) for WP2; sampling dates aligned with experiments.
- 2016–2017: soil sampling schedules outlined; 2018: five topsoil samples per site per land use.
- 5.4.1–5.4.16 cover a wide suite of soil analyses:
  - Nitrogen metrics: NH4+, NO3-, amino acids, peptides, mineralisable N.
  - Dissolved organic carbon and total dissolved N (DOC/TDN); DON inferred.
  - Microbial biomass C and N (MBC/MBN); soil microbial QA/QC in labs.
  - Aggregate size distribution; soil texture (sand, silt, clay) via laser diffraction.
  - Soil moisture and soil organic matter (SOM) by LOI; pH and electrical conductivity (EC).
  - Base cations (Na, K, Ca, Mg).
  - Total soil C and N; total P; POXC as a quality carbon metric.
  - Phosphorus fractions: citric acid extractable P, acetic acid extractable P, Olsen-P.
  - DNA, nitrogen cycling genes: qPCR targeting nifH, amoA (AOB/AOA), nirK/nirS, nosZ, ureC; microbial diversity indices (Shannon, richness) from amplicon sequencing (16S rRNA and ITS).
  - Infiltration and water release curves: hydraulic conductivity and soil-water characteristic curves.
- QA/QC across soil analyses included lab standards, occasional reference soils, replicates, and data validation before release.

### 5.4.13–5.4.16 Molecular and Diversity Analyses
- DNA extractions and qPCR for nitrogen-cycle genes to quantify functional groups.
- Amplicon sequencing (16S rRNA for bacteria/archaea; ITS for fungi) on Illumina MiSeq; data processed with standard pipelines; rarefaction and QA steps described.
- Diversity metrics (Shannon, richness) computed in R.

## Data Management, QA/QC, and Access
- Data organized by WP1 and WP2 protocols; process and storage through LIMS and spreadsheets; cross-lab QA procedures implemented.
- Reproducibility supported by detailed methods, standard curves, and QA checks; use of standard methods and controls.
- Outputs include a project website and peer-reviewed publications; datasets referenced in published work and accessible via project pages.

## Outputs, Publications, and Access
- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Notable publications deriving from datasets (examples):
  - Assessing the benefits and wider costs of different N fertilisers for grassland agriculture.
  - Advanced processing of food waste-based digestate for mitigating nitrogen losses in winter wheat.
- Datasets underpinning these outputs include extensive field data, soil metrics, gas flux measurements, and molecular analyses.