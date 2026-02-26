# Countryside Survey vegetation plots 2020_21

- Overview and purpose
  - Countryside Survey is a long-running UK study of natural resources, enabling comparisons over time to detect changes in soils, vegetation, streams, habitats, and landscape features.
  - The 2019 onward rolling program repeats surveys on a five-year cycle (500 squares total), buffering results against climate variability and maximizing site coverage nationally.
  - Data support national and sub-national indicators for Great Britain and its constituent countries; aims to provide robust, time-series insights into countryside condition.

- Design and sampling
  - 500 x 1km squares are randomly selected each five-year cycle and stratified by the Land Classification of Great Britain.
  - Approximately 100 squares are visited per year; 78- year logic includes the long-running 256 squares from 1978 to maintain the longest time series.
  - Squares containing more than 75% urban land or more than 90% sea are excluded from sampling.

- Data collection and protocols
  - Field data are collected by trained botanists following standard protocols (Smart et al., 2020) with intensive pre-survey training to ensure consistency.
  - Surveys are supervised by experienced project staff; 10% of plots are re-surveyed for quality assurance, with QA conducted by the same assessor since 1990.
  - Independent validation aligns plot locations and broader habitat classification with JNCC broad/priority habitat units.

- Data products and structure
  - Two primary data files for 2020–2021:
    - Vegetation Plot - Plot Information (UKCEHCS_VEGETATION_PLOTS_2020_21.csv)
      - Key fields include: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, plot size descriptors, habitat designations (PLOT_BH, PLOT_PH), country (England/Scotland/Wales), county, environmental zone (ENV_ZONE_2007), land classification (LC07, LC07_NUM), and related descriptors.
    - Vegetation Plot - Species List (UKCEHCS_VEGETATION_PLOT_SPECIES_2020_21.csv)
      - Includes: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, species identifiers (BRC_NUMBER), nest/cover metrics (NEST_LEVEL, ZERO_COVER, FIRST_COVER, TOTAL_COVER), and species nomenclature aligned to Stace (1997).
  - Taxonomy and habitat references underpin data fields (e.g., Stace nomenclature; Jackson 2000 habitat guidance; Maddock 2008 BAP descriptions).

- Standards, metadata, and documentation
  - Data collection relies on the UK-SCAPE field survey handbook (2020) and supporting methodological documents; references include foundational CEH and CS reports.
  - Species nomenclature follows Stace (1997) for consistency across datasets.
  - Documentation supports interoperability with ITE Land Classification (Bunce et al. 2007) and JNCC biodiversity classifications.

- Data governance and sharing
  - Data are prepared for upload to relevant portals and catalogues; extensive metadata and methodology are documented to support reuse.
  - The rolling program and standardized methods facilitate updates and ongoing comparability across cycles.
  - Potential governance considerations include maintaining data quality, updating habitat and land-class codes, and ensuring consistent metadata for discoverability and reuse.

- Context and references
  - The dataset is part of a broader Countryside Survey lineage with key outputs and methodological references spanning 1996–2012 and the ongoing 2019 rolling program.
  - Core methodological and contextual sources include Smart et al. (2020) field handbook, Stace (1997), Jackson (2000), Maddock (2008), Bunce et al. (2007), Carey et al. (2008), Norton et al. (2012), and Scott (2008).