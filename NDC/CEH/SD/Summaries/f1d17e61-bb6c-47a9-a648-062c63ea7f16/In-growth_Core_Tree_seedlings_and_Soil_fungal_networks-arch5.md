# In-growth core experiments

- Purpose and scope
  - Two independent mesh-core experiments test whether external mycorrhizal networks influence seedling survival and growth.
  - Focused on ten common tree species from a subtropical forest in Heishiding Nature Reserve, Guangdong, China (five ECM, five AM).
  - Seedling growth experiment running March 2017–January 2018; survival experiment March–August 2018.

- Study site and climate context
  - Heishiding Nature Reserve, 4200 ha subtropical evergreen broad-leaved forest.
  - Tropically influenced, subtropical moist monsoon climate; mean annual temp 19.6 °C; 1744 mm annual rainfall with a pronounced dry season Oct–Mar.

- Experimental design and setup
  - Mesh-core experiments to separate root vs. hyphal interactions:
    - Core dimensions: 16 cm diameter, 30 cm depth.
    - Windows: six 8-cm windows at 4–12 cm and 16–24 cm depths.
    - Mesh treatments: 35 µm (allows hyphae) vs 0.5 µm (excludes hyphae and roots).
    - External protection: 2 mm nylon mesh on sides/bottom to prevent soil fauna damage.
  - Site selection and replication
    - Six cores per focal species per site; 12 cores per species for growth experiment; replication varies by experiment (see data section).
    - Seedling transplantation: one month after transplant, with replacement of dead/poorly growing individuals.
  - Species and functional groups
    - ECM species: Castanopsis faberi, Castanopsis fissa, Cyclobalanopsis hui, Lithocarpus haipinii, Engelhardtia fenzelii.
    - AM species: Schima superba, Cryptocarya concinna, Canarium album, Ormosia glaberrima, Artocarpus styracifolius.
  - Seedling handling and timing
    - Seeds collected autumn/winter 2015 (growth) and 2017 (survival).
    - Seeds surface-sterilized and germinated; transplanted as one-year-old seedlings into cores.
  - Measurements and harvest
    - Growth: 9 months; biomass separated into shoot and root, dried at 60 °C for 72 h.
    - Survival: 4 months; harvest to assess live/dead status and biomass.
    - Mycorrhizal colonization: assessed via grid-line intersection for AM (aseptate hyphae with arbuscules/vesicles) and ECM (mantle/Hartig net) colonization on 10 fine root fragments per seedling.
  - Environmental monitoring
    - Soil temperature and moisture measured with HydraProbe sensors in each core.
    - Measurements taken at three time points: early, middle, and end of experiments.

- Data products and structure
  - Tree_Seedling_Survival.csv
    - SpCode: focal species code (Table 1).
    - MycorrhizalType: ECM or AM.
    - MeshSize: L (35 µm) or S (0.5 µm).
    - Core: core number (1–6) per species.
    - Survival: 1 = live, 0 = dead.
  - Tree_Seedling_Growth.csv
    - Site: six sites, each dominated by a focal species.
    - SiteMycorrhizalType: ECM or AM for the site.
    - Core: core number (1–12) within each site.
    - MeshSize and MeshSizeNum: 35 µm (35) or 0.5 µm (0.5).
    - Species: seedling species (coded; Table 1).
    - SpMycorrhizalType: seedling’s mycorrhizal type (ECM/AM).
    - ID: seedling identifier within a core.
    - HeightInitial, Height: seedling height at transplant and harvest.
    - RootBiomass, TotalBiomass: dry masses at harvest.
  - Tree_Seedling_Root_Colonization.csv
    - Site, SiteMycorrhizalType, Core, MeshSize, MeshSizeNum, Species, SpMycorrhizalType.
    - SiteType: Con (conspecific-dominated site) or Hetero (heterospecific-dominated).
    - ID: seedling identifier.
    - Yes, No: counts of roots with/without mycorrhizal colonization.
    - Rate: colonization rate (Yes / (Yes + No)).
  - In-growth_Core_Enviroment.csv
    - Site, MycorrhizalType, Core, MeshSize, Temp/Humidity measurements
    - Temp20170526, Humidity20170526; Temp20170926, Humidity20170926; Temp20180117, Humidity20180117
    - Temporal coverage of soil temperature and moisture by core and mesh treatment.

- Species codes and table reference
  - Table 1 provides the six focal species with family, mycorrhizal type, and experimental usage (Survival, Growth, or both).

- Data provenance, quality, and processing notes
  - Seedling handling: regular replacement of individuals post-transplant to maintain healthy cohorts.
  - Colonization assessment: grid-line intersection method with specified criteria for AM and ECM.
  - Soil and environmental data collection: standardized HydraProbe instrumentation; repeated measurements to capture temporal variation.
  - Documentation and metadata
    - Each dataset includes explicit column definitions, coding schemes, and cross-references to the focal species table.
    - Codes (SpCode, Core, Site, etc.) enable traceability from raw seedlings to core-level treatments and site contexts.

- Relevance for data governance and stewardship
  - Clear data schema with consistent coding across datasets facilitates discoverability, interoperability, and reuse.
  - Explicit documentation of mycorrhizal type, mesh treatments, core IDs, site contexts, and measurement timings supports reproducibility and auditability.
  If adopting best practices for data stewardship, ensure:
  - Centralized metadata catalog linking SpCode, Site, Core, and Species to full names and attributes.
  - Unit standardization (e.g., temperatures in °C, biomass in g, percentages for humidity, etc.).
  - Versioning and data provenance to track any reprocessing or corrections.
  - Access controls and licensing that enable reuse while preserving dataset integrity.
  - Data quality notes capturing potential sources of bias (e.g., manual replacements, seed source variability, potential core drainage effects).

- Practical considerations for reuse
  - Suitable for analyses on how mycorrhizal associations (ECM vs AM) and hyphal connectivity (mesh size) influence seedling survival, growth, root colonization, and biomass accumulation under different neighbor contexts.
  - Requires alignment with Table 1 for species-name resolution and careful interpretation of SpCode, Core, MeshSize, and Site variables to ensure correct aggregation and comparisons.