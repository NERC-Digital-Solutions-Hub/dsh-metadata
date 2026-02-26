# Eurasian pollen data from 21 kiloannum to the present

- Overview and aim
  - Describes a data collection workshop held in Winchester (April 2008) to aggregate unpublished pollen data from contributors mostly from the Former Soviet Union.
  - Objective: define the most likely vegetation types (biomes) represented by fossil pollen from the Last Glacial Maximum (~21 ka) to the present.
  - Dataset supports interpretation of palaeo-vegetation change and informs biomes over time.

- Dataset scope and provenance
  - 96 sites spanning 24°E (western Ukraine/Belarus) to eastern Siberia; north of 40°N.
  - 99 entities (e.g., multiple cores per site; multiple sections per terrestrial exposure).
  - Contributors conducted fieldwork and sample analysis; workshop added site-level context (bog vs lake, surrounding vegetation).

- Methods and data processing
  - Age modelling
    - Calibrated radiocarbon dating and age models produced using CLAM v1.2 (Blauuw, 2010).
    - Each sample includes calibrated age with error estimates.
  - Taxonomy and data cleansing
    - Original taxon names (TaxonName) retained alongside TaxonClean, which is standardized to ITIS taxonomy.
    - Regional naming differences acknowledged (e.g., Duschekia fruticosa = Alnus fruticosa).
    - Non-pollen identifications deleted (e.g., Dyadosporites as fungus).
    - Taxonomy checked for consistency; redundancy-free taxonomy produced (Taxonomy table).
  - Handling unidentified data
    - Instances where objects could not be identified recorded as question marks; TaxonClean records reflect deletions and are not used in analyses.
  - Data quality and transparency
    - Documentation of age model details, number of radiocarbon dates, and outliers removed.
    - Local site information captured to aid interpretation (e.g., site type, local vegetation).

- Data structure and metadata
  - Six interrelated tables:
    - Site Table: SiteID, SiteName, DataSubmitter, SurfaceSample, Elevation, LatDD, LonDD, Notes.
    - Entity Table: SiteID, SiteName, EntityID, EntityName, LocalVeg, Age_model_ID, Age_model, SampleUsage, No_of_rc_dates, Outliers, Site_Description_notes.
    - Sample Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, Cal_yr_BP, Error, AgeSlice, SampleUsage.
    - Pollen Table: SiteID, SiteName, EntityID, EntityName, SampleID, DepthCM, TaxonName, TaxonClean, ITIS, PollenCount.
    - Age Model Table: Age Model ID, Age Model description.
    - Taxonomy Table: TaxonName, TaxonClean.
  - Metadata purpose
    - Provides provenance, sampling context, age information, taxonomic standardization, and data lineage to support reproducibility and policy-relevant interpretation.

- Data availability and publication status
  - Full database to be available via the Southampton University website.
  - Data intended for publication in Quaternary Science Reviews (2017, in press).
  - References include Blauuw (2010) for age modelling methods.

- Implications for monitoring frameworks
  - Demonstrates a robust workflow for building environmental health datasets:
    - multi-source data integration with provenance and context
    - standardization of taxonomy to enable comparability
    - transparent age modelling with error estimates
    - explicit data governance around sharing and metadata
  - Highlights practical barriers aligned with monitoring challenges:
    - data sharing and metadata completeness
    - ensuring up-to-date data and avoiding silos
    - balancing openness with data origin and rights

- Key takeaways for policy-relevant monitoring
  - A structured, metadata-rich dataset enables consistent interpretation of long-term vegetation change and biome assignments.
  - Standardized taxonomy and clear age models improve reliability of environmental indicators used in policy evaluation.
  - Public data sharing (with clear provenance) supports transparency, comparability, and downstream monitoring activities.