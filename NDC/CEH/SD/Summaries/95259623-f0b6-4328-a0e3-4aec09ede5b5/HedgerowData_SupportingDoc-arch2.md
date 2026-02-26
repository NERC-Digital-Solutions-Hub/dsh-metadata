# Biodiversity and structural data from hedgerow management and rejuvenation experiments in England, 2005-2016

## Overview
- Long-running hedgerow experiments in England (2005–2016) to evaluate management and restoration on biodiversity and habitat resources under agri-environment schemes (ELS/HLS).
- Three linked experiments:
  - Experiment 1: effects of timing and cutting frequency on hawthorn-based habitat quality and resource provisioning; includes unmanaged controls.
  - Experiment 2: factorial study of timing, intensity, and frequency of hedgerow cutting across five field sites.
  - Experiment 3: rejuvenation treatments to restore hedgerow structure (and subsequent management) across multiple sites.
- Data intended for monitoring environmental health and policy performance over time, with standardized collection and quality controls.

## Experimental design and scope
- Experiment 1 (2006–2014): randomised plot experiment on four 1961 Monks Wood hedgerows; treatments vary cutting frequency (annual, biennial, triennial) and cutting timing (autumn vs winter); two unmanaged controls; replication 8 for annual and 4 for biennial/triennial per year.
- Experiment 2 (2010–2016): randomised block design across five sites (MG, WO, WB, WM, YC); full factorial treatments: time of cutting (Autumn vs Late Winter), intensity (Standard vs Incremental), frequency (Annual, Once every two years, Once every three years); 3 replicates per site per treatment; plots 15–20 m long.
- Experiment 3 (2010–2013 rejuvenation + 2011–2013 management): 12 m plots across five sites; rejuvenation techniques (Midlands hedge-laying, Conservation hedge-laying, Wildlife hedging, Circular saw reshaping, Coppicing, Control); split-plot management (no cutting vs periodic cutting); multiple site-specific replication.
- Field sites: five across England with hedgerows dominated by hawthorn, blackthorn, or mixed species (e.g., Marsh Gibbon MG; Woburn WO; Waddesdon WB; Waddesdon mixed WM; Yarcombe YC; Monks Wood MW; Newbottle NE; Upcoate Grange UG; Wimpole WH; Crowmarsh Battle CB).
- Key measures included biodiversity of flora and fauna, hedgerow structure, berry provision, and regrowth dynamics.

## Data components and what they measure
- Biodiversity and floral resources
  - BaselineSpecies.csv: species present, surface cover, and depth of penetration into hedge.
  - Flowers.csv: flower counts and percent cover by species within plots/quadrats.
  - Flower-related Dimensions.csv: hedge dimensions used to derive plot area for standardizing flower counts.
  - Pollinators*.csv and PollinatorsFieldMarginFlowers.csv: pollinator visitation rates and flowering plant presence in hedgerow bases and margins; taxa and pollinator groupings; environmental covariates (temperature, wind, cloud cover).
  - PollinatorsFlowersCounts.csv / PollinatorsFlowersQuadrats.csv / PollinatorsHedgeFlowers.csv: additional flower and pollinator data including quadrat-level counts and hedge-base flowering.
  - Invertebrates*.csv and InvertebratesWeight.csv: invertebrate counts by taxa and biomass, sampling method (beating, guttering), and weight data by taxa/groups.
  - InvertebrateEggSurveys.csv: counts of eggs for selected Lepidoptera species.
- Berry provisioning for wildlife
  - Berries.csv and BerriesQuadrats.csv: total berry counts and weights by species, with quadrat-level data to enable back-calculation of plot totals.
- Hedge structure and gaps
  - Gap.csv: gap metrics from hedge photos (area, counts, max/min axis, etc.) by height class and photo year.
  - Structure.csv: hedge "coverage" and gap data parsed from photos; hedge vs sheet classification.
- Hedge growth and regrowth after management
  - RegrowthAerial.csv, RegrowthBranch.csv, RegrowthLeaves.csv, RegrowthSeedlings.csv, RegrowthShoots.csv, RegrowthStool.csv, RegrowthTotals.csv, RegrowthWeight.csv: regrowth metrics for Crataegus monogyna and other species where applicable, including aerial regrowth, branch and shoot growth, stool counts, seedling establishment, and biomass (fresh/dry).
  - ShootCount.csv, ShootMeasurements.csv: counts and measurements of new shoots, including twig data and fresh/dry weights.
- Data recording and metadata
  - Recording of data: standardized sheets transcribed to Excel then loaded into Oracle database; QA checks described.
  - Height/width/gappiness metrics (BaselineParameters.csv; Dimensions.csv) to characterize hedge structure.
  - Treatment codes (TREATMENT) documented and mapped across data files (see below).

## Data collection, QA and quality
- Standard protocols used across all data collection; experienced field surveyors; expert checks of species lists.
- Data checked for anomalies during transcription and after import to Oracle.
- Visit date and visit year included; some historic data pre-date the main study period ( Experiment 1 data may include older records with only year available).
- Notable data issue: an autumn 2014 error at Marsh Gibbon led to cessation of MG monitoring from 2015 onward.
- Missing values reflect field collection gaps; extensive post-upload QA performed.

## Data structure, codes and access
- Data organized in multiple CSV files exported from an Oracle database (as of early 2020).
- Treatment coding: 1–25 codes across experiments; a reference mapping is provided (examples below):
  - Annual, standard, autumn (codes 1–3)
  - Biennial, standard, autumn (codes 2–3 placeholder in table, actual mapping present in dataset)
  - Triennial, incremental, autumn
  - Annual, incremental, autumn
  - Biennial, incremental, autumn
  - Triennial, incremental, winter
  - Control, uncut
  - Hedgelaying, uncut
  - Conservation hedgelaying, uncut
  - Wildlife hedging, uncut
  - Coppicing, uncut
  - Circular saw, uncut
  - And variations with “cut twice in 5 years” or “annual cut”
- Data files include: BaselineSpecies.csv, BaselineParameters.csv, Flowers.csv, Dimensions.csv, Berries.csv, BerriesQuadrats.csv, Pollinators.csv, PollinatorsFieldMarginFlowers.csv, PollinatorsFlowersCounts.csv, PollinatorsFlowersQuadrats.csv, PollinatorsHedgeFlowers.csv, Invertebrates.csv, InvertebratesWeight.csv, InvertebrateEggSurveys.csv, Gap.csv, Structure.csv, ShootCount.csv, ShootMeasurements.csv, RegrowthAerial.csv, RegrowthBranch.csv, RegrowthLeaves.csv, RegrowthSeedlings.csv, RegrowthShoots.csv, RegrowthStool.csv, RegrowthTotals.csv, RegrowthWeight.csv.

## Data quality and limitations
- Data standardized for time-series monitoring and cross-site comparisons; dated and site-coded for reproducibility.
- Some historic data may pre-date the core experimental period; exact dates may be missing (year-only stamps).
- One site experienced an inadvertent drastic disturbance (MG 2014) affecting subsequent treatments and monitoring.
- Results rely on assumption of uniform measurement protocols and consistent data capture across sites and years.

## Practical value for environment monitoring and policy performance
- Enables long-term monitoring of hedgerow biodiversity and habitat provisioning in response to management regimes promoted by ELS and HLS.
- Facilitates cross-site comparisons of effects of cutting timing, frequency, intensity, and rejuvenation methods on:
  - Flower abundance and plant species composition
  - Berry production and winter resources for wildlife
  - Pollinator visitation and pollination potential
  - Invertebrate diversity and biomass
  - Hedge structural complexity and gaps
  - Regrowth dynamics and biomass production after rejuvenation
- Supports evaluation of hedgerow management policies by linking management actions to ecological outcomes over time.
- Data standardization and the explicit treatment code mapping support integration into monitoring portals and dashboards, enabling consistent reporting and scrutiny.

## Additional notes
- The dataset has been produced with explicit quality control and documentation to support reuse in environmental monitoring contexts.
- Funding and management: Defra BD2114 project; UK Centre for Ecology & Hydrology (UKCEH). Acknowledgements and references accompany the data.

## References and acknowledgments
- References include Croxton et al. (2004), Maudsley et al. (2002), Sparks & Croxton (2007).
- Acknowledgements list individuals who assisted with data collection.
- Funding through Defra BD2114 and UKCEH.