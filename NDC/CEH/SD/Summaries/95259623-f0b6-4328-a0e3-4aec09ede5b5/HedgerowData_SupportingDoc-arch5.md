# Biodiversity and structural data from hedgerow management and rejuvenation experiments in England, 2005-2016

- A set of long-running hedgerow experiments in England (2005–2016) collecting biodiversity and hedgerow structure data to assess management and restoration options under agri-environment schemes.
- Datasets span species composition, flowering and berry production, pollinators, invertebrates, and hedgerow structure and regrowth.

## Aims and scope

- Examine effects of hedgerow cutting management on wildlife habitat quality/quantity and food resources.
- Identify, develop, and test low-cost, practical hedgerow restoration options for large-scale implementation.
- Data cover three linked experiments with varying experimental designs and management treatments.

## Experimental designs

- Experiment 1 (2006–2014): Randomised plots testing cutting timing (autumn vs winter) and cutting frequency (annual, every two years, every three years) plus unmanaged controls on four Monks Wood hedgerows.
- Experiment 2 (2010–2016): Randomised block design to study timing (early autumn vs late winter), intensity (standard cut vs incrementally raising cutter bar), and frequency (annual, every two years, every three years) across five sites with 15–20 m hedge sections in full factorial (2 × 2 × 3).
- Experiment 3 (2010–2013 rejuvenation and post-treatment management): 12 replicates of each rejuvenation technique across five sites in a split-plot design, assessing six rejuvenation methods (Midlands hedge-laying, Conservation hedge-laying, Wildlife hedging, Circular saw reshaping, Coppicing, Control) followed by varied post-rejuvenation management (annual, every 2–3 years, uncut). Rejuvenation applied in November 2010; management 2011–2013.

## Data collected and key variables

- Vegetation composition and baseline parameters (BaselineSpecies.csv; BaselineParameters.csv) including species presence, cover, depth, hedge height/width, gaps, historic management, and adjacent land features.
- Flower production and hedge dimensions (Flowers.csv; Dimensions.csv) with per-plot counts/cover, quadrat data, and hedge dimensions.
- Berry availability (Berries.csv; BerriesQuadrats.csv) including total and subsample counts, weights, and quadrat-level data.
- Pollinators and flowering plant context (Pollinators.csv; PollinatorsFieldMarginFlowers.csv; PollinatorsFlowersCounts.csv; PollinatorsFlowersQuadrats.csv; PollinatorsHedgeFlowers.csv) with visitation rates, pollinator taxa, temperature/cloud/wind, and field-margin flowering context.
- Invertebrates (Invertebrates.csv; InvertebratesWeight.csv; InvertebrateEggSurveys.csv) detailing counts, taxa, sampling methods (beating, guttering), and egg surveys for select Lepidoptera.
- Hedge structure and gaps (Gap.csv; Structure.csv) including gap area, hedge percentage, and image-based structure metrics.
- Hedge regrowth (RegrowthAerial.csv; RegrowthBranch.csv; RegrowthLeaves.csv; RegrowthSeedlings.csv; RegrowthShoots.csv; RegrowthStool.csv; RegrowthTotals.csv; RegrowthWeight.csv) detailing regrowth by year, plant part, stool/branch metrics, twig data, shoot length/diameter, and biomass.
- Data capture and identifiers: standardized field sheets, transcribed to Excel, then loaded into an Oracle database; consistent, experiment-wide identifiers for cross-dataset linkage.

## Data structure, provenance, and quality

- Data were collected using standard protocols by experienced field surveyors; species lists expert-checked; checks for anomalous values during entry and after import.
- Visit dates and visit years included; historic pre-date data present for context (experiment 1).
- Documentation of data collection and coding: extensive metadata on treatment codes, experimental design, and site details; some codes differ from original setups for interoperability.
- Notable data issues: one 2014 MG site cutting error halted treatment application at that site; winter cutting not applied at WB site due to site constraints; occasional missing values attributed to survey omissions.
- Files are self-describing with explicit field mappings and data definitions; data exported from Oracle DB between Jan–Feb 2020.

## Regions, sites, and temporal coverage

- England-based hedgerow field sites; five main field sites with coordinates provided for reproducibility and spatial analysis.
- Time span across experiments: 2005–2016 for management trials; rejuvenation applied in 2010 with follow-up through 2013; data exports in 2020.

## Data governance and reuse considerations

- Data governed by Defra Defra BD2114 program (Effects of hedgerow management and restoration on biodiversity), managed by UKCEH.
- File set enables cross-experiment integration: linking vegetation, flowering/berries, pollinators, invertebrates, and structural metrics to management treatments.
- Units and measurement details vary by dataset (e.g., hedge height in metres vs centimetres; depth classes for plant occupancy), requiring careful harmonization for meta-analysis.
- Comprehensive documentation supports data discovery, traceability, and reproducibility for researchers, data stewards, and policy evaluators.

## Practical takeaways for Data Stewards

- The collection provides a robust, multi-taxa, multi-dataset resource aligned to hedgerow management experiments, suitable for governance, metadata curation, and cross-study analyses.
- Ensure consistent cross-walking of treatment codes, site identifiers, and temporal markers when integrating datasets.
- Maintain provenance trails from field sheets to Excel to Oracle, including QC steps and any code mappings (e.g., treatment descriptions 1–25).
- Be mindful of unit differences and historical data peculiarities when enabling downstream reuse and comparisons.
- Document site-specific anomalies (e.g., MG 2014 cut error; WB winter cutting absence) in data governance records to aid correct interpretation.