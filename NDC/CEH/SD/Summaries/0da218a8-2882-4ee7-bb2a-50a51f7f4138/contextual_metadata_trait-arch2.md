# Data set description

- Purpose and scope:
  - A dataset describing six functional traits of woody plants (Leaf Area, Specific Leaf Area SLA, Leaf Dry Matter Content LDMC, Leaf Thickness Lth, Wood Density WD, Bark Thickness BT) plus concentrations of C, N, P, Ca, Mg, K in leaves, plus leaf and wood measurements to enable Wood Density calculations.
  - Includes plot locations and locality parameters to assess trait variation across environmental gradients and perturbation levels within the BioResilience project in Colombia.
  - Aimed at understanding how trait expression differs along an altitudinal gradient and perturbation gradient and how traits relate to ecosystem processes and forest resilience.

- Study design and sampling framework:
  - 27 permanent forest monitoring plots (0.5 ha each) distributed across an altitudinal gradient: lowlands (0–1200 m), midlands (1200–2200 m), highlands (2200–3200 m).
  - Perturbation gradient categories: low (>30 years since last perturbation), medium (20–30 years), high (<20 years).
  - Locations include Quinchas (lowlands), Encino and Pedro Palo (midlands), Encenillo and Martos (highlands).
  - In each plot, 20 or 5 individuals were sampled depending on location, targeting the most representative or dominant species; total sampling across all plots: 825 individuals from 27 plots.
  - Leaves sampled: 10 leaves per individual; measurements include leaf area, fresh mass, dry mass, and leaf thickness at base, middle, and top.
  - Wood sampling: one branch per individual for wood density (volume via water displacement; mass after oven-drying); five bark thickness measures per individual.
  - Data collection occurred 2019–2022, with trait measurements completed by 2022; nutrient data calculated in batches in 2022.

- Traits, measurements, and units:
  - Traits: Leaf Area (mm2), SLA (mm2/mg), LDMC (mg/g), Leaf Thickness (mm), Wood Density (g/cm3), Bark Thickness (mm); Nutrients: C, N, P, Ca, Mg, K (mg/g).
  - Leaves: ten leaves per individual measured for fresh mass, area, thickness, and dry mass; SLA and LDMC derived from leaf area and masses.
  - Wood: volume (mm3) for density calculations; dry mass (g) for density computations.
  - Bark: thickness (mm) measured with micrometer (five measurements per individual).
  - Data units and value ranges for each variable are provided in the dataset metadata (e.g., C: 364–1200 mg/g; SLA: 0.932–82.017 mm2/mg; leaf_area_ave: 35.4–335,673.4 mm2, etc.).

- Data files and structure:
  - Four CSV files:
    - traitnoreplicatesbr: plot-level and per-tree trait/nutrient values (23 columns: e.g., Plot_code, Altitude, Perturbation, Locality, Tag_No, Family_Name, Species_Name, C, N, P, Ca, Mg, K, SLA, LDMC, leaf_thickness_ave, wood_density, bark_thickness_ave, leaf_area_ave, leaf_mass_fresh_ave, leaf_dry_mass_ave, volume_fresh, wood_mass_dry).
    - traitleafreplicatesbr: ten leaves per individual replicates (11 columns: Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_part, Leaf_area_1, Leaf_fresh_mass_1, Leaf_dry_mass_1).
    - traitleafpartreplicatesbr: ten leaves per individual measured in three leaf sections (9 columns: Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_Part, leaf_thickness_1).
    - traitbarkreplicatesbr: five bark thickness measurements per individual (9 columns: Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_Part, Bark_thickness_1).
  - Data columns include consistent metadata: Plot_code, Altitude category, Perturbation category, Locality, Tag_No, Family_Name, Species_Name, along with measured variables and units.

- Methods and quality control:
  - Field and lab methods aligned with Salgado-Negret et al. (2016) for functional trait measurement.
  - Nutrient concentrations derived using standard methods (C by elemental analysis; N by Dumas; P by phosphomolybdo-vanadate; Ca/Mg/K by calcination and atomic absorption; Na via similar procedures).
  - Leaves measured for area via scanning; thickness measured with Mitutoyo micrometer; SLA and LDMC calculated from fresh/dry masses; wood density calculated as dry wood mass divided by fresh wood volume (volume via Archimedes principle); leaf and wood volumes measured using appropriate techniques.
  - Instrument calibration and accuracy checks prior to measurements; external quality control reviews for database structure, missing data, data typing, and metadata validation.

- Context and references:
  - Ties to BioResilience project examining forest resilience after Colombia’s post-conflict period.
  - Provides a dataset enabling cross-site comparisons of trait expression under different environmental and perturbation conditions.
  - References include ecological and methodological sources such as Holdridge, Cuatrecasas, Salgado-Negret et al. (2016), and supporting regional ecological studies.

- Key applications for environmental monitoring:
  - Standardized, auditable trait and nutrient datasets across gradients for monitoring ecosystem health and resilience.
  - Enables scrutiny of how perturbation and altitude influence plant functional traits and associated ecosystem processes.
  - Supports data sharing and integration with monitoring portals through clear data structure and quality controls.