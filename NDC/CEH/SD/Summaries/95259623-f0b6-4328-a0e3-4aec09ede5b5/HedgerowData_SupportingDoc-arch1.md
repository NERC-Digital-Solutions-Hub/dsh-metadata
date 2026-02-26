# Biodiversity and structural data from hedgerow management and rejuvenation experiments in England, 2005-2016

- Aim and scope
  - Long-running hedgerow experiments in England (2005–2016) to evaluate how hedgerow cutting regimes and rejuvenation strategies affect wildlife habitat quality, food resources, and restoration options.
  - Two linked aims: (1) assess effects of simple cutting regimes promoted by ELS/HLS on habitat quality and resources; (2) identify and test low-cost restoration options for large-scale hedgerows under ELS/HLS.
  - Experimental work designed to inform practical hedgerow management and restoration decisions.

- Experimental designs at a glance
  - Experiment 1 (2006–2014, Monks Wood, Cambridgeshire)
    - Randomised plots testing timing (autumn vs winter) and cutting frequency (annual, every 2 years, every 3 years) with two unmanaged controls.
    - Focus: hawthorn flower production, berry provision for overwintering wildlife, and hedgerow structure.
  - Experiment 2 (2010–2016, five field sites)
    - Randomised block design with full factorial 2 × 2 × 3: time of cutting (autumn vs late winter), intensity of cutting, and frequency (annual, every 2 years, every 3 years).
    - Focus: plant diversity/flowering in basal flora and associated biodiversity metrics.
  - Experiment 3 (2010 rejuvenation and subsequent management, five sites)
    - Rejuvenation treatments ( Midlands hedge-laying, Conservation hedge-laying, Wildlife hedging, Circular saw reshaping, Coppicing, plus Control) applied to 24 m plots in a split-plot design.
    - Post-rejuvenation management: annual, or every 2–3 years, or uncut; includes an additional annual treatment at one site.
    - Emphasises hedgerow structure, regrowth, and subsequent management effects.

- Field sites and hedgerow types
  - Sites include Marsh Gibbon (MG), Woburn (WO), Waddesdon (WB; blackthorn-dominated and mixed sites), Yarcombe (YC; mature mixed hedge), and others (WM).
  - Some sites contain hawthorn-dominated hedgerows; one MG site experienced an operational error in 2014 affecting treatments.

- Data collected (major data domains and files)
  - Vegetation composition
    - BaselineSpecies.csv, BaselineParameters.csv
    - Baseline measures of species presence, cover, depth in hedge plots; parameter metadata.
  - Flower production and plant structure
    - Flowers.csv, Dimensions.csv
    - Annual flower counts or cover for hawthorn, blackthorn, bramble; plot dimensions and height/width data.
  - Berry availability over winter
    - Berries.csv, BerriesQuadrats.csv
    - Total and subsample berry counts and weights by species; quadrat-level data.
  - Pollinator data
    - Pollinators.csv, PollinatorsFieldMarginFlowers.csv, PollinatorsFlowersCounts.csv, PollinatorsFlowersQuadrats.csv, PollinatorsHedgeFlowers.csv
    - Timed pollinator observations, pollinator taxa, flower associations, and margin-plot data.
  - Invertebrates
    - Invertebrates.csv, InvertebratesWeight.csv, InvertebrateEggSurveys.csv
    - Invertebrate counts by taxa, weight data, and egg surveys for select Lepidoptera.
  - Hedge structure and gaps
    - Gap.csv, Structure.csv
    - Image-based measures of hedge gaps, hedge percentage, and structural metrics across height classes and photo years.
  - Hedgerow regrowth and shoots
    - RegrowthAerial.csv, RegrowthBranch.csv, RegrowthLeaves.csv, RegrowthSeedlings.csv, RegrowthShoots.csv, RegrowthStool.csv, RegrowthTotals.csv, RegrowthWeight.csv
    - Aerial regrowth, branch regrowth, seedling development, stool regrowth, and biomass/weight metrics across regrowth years.
  - Shoots and regrowth (Experiment 2 focus)
    - ShootCount.csv, ShootMeasurements.csv
    - Counts and measurements of shoots by hedge position, species, twig data, and biomass indicators.
  - Data capture and provenance
    - Data recorded on standardized sheets, transcribed to Excel, imported into Oracle; consistent coding scheme across datasets.
    - Visit dates included; historic data may pre-date the main experiments (Experiment 1 data partly historic).

- Data structure and identifiers
  - Most datasets use composite keys including experiment, site, plot, aspect, visit date/year, and species or taxon name.
  - Treatment coding (1–25) aligns with a shared treatment table; multiple coding variants exist across files for compatibility.
  - Units and dimensions vary by dataset (e.g., height in metres or cm, area in cm2, weights in g).

- Key measurements and metrics
  - Biodiversity indicators: plant species composition, flowering coverage and counts, berry production and biomass, pollinator visitation rates, and invertebrate abundance/biomass.
  - Hedgerow structure: hedge density, gaps, height/width, and gappiness across hedge depth classes.
  - Rejuvenation and regrowth: aerial regrowth, branch/shoot regrowth, seedling recruitment, dead leaf cover, twig measurements, and regrowth biomass.

- Quality, scope, and limitations
  - Quality controls: standardized protocols, expert verification of species lists, anomaly checks during data entry and import.
  - Visit dates and year included; some historic data lack exact dates (only year) for Experiment 1.
  - Some site-specific issues (e.g., Marsh Gibbon 2014 cutting error) affected treatment application and monitoring continuity.
  - Data sets are designed for cross-site, cross-experiment integration to analyze treatment effects on biodiversity and hedgerow structure.

- Potential uses and analytical opportunities
  - Compare effects of cutting timing and frequency on flowering, berry yield, and hedgerow wildlife resources.
  - Assess how rejuvenation methods influence hedgerow regrowth, structure, and long-term biodiversity outcomes.
  - Explore relationships between hedge structure (gaps, density) and pollinator/invertebrate communities.
  - Examine cross-experiment consistency and scalability of management strategies under ELS/HLS frameworks.
  - Integrate vegetation, pollinator, invertebrate, and structural data to model ecosystem responses to hedgerow management.

- References, acknowledgments, and funding
  - Foundational references: Croxton et al. (2004), Maudsley et al. (2002), Sparks & Croxton (2007).
  - Acknowledgements of contributors; funding from Defra (BD2114) and management by UK Centre for Ecology & Hydrology (UKCEH).