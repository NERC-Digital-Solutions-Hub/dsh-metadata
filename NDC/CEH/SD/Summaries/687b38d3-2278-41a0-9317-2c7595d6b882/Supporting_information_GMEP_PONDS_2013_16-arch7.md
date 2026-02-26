# FIELD HANDBOOK Freshwater, Glastir Monitoring & Evaluation Programme

## Purpose and scope
- Documentation of pond field surveys in Wales as part of the Glastir Monitoring & Evaluation Programme (GMEP).
- Produces map-based and tabular data on pond characteristics, biology (macrophytes and macroinvertebrates), chemistry, and environmental context for ecological quality assessment (PSYM/IBI).

## Survey design and sampling framework
- Sampling unit: 1 km survey squares, with random/proportional sampling across strata to allocate survey effort.
- Half of samples targeted at Glastir priority areas; avoid squares with >75% urban land or >90% sea.
- Data confidentiality: plots shown at 10 km resolution on maps.
- Pond definitions and boundary scope: outer boundary defined by the winter maximum water level; survey may include areas outside the square for complete pond assessment.

## Field workflow and data collection
- Field data captured on tablet PCs and entered into a central database.
- Primary field forms:
  - Pond Checklist (water chemistry and macroinvertebrate survey details)
  - Pond Attributes (pond characteristics and environmental information)
  - Pond Plants (macrophyte survey data)
- Macrophyte and macroinvertebrate surveys are conducted within the pond boundary; photographs and sketch maps accompany surveys.
- Two-person survey teams (A = aquatic fauna/chemistry, B = plant identification and attributes) with defined task sequence.
- Safety considerations and health-and-safety assessment conducted prior to sampling.

## Pond definitions, boundaries, and age
- Pond: 25 m2 to 2 ha, usually water for at least four months/year; includes temporary ponds.
- Outer boundary identified by markers such as shifts in vegetation or water marks; survey may include boundary areas outside the mapped square.
- Pond age: record age for new ponds (up to ~10 years) using owner/land manager information or physical indicators.

## Measurements and methods (field)
- Water chemistry (headwater head): measure pH, conductivity, turbidity in the field; collect filtered and unfiltered samples for SRP, TON, and alkalinity.
- Turbidity estimation: categorize visually (clear to turbid).
- Equipment: Hanna Combi pH/EC meter; 50 ml filtered samples for chemical determinands.
- Sampling protocol: three bottles per pond, with careful labeling and on-site filtering where needed.
- Data capture: record all readings on the Pond Checklist and ensure square/pond identifiers.

## Pond attributes, photography, and mapping
- Photograph the pond (1–2 shots) with a marker board displaying pond survey identifiers (P for pond survey, pond reference, square number).
- Perimeter survey: walk the boundary, note inflows/outflows, land use, and features; sketch the pond outline and estimate area; include scale and north.
- Recording of pond size, water depth, sediment depth, drawdown height (vertical difference between winter maximum and current level), pond permanence, inflows/outflows, and pond base composition (clay/silt, gravel, rock, peat, etc.).

## Macrophyte (aquatic plants) survey
- Objective: record all wetland plant species within the pond boundary and estimate total plant cover across submerged, floating-leaved, and emergent categories.
- Identification: field keys; identify to species where possible; collect samples for difficult taxa; rare species require careful handling and potential verification.
- Data entry: use Pond Plants forms; abundance is categorized (Dominant, Abundant, Frequent, Occasional, Rare) and cover percentages recorded.
- Specimen handling: press or pickle samples; label specimens with pond and square identifiers; follow verification procedures for rare species.
- Documentation: species list, tape measures for cover, and shading/overhang assessments.

## Macroinvertebrate survey
- Habitat-based sampling: identify 5–10 habitats (e.g., sedges, shallows, submerged vegetation, inflows) and allocate sampling time (3 minutes total, divided by habitat count; sub-samples as needed).
- Sampling: 25 cm2 pond-net with 900 µm mesh; kick sampling of soft sediments; avoid over-collection of vegetation.
- Additional search: 1 minute of searching on surface and under stones/logs to catch missed taxa.
- Fixing and storage: preserve samples in formalin, label with pond/square/date, and store in labeled storage pots for transport.
- Sorting and transport: maintain clean nets; document all data on field forms; transport in labeled containers with appropriate hazard documentation.

## Environmental survey and land use
- Record environmental attributes (LC – Land Classification), multiple coordinates (EASTING/NORTHING in OSGB 1936), and year.
- Surrounding land use: quantify land use within two distance zones around the pond perimeter (0–5 m and 0–100 m) across predefined categories (trees/woodland, arable, urban, roads, grasslands, etc.).
- Shade and overhang: quantify shade from overhanging woody vegetation and shading along pond margins.

## Laboratory protocols and analyses
- Phosphate (PO4-P), Total Dissolved Nitrogen (TDN), alkalinity: analyzed at UK Centre for Ecology and Hydrology (UKCEH) using accredited methods.
- Analytical methods include colorimetric phosphate determination, chemiluminescent nitrogen measurement, and automatic titration for alkalinity.
- PSYM (Predictive System for Multimetrics) used to compute pond biological quality from plant and invertebrate metrics, comparing observed metrics to modeled ideal conditions.

## Data quality, QA, and standards
- QA framework aligned with DEFRA Joint Codes of Practice (JCoPR) for robust, auditable science and data handling.
- PSYM and IBI are used to interpret ecological quality; metrics are reported with categorical interpretations (good, moderate, poor, very poor).
- Data are standardized and stored in structured CSV tables with explicit fields and coding (e.g., LC codes, 10 km coordinates).

## Data structure and example datasets
- Tables (examples):
  - GMEP_POND_INVERTS_2013_16.csv: pond-wise macroinvertebrate taxa counts by square/year.
  - GMEP_POND_MACROPHYTES_2013_16.csv: macrophyte species, category (submerged, floating, emergent, etc.), and abundance.
  - GMEP_POND_MACROPHYTES_SUMMARY_2013_16.csv: summary metrics for aquatic vegetation, including percent cover by category and PSYM/IBI indicators.
  - GMEP_POND_ENV_SURVEY_2013_16.csv: environmental variables (LC, coordinates, variable descriptions, values).
  - GMEP_POND_CHEMISTRY_2013_16.csv: chemistry determinands (SAMPLE_DATE, DETERMINAND, VALUE, UNITS).
- Key fields across datasets: SQ_ID, YEAR, LC, EASTING_10km, NORTHING_10km, POND/pond references, TAXA_NAME, SPECIES, ABUNDANCE, VALUE, PSYM, IBI, ADEQUATELY, IF_NO_DESCRIBE, etc.
- Output conventions: coordinates in OSGB 1936; data plotted at 10 km resolution for confidentiality; abundance and cover data standardized with defined scales.

## Weather, safety, and field logistics
- Safety considerations govern sampling feasibility; high-risk conditions prevent sampling.
- Team roles and task sequence are designed to optimize data quality and field efficiency.
- Transport and storage: samples managed with labeled containers, hazard documentation, and transit in secure storage boxes with appropriate labeling.

## Outputs and usage for GIS
- GIS-ready outputs include:
  - Spatial layers of pond locations, extents, and boundary delineations.
  - Boundary shading and overhang metrics (shade percentages).
  - Land-use composition in 0–5 m and 0–100 m buffers around ponds.
  - Temporal data (YEAR) and land classification (LC) overlays for change detection.
  - Biological quality indicators (PSYM, IBI) and percentage cover for macrophyte groups.
  - Photographs with geotagging markers for site re-visitation.
- Data products support map-based exploration and policy/research analyses, enabling identification of degraded ponds, priority areas for conservation, and relationships between land use, water chemistry, and aquatic communities.

## References and contact points
- Key references include Bunce et al. 2007 (ITE Land Classification), Howard 2002 (PSYM), O'Hare et al. 2013 (FIELD HANDBOOK Freshwater), and related CEH/GMEP reports.
- Project team contacts span GMEP leadership, data management, field teams, and lab analysis staff.