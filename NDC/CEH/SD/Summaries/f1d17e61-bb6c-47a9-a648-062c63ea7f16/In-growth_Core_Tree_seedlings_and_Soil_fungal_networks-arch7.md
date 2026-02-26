# Study site

## Location and climate
- Heishiding Nature Reserve, Guangdong Province, south China (111°53'E, 23°27'N), altitude 150–927 m above sea level.
- Subtropical moist monsoon climate; mean annual temperature 19.6 °C; monthly 10.6–28.4 °C.
- Annual precipitation ~1744 mm, concentrated Apr–Sep (79%); pronounced dry season Oct–Mar.

## Experimental design and objectives
- Purpose: test whether seedlings benefit from external mycorrhizal hyphal connections to neighbouring plants using mesh-core setups.
- Two independent in-growth core experiments:
  - Seedling survival: conducted Mar–Aug 2018; eight species transplanted; 768 seedlings total.
  - Seedling growth: conducted Mar 2017–Jan 2018; six species transplanted; 432 seedlings total.
- Focal tree species (Table 1): 5 ectomycorrhizal (ECM) and 5 arbuscular mycorrhizal (AM) species; seeds collected in 2015 (growth) and 2017 (survival).

## Mesh core design and treatment
- Cores: 16 cm diameter, 30 cm depth PVC tubes; six 8 cm windows per core (three at 4–12 cm depth, three at 16–24 cm).
- Inner liners: 35 µm mesh to allow mycorrhizal hyphae but exclude roots; 0.5 µm mesh to exclude both hyphae and roots.
- Outer protection: 2 mm nylon mesh to prevent soil fauna damage.
- In-growth depth: cores inserted to 28 cm depth; soil mixed and backfilled; cores stood 4 weeks before transplantation.

## Field setup and replication
- Sites: one 30×30 m plot per focal species; DBH-weighted relative abundance of focal species >30%; no adults of other study species within site.
- Core placement: 12 cores per site, randomly distributed within a 3×2 m area; 30–50 cm between cores; six cores per focal species.
- Transplantation: seedlings transplanted into cores 1 week after transfer; dead/poorly growing seedlings replaced.

## Species and mycorrhizal types
- ECM species: Castanopsis fabri, Castanopsis fissa, Cyclobalanopsis hui, Lithocarpus haipinii, Engelhardia fenzelii.
- AM species: Schima superba, Cryptocarya concinna, Canarium album, Ormosia glaberrima, Artocarpus styracifolius.

## Measurements and laboratory analyses
- Harvest and biomass: after growth (4 months for survival; 9 months for growth), seedlings harvested; shoot and root separated; dry weights (60 °C, 72 h) measured.
- Mycorrhizal colonization: assessed via grid-line intersection method; AM colonization (aseptate hyphae with arbuscules/vesicles); ECM colonization (mantle + Hartig net on root tips).
- Fine-root sampling: 10 fragments per seedling collected for colonization analyses.
- Soil moisture and temperature: HydraProbe sensors used to monitor soil conditions; measurements taken at beginning, middle, end of experiments.

## Data outputs and structure
- Seedling survival data (Tree_Seedling_Survival.csv)
  - SpCode, MycorrhizalType (ECM/AM), MeshSize (L/S), Core (1–6), Survival (1 live, 0 dead).
- Seedling growth data (Tree_Seedling_Growth.csv)
  - Site, SiteMycorrhizalType (ECM/AM), Core (1–12), MeshSize (L/S), MeshSizeNum (35/0.5), Species, SpMycorrhizalType, ID, HeightInitial, Height, RootBiomass, TotalBiomass.
- Root colonization data (Tree_Seedling_Root_Colonization.csv)
  - Site, SiteMycorrhizalType, Core, MeshSize, MeshSizeNum, Species, SpMycorrhizalType, SiteType (Con/Hetero), ID, Yes (count with colonization), No (without colonization), Rate (percentage Yes/(Yes+No)).
- Environmental data by core (In-growth_Core_Enviroment.csv)
  - Site, MycorrhizalType, Core, MeshSize, Temp/Humidity columns across dates (Temp20170526, Humidity20170526, Temp20170926, Humidity20170526, Temp20180117, Humidity20180117).

## Notes on scope and timeline
- Growth experiment: March 2017–January 2018 (nine months).
- Survival experiment: March–August 2018 (four months).
- Seed collection and preparation occurred in 2015 and 2017; seedlings used were one year old at time of transplant in the growth experiment.