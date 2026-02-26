# Data set description

- Purpose and scope
  - Provides information on functional traits of woody plants and leaf/wood nutrients to assess how trait expression relates to a perturbation gradient and altitude in Andean Colombia.
  - Part of the BioResilience project, aiming to understand forest resilience and ecosystem processes after the post-conflict period; supported by the UK Natural Environment Research Council (NE/R017980/1).

- Study design and location
  - Permanent monitoring plots: 27 plots of 0.5 hectares each.
  - Spatial gradient: altitudinal (lowlands 0–1200 m, midlands 1200–2200 m, highlands 2200–3200 m).
  - Anthropogenic perturbation gradient: low, medium, high perturbation with respective recovery times (low >30 years; medium 20–30 years; high <20 years).
  - Locations include Quinchas (lowlands), Encino and Pedro Palo (midlands), Encenillo and Martos (highlands) across several reserves and private properties.
  - Plot coordinates and details are organized in a table (Table 1) with plot code, perturbation level, altitude name/number, latitude, and longitude.

- Functional traits and nutrients
  - Six leaf/wood traits: Leaf Area (LA), Specific Leaf Area (SLA), Leaf Dry Matter Content (LDMC), Leaf Thickness (Lth), Wood Density (WD), Bark Thickness (BT).
  - Nutrients in leaves: Carbon (C), Nitrogen (N), Phosphorus (P), Calcium (Ca), Magnesium (Mg), Potassium (K).
  - Additional measurements: leaf fresh mass, leaf dry mass, fresh wood volume, and dry wood mass used to compute Wood Density.
  - Objective: determine how trait expression varies with perturbation and altitude and how traits relate to ecosystem processes.

- Sampling regime and data collected
  - Tree selection: in each plot, select trees tall enough to expose treetop, with species dominance prioritized by local context; for lowlands, at least 4 nearby trees; for other locations, focus on dominant species.
  - Sampling per plot: 20 random individuals in lowlands and Encino (midlands); 5 individuals per plot at other locations; total of 825 individuals sampled across all plots.
  - Leaves: ten leaves per individual collected, with leaves weighed fresh, scanned for area, thickness measured at base/middle/top, dried to calculate SLA and LDMC.
  - Wood and bark: one branch sampled per individual for wood density; five bark thickness measurements per individual.
  - Nutrient analysis: leaf tissue analyzed to determine C, N, P, Ca, Mg, K using specified methods (C by elemental analysis, N by Dumas, P by phosphomolybdo-vanadate colorimetry, Ca/Mg/K by calcination and atomic absorption).

- Data collection methods and instruments
  - Field equipment includes pole pruners, pruning shears, bags, masking tape, markers, plastic bottles, chlorine storage, scalpel, oven, silica gel, balances, thread and needle, glass volume containers, and scanners for leaf area.
  - Leaf area measured with a Canon scanner; leaf thickness measured with a Mitutoyo micrometer; wood density via Archimedes’ principle and volume via water displacement; bark thickness by micrometer.
  - Trait measurement protocol follows Salgado-Negret et al. (2016).

- Calibration, quality control, and metadata
  - Calibration: instruments pre-calibrated; accuracy verified prior to measurements.
  - Quality control: external review of databases and metadata for accuracy, completeness, consistency, missing values, duplicates, and data typing.
  - Metadata and data structure checks ensure reliable, usable datasets with defined units, valid ranges, and data provenance.

- Data structure and files
  - Four CSV data files:
    - traitnoreplicatesbr: trait data per plot/individual without leaf duplicates. Columns include Plot_code, Altitude, Perturbation, Locality, Tag_No, Family_Name, Species_Name, C, N, P, Ca, Mg, K, SLA, LDMC, leaf_thickness_ave, wood_density, bark_thickness_ave, leaf_area_ave, leaf_mass_fresh_ave, leaf_dry_mass_ave, volume_fresh, wood_mass_dry.
    - traitleafreplicatesbr: ten leaves per individual data. Columns include Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_part, Leaf_area_1, Leaf_fresh_mass_1, Leaf_dry_mass_1.
    - traitleafpartreplicatesbr: leaf-part measurements (base/middle/top) for ten leaves per individual. Columns include Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_Part, leaf_thickness_1.
    - traitbarkreplicatesbr: bark measurements for five samples per individual. Columns include Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_Part, Bark_thickness_1.
  - Data fields include explicit units, value ranges, and measurement names for each trait and sample part, with detailed descriptions of each column and replication structure.

- Data provenance and references
  - Data collected under the BioResilience framework with extensive regional ecological context.
  - References provided for methods, sites, and ecological context (e.g., Salgado-Negret 2016 protocol; Holdridge life zones; local Colombian reserve descriptions).

- Potential uses for monitoring and policy
  - Enables monitoring of forest functional trait variation across altitude and disturbance regimes.
  - Supports assessment of resilience drivers and ecosystem functioning in Andean forests.
  - Provides standardized metadata and quality controls aligning with data governance needs for environmental monitoring and decision-making.