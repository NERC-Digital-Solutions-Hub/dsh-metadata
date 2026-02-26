# Study site

- Purpose and scope
  - Field study to test whether ectomycorrhizal (ECM) and arbuscular mycorrhizal (AM) networks influence seedling survival and growth through external mycorrhizal hyphal connections.
  - Utilizes mesh-core hyphal exclusion to separate root and hyphae effects from soil microbial effects.
  - Provides detailed methodological and dataset groundwork for assessing mycorrhizal influence on forest regeneration.

- Site and climate
  - Location: Heishiding Nature Reserve, Guangdong Province, south China (4200 ha subtropical evergreen broad-leaved forest).
  - Climate: subtropical moist monsoon; mean annual temperature ~19.6 °C; 1744 mm annual rainfall (mostly Apr–Sep); pronounced dry season Oct–Mar.

- Focal organisms
  - Ten common tree species selected; evenly split between ECM and AM types:
    - ECM: Castanopsis fabri, Castanopsis fissa, Cyclobalanopsis hui, Lithocarpus haipinii, Engelhardia fenzelii.
    - AM: Schima superba, Cryptocarya concinna, Canarium album, Ormosia glaberrima, Artocarpus styracifolius.
  - Seedlings grown from seeds collected in 2015 (growth) and 2017 (survival); seeds surface-sterilized and germinated in sterile conditions before transplantation.

- Experimental design (in-growth core experiments)
  - Hyphal exclusion mechanism
    - Mesh cores with two pore sizes:
      - Large mesh: 35 µm (allows hyphae, excludes roots of neighboring plants).
      - Small mesh: 0.5 µm (prevents both roots and hyphae; only free-living microorganisms pass).
  - Core setup
    - Cylindrical cores: 16 cm diameter × 30 cm deep; six 8-cm windows; lined with 35 µm and/or 0.5 µm nylon mesh; outer 2 mm mesh to protect inner mesh.
  - Seedling survival experiment
    - 8 focal species transplanted into conspecific-dominated sites; 12 cores per mesh size per site; 8 seedlings per core.
    - Total: 768 seedlings (8 species × 2 mesh sizes × 6 cores × 8 seedlings per core).
  - Seedling growth experiment
    - Full reciprocal design: 6 focal species (3 ECM, 3 AM) × 6 sites (each dominated by one focal species) × 2 mesh sizes × 6 seedlings per core.
    - One-year-old seedlings; total: 432 seedlings.
  - Site and replication
    - For each focal species, a 30 × 30 m site with focal species dominance (DBH-weighted >30% among DBH ≥5 cm) and no adult individuals of other study species within the site.
    - Cores randomly placed within a 3 × 2 m area (30–50 cm apart). Soil mixed and cores backfilled; 4 weeks recovery before transplantation.
  - Harvest and measurements
    - Growth: 4 months (survival program) or 9 months (growth program) before harvest.
    - Biomass: total, shoot, and root dry weights after oven-drying at 60 °C for 72 h.
    - Mycorrhizal colonization: root samples analyzed by grid-line intersection; AM (aseptate hyphae, arbuscules, vesicles) and ECM (mantle and Hartig net) indicators recorded.
  - Environmental monitoring within cores
    - Soil moisture and temperature tracked with HydraProbe sensors at three times: beginning, middle, end of experiments.

- Data collection and variables (datasets)
  - Tree_Seedling_Survival.csv
    - SpCode, MeshSize, Core, Survival (live/dead), MycorrhizalType, etc.
  - Tree_Seedling_Growth.csv
    - Site, SiteMycorrhizalType, Core, MeshSize, MeshSizeNum, Species, SpMycorrhizalType, ID, HeightInitial, Height, RootBiomass, TotalBiomass, etc.
  - Tree_Seedling_Root_Colonization.csv
    - Site, SiteMycorrhizalType, Core, MeshSize, MeshSizeNum, Species, SpMycorrhizalType, SiteType (Con vs Hetero), ID, Yes (count of colonized roots), No (non-colonized), Rate (percentage colonized).
  - In-growth_Core_Enviroment.csv
    - Site, MycorrhizalType, Core, MeshSize, Temp20170526, Humidity20170526, Temp20170926, Humidity20170526, Temp20180117, Humidity20180117 (soil temperature and moisture at three dates).
  - Dataset structure notes
    - Each file ties to six sites and ten focal species via codes in Table 1; clear metadata fields for species, mycorrhizal type, core, mesh size, site, and experimental context.

- Relevance to monitoring and data governance
  - Demonstrates a rigorous, replicated field design for monitoring ecological interactions (mycorrhizal networks) and seedling performance, producing multiple outcome measures (survival, growth, biomass, root colonization, soil conditions).
  - Emphasizes data provenance and metadata (species codes, mycorrhizal type, mesh treatments, core identifiers, site context) to support data reuse and cross-study comparisons.
  - Highlights potential data-sharing considerations (publicly sharing underlying data and metadata; ensuring data quality, transformation, and governance standards at the source).
  - Provides a comprehensive blueprint for collecting environmental health indicators (biological responses plus soil microhabitat data) that can inform forest health monitoring and policy-relevant decision making.