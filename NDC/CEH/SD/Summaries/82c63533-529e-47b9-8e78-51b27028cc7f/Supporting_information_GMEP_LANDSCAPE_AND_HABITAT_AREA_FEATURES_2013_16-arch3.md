# Glastir Monitoring and Evaluation Programme (GMEP)

- Overview and purpose
  - Wales-wide monitoring initiative established by the Welsh Government in 2013 to assess the effects of the Glastir agri-environment schemes on the environment.
  - Aims to contribute evidence for biodiversity trends, woodland creation/management, and progression towards goals under the Convention on Biological Diversity (CBD) 2020.
  - Provides indicators relevant to tracking the Well-Being of Future Generations (Wales) Act 2015, including area estimates for semi-natural habitats and healthy ecosystems.

- Monitoring design and cycle
  - 4-year rolling survey cycle (first cycle 2013–2016) to maximize site coverage while enabling year-on-year trend detection.
  - Two integrated components:
    - Wider Wales Component: baseline estimation, national trends, national reporting of Glastir.
    - Targeted Component: links specifically to Glastir priority areas.
  - Common spatial unit: 1 km square to enable data integration across scales and potential future linkage with the Countryside Survey of Great Britain.
  - Sample: 300 x 1 km squares over the cycle; stratified sampling with half from random, stratum-defined 1 km squares and half targeted at Glastir priorities.
  - Exclusions: squares with >75% urban land or >90% sea are removed.

- Sampling framework and data integration
  - Sampling strata derived from the Land Classification of Great Britain (ITE Land Classification 2007) to minimize within-stratum heterogeneity and maximize between-stratum differences.
  - Proportional sampling by stratum size to optimize survey effort.
  - Design aligned with Countryside Survey methodologies to enable future integration across GB.

- Data collection methods and fieldwork
  - In each 1 km square, areal, line, and point features mapped on base maps using predefined coded options (habitat, land use, management, vegetation descriptors, etc.).
  - Electronic data capture with CS Surveyor (CEH/Esri UK) to standardize data entry, reduce post-survey digitising, and enable rapid data quality checks.
  - Field data include: Biodiversity Broad/Priority Habitats, land use, vegetation types, structure, management practices, and site-specific descriptors (e.g., tree diameter, verge widths).
  - Referenced through GMEP Field Mapping Handbooks for detailed methodology.

- Data files and schema
  - LANDSCAPE_AND_HABITAT_AREA_FEATURE_2013_16.csv: core areas of broad and priority habitats sampled across 300 squares; key fields include SQ_ID, POLY_ID, BHCODE, BHDESC, AREA, coordinates, YEAR, LC, etc.
  - LANDSCAPE_AREA_FEATURE_ATT_2013_16.csv: attributes for mapped landscape/habitat areas; includes thematic fields such as THEME, HABITAT_NAME, MOSAIC_PC_AREA, VEGETATION descriptors (SPECIES, SPECIES_COVER, SWARD_COVER, SWARD_HEIGHT, etc.), physical attributes (MODAL_DBH, ROAD_VERGE_WIDTHS), and YEAR.
  - Species nomenclature follows Stace (1997); additional field details provided in the GMEP Field Handbooks.
  - Data quality and consistency are reinforced by standardized coding and documentation.

- Quality assurance and data quality
  - Surveys conducted by experienced botanical survey teams with formal training to ensure consistency.
  - Use of CS Surveyor with mandatory data entry fields, prompts, and checks to reduce errors and ensure full coverage of mapped components.
  - Field teams supervised by senior staff; a QA (QC) exercise involves a second survey team repeating all or part of a square to identify issues and feed back to field teams for improvement.
  - Prompt data transfer to offices enables timely data checks and issue resolution.

- Governance, openness, and data management
  - Outputs include reports, charts, and dashboards; underlying data are managed with attention to quality, clarity, and clear presentation of findings.
  - Metadata and data quality are central to enabling verification and reuse; links to national datasets (e.g., Land Classification) and peer-reviewed handbooks support interoperability.
  - The project maintains a website (gmep.wales) with publications, methodologies, and results to support transparency and stakeholder engagement.
  - Metadata and data governance considerations are addressed through field handbooks, standardized data formats, and open dissemination of methodologies and results.

- References, publications, and documentation
  - Field handbooks (Mapping Field Handbook parts 1 and 2) detailing habitat attributes, mosaics, and digital mapping.
  - Key methodological references: ITE Land Classification 2007; UK Biodiversity Action Plan habitat descriptions; Stace flora nomenclature.
  - Annual and final reports to Welsh Government; citations to CEH and NERC documentation for methodology and data handling.

- Appendices: roles and teams
  - Roles and responsibilities listed (e.g., GMEP Lead Scientist, Habitats work package lead, data management, GIS, sampling design, statisticians).
  - Field survey teams named, showing structured governance and team-based implementation.

- Practical implications for monitoring framework authors
  - Demonstrates how to design a multi-masure, ecosystem-based monitoring program with integration across scales.
  - Shows the value of a rolling 4-year cycle to balance geographic coverage with temporal trend analysis.
  - Highlights the importance of standardized spatial units (1 km squares) and alignment with existing national surveys to enable data integration.
  - Emphasizes rigorous QA processes, digital capture to minimize errors, and feedback loops for continuous improvement.
  - Underlines data governance considerations: metadata completeness, data sharing, transparency, and clear documentation to support policy evaluation and future decision-making.