Plant tissue 33 P (radio-isotope P) content from a 33 P tracer study to determine the uptake of P by seven different grassland plant species from three different P chemical forms in soil

- Purpose and scope
  - Investigates uptake of 33P from three P sources (orthophosphate, DNA, calcium phosphate) by seven grassland species.
  - Aims to determine whether co-occurring species show niche differentiation in P source use.
  - Data encompass uptake as KBq per gram of shoot and related measures.

- Setting and timeline
  - Location: Arthur Willis Environment Centre, University of Sheffield, UK.
  - Year: 2010 (with plant surveys conducted in 2011).

- Experimental design
  - Model plant communities grown in 1 L pots using limestone grassland natural soil.
  - Growth period: 30 weeks in a climate-controlled greenhouse (day 18°C, night 15°C).
  - Treatments: three 33P-labelled P sources injected at 10 points per pot to ensure P distribution.
  - Community composition: monocultures of seven species or a 7-species mix consisting of Agrostis capillaris, Festuca ovina, Carex flacca, Carex caryophyllea, Lotus corniculatus, Plantago lanceolata, Rumex acetosa.
  - Replication: seven replicates for each P-source × plant-community combination.
  - Soil and plant sampling: soil-origin plants and a survey of surrounding Wardlow limestone flora.

- Data collection and analysis
  - Harvest: aboveground biomass six days after 33P injection; samples separated by species in mixed communities.
  - Processing: biomass dried, ground, acid-digested, and chemically treated before scintillation counting.
  - Measurement: 33P content determined via liquid scintillation counting; results expressed as KBq per gram of shoot.

- Instrumentation and laboratory methods
  - Scintillation counting: Packard Tri-carb 3100TR.
  - Analytical workflow: harvest → drying and grinding → 350°C sulfuric acid digestion for 10 minutes → hydrogen peroxide treatment → dilution → scintillation counting.
  - Units: uptake expressed as MBq per pot and per gram dry weight; % uptake per pot and per gram.

- Data structure and variables
  - Four CSV files:
    - PuptakeFromCalciumphosphate
    - PuptakeFromDNA
    - PuptakeFromOrthophosphate
    - WardlowLimestoneSpeciesCover2011
  - PuptakeFrom* files (11 columns each): MixMono, Species, PotRep, LiveDead, DryWtg, DPMperPot, MBqperPot, PotBiomassg, TotalMBqPerPot, %UptakePerPot, %UptakePerG.
  - WardlowLimestoneSpeciesCover2011: Quadrat, SpecName, PercCov.
  - Coding and interpretation:
    - MixMono indicates monoculture (Mono) or mixed community (Mix).
    - Species codes correspond to seven target grassland species.
    - PotRep distinguishes pot-level replicates and cross-referencing in monocultures vs. mixed pots.
    - LiveDead, DryWtg, DPMperPot, MBqperPot, TotalMBqPerPot, %UptakePerPot, %UptakePerG provide detailed uptake metrics.
  - Data provenance: includes explicit documentation of variable names and measurement procedures.

- Metadata and survey data
  - Wardlow limestone plant survey (WardlowLimestoneSpeciesCover2011) provides quadrat-level species cover data (PercCov) to contextualize field community composition.
  - Quadrat-level identifications link species presence to sampling areas.

- Completeness, quality, and governance considerations
  - Dataset is complete except for a small number of missing data points due to sample contamination that were removed from analysis.
  - Transparent documentation of experimental methods, instrument calibration, and data structure supports reproducibility.
  - Metadata thoroughness aids data sharing and verification; potential barriers include public sharing of datasets and need for clear provenance and data management standards.

- Relevance for monitoring and policy evaluation
  - Demonstrates end-to-end data lifecycle: from experimental design and data collection to processing, analysis, and structured data outputs.
  - Highlights importance of metadata completeness, data provenance, and clear data governance to enable policy-relevant monitoring and cross-study comparability.
  - Provides a template for capturing uptake of environmental resources across species, useful for assessing niche differentiation and resource-use policies in ecosystems.