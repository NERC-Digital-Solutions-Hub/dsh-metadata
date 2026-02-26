# Data set description

- A comprehensive dataset on functional traits and leaf/wood chemistry of woody plants in Andean Colombia, collected under the BioResilience project (post-conflict forest resilience). Contains six plant traits, leaf nutrients, leaf and wood measurements, and bark traits, plus plot-level metadata. Data collected 2019–2022 across 27 permanent monitoring plots (0.5 ha each) along an altitudinal gradient and a perturbation gradient.

- Purpose and scope
  - Investigates how expression of functional traits varies along perturbation and altitude, and how traits relate to ecosystem processes and forest resilience.
  - Supports correlation analyses, pattern discovery, and predictive insights for ecosystem functioning under disturbance.

- Experimental design and sampling regime
  - Permanent plots: 27 plots of 0.5 ha, distributed across lowlands (0–1200 m), midlands (1200–2200 m), and highlands (2200–3200 m).
  - Perturbation gradient: low, medium, high disturbance/recovery levels; three plots per perturbation level and altitude category, totaling 27 plots.
  - Sampling within plots: 825 individuals sampled in total.
  - Individual-level sampling: 20 individuals per plot in the lowlands and Encino Midlands; five individuals per plot in other locations; targeted sampling of the most representative or dominant species (covering 50–90% of dominance per plot).
  - Leaves and wood: from each selected tree, a branch (~1 m) collected; ten leaves per individual used for leaf trait and nutrient analyses; wood sampled from the same branch; bark thickness measured on multiple samples.

- Location details and biodiversity context
  - Lowlands: Quinchas (Puerto Boyacá, Boyacá) and nearby private properties, with warm temperatures (~24°C) and bimodal rainfall.
  - Midlands: Cachalú (Encino and Charala, Santander) and Pedro Palo/Tenasucá area in Cundinamarca, with cool temperatures and bimodal rainfall.
  - Highlands: Encenillo (Guasca) and Martos (Guatavita, Cundinamarca), with sub-Andean to high-Andean forest types and higher elevations.
  - Plot coordinates and locality information are provided (Table 1 in the dataset documentation).

- Traits, measurements, and nutrient analyses
  - Functional traits (six): Leaf Area, Specific Leaf Area (SLA), Leaf Dry Matter Content (LDMC), Leaf Thickness (Lth), Wood Density (WD), Bark Thickness (BT).
  - Leaf nutrients: Carbon (C), Nitrogen (N), Phosphorus (P), Calcium (Ca), Magnesium (Mg), Potassium (K); derived from elemental analyses and standard chemical methods.
  - Leaf morphometrics: leaf fresh mass, leaf dry mass, leaf area, leaf thickness; wood volume (fresh) and wood mass (dry) for WD calculation; bark thickness measurements.
  - Units and calculation details are provided (e.g., C/N/P/Ca/Mg/K in mg/g; SLA in mm2/mg; leaf area in mm2; leaf thickness in mm; wood density in g/cm3; volume_fresh in mm3; leaf masses in g).

- Data collection, processing, and quality assurance
  - Field equipment and laboratory methods align with Salgado-Negret et al. (2016) trait protocol.
  - Instrument calibration and verification performed prior to measurements; balances and micrometers calibrated.
  - Quality control included independent review of database structure, missing values, data typing, duplicates, and metadata consistency by personnel outside the traits team.
  - Data and metadata are prepared with attention to accuracy, completeness, and cross-dataset consistency.

- Data structure and files
  - Four CSV files:
    - traitnoreplicatesbr: 23 columns (plot metadata, location, trait values, and predicted/unit descriptors).
    - traitleafreplicatesbr: 11 columns (per-leaf replicates: leaf_area_1, leaf_fresh_mass_1, leaf_dry_mass_1, etc.).
    - traitleafpartreplicatesbr: 9 columns (leaf_thickness_1 and related fields across parts of the leaf).
    - traitbarkreplicatesbr: 9 columns (bark_thickness_1 and related fields).
  - The first file includes summary trait values per plot/individual (C, N, P, Ca, Mg, K, SLA, LDMC, leaf_thickness_ave, WD, BT, leaf_area_ave, leaf_mass_fresh_ave, leaf_dry_mass_ave, volume_fresh, wood_mass_dry).
  - The second file provides per-leaf replicates for leaf_area_1, leaf_fresh_mass_1, leaf_dry_mass_1 across up to ten leaves per individual.
  - The third file contains per-leaf-part replicates for leaf_thickness_1 (base, middle, top sections).
  - The fourth file contains bark_thickness_1 replicates (five measurements per individual).
  - Altitude categories, perturbation levels, locality, plot codes, Tag_No, species, and sample-part identifiers are consistently included.

- Practical considerations for analysts
  - Enables cross-site, cross-gradient analyses of trait variation and nutrient content, with robust metadata on plot location, altitude, and perturbation level.
  - Large, multi-replicate trait dataset suitable for correlational analyses, mixed-effects modeling across plots, and investigation of trait–environment relationships related to ecosystem processes and resilience.
  - Data gaps and site-specific sampling intensity (e.g., 20 individuals per plot in some sites vs. 5 in others) should be accounted for in modeling.

- References and provenance
  - Data generated under BioResilience project, with supporting ecological and geographical context provided in the accompanying references (Avella-M, CAR, Cuatrecasas, Holdridge, IDEAM, IGAC, Rojas et al., etc.).
  - Methods align with established plant trait protocols (Salgado-Negret et al., 2016).