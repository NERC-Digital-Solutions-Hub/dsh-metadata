# Yield of winter-sown oilseed rape plants in relation to insect pollination

## Overview
- A multi-year dataset (2013–2015) from the Wessex BESS project examining winter-sown oilseed rape yield in relation to insect pollination and ecosystem services from beneficial insects.
- Data can be linked with natural enemy and pollinator datasets from the same project.

## Study design and data collection
- Location and duration
  - 14 farms in southern England; three-year study (2013–2015).
- Field and sampling structure
  - Fields segmented into transects and sampling points (8 m, 20.5 m, 32 m, 44.5 m, 58 m from field edge).
  - Transects chosen to include hedges and margins where possible.
- Treatments and experimental design
  - Pollination treatments: open-pollinated vs. bagged (pollination exclusion) plants.
  - 2013 and 2015: two plants per sampling point assigned to open or bagged treatments.
  - 2014: open-pollinated treatment only.
  - Pollination efficacy tested via pollen transfer slides exposed in-field and later counted in the lab.
- Measurements and timelines
  - Yield data collected at harvest; plants tagged during flowering to monitor pollination treatment effects.
  - Flowering and post-flowering stages tracked; desiccation and harvest windows observed.
- Crop and management
  - Winter sown oilseed rape (Brassica napus L.); farmers’ seed varieties and treatments recorded.

## Data files and structure
- Four CSV files with linked keys:
  - NERCYieldFieldData.csv
    - Field-level yield data by FarmID, FieldID, YearHarv, VarietyCode, HybridConventional, Yield_tHa.
    - Includes SeedTreatment and up to three seed treatment columns (ST1–ST3).
  - NERCPlantData.csv
    - Plant-level observations: FieldID, TransectID, PointCode, PlantID, Treatment (A=open, B=bagged, wind), NoRacemes, SeedPerPlant, SeedWeight.
    - Notes minimal missing data (NoRacemes nearly complete).
  - NERCRacemePart.csv
    - Raceme-level parts: PlantID, RacemeID, RacemePosition (B/M/T), RacemePart (B/M/T), NoSplitPods, NoPodsExitHoles, TotalRipePods, TotalPodsPerPart.
    - Some minor missing data in specific fields (e.g., NoSplitPods, NoExitHoles).
  - NERCSeedsPerPod.csv
    - Pod-level seed data: RacemeID, RacemePartID, Parasitised, NoSeed, WeightSeedPod.
    - Small amounts of missing data (e.g., WeightSeedPod, NoSeed).
- Linking and metadata
  - Core linking fields flagged with * for cross-dataset joins (e.g., FarmID, FieldID, PlantID, RacemeID).
  - Metadata includes variable descriptions, units, and notes on treatment prevalence.

## Key metrics and outcomes
- Yield metrics
  - Yield_tHa per field/farm and year.
- Plant and seed metrics
  - Number of racemes per plant, seeds per plant, seed weight per plant.
- Pod and raceme metrics
  - Pod-level metrics: ripe pods, split pods, pods with evidence of parasitism, and total pods per raceme part.
  - Pod and seed weights aggregated to plant and field levels.
- Pollination verification
  - Effectiveness of pollination bags quantified via pollen grain counts from lab slides.

## Data quality, completeness, and limitations
- Quality assurances
  - Field and lab personnel trained; standardized protocols; data captured in MS Access to minimize duplicates; anomaly checks performed.
- Missing data
  - Some missing values due to field losses; overall missing rates documented in file metadata.
  - ST1–ST3 (seed treatments) may be blank where not used rather than missing.
- Sample sizes (per year)
  - 2013A: 58 analysed plants
  - 2013B: 50 analysed plants
  - 2014A: 180 analysed plants
  - 2015A: 154 analysed plants
  - 2015B: 156 analysed plants
- General caveats
  - Patchy data across farms and fields; variability in seed treatments chosen by farmers; some data strata only represented in certain years.

## Ethics and provenance
- Ethical approval obtained from CLES Penryn Research Ethics Committee (University of Exeter).

## Data usage and integration with other datasets
- The dataset can be analyzed to assess the impact of insect pollination on yield and seed production, both at plant and field scales.
- Possible integration with related Wessex BESS datasets on pollinators and natural enemies to explore ecosystem service relationships.
- Linking keys facilitate combining yield data with insect pollination, field management, and location-level metadata.

## Practical guidance for data support and product generation
- Suggested analyses and products
  - Compare yield_tHa across open vs bagged treatments, controlling for year, field, and farm effects.
  - Explore relationships between pollination treatment and seed metrics (SeedPerPlant, SeedWeight) and raceme-level outcomes (TotalRipePods, NoSplitPods).
  - Build dashboards showing yield by farm and year, stratified by pollination treatment and seed treatments.
  - Create data dictionaries and lineage diagrams to accompany the four files and their linking keys.
- Data preparation considerations
  - Join NERCYieldFieldData with NERCPlantData on FieldID and PlantID; extend to NERCRacemePart via RacemeID; link to NERCSeedsPerPod via RacemeID and RacemePartID.
  - Handle blanks in seed treatment fields as “not used” rather than missing data.
  - Account for year-specific treatment structures (2013/2015 vs 2014).
- Quality checks to run
  - Verify consistency of PlantID, RacemeID, and FieldID across files.
  - Check for outliers in yield, seed weight, and pod counts; consult metadata for expected ranges.
  - Assess missing data patterns to determine imputation or exclusion criteria for analyses.