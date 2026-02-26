# In-growth Core Experiments

## Study site
- Location: Heishiding Nature Reserve, Guangdong Province, China (111°53'E, 23°27'N; 150–927 m a.s.l.)
- Forest type: Subtropical evergreen broad-leaved forest covering about 4200 ha
- Climate: Tropic of Cancer region with subtropical moist monsoon climate
- Climate details: Mean annual temp 19.6 °C; Jan 10.6 °C to Jul 28.4 °C; ~1744 mm annual rainfall (mostly Apr–Sep)

## Experimental design: objectives and approach
- Primary aim: Test whether seedlings benefit from mycorrhizal hyphal connections to neighbouring plants using mesh-core exclusions
- Two independent experiments conducted:
  - Seedling survival using mesh-core exclusions
  - Seedling growth using a full reciprocal design across focal species and sites
- Focal species: Ten common tree species (five ectomycorrhizal ECM and five arbuscular mycorrhizal AM) including examples such as Castanopsis faberi, Castanopsis fissa, Cyclobalanopsis hui (ECM) and Schima superba, Cryptocarya concinna, Artocarpus styracifolius (AM)
- Seed collection: Autumn/Winter 2015 (growth) and 2017 (survival)
- Seedling preparation: Surface-sterilized seeds; germination in sterilized soil-sand mix; one-year cultivation before transplantation in growth experiment
- Transplant timeframe: Approximately one month after germination
- Core design: Mesh-walled cores (16 cm diameter, 30 cm deep) with six 8-cm windows; cores lined with either 35 µm (allows hyphae, excludes roots) or 0.5 µm (excludes both roots and hyphae) nylon mesh
- Core protection: Sides and bottom covered with 2 mm nylon mesh to protect against soil fauna
- Experimental sites: Each focal species assigned to a 30 × 30 m site with dominance criteria (DBH-weighted abundance > 30% among DBH ≥ 5 cm, no adult individuals of other study species nearby)

## Treatments and layout
- Seedling survival experiment:
  - 12 mesh cores per focal species per site
  - 8 seedlings per core
  - 768 seedlings in total (8 species × 2 mesh sizes × 6 core replicates × 8 seedlings per core)
- Seedling growth experiment:
  - Full reciprocal design across 6 sites, 6 focal species (3 ECM, 3 AM)
  - 2 mesh sizes (35 µm and 0.5 µm)
  - 12 cores per site, 6 seedlings per core
  - 432 seedlings in total
- Randomization and replacement:
  - Seedlings randomly transplanted into cores
  - Dead/poorly growing individuals replaced after one week
  - Growth: 9 months; Survival: 4 months

## Measurements and analyses
- Harvest and biomass:
  - After growth/survival periods, seeds harvested; seedlings detached, separated into shoot and root; dried at 60 °C for 72 hours
  - Biomass metrics: shoot biomass, root biomass, total seedling biomass
- Mycorrhizal colonization:
  - Root samples analyzed for AM colonization (aseptate hyphae, arbuscules, vesicles) and ECM colonization (mantle and Hartig net)
  - Grid-line intersection method used
- Soil and moisture monitoring:
  - HydraProbe sensors used to measure soil moisture and temperature
  - Measurements at three time points: early, mid, late stages of experiments
- Root colonization data:
  - Root samples examined for mycorrhizal colonization across cores, with counts for colonized vs non-colonized roots
  - Rate calculated as colonized/(colonized + non-colonized)

## Data files and key variables
- Tree_Seedling_Survival.csv
  - SpCode: focal species code
  - MycorrhizalType: ECM or AM
  - MeshSize: L (35 µm) or S (0.5 µm)
  - Core: core number (1–6 per species)
  - Survival: 1 (live) or 0 (dead)

- Tree_Seedling_Growth.csv
  - Site: six sites (full species names via Table 1)
  - SiteMycorrhizalType: ECM or AM
  - Core: core number per site (12 cores/site)
  - MeshSize / MeshSizeNum: mesh size (L/35 µm or S/0.5 µm)
  - Species: seedling species codes (six codes)
  - SpMycorrhizalType: ECM or AM
  - ID: seedling identifier within each core
  - HeightInitial: initial seedling height (cm)
  - Height: final seedling height at harvest (cm)
  - RootBiomass: root dry mass (g)
  - TotalBiomass: total dry mass (g)

- Tree_Seedling_Root_Colonization.csv
  - Site, SiteMycorrhizalType, Core, MeshSize, MeshSizeNum
  - Species, SpMycorrhizalType
  - SiteType: Con (conspecific-dominated site) or Hetero (heterospecific-dominated site)
  - ID: seedling individual ID
  - Yes: number of roots with mycorrhizal colonization
  - No: number of roots without colonization
  - Rate: colonization rate as Yes/(Yes + No)

- In-growth_Core_Enviroment.csv
  - Site, MycorrhizalType, Core, MeshSize, MeshSizeNum
  - Temp20170526 / Humidity20170526: soil temperature and moisture (2017-05-26)
  - Temp20170926 / Humidity20170926: soil temperature and moisture (2017-09-26)
  - Temp20180117 / Humidity20180117: soil temperature and moisture (2018-01-17)

## Notes and context
- Table 1 (referenced) lists the focal species with family, mycorrhizal type, species code, and which experiment(s) they were used in
- The study compares ECM vs AM contexts and two mesh sizes to assess reliance on mycorrhizal networks and potential effects on seedling performance
- Environmental measurements included to assess potential water-logging within cores due to restricted drainage
- Data support potential analyses:
  - Effect of mycorrhizal connectivity (via mesh access) on seedling survival and growth
  - Influence of mesh size on mycorrhizal colonization rates
  - Differences between ECM and AM seedlings in growth and colonization
  - Effects of site type (conspecific vs heterospecific dominance) on root colonization and seedling performance