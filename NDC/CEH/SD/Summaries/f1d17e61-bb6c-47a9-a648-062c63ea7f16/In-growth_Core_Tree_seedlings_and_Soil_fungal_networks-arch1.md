# Study site

- Location and climate
  - Heishiding Nature Reserve, Guangdong Province, south China (111°53′E, 23°27′N)
  - 4200 ha subtropical evergreen broad-leaved forest
  - Subtropical moist monsoon climate; mean annual temp 19.6 °C; 10.6–28.4 °C monthly range
  - Annual rainfall ~1744 mm (79% Apr–Sep); pronounced dry season Oct–Mar

- Experimental objective
  - Test whether seedlings benefit from mycorrhizal hyphal connections to neighboring plants via external mycorrhizal networks
  - Use mesh-core hyphal exclusion to compare seedling survival and growth with and without access to neighboring mycelium

- Site and focal species selection
  - 10 focal tree species (5 ECM, 5 AM)
    - ECM: Castanopsis fabri, Castanopsis fissa, Cyclobalanopsis hui, Lithocarpus haipinii, Engelhardia fenzelii
    - AM: Schima superba, Cryptocarya concinna, Canarium album, Ormosia glaberrima, Artocarpus styracifolius
  - Seeds collected in autumn–winter of 2015 (growth) and 2017 (survival)
  - Sites selected per focal species: 30 × 30 m plots dominated by the focal species (DBH-weighted abundance >30% among DBH ≥ 5 cm); no adults of other study species within each site

In-growth core experiments

- Mesh-core design and purpose
  - Core details: 16 cm diameter × 30 cm deep; 28 cm soil depth allocation; six 8 cm windows distributed along the side
  - Mesh treatments:
    - Large mesh (L): 35 µm to allow mycorrhizal hyphae but exclude roots
    - Small mesh (S): 0.5 µm to exclude both roots and hyphae (only free-living microorganisms pass)
  - Outer protection: 2 mm nylon mesh around sides/bottom to prevent soil fauna damage
  - Core deployment: 12 cores per focal species, randomly placed within a 3 × 2 m area; cores transplanted after 4 weeks of soil disturbance recovery
  - Depth: cores inserted to 28 cm

- Seedling preparation and transplantation
  - Seedlings: germinated from collected seeds; grown to transplant stage
  - Transplantation into cores: random selection of healthy seedlings
  - Post-transplant replacement: seedlings dead or poorly growing were replaced within 1 week
  - Experimental durations:
    - Survival experiment: 4 months growth in cores, then harvest
    - Growth experiment: 9 months growth in cores, then harvest

Seedling survival experiment

- Experimental design
  - 8 focal species, 12 cores per species per mesh size, 8 seedlings per core
  - Total: 768 seedlings (8 species × 2 mesh sizes × 6 cores × 8 seedlings per core)
  - Goal: evaluate survival under different hyphal access conditions

Seedling growth experiment

- Experimental design
  - Reciprocal full-factor design across six focal species (ECM and AM)
  - Sites: six local dominant sites (one per focal species)
  - Core/seedling arrangement: 12 cores per site; six seedlings per core
  - Treatments:
    - Species × site composition: six focal species × six corresponding Dominated-by-all-site types
    - Mesh sizes: two levels (L = 35 µm, S = 0.5 µm)
  - Seedlings: one-year-old at transplant; 432 seedlings total

Morphology, biomass, and mycorrhizal assessment

- Harvest and measurements
  - Harvest after 4 months (survival) or 9 months (growth)
  - Seedlings washed; separated into shoot and root; dry weights after 60 °C for 72 h
  - Biometrics: Height Initial (cm), Height (cm), Root Biomass (g), Total Biomass (g)

- Mycorrhizal colonization
  - Fine root samples: 10 fragments per seedling (1 cm each)
  - Analysis: grid-line intersection method
  - Mycorrhizal definitions:
    - AM: aseptate hyphae with arbuscules and vesicles
    - ECM: percentage of colonized root tips with mantle and Hartig net

- Soil microclimate within cores
  - Soil moisture content and temperature measured with HydraProbe sensors
  - Measurements at three phases: early, middle, and late in the experiments

Data files and structure

- Tree_Seedling_Survival.csv
  - Columns:
    - SpCode: focal species code (Table 1)
    - MycorrhizalType: ECM or AM
    - MeshSize: L (35 µm) or S (0.5 µm)
    - Core: core number (1–6 per focal species)
    - Survival: 1 = live, 0 = dead

- Tree_Seedling_Growth.csv
  - Columns:
    - Site: site label (six levels; local dominant site per focal species)
    - SiteMycorrhizalType: ECM or AM
    - Core: ingrowth core number (12 cores per site; codes 1–18 non-contiguous)
    - MeshSize: L or S
    - MeshSizeNum: numeric codes 35 or 0.5
    - Species: seedling species codes (Table 1)
    - SpMycorrhizalType: ECM or AM
    - ID: seedling identifier within each core
    - HeightInitial: seedling height at transplant (cm)
    - Height: seedling height at harvest (cm)
    - RootBiomass: seedling root dry mass (g)
    - TotalBiomass: seedling total dry mass (g)

- Tree_Seedling_Root_Colonization.csv
  - Columns:
    - Site: site label
    - SiteMycorrhizalType: ECM or AM
    - Core: core number
    - MeshSize: L or S
    - MeshSizeNum: 35 or 0.5
    - Species: seedling species codes
    - SpMycorrhizalType: ECM or AM
    - SiteType: Con (conspecific-dominated) or Hetero (heterospecific-dominated)
    - ID: seedling individual identifier
    - Yes: number of roots with mycorrhizal colonization detected
    - No: number of roots without colonization
    - Rate: colonization rate (Yes / (Yes + No))

- In-growth_Core_Enviroment.csv
  - Columns:
    - Site: site label
    - MycorrhizalType: ECM or AM
    - Core: core number
    - MeshSize: L or S
    - Temp20170526: soil temperature (°C) on 2017-05-26
    - Humidity20170526: soil moisture (%) on 2017-05-26
    - Temp20170926: soil temperature (°C) on 2017-09-26
    - Humidity20170526: soil moisture (%) on 2017-05-26
    - Temp20180117: soil temperature (°C) on 2018-01-17
    - Humidity20180117: soil moisture (%) on 2018-01-17

- Table 1 (referenced)
  - Provides full species names for codes (Cf aberi, Cf isa, etc.) and their mycorrhizal type (ECM or AM)
  - Used to map codes to species in the datasets

Key analytical opportunities

- Compare seedling survival and growth across:
  - Mycorrhizal type (ECM vs AM)
  - Hyphal access (L vs S mesh sizes)
  - Site type (conspecific-dominated vs heterospecific site)
  - Species identity and whether ECM or AM responds differently to mesh treatments
- Assess mycorrhizal colonization rates by species, mesh size, and site context
- Link environmental microclimate data (temperature, humidity) within cores to seedling performance and colonization
- Integrate datasets to examine how external mycelial networks influence biomass accumulation, height growth, and survival probabilities across multiple combinations of species, site, and mesh treatment

Note: Data are organized to enable cross-dactor analyses, with explicit codes to map species and treatments across four CSV files and associated environment measurements.