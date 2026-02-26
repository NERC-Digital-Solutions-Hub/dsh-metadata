# Biodiversity and structural data from hedgerow management and rejuvenation experiments in England, 2005-2016

## Overview
- A comprehensive dataset from long-running hedgerow experiments in England (2005–2016) focused on management to maintain and restore hedgerow biodiversity and habitat quality under agri-environment schemes.
- Three interconnected experiments (1–3) captured a wide range of management practices, including cutting timing, frequency, intensity, and hedgerow rejuvenation techniques.
- Measured outputs cover vegetation composition, flowering and berry production, pollinator and invertebrate activity, and hedgerow structural characteristics.

## Experimental Design and Sites
- Experiment 1 (2006–2014): Randomised plot experiment testing effects of hedgerow cutting timing (autumn/winter) and cutting frequency (annual, 2-year, 3-year) on hawthorn-based hedgerows at Monks Wood, with adjacent unmanaged controls.
- Experiment 2 (2010–2016): Randomised block experiment across four field sites to test:
  - Time of cutting (early autumn vs. late winter)
  - Intensity of cutting (standard cut back to old cut line vs. incremental height increase)
  - Frequency of cutting (annual, every two years, every three years)
  - Full factorial design with three replicates per site (contiguous hedgerow blocks 15–20 m long).
- Experiment 3 (2010 rejuvenation year; 2011–2013 management): Rejuvenation treatments applied to 24 m plots, including Midlands hedge-laying, Conservation hedge-laying, Wildlife hedging, Circular saw reshaping, Coppicing, and Control. Post-rejuvenation management varied (annual vs. every two to three years, uncut) in a split-plot design across five field sites (MW, NE, UG, WH, CB).
- Field sites: Marsh Gibbon (MG), Woburn (WO), Waddesdon (WB), Yarcombe (YC), Monks Wood (MW), Newbottle Estate (NE), Upcoate Grange (UG), Crowmarsh Battle (CB), and Waddesdon Blackthorn (WB) with specific site characteristics and planting histories.

## Data Collected and Key Variables
- Vegetation composition and structure
  - BaselineSpecies.csv and BaselineParameters.csv: species presence, cover, depth in hedge plots; structural parameters (height, width, gaps, historic management, adjacent land, margins, ditch adjacency).
  - Hedge structure metrics derived from high-resolution winter photographs: Gap.csv and Structure.csv (hedge vs. gaps; area, max/min axes, and hedgerow vs. sheet classification).
- Flowering and berry production
  - Flowers.csv and FlowersCounts/Quadrats (Dimensions.csv): counts and percent cover of hawthorn, blackthorn, bramble flowers; quadrat-level sampling and measurement of hedge area.
  - Berries.csv and BerriesQuadrats.csv: total berry counts and biomass per species; quadrat-level berry data allowing cross-check with plot totals.
- Pollinators and associated flora
  - Pollinators.csv, PollinatorsFieldMarginFlowers.csv, PollinatorsFlowersCounts.csv, PollinatorsFlowersQuadrats.csv, PollinatorsHedgeFlowers.csv: timed pollinator observations, species/taxa, visitation counts, temperature, wind, cloud cover, and habitat context (hedge base and margins).
  - Field-margin flora data and cross-linking with hedge flora to assess pollinator-resource relationships.
- Invertebrates
  - Invertebrates.csv and InvertebratesWeight.csv: counts and biomass by taxa, with sampling method (beating or guttering) and taxon grouping; weight data for higher-level groups.
  - InvertebrateEggSurveys.csv: counts of Lepidoptera eggs for selected species.
- Regrowth and hedgerow recovery (Experiment 2 & 3)
  - ShootRegrowth: RegrowthAerial.csv, RegrowthBranch.csv, RegrowthLeaves.csv, RegrowthSeedlings.csv, RegrowthShoots.csv, RegrowthStool.csv, RegrowthTotals.csv, RegrowthWeight.csv: aerial regrowth, branch regrowth, seedling recruitment, stool regrowth, branch/shoot biomass and weights.
  - ShootCount.csv and ShootMeasurements.csv: shoot counts and detailed measurements for regrowth assessment (height, diameter, weight, twig data).
  - Regrowth data cover Crataegus monogyna primarily, with multiple sites.
- Data recording and provenance
  - Data captured on standardized recording sheets by experienced surveyors.
  - Transcribed to Excel, then loaded into an Oracle database with quality checks during transcription and import.
  - Data across experiments linked via consistent identifiers: experiment, site, plot, aspect, visit date/year, treatment codes, and species/taxa names.
- Data codes and interpretation
  - Treatment codes (1–25) map to specific combinations of timing, frequency, intensity, rejuvenation or control conditions; a dedicated code table explains annual/biennial/triennial, autumn/winter timing, standard vs incremental cutting, and various rejuvenation techniques.

## Quality, Governance, and Notes
- Standardized protocols, experienced field surveyors, expert validation of species lists.
- Systematic data checks to identify anomalies during transcription and after database import.
- Historic data present in baseline and some experiments; visit date and visit year recorded where possible.
- Missing values typically reflect field collection gaps rather than data corruption; a thorough data check and curation were performed at upload.
- Notable site-specific issues: MG site experienced an contractor error in 2014 causing cessation of treatments at that site from 2015 onward; winter cutting not applied at WB due to site-specific constraints.

## File Structure and Data Dictionary Highlights
- Vegetation and baseline data
  - BaselineSpecies.csv: species presence, surface cover, depth category per hedge plot and year.
  - BaselineParameters.csv: hedge height/width measurements, gaps, land-adjacency metrics, historic management, ditch adjacency, field margins.
  - Dimensions.csv: hedge height/width measurements across replicates.
- Flowering and berries
  - Flowers.csv: per-plot counts or percent cover for target species; quadrat-level data when applicable.
  - Berries.csv and BerriesQuadrats.csv: total and subsample berry metrics; biomass (fresh/dry) and sample sizes.
- Pollination ecology
  - Pollinators*.csv: timed pollinator observations with taxa, counts, temperatures, weather context, and sampling area.
  - PollinatorsFieldMarginFlowers.csv and PollinatorsFlowersQuadrats.csv: field-margin and quadrat-level flower data used to contextualize pollinator resources.
  - PollinatorsFlowersCounts.csv: cross-matched flower counts for selected plant species.
- Invertebrates
  - Invertebrates.csv and InvertebratesWeight.csv: taxa counts and biomass by sampling method and taxon group.
  - InvertebrateEggSurveys.csv: Lepidoptera egg counts by site and year.
- Hedge structure and gaps
  - Gap.csv: gap counts and areas by hedge plot, height class, and photo year.
  - Structure.csv: hedge/structure coverage and area metrics derived from photos.
- Hedge regrowth and rejuvenation
  - ShootCount.csv and ShootMeasurements.csv: regrowth counts and shoot metrics by site, year, position, species, twig data.
  - RegrowthAerial.csv, RegrowthBranch.csv, RegrowthLeaves.csv, RegrowthSeedlings.csv, RegrowthShoots.csv, RegrowthStool.csv, RegrowthTotals.csv, RegrowthWeight.csv: multi-faceted data on regrowth dynamics, biomass, leaf and wood metrics, and seedling regeneration.
- Data management and treatment mapping
  - Treatment codes table accompanying the data to interpret experimental design (annual/biennial/triennial, autumn/winter timing, standard vs incremental cutting, rejuvenation vs control).

## Accessing and Using the Data
- The dataset provides rich, multi-year, multi-site monitoring coverage of hedgerow management effects on biodiversity and habitat structure.
- It supports analyses of how timing, frequency, intensity of cutting, and rejuvenation interventions influence plant communities, flowering and fruiting resources, pollinator activity, invertebrate diversity, and hedgerow architecture.
- Provenance and metadata are embedded through explicit file descriptions, standardized recording practices, and a coherent coding system for treatments and experiments, aiding comparability and integration into monitoring frameworks.

## Acknowledgements and Funding
- Recognizes contributions from field teams, data collectors, and analysts.
- Funded by Defra (BD2114) and managed by UK Centre for Ecology & Hydrology (UKCEH).