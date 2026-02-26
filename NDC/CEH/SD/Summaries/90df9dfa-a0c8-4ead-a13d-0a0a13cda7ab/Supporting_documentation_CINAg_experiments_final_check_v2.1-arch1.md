# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Overview: Documentation for the CINAg project, detailing experimental design, data collection, protocols, and data processing related to improving nitrogen use and reducing environmental Nr losses.
- Aim of the data: Facilitate analysis of nitrogen cycling, NUE indicators, soil-health metrics, and predictive understanding to inform farm practices and policy; support knowledge transfer to farmers via established programs.

## Project aims and structure

- Primary objectives:
  - Develop novel indicators of nitrogen use efficiency (NUE) and holistic soil-health metrics combining real-time physical/chemical data.
  - Test and develop on-field experiments and farm platforms for sustainable intensification.
  - Translate findings to Chinese farmers through the Science and Technology Backyard program.
- Work packages (WP):
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## Experimental footprint: locations and sites

- Four UK farm platforms (2016–2017):
  - North Wyke (NW), Harpenden (HA), Henfaes (HF), Easter Bush (EB)
  - Experiments included inorganic fertilizer grass trials and a digestate trial on winter wheat; additional grass trials at EB and HA in 2017.
- UK-wide sampling (2018):
  - Nine sites across Scotland, Wales, and England with at least two land uses per site (e.g., arable, pasture, silage, park grass), enabling broader soil-plant N dynamics assessment.
- Site information:
  - Detailed coordinates and field names; soil types and textures characterized per site; climate context (MAT, MAP) provided.

## Meteorological and soil data collection

- NW and HF:
  - Daily rainfall and daily temperature metrics at site, with soil moisture sensors (SDI-12) at shallow depth for soil moisture status.
- EB:
  - Soil temperature and water-filled pore space (WFPS) measured with handheld probes; long-term meteorological data from a permanent Edwards Bush station (30-min intervals).
- Purpose: support flux calculations (NH3, N2O) and soil N metrics under varying weather/climate contexts.

## Experimental designs and treatments

- Inorganic fertilizer experiments (grass trials, 2016; EB also 2017):
  - Complete randomized block design; four treatments: Urea (U), Urea with urease inhibitor (IU), Ammonium nitrate (AN), and Control.
  - Total N application around 240 kg N ha-1; plots sub-divided for NH3 measurement, N2O measurement, and biomass/yield assessments.
- Digestate experiment (winter wheat, 2017):
  - Complete randomized block design at NW and HF with five digestate treatments plus control; additional subplots for harvest and sampling.
  - Target N application 190 kg N ha-1 as digestate; digestate application bands per plot; timing in March–April 2017.
- EB grass trials (2016–2017):
  - Additional involvement as part of multi-site setup; site-specific layouts described.
- 2018 UK-wide sampling:
  - Expanded scope to include nine sites with diverse land uses for soil and above-ground biomass measurements.

## Protocols and data processing

- General approach:
  - Protocols specified separately for WP1 (process-level measurements) and WP2 (treatments and validations). All plots sampled on the same day per site; harvest timing aligned with farm managers’ guidance.
- 5.1 Yields and biomass
  - Grass yields (DM) and quality metrics (crude protein, ME, fibres, ash, digestibility) via NIR; above-ground biomass measured per site with region-specific harvest methods.
  - Wheat grain/straw yields and components measured; grain moisture and TGW reported; end-of-season biomass for NW/HF EB.
- 5.2 N content, N offtake, NUE
  - Grass N content from crude protein (factor 6.25); N offtake calculated from yields and N content; NUE calculated relative to N applied and control plots.
  - EB sites used Kjeldahl total N analysis; NUE calculated similarly.
- 5.3 Greenhouse gases: NH3 and N2O
  - NH3: small wind tunnels with acid traps; cumulative emissions calculated via area-under-the-curve; EB used dispersion-model-based NH3 flux estimation (FIDES) with air samplers for background and plot-centered sampling.
  - N2O: manual and automatic static chambers; sampling frequency tailored to treatment and site; concentration analyses via GC with headspace; cumulative fluxes computed with area-under-the-curve; digestion/dose-normalized metrics used for cross-treatment comparisons.
  - Bayesian/MCMC methods employed (JAGS) to estimate cumulative emissions and to model N2O flux dynamics (lognormal framework, time-to-peak, decay).
- 5.4 Soil sampling and metrics
  - WP1: Topsoil (0–15 cm) cores; diverse sampling dates (T0, T1, T2 in 2016; post-digestate initiation in 2017; 2018 sampling by land use/site).
  - WP2: Intensive soil sampling after N fertiliser events; depth 0–10 cm for NH4+ and NO3-; additional sampling within sampling plots for digestate experiments.
  - Soil nitrogen metrics: NH4+, NO3-, amino acids, peptides, mineralisable N; extractions with 1 M KCl; colorimetric and fluorometric assays.
  - DOC and TDN measured from K2SO4 extracts; microbial biomass carbon and nitrogen (MBC/MBN) via fumigation extraction; aggregate size distribution; soil texture (laser diffraction), moisture and SOM (LOI), pH, EC; base cations (Na, K, Ca, Mg) by ICP-OES after ammonium acetate extraction; total soil C and N by elemental analysis; total P by H2O2/H2SO4 digestion and colorimetry.
  - POXC and various P fractions (CEH Bangor CEH; Olsen-P; acetic-citrate extractable P) analyzed with colorimetric methods and calibrations.
  - DNA and nitrogen-cycle genes:
    - DNA extraction from soil; qPCR targets include nifH, amoA (AOB and AOA), nirK, nirS, nosZ (clade I and II), ureC; 16S rRNA and ITS amplicon sequencing for bacterial/ fungal diversity.
  - Microbial diversity indices: Shannon, Richness; OTUs/Actual Sequence Variants; analysis pipelines using GreenGenes, UNITE, DADA2; rarified diversity metrics.
  - Soil hydraulic properties: water infiltration (mini-disk infiltrometer), water retention curves (HyProp and WP4) with Mualem–Durner and Peters–Durner models.
  - QA/QC: use of reference standards, random replicates, LIMS integration; cross-lab QA processes; data validation steps prior to project management review.
- Data processing and analytics
  - Data compiled in Excel; metabolic- and molecular- level analyses performed across WP1 and WP2; dedicated statistical workflows in R; Bayesian methods (MCMC via JAGS) for N2O flux in field trials.
  - Metadata, data provenance, and datasets intended to be uploaded to portals with metadata to support discoverability.

## Data management, outputs, and dissemination

- Data handling philosophy:
  - Emphasis on tracking data sources and making datasets discoverable with metadata; alignment with project’s aim to inform policy and farm practice.
- Publications and datasets:
  - Carswell et al. 2018: Assessing the benefits and wider costs of different N fertilisers for grassland agriculture.
  - Sánchez-Rodríguez et al. 2018: Advanced processing of food waste-based digestate for mitigating nitrogen losses in winter wheat.
- Project portal and links:
  - Project webpage: www.rothamsted.ac.uk/international/china/cinag
  - Data-driven results feed into broader scientific outputs and policy-relevant insights.

## Appendices and references

- Appendix A contains detailed tables for inorganic fertilizer experiments and digestate experiments (application rates, dates, and plot layouts).
- References span soil-chemistry methods, N-cycle modeling, and molecular approaches (qPCR, amplicon sequencing) used across WP1–WP4.