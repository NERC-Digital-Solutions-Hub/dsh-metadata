# Yield of winter-sown oilseed rape plants in relation to insect pollination

- Aim
  - Collect yield data on winter sown oilseed rape in relation to insect pollination and ecosystem services provided by beneficial insects.
  - Data can be linked to the natural enemy and pollinator datasets from the Wessex BESS project.

- Study scope and context
  - 14 farms in southern England, collected over three years (2013–2015).
  - Data can be linked across datasets via FarmID, FieldID, Field/Transect/Point identifiers, and plant/raceme identifiers.

- Datasets included
  - NERCYieldFieldData.csv
    - Field-level yield data per farm/field/year; includes variety, hybrid/conventional status, seed treatments, and yield (t/ha).
  - NERCPlantData.csv
    - Plant-level data within fields/transects/points; includes treatment (open, bagged, wind), number of racemes, seeds per plant, seed weight.
  - NERCRacemePart.csv
    - Pod-level data by raceme part; includes raceme position and part, parasitism indicators, pod counts (split, ripe), total pods per part.
  - NERCSeedsPerPod.csv
    - Pod-level seed data; includes pod seeds per pod, weight per pod, parasitism, and related raceme/part identifiers.

- Data collection design and methods
  - Field setup
    - Three 58 m transects per field; transects selected perpendicular to field edge to capture hedges/margins where possible.
    - Sampling points along transects at 8 m, 20.5 m, 32 m, 44.5 m, and 58 m into the crop.
    - Field and plant identifiers: FarmID, FieldID, TransectID, PointID; plants tagged for treatment assessment.
  - Treatments and pollination assessment
    - 2013 and 2015: random assignment of plants to open pollination or pollination bag treatment.
    2014: open pollination only.
    - Pollination bag effectiveness tested via pollen slides; pollen transfer quantified under lab conditions.
  - Laboratory and phenotypic measurements
    - Harvest window between desiccation and harvest; despication using herbicide as standard practice.
    - Raceme and pod analyses: number of racemes, seeds per raceme, seed weight, pod parasitism indicators, pod split data.
    - Seed extraction and counting using seed counters; plant-level seed totals and weights recorded.
  - Sample sizes (illustrative)
    - 2013A: 58 plants analysed; 2013B: 50; 2014A: 180; 2015A: 154; 2015B: 156.
  - Data linkage
    - Data are designed to be linked across datasets through unique identifiers (FarmID, FieldID, TransectID, PointCode, PlantID, RacemeID, RacemePartID).

- Data quality assurance and ethics
  - Field and lab staff trained under a standardized protocol; data recorded on standardized forms.
  - Data entered into an MS Access database with duplicate checks; anomaly checks performed.
  - Some missing values due to field recorder error; metadata notes percent missing per file.
  - Ethics approval obtained from the CLES Penryn Research Ethics Committee (University of Exeter).

- Data structure and metadata notes
  - Linking keys across datasets
    - FarmID, FieldID, YearHarv in yield data; FieldID, TransectID, PointCode, PlantID in plant data; RacemeID and RacemePartIDs in raceme and seed datasets.
  - Variables and units
    - Yield_tHa: tonnes per hectare (field-level yield).
    - SeedTreatment and ST1/ST2/ST3: qualitative indicators of seed treatments; multiple values possible per sample.
    - Continuous measures include DistanceFromEdge (metres), SeedPerPlant (count), SeedWeight (grams), NoRacemes, NoSplitPods, TotalRipePods, WeightSeedPod.
  - Data quality notes
    - NERCYieldFieldData: No missing data reported.
    - NERCPlantData: NoRacemes has one missing data point (0.17%); other fields largely complete.
    - NERCRacemePart: NoSplitPods, NoExitHoles, TotalRipePods have minimal missing data (0.2–0.3%); other fields complete.
    - NERCSeedsPerPod: 23 pods missing seed weight (0.2%); other seed-related metrics largely complete.

- Governance and usage considerations for data stewards
  - Interoperability
    - Clear primary keys and cross-dataset linkage to enable integrated analyses of yield, plant-level traits, raceme/pod traits, and seed metrics.
  - provenance and traceability
    - Documented collection timeline (2013–2015), locations, field-level practices, and lab protocols; ethically approved processes.
  - Limitations and caveats
    - Field losses resulted in varying sample sizes by year/field; seed treatments vary by farmer preference, so missing ST cells do not imply data absence but non-application.
  - Intended reuse
    - Data can be linked with Wessex BESS natural enemy and pollinator datasets; suitable for studies on pollination services and ecosystem services in crop systems.

- Accessibility and context
  - Data originate from the NERC BESS program and are designed to support wider analyses of pollination effects on crop yield and ecosystem services.
  - Metadata provides explicit field-level identifiers, treatment details, and unit definitions to support discovery and reuse.