# Study site

- Location: Heishiding Nature Reserve, Guangdong Province, south China; 4200 ha subtropical evergreen broad-leaved forest.
- Coordinates: 111°53'E, 23°27'N; elevation 150–927 m a.s.l.
- Climate: Tropic/subtropical moist monsoon; mean annual temperature 19.6 °C; 10.6 °C (Jan) to 28.4 °C (Jul); ~1744 mm annual precipitation (mainly Apr–Sep); pronounced dry season Oct–Mar.

## Experimental approach

- Objective: Test whether external mycorrhizal networks influence seedling survival and growth via two independent hyphal exclusion experiments using mesh cores.
- Core design: Mesh cores (16 cm diameter × 30 cm deep) with six side windows; covered with 35 µm or 0.5 µm nylon mesh to create a gradient that permits/blocks mycorrhizal hyphae and roots.
- Recovery and setup: Cores inserted at 28 cm depth in selected sites, soil mixed and backfilled, cores stood for 4 weeks before seedling transplantation.
- Replication and timing:
  - Survival experiment: 12 cores per focal species per site (6 replicates per mesh size) with 8 seedlings per core; total 768 seedlings across 8 species.
  - Growth experiment: Full reciprocal design across 6 focal species and 6 sites; 432 seedlings total.
- Measurements and duration:
  - Growth: 9 months
  - Survival: 4 months
  - Harvest: shoot and root biomass; dry weights after 60 °C, 72 h
  - Root colonization: mycorrhizal status via grid-line intersection method; AM (aseptate hyphae, arbuscules, vesicles) and ECM (mantle + Hartig net) indicators
  - Environmental: soil moisture and temperature via HydraProbe sensors at three time points (beginning, middle, end)

## Focal species and mycorrhizal types

- ECM (five species): Castanopsis fabri, Castanopsis fissa, Cyclobalanopsis hui, Lithocarpus haipinii, Engelhardia fenzelii
- AM (five species): Schima superba, Cryptocarya concinna, Canarium album, Ormosia glaberrima, Artocarpus styracifolius
- Codes used in data: Cfab, Cfis, Chui, Lhai, Efen (ECM) and Ssup, Ccon, Calb, Ogla, Asty (AM)

## Data collection, structure, and variables

- Survival data (Tree_Seedling_Survival.csv):
  - SpCode, MycorrhizalType (ECM/AM), MeshSize (L or S), Core (1–6), Survival (1 live, 0 dead)
- Growth data (Tree_Seedling_Growth.csv):
  - Site, SiteMycorrhizalType (ECM/AM), Core, MeshSize, MeshSizeNum (35 or 0.5), Species, SpMycorrhizalType (ECM/AM), ID
  - InitialHeight, Height, RootBiomass, TotalBiomass
- Root colonization data (Tree_Seedling_Root_Colonization.csv):
  - Site, SiteMycorrhizalType, Core, MeshSize, MeshSizeNum, Species, SpMycorrhizalType, SiteType (Con vs Hetero)
  - ID, Yes (roots with colonization), No (roots without), Rate (Yes/(Yes+No))
- Environmental core data (In-growth_Core_Enviroment.csv):
  - Site, MycorrhizalType, Core, MeshSize, Temp20170526, Humidity20170526
  - Temp20170926, Humidity20170526, Temp20180117, Humidity20180117
- Site-level and experimental metadata, including the relationship between site dominance (conspecific vs heterospecific) and core placement

## Data governance, quality, and considerations

- Metadata clarity: clear codes for sites, cores, and mesh treatments; ensure consistent naming across CSVs (Site, Core, MeshSize, MeshSizeNum).
- Data integrity: continuous tracking of seedling IDs (ID) across growth and colonization datasets for longitudinal analyses.
- Measurement consistency: standardized protocols for biomass, height, root sampling, and mycorrhizal assessment (grid-line intersection method) to enable cross-study comparability.
- Data granularity and access: documentation of the two mesh treatments (35 µm vs 0.5 µm) is critical, as it determines whether roots or hyphae can access treatments; potential water-logging considerations noted via soil moisture measurements.
- Data quality challenges: potential discontinuities in Core numbering (Cores coded 1–6 within each site/species; Growth data uses a broader 1–18 coding across sites) and occasional label inconsistencies (e.g., repeated humidity columns) should be harmonized in a data dictionary.

## Practical takeaways for data strategy

- Establish a central data dictionary capturing variable names, units, allowed values, and provenance for all five CSV files.
- Implement a consistent ontology for SpCode and Site identifiers to enable joins across Survival, Growth, Root Colonization, and Enviroment datasets.
- Align data collection schedules and metadata to support user needs for ecological network effects, cross-species comparisons, and potential policy- or management-oriented insights.
- Ensure data discoverability and reuse by preserving core IDs, mesh treatment distinctions, and mycorrhizal type classifications across datasets.