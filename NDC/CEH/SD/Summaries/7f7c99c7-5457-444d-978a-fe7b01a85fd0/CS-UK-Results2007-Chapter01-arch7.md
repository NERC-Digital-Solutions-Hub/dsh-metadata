# Countryside Survey 2007

- Purpose and scope
  - Large-scale national survey to provide hard scientific evidence on plants, habitats, soils, and watercourses to inform countryside management and policy.
  - Two main components: Field Survey (habitats, vegetation, soils 0–15 cm, and freshwater) and a Land Cover Map derived from satellite data (to be published in 2009).

- GIS and data architecture
  - Core spatial unit: 1 km x 1 km sample squares; 591 squares surveyed in 2007 (England: 289, Wales: 107, Scotland: 195).
  - Northern Ireland: 0.5 km x 0.5 km squares (NICS) with 288 squares for UK-wide integration.
  - All Broad Habitats and Priority Habitats mapped within each square as polygons; linear features (hedges, walls, fences, roads) recorded with a hierarchical classification.
  - A single, geographically referenced CEH/ESRI-based GIS database links:
    - Habitat polygons
    - Vegetation plots (up to ~67 plots per square)
    - Soil sampling points (0–15 cm)
    - Freshwater data (streams and ponds)
  - Data capture moved from paper to electronic field forms, GPS-enabled plot relocation, and a web-based data management system for regular data uploads/downloads.

- Habitat classification and reporting
  - Broad Habitat framework: 45 Land Classes stratified across GB; 27 Broad Habitats (e.g., Broadleaved/Mixed/Yew Woodland, Coniferous Woodland, Arable/Horticultural Land, Grasslands, Bracken/Heath, Fens, Rivers/Streams, Ponds, Built-up areas, etc.).
  - Priority Habitats (65 total) identified in the UK Biodiversity Action Plan; four spatial masks used for Priority Habitat estimation (Scotland masks, JNCC woodland masks, English Natural Areas masks, Welsh upland mask).
  - Vegetation condition summarized using Aggregate Classes (AC1–AC8) to allow cross-year comparison (1978–2007). ACs group species composition and relate to Broad Habitats.
  - Reporting framework provides area estimates (in 000s ha), changes (1998–2007 for some bands; 1990–1998–2007 for GB), and vegetation condition measures with significance levels and directional arrows.

- Data collection and measurement methods
  - Field survey teams trained with standardized methods; consistent identification/recording across CS.
  - Surveys conducted with bespoke CEH GIS software on rugged hardware (laptops with GPS, Itronix devices).
  - Vegetation sampling: multiple plot types per square; 30 plots per square on average; fixed in space for multi-year tracking; relocation aided by GPS, photographs, and paper records.
  - Soil sampling: five Main Plots per square; 0–15 cm samples analyzed for pH, carbon concentration, bulk density, and other soil properties; methodology documented in Annex 4.
  - Freshwater sampling: headwater streams (biological condition via macro-invertebrates; plant communities for eutrophication indicators), stream habitat surveys (River Habitat Survey), and pond assessments (using PSYM and plant-based criteria) in selected squares.

- Conceptual framework for changes and analyses
  - Change in Broad Habitats estimated through a bootstrapped statistical model to maximize use of all available squares across years.
  - Conversion flows between Broad Habitats (1998–2007) presented to indicate net direction of habitat change, acknowledging potential mapping or data-processing noise.
  - Long-term vegetation change (1978–2007) tracked by assigning plots to the Aggregate Class they belonged to in 1978, enabling cohort analyses across decades.

- Northern Ireland integration (NICS)
  - Independent NI Countryside Survey mirrored GB CS principles, with regional habitat masks and alignment to UK Broad Habitat definitions.
  - Phased sampling: baseline (1986–1991), 1998 update, and 2007 (0.5% intensity, 288 squares) to derive NI Broad Habitat estimates integrated with GB results.

- Outputs, data products, and accessibility
  - Field Survey results feed into national and regional summaries; the Land Cover Map (satellite-based) released in 2009.
  - Results presented at UK and GB levels, with country-level reports for England, Scotland, and Wales published separately in 2009.
  - Supporting materials include:
    - Annex 2: Habitat keys
    - Annex 3: Vegetation plot details
    - Annex 4: Soils Manual
    - Annex 5: Statistical annex (change modelling)
  - Website and contact details provided for data access and further information (Countryside Survey: countrysidesurvey.org.uk).

- Practical implications for GIS specialists
  - Standardized, linked geo-databases enable robust analysis of area, change, and condition across decades.
  - Use of Broad and Priority Habitat classifications with compatible translation from older data via back-translation and 1998 mappings to support longitudinal analyses.
  - Ability to compute habitat conversion flows, linear feature lengths, and pond/stream condition metrics within a consistent GIS framework.
  - Data captured and stored through an integrated, geo-referenced system supporting multi-year relocation of fixed vegetation plots and spatially explicit soil and freshwater measurements.
  - Upcoming Land Cover Map provides a complementary satellite-derived layer aligned with the field-based GIS dataset for integrated mapping and visualization.