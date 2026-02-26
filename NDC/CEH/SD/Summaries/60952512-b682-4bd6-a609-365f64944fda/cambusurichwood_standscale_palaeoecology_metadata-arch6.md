# Metadata

- A stand-scale palaeoecological dataset from Cambusurich Wood, Scotland, captured during a study of long-term dynamics in ancient temperate woodland of high conservation value. Site: Cambusurich Wood SSSI (Ordnance Survey grid NN 62741 34679). Sampling occurred in October 2020 using duplicate peat cores from an 8.5 x 7 m peat-infilled forest hollow named Camb. The work was supported by the Natural Environment Research Council (Grant NE/S007377/1).

- Scope and proxies:
  - Microfossils: pollen, non-pollen palynomorphs, spores, microcharcoal (one core set).
  - Macroremains: plant macrofossils and macrocharcoal (second core set).
  - Chronology and loss-on-ignition (LOI) derived from the same core as the microfossil analyses.
  - Supports a multi-proxy reconstruction of past vegetation and sediment characteristics.

- Data provenance and relationships:
  - Data generated as part of a coordinated study of long-term woodland dynamics.
  - Duplicate cores allow cross-validation between microfossil and macrofossil datasets.
  - Chronological controls include AMS radiocarbon dating and 210Pb measurements.
  - LOI measurements follow the Heiri et al. (2001) protocol.

- Access and provenance notes:
  - Data are organized into several CSV files, each detailing specific proxies or chronology-related measurements.
  - The dataset provides raw counts and semi-quantitative scale data, enabling re-analysis, scaling, or integration with other proxy records.
  - Supporting literature is provided to contextualize methods and interpretations.

- Data products and formats:
  - CambusurichWood_Raw_Microfossil_Data.csv: per-sample metrics including sample mid-depth (cm), sample volume (cm3), exotic lycopodium addition/counts/tablets, and raw counts for pollen, spores, non-pollen palynomorphs, and microcharcoal (Rows 6-120 represent raw data).
  - CambusurichWood_Raw_Macrofossil_Data.csv: per-sample metrics including sample mid-depth (cm), sample volume; macrofossil counts across various tissue types (Rows 3-76) with a four-point semi-quantitative scale (x, xx, xxx, xxxx) and macrocharcoal counts in size classes (Rows 77-80).
  - CambusurichWood_Chronological_Controls.csv: depth (cm), lab code, material description, 14C age (years BP), and dating error.
  - CambusurichWood_Loss_On_Ignition.csv: mid-depth (cm) and LOI percentage.
  - CambusurichWood_Troels_Smith.csv: depth boundaries (cm) and sediment components described using the Troels-Smith system.

- Key data characteristics:
  - Depth references are provided as mid-depths (1 cm and 2 cm thick peat subsamples) relevant for stratigraphic interpretation.
  - Macrofaunal data include both raw counts and semi-quantitative presence/abundance indicators.
  - Chronological controls combine AMS radiocarbon dates and 210Pb data, with associated age uncertainties.

- Data quality and usability considerations:
  - The dataset spans multiple proxies with distinct measurement scales, requiring careful harmonization for integrated analyses.
  - Some fields are presented as raw counts (microfossils) or as categorical abundance scales (macroremains), necessitating appropriate data transformation for quantitative synthesis.
  - The use of duplicate cores enhances reliability but requires alignment of sample depths and depth references across datasets.

- Supporting literature:
  - References cover pollen type catalogs, palaeoecological methods for pollen and macrofossil analysis, LOI methodology, and key analytical techniques (e.g., Stockmarr 1971 for pollen tablets, Heiri et al. 2001 for LOI, Troels-Smith 1955 sediment description, among others).

- Potential uses and audience:
  - Enables multi-proxy reconstructions of past woodland dynamics and sedimentation.
  - Suitable for data-support activities such as data packaging, cleaning, combining proxies, and creating end-user data products (dashboards, pivot tables, charts) to enable self-service exploration.
  - Data can be cross-referenced with the listed supporting literature to validate methods and interpretations.