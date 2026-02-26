# The Glastir Monitoring and Evaluation Programme (GMEP)

- Purpose and context
  - Welsh Government monitoring programme (GMEP) established in 2013 to assess the environmental effects of the Glastir agri-environment scheme.
  - Aims to measure biodiversity, woodland creation/management, and provide an independent estimate of changes in semi-natural habitat.
  - Data contribute to tracking progress towards reversing native biodiversity decline and meeting obligations under the Convention on Biological Diversity (2020).
  - Supports indicators for the Well-Being of Future Generations Act 2015, including the area of healthy ecosystems in Wales.

- Survey design and sampling
  - Four-year rolling survey cycle (2013–2016) to maximise site coverage while detecting year-on-year changes cost-effectively.
  - Two components: Wider Wales Component (baseline estimates and national trends) and Targeted Component (Glastir priority areas).
  - All data integrated using a common spatial unit: 1 km squares; total of 300 squares surveyed over the cycle.
  - Sampling framework follows the Countryside Survey of Great Britain methodology to enable future integration.
  - Strata defined by the Land Classification of Great Britain (ITE framework); half the squares sampled randomly within strata, half targeted at Glastir priority areas.
  - Exclusions: squares with >75% urban land or >90% sea (based on LCM2007 and high-tide data).

- Data collection methods and variables
  - Within each 1 km square, areal, line, and point features are mapped onto base maps using predetermined coded options.
  - Electronic data capture with CS Surveyor (CEH/Esri) to record:
    - Biodiversity Broad/Priority Habitat codes and descriptions
    - Land use and land management (cropping, grazing, recreation, timber, burning, etc.)
    - Dominant vegetation species, vegetation descriptors, and other land-use attributes
  - Data organized in structured CSV files:
    - LANDSCAPE_AND_HABITAT_AREA_FEATURE_2013_16.csv: areas of broad/priority habitats across 300 squares; includes square and polygon IDs, habitat codes/descriptions, area, coordinates, year, and land-class information.
    - LANDSCAPE_AREA_FEATURE_ATT_2013_16.csv: additional attributes for mapped habitat areas (themes, habitat names, mosaic areas, vegetation attributes, structure, and related qualifiers).
  - Vegetation nomenclature follows Stace (1997); species data recorded where relevant.

- Quality Assurance (QA) and data quality
  - Surveys conducted by experienced botanical survey teams; intensive pre-survey training to ensure consistency with field handbooks.
  - Electronic data capture reduces post-survey digitising errors; mandatory fields and prompts to ensure complete, accurate data.
  - Data transferred to the office promptly for timely checks; field staff and managers maintain ongoing communication.
  - QC exercises involve a second team re-surveying all or part of a square; findings fed back to improve recording.

- Outputs, relevance, and references
  - Provides robust estimates of broad habitat extent and changes in semi-natural habitats, contributing to national indicators.
  - Supports evidence for biodiversity targets and ecosystem health in Wales.
  - References include: ITE Land Classification (GB 2007), field handbooks (Maskell et al. 2016), annual and final GMEP reports, and related biodiversity publications.
  - Access to methodology and results via the Glastir Monitoring & Evaluation Programme website (gmep.wales) and linked field handbooks.

- Appendix and governance
  - Appendix 1 lists roles, tasks, and responsibilities (e.g., lead scientist, field team managers, database and GIS specialists, and vegetation experts).
  - Field survey teams comprise a broad roster of surveyors and coordinators.
  - Emphasis on structured project management, data stewardship, and team coordination to sustain long-term monitoring.

- Data integration and future work
  - The shared 1 km square sampling framework enables integration with other national surveys (e.g., Countryside Survey) and potential future GB-wide analyses.
  - Ongoing capability to link landscape/habitat data with biodiversity indicators for monitoring policy performance over time.