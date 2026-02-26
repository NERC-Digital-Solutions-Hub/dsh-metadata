# Biodiversity and structural data from hedgerow management and rejuvenation experiments in England, 2005-2016

## Overview
- A set of long-running hedgerow experiments in England (2005–2016) funded by Defra (BD2114) to study effects of hedgerow management on biodiversity and habitat quality, and to develop practical restoration options.
- Three linked experiments with randomised and factorial designs across multiple field sites:
  - Experiment 1: effects of hedgerow cutting timing (autumn vs winter) and frequency (annual, 2-year, 3-year) on hawthorn-based biodiversity and hedgerow structure.
  - Experiment 2: effects of timing, intensity, and frequency of cutting on herbaceous and woody diversity at four sites.
  - Experiment 3: rejuvenation treatments (e.g., Midlands/conservation hedgelaying, wildlife hedging, circular saw, coppicing) plus subsequent management, across five field sites.
- Data cover biodiversity (flowers, berries, pollinators, invertebrates), vegetation composition, hedgerow structure, and regrowth processes.
- Data collected using standardized protocols, transcribed to Excel, and stored in an Oracle database; includes historic pre-2005 data for Experiment 1.

## Experimental design and field sites
- Experiment 1 (2006–2014): randomised plots across four hedgerows on former arable land near Monks Wood, testing cutting frequency and timing.
- Experiment 2 (2010–2016): full factorial 2 × 2 × 3 design (time of cutting, intensity, frequency) applied at five sites: Marsh Gibbon (MG), Woburn (WO), Waddesdon Blackthorn (WB), Waddesdon Mixed (WM), Yarcombe (YC).
- Experiment 3 (2010–2013 rejuvenation and post-treatment management): five sites (MW, NE, UG, WH, CB) where rejuvenation treatments were applied to hedgerows, followed by a split-plot management regime.
- Notable events: one MG block suffered an operational error in 2014 causing cessation of monitoring at that site; WB winter cutting not applied due to hedge condition.

## Data collected and main variables
- Vegetation composition and baseline parameters
  - BaselineSpecies.csv: species presence, cover, and depth within hedge plots.
  - BaselineParameters.csv: non-species parameters (e.g., hedge height/width, gaps, historic management, margins).
- Flower production and hedge dimensions
  - Flowers.csv: flower counts/cover for target species; quadrat-level data where applicable.
  - Dimensions.csv: hedge height and width measurements across replicates.
- Berry availability
  - Berries.csv: total and biomass of berries by species; sampling details and subsamples.
  - BerriesQuadrats.csv: quadrat-level berry counts/cover by species.
- Pollinators and pollinator-plant interactions
  - Pollinators.csv, PollinatorsFieldMarginFlowers.csv, PollinatorsFlowersCounts.csv, PollinatorsFlowersQuadrats.csv, PollinatorsHedgeFlowers.csv: timed visitation counts, flower presence, pollinator taxa, and field-margin flora data.
  - Data include temperature, wind, cloud cover, and pollinator taxonomic resolution.
- Invertebrates
  - Invertebrates.csv, InvertebratesWeight.csv, InvertebrateEggSurveys.csv: counts and weights by taxa; sampling methods (beating, guttering); Lepidoptera eggs for select species.
- Hedge structure
  - Gap.csv: gaps/hedge area derived from photos, by height class and year.
  - Structure.csv: hedge coverage estimates from photos, including hedge vs. gap metrics.
- Hedgerow regrowth and regrowth metrics (Experiment 2 and 3)
  - RegrowthAerial.csv, RegrowthBranch.csv, RegrowthLeaves.csv, RegrowthSeedlings.csv, RegrowthShoots.csv, RegrowthStool.csv, RegrowthTotals.csv, RegrowthWeight.csv: aerial regrowth, branch regrowth, seedling counts, basal stool measurements, shoot lengths, diameters, weights.
  - ShootCount.csv, ShootMeasurements.csv: integrity and extension measurements of regrowth shoots.
- Recording and data management
  - Data collected on standardized sheets, transcribed to Excel, then loaded into Oracle DB with data quality checks.
  - Treatment codes and a mapping table provided to interpret experimental treatments (e.g., annual/biennial/triennial, autumn/winter, standard vs incremental cutting, rejuvenation types).

## Data structure and access
- File types (examples of key files)
  - BaselineSpecies.csv, BaselineParameters.csv: baseline hedge species and site parameters.
  - Flowers.csv, Dimensions.csv: flower data and hedge dimensions.
  - Berries.csv, BerriesQuadrats.csv: berry counts/weights; quadrat data.
  - Pollinators.csv, PollinatorsFieldMarginFlowers.csv, PollinatorsFlowersCounts.csv, PollinatorsFlowersQuadrats.csv, PollinatorsHedgeFlowers.csv: pollinator observations and plant-pollinator context.
  - Invertebrates.csv, InvertebratesWeight.csv, InvertebrateEggSurveys.csv: invertebrate abundance and weights; eggs for select species.
  - Gap.csv, Structure.csv: hedgerow gaps and structural metrics from imagery.
  - RegrowthAerial.csv, RegrowthBranch.csv, RegrowthLeaves.csv, RegrowthSeedlings.csv, RegrowthShoots.csv, RegrowthStool.csv, RegrowthTotals.csv, RegrowthWeight.csv: regrowth datasets by type.
  - ShootCount.csv, ShootMeasurements.csv: regrowth at Experiment 2 sites.
- Identifiers and metadata
  - Records are identified by combinations of EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, ASPECT, VISIT_DATE/YEAR, and species/taxa.
  - Photos and image-derived metrics include HEIGHT_CLASS and HEDGE_PERCENTAGE/AREA metrics.
- Data provenance and quality
  - Standardized data collection protocols; expert validation of species lists; anomaly checks during transcription and database import.
  - Some historic data pre-date the formal visit-year convention (Experiment 1). Missing values reflect survey lapses and were noted during data curation.

## Site and sampling notes
- Field sites involved across multiple hedgerow types:
  - MG (Marsh Gibbon), WO (Woburn), WB (Waddesdon Blackthorn), WM (Waddesdon Mixed), YC (Yarcombe) for Experiment 2.
  - MW (Monks Wood), NE (Newbottle Estate), UG (Upcoate Grange), WH (Wimpole Hall), CB (Crowmarsh Battle) for Experiment 3.
- Sampling included seasonal timing (autumn and winter cuts), multiple years, and both fixed plots and contiguous hedge sections.

## How the data can be used (data products and analyses)
- Assess the biodiversity outcomes of different hedgerow management strategies (cutting timing/frequency, intensity, rejuvenation methods) across taxa (flowers, berries, pollinators, invertebrates) and structure.
- Compare across experiments to identify robust management practices that enhance habitat quality and resource provisioning for wildlife.
- Link vegetation structure (gaps, hedge density) to biodiversity metrics and regrowth dynamics over time.
- Build data products (dashboards, reports) enabling end-users to explore plots by treatment, site, and year, and to examine flowering/berry provisioning and pollinator service potential.

## Notable limitations and considerations
- Experimental complication: Marsh Gibbon site experienced an autumn 2014 contractor error, ending treatment application and monitoring from 2015 onward at that site.
- WB winter-cutting treatments were not applied at WB due to hedge conditions.
- Some historic Experiment 1 data exist without exact dates (only year) for pre-visit records.
- Data gaps reflect occasional missing measurements or recording oversights, though quality control steps are described.

## References and acknowledgments
- References to foundational restoration studies and hedgerow management work are provided.
- Acknowledgments to key data collectors and contributors; funding from Defra and management by UK Centre for Ecology & Hydrology (UKCEH).