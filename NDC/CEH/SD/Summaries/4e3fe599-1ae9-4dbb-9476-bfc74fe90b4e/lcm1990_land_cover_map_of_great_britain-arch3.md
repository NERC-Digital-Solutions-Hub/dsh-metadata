# Land Cover Map of Great Britain (1990)

- Purpose and scope
  - Digital dataset classifying land cover types into 25 classes at 25 m resolution, derived from Landsat 5 Thematic Mapper.
  - Aimed to support planning, management, and monitoring across sectors (agriculture, ecology, conservation, forestry, water, urban planning, transport, recreation, minerals).
  - Provides a baseline national land cover map, the first comprehensive satellite-based map for Britain.

- Data, methods, and structure
  - Data sources and processing
    - Supervised maximum likelihood classification of Landsat TM data.
    - Combines summer and winter imagery to improve accuracy; cloud and data gaps noted.
  - Spatial resolution and coverage
    - 25 m grid; maps land cover types across Britain with field-scale detail; features as small as about 1 ha detectable under favorable conditions.
    - Registration accuracy to vector field maps about 20 m (0.8 pixels average displacement).
  - Data products
    - Stand-alone 25 m data: single layer with values 0–25 representing 25 target classes.
    - 1 km summary data: 17 “key” classes; each 1 km cell contains the percentage share (0–100) of that key class within the cell, presented as separate bands for each key class (A–Q order).
  - Classification scheme
    - 25 target classes cover sea, inland water, beaches/bare ground, saltmarsh, grass/heaths/moorlands, pastures, bogs, arable, suburban/rural development, urban development, inland bare ground, and unclassified.
    - Appendix 1/2 explain class definitions, aggregation possibilities (e.g., 25 vs 17-class outputs), and the ecological and management context behind class distinctions.

- Accuracy, validation, and cautions
  - Overall accuracy and interpretation
    - Ground-truth data are limited; comparisons show variability in accuracy depending on class definitions and detail level.
    - When compared to independent ground data for 508 one-kilometre squares, overall correspondence is around 67% (including boundary pixels) or 71–76% after accounting for boundary pixels and temporal changes; without boundaries, correspondence can rise to ~82%.
    - Realistic accuracy is generally considered around 80–85% under plausible interpretation differences and temporal change.
  - Error sources and characteristics
    - Major map errors stem from mixed boundary pixels (about 40% of pixels border class boundaries); excluding these raises correspondence to ~71–82%.
    - Misclassification vs mis-registration can be difficult to disentangle in dissected landscapes.
    - Differences in class definitions (e.g., hydrological vs botanical criteria for bogs) complicate direct comparisons with field surveys.
  - Temporal context
    - Some observed changes reflect actual land-cover changes between the dates of imagery used (often ~2-year gaps).

- Data access, licensing, and use
  - Licencing and charges
    - Data provided under Licence; pricing in three bands: commercial, non-commercial, and research; UK academics may receive reductions.
  - Availability
    - Data can be supplied for any area of Britain; orders configured to end-user needs.
    - Formats and licensing options accommodate single-user to corporate/multi-site use; new licence forms can be developed.
  - Related data products
    - Land Cover Map 2000 (update) is available; further information and samples are on the Countryside 2000 platform, with data downloadable via the Countryside Information System.
  - Access and governance guidance
    - Notes emphasize data are land cover (not land use) and reflect dominant cover at imaging times.
    - DAR (Data Assessment Report) accompanies data to collect user feedback, issues, and analysis notes.

- Practical guidance for monitoring frameworks
  - Suitability and limitations for policy monitoring
    - Useful for monitoring landscape change, habitat distribution, and broad-scale environmental assessments.
    - Users should be cautious when interpreting accuracy and when aggregating classes; class definitions and time points influence results.
  - Metadata and data quality
    - Metadata gaps can hinder verification; the dataset includes guidance on interpretation and potential need for custom aggregations in GIS.
    - Transformation between 25 m classes and 1 km summaries requires careful handling to preserve meaningful proportions.
  - Data governance and transparency
    - Public sharing of underlying data is encouraged but can be a barrier; licensing and versioning considerations are important for reproducibility.
    - Data quality assurance, documentation, and version control are essential for monitoring frameworks.

- Applications and examples
  - Suitable for planning and evaluating processes in agriculture, ecology, conservation, forestry, water resources, urban planning, transport, and environmental assessment.
  - Examples include detecting land-cover changes, mapping invasive or habitat-impacted areas (e.g., bracken in health studies), environmental assessments of infrastructure projects, and guiding telecommunications planning.

- Notes and additional resources
  - Appendix 2 provides a color mapping recipe for LCM1990 classes.
  - The document also discusses the relationship between lowland and upland classifications, management-driven spectral variation in grasslands, and the potential for bespoke 17-class aggregations in GIS.
  - References and related work are listed, including links to the Countryside 2000 project and CEH Wallingford contact details for data access.

- Contact and follow-up
  - Data provider: CEH Wallingford, Land Cover Map Sales; contact and licensing details provided for licensing, data orders, and further information.