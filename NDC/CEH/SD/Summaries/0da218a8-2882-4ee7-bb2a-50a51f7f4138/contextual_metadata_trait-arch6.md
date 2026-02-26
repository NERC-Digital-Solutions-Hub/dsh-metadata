# Data set description

- This dataset documents six functional traits for woody plants (Leaf Area, Specific Leaf Area SLA, Leaf Dry Matter Content LDMC, Leaf Thickness Lth, Wood Density WD, Bark Thickness BT) plus leaf nutrient concentrations (C, N, P, Ca, Mg, K), leaf fresh mass, leaf dry mass, and wood volume/mass used to calculate Wood Density.
- Additional context includes plot location, locality parameters, and sampling details (ten leaves per individual for leaf traits; multiple measurements per leaf section and per component for other traits) collected between 2019 and 2022.
- Study scope: 27 forest monitoring plots (0.5 ha each) along an altitudinal gradient (lowland, mid-elevation, highland) and a perturbation gradient (low, medium, high) in Andean Colombia.
- Purpose: investigate how functional trait expression and trait–ecosystem process relationships vary with perturbation and across environments; part of the BioResilience project funded by the UK Natural Environment Research Council (NE/R017980/1).

- Data collection context:
  - Permanent monitoring plots distributed across three landscapes:
    - Lowlands: Quinchas
    - Midlands: Encino and Pedro Palo
    - Highlands: Encenillo and Martos
  - Perturbation gradient categories reflect recovery time since last disturbance (low >30 years, medium 20–30 years, high <20 years).
  - Sampling strategy aimed at capturing dominant species and sun-exposed branches; across plots, 825 individuals were sampled (20 individuals per plot in lowlands/Encino, 5 per plot in other locations; sampling 50–90% of representative species).

- Data collection and trait derivation:
  - Nutrients: C, N, P, Ca, Mg, K measured with various analyses; results reported in mg/g.
  - Leaf traits: leaf area (LA) from scanned leaves; leaf thickness measured at three leaf sections; SLA and LDMC calculated from leaf mass and area; fresh and dry leaf masses recorded.
  - Wood traits: wood density derived from wood mass and volume (volume by water displacement; density in g/cm3); bark thickness measured with a micrometer.
  - Three data capture scales:
    - Trait set without replicates per individual (traitnoreplicatesbr)
    - Ten leaves per individual (traitleafreplicatesbr)
    - Leaf part-specific measurements (traitleafpartreplicatesbr)
    - Bark replicates per individual (traitbarkreplicatesbr)

- Data structure and files:
  - Four CSV files:
    - traitnoreplicatesbr: per-individual trait data (location, plot, canopy, taxonomy; C, N, P, Ca, Mg, K; SLA, LDMC, leaf_thickness_ave, WD, bark_thickness_ave, leaf_area_ave, leaf_mass_fresh_ave, leaf_dry_mass_ave, volume_fresh, wood_mass_dry)
    - traitleafreplicatesbr: ten leaves per individual (leaf_area_1, leaf_fresh_mass_1, leaf_dry_mass_1)
    - traitleafpartreplicatesbr: leaf thickness replicated across base/middle/top (leaf_thickness_1)
    - traitbarkreplicatesbr: bark thickness replicated (bark_thickness_1)
  - Key fields common across datasets: Altitude (lowlands 0–1200 m, midlands 1200–2200 m, highlands 2200–3200 m), Perturbation (low/medium/high), Locality (Quinchas, Pedro Palo, Encino, EncENillo, Martos), Plot_code, Tag_No, Family_Name, Species_Name, plus trait-specific measurements and units.

- Measurement methods and units:
  - Elements in mg/g for C, N, P, Ca, Mg, K; SLA in mm2/mg; LDMC in mg/g; leaf_thickness_ave in mm; leaf_area_ave in mm2; leaf_mass_fresh_ave and leaf_dry_mass_ave in g; volume_fresh in mm3; wood_mass_dry in g; wood_density in g/cm3; bark_thickness_ave in mm.
  - Leaf traits measured on multiple leaves per individual; wood density calculated from dry mass and fresh volume; leaf area via scanner; thickness measured with Mitutoyo micrometers; volumes determined by water displacement.

- Experimental design and timing:
  - Plots installed 2017–2020; trait measurements completed by 2022 (with different plots sampled at different times: Quinchas in 2019; Encino/Pedro Palo and Martos/Encenillo mostly around 2022).
  - Nutrients processed in 2022 at Universidad Nacional de Colombia.
  - Sampling intensity varied by location to capture community representation and dominance.

- Quality control and provenance:
  - Instrument calibration and verification prior to measurements; use of calibrated balances and micrometers.
  - Independent cross-checks of databases and metadata for accuracy, completeness, consistency, and removal of duplicates; metadata validation to ensure reliability and reproducibility.

- Geographic and ecological context:
  - Data collected across five Colombian locations on an altitudinal gradient and a forest perturbation gradient, enabling analyses of trait variation and ecosystem resilience under disturbance.
  - Contextual background references provided for site characterizations and ecosystem descriptions.

- Relevance and potential use:
  - Enables analyses of trait–environment interactions, perturbation effects on functional traits, and links between trait expression and ecosystem processes in Andean forests.
  - Supports data products such as dashboards, self-serve datasets, and policy-relevant summaries for forest resilience and management under disturbance.