# In-growth core experiments

## Study site and environmental context
- Field location: Heishiding Nature Reserve, Guangdong Province, south China (111°53'E, 23°27'N), 150–927 m above sea level.
- Habitat: 4200 ha subtropical evergreen broad-leaved forest.
- Climate: subtropical moist monsoon; mean annual temperature 19.6 °C; monthly range 10.6–28.4 °C; ~1744 mm annual precipitation with a pronounced dry season (Oct–Mar).
- Purpose: evaluate whether seedling performance is affected by external mycorrhizal networks via hyphal connections to neighboring plants using mesh-core experiments.

## Experimental design and focal species
- Two independent hyphal exclusion experiments conducted with mesh cores:
  - Seedling survival experiment (Mar–Aug 2018): 8 focal species.
  - Seedling growth experiment (Mar 2017–Jan 2018; harvest after 9 months in 2018): 6 focal species.
- Focal species: 10 species total (5 ectomycorrhizal ECM: Castanopsis faberi, Castanopsis fissa, Cyclobalanopsis hui, Lithocarpus haipinii, Engelhardia fenzelii; 5 arbuscular mycorrhizal AM: Schima superba, Cryptocarya concinna, Canarium album, Ormosia glaberrima, Artocarpus styracifolius).
- Mycorrhizal type categorization used: ECM vs AM.

## Mesh core apparatus and treatments
- Core dimensions and construction: 16 cm diameter, 30 cm deep PVC cores with six 8 cm windows; lined with 35 µm mesh and a 0.5 µm mesh to control root and hyphae access; outer sides/bottom covered with 2 mm mesh to prevent soil fauna damage.
- Mesh size treatments:
  - Large mesh (L): 35 µm, allowing hyphae but excluding neighboring roots.
  - Small mesh (S): 0.5 µm, excluding both roots and hyphae (only free-living microbes pass).
- Placement: 12 cores per site (3 × 2 m center area per focal species), depth 28 cm, soil mixed and backfilled; cores stood 4 weeks before transplantation.
- Core assignment: six cores per mesh size per focal site; cores randomly distributed with 30–50 cm spacing.

## Site selection, replication, and transplant design
- Site selection: for each focal species, one 30 × 30 m site with DBH-weighted relative abundance of the focal species >30% among trees (DBH ≥ 5 cm); no adult individuals of other study species within the site.
- Seedling transplantation:
  - Survival experiment: 768 seedlings total (8 species × 2 mesh sizes × 6 cores × 8 seedlings per core).
  - Growth experiment: 432 seedlings total (6 species × 6 sites × 2 mesh sizes × 6 seedlings per core) in a full reciprocal design.
- Handling after transplant: seedlings were checked one week post-transplant; dead or poorly growing seedlings replaced.

## Experimental procedures and timeline
- Seed collection and germination: fruits/seeds collected in autumn/winter 2015 (growth) and 2017 (survival); surface-sterilized; germinated in sterilized soil-sand mix; seedlings acclimated in culture for seedling-growth experiment prior to transplantation.
- Growth and harvesting:
  - Growth experiment: seedlings grown for 9 months before harvest.
  - Survival experiment: seedlings grown for 4 months before harvest.
- Harvesting procedure: seedlings separated into shoots and roots, dried at 60 °C for 72 hours to obtain shoot, root, and total biomass; 10 fine root fragments collected per seedling for mycorrhizal analysis.

## Measurements and laboratory analyses
- Mycorrhizal colonization assessment:
  - Root samples analyzed via grid-line intersection method.
  - AM colonization identified by aseptate hyphae, arbuscules, vesicles.
  - ECM colonization quantified by mantle presence and Hartig net.
- Biomass measurements: shoot and root dry weights; total biomass.
- Sample preservation: root and soil samples collected from each core for laboratory assays.

## Environmental monitoring within cores
- Soil moisture and temperature were measured in each core using HydraProbe sensors.
- Measurements taken at three time points: early, middle, and late stages of the experiments (beginning, middle, end).

## Data outputs and file schemas
- Tree_Seedling_Survival.csv
  - SpCode, MycorrhizalType (ECM vs AM), MeshSize (L vs S), Core (1–6), Survival (1 live, 0 dead).
- Tree_Seedling_Growth.csv
  - Site, SiteMycorrhizalType (ECM vs AM), Core (1–12), MeshSize (L vs S), MeshSizeNum (35 vs 0.5), Species, SpMycorrhizalType, ID, HeightInitial (cm), Height (cm), RootBiomass (g), TotalBiomass (g).
- Tree_Seedling_Root_Colonization.csv
  - Site, SiteMycorrhizalType, Core, MeshSize, MeshSizeNum, Species, SpMycorrhizalType, SiteType (Con vs Hetero), ID, Yes (count of roots with colonization), No (count without colonization), Rate (Yes/(Yes+No)).
- In-growth_Core_Enviroment.csv
  - Site, MycorrhizalType, Core, MeshSize, MeshSizeNum, Species, SpMycorrhizalType, SiteType, ID, Temp/Humidity measurements across three dates (2017-05-26, 2017-09-26, 2018-01-17).

## Data quality, stewardship, and reuse
- Procedures emphasize verification, quality assurance, data cleaning, and transformation of data prior to analysis.
- Outputs are presented in clear formats (survival, growth, colonization, environmental measurements) suitable for standardised monitoring and cross-study comparisons.
- Datasets are structured to be stored and uploaded to appropriate data portals; designed to be combined with additional environmental or ecological data for enhanced utility.

## Relevance to environmental monitoring and policy evaluation
- Provides standardized, traceable data on seedling performance and mycorrhizal interactions under controlled soil conditions.
- Enables assessment of the role of mycorrhizal networks in seedling survival and growth, contributing to understanding forest health and resilience.
- Offers a framework for integrating root-colonization and soil microclimate data into broader environmental monitoring programs.
- Highlights data accessibility and interoperability challenges and opportunities to increase the value of monitoring datasets through data sharing and integration.