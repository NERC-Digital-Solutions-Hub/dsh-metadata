# Glastir Monitoring & Evaluation Programme FIELD HANDBOOK Freshwater , Version 2013.02

- Purpose and scope
  - Field handbook for identifying environmental health measures to scrutinise policy, evaluate outcomes, and inform future decisions within the Glastir Monitoring & Evaluation Programme (GMEP).
  - Uses standardized field, laboratory, and data-management procedures to generate comparable indicators of pond condition and ecological quality.

- Sampling design and survey frame
  - Survey squares are stratified within the Land Classification framework; sampling effort is allocated proportionally by stratum size, with half of randomly selected squares additionally targeted at Glastir priority areas.
  - Exclusions: squares with more than 75% urban land or more than 90% sea are excluded.
  - Pond sampling: within each square containing ponds, one pond is randomly selected as the ‘survey pond’; pond surveys proceed only after this selection is made.

- Pond definitions and boundary concepts
  - A pond is defined as 25 m2 to 2 ha, usually holding water for at least four months per year.
  - Outer boundary is the winter maximum water level; survey may include areas outside the square boundary for boundary assessment.
  - Boundary identification relies on changes in vegetation, physical features, and water level indicators; drawdown and permanence are recorded.

- Field data collection and forms
  - Primary data collection forms: Pond Checklist, Pond Attributes, Pond Plants, and Pond Macroinvertebrate Survey.
  - Data entry via PC tablets; each form requires square number, pond number, and survey date at the top.
  - Data elements include water chemistry (field measurements), nutrient and alkalinity analyses (Filtration protocol), pond attributes, macrophyte details, and macroinvertebrate data.
  - Photographs: one or two photos per pond; include a marker board with pond and square identifiers to aid relocation.

- Health and safety and field workflow
  - Two-person teams (Surveyor A and Surveyor B) per pond; roles include sampling water chemistry, photographing, recording attributes, collecting macroinvertebrate samples, and conducting plant surveys.
  - Safety considerations cover access, weather, substrate stability, aquatic vegetation hazards, and high-risk conditions; stop sampling if risk thresholds are exceeded.
  - Sequence of tasks emphasizes securing pond location details, measuring water chemistry before disturbance, collecting macroinvertebrate and plant data, and dispatching samples.

- Habitat survey and macrophyte survey (plants)
  - Macrophyte aims: record all wetland plant species within the pond boundary, estimate abundance, measure total cover for submerged, floating-leaved, and emergent categories, and assess shade.
  - Identification and sampling: walk/wade to survey accessible areas; use grapnel for deeper areas; rare species flagged for verification; specimens may be collected or photographed for confirmation.
  - Specimen handling: field-pressing, preserving, and, where necessary, sending samples to Freshwater Habitats Trust for verification; detailed guidance on pressing, preservation in alcohol, and labeling.
  - Data handling: abundance coded using D/A/F/O/R categories; plant names organized alphabetically within submerged, floating-leaved, and emergent groups; two-part data sheets for comprehensive entry.

- Macroinvertebrate survey
  - Aims: achieve a comprehensive species list across pond habitats within a 3-minute net sampling (plus 1 minute of search).
  - Habitat selection: sample main pond habitats (e.g., Carex stands, shallows, inflows, submerged vegetation, marginal grasses, etc.); allocate time proportionally to habitat count and area.
  - Sampling protocol: use standard 25 cm2 net with 900 µm mesh; vigorous netting with brief kick-sampling of soft substrates; avoid disturbing deep soft sediments; identify and record amphibians and fish encountered.
  - Additional search: perform a 1-minute extra search for surface, beneath rocks/logs to add species.
  - Sample preservation and transport: field-preserved in 4% formalin; labeled in triplicate containers; use robust transit packaging; maintain chain-of-custody and avoid cross-contamination.

- Data handling, laboratory analyses, and QA
  - Water samples sent to UK Centre for Ecology and Hydrology (UKCEH) Lancaster for chemical analyses; methods include colorimetric phosphate determination, TDN/TN, and alkalinity via automated titration.
  - PSYM methodology to compute pond biological quality (Howard 2002): combines plant and invertebrate metrics with environmental data to yield an overall quality status and diagnose degradation drivers.
  - Quality assurance follows DEFRA Joint Codes of Practice (JCoPR) to ensure robust, repeatable, auditable results.
  - Data structures: standardized CSV tables for invertebrates, macrophytes (presence and abundance), macrophyte summary (cover and shade metrics), environmental survey attributes, and chemistry data, each with site identifiers, coordinates, year, and land-class classifications.

- Biological quality and interpretation
  - PSYM outputs a single index of integrity; higher scores indicate closer to an undegraded state. Metrics can be examined individually to diagnose issues such as eutrophication or metal contamination.
  - IBI-like components include an Index of Biotic Integrity (IBI) for pond ecosystems and PSYM-based categorical assessments (good, moderate, poor, very poor).

- Data structure and variable definitions (examples)
  - Invertebrates: GMEP_POND_INVERTS_2013_16.csv with square ID, year, taxon name, and count.
  - Macrophytes: GMEP_POND_MACROPHYTES_2013_16.csv with square ID, species, category, abundance; plus GMEP_POND_MACROPHYTES_SUMMARY_2013_16.csv with cover percentages and shade metrics.
  - Environment: GMEP_POND_ENV_SURVEY_2013_16.csv capturing pond environmental attributes (variable name and value) across coordinates and year.
  - Chemistry: GMEP_POND_CHEMISTRY_2013_16.csv listing site type, sample date, determinand, value, units, and notes.
  - All datasets include location identifiers (SQ_ID), 10 km coordinates (EASTING/NORTHING_10km), and Land Classification (LC).

- References, authors, and governance
  - Field handbook draws on O'Hare et al. 2013; PSYM methodology (Howard 2002); Glastir monitoring reports (Emmett et al. 2014, 2017); and relevant flora/fauna references.
  - Data and project teams include GMEP leadership, Freshwater Habitats Trust, and cross-disciplinary field teams; QA and informatics management roles described.

- Specific challenges for monitoring-framework authors (alignment with archetype)
  - Data gaps and access: integrating comprehensive field data with robust metadata across time.
  - Silos and data sharing: ensuring underlying data are shared appropriately for governance and reuse.
  - Metadata quality and data transformation: maintaining clear documentation and transformation rules for consistent analysis.
  - Communicating complex findings: translating PSYM and habitat metrics into actionable policy insights.
  - Data governance: establishing open data standards, storage, versioning, and transparency.

- Key takeaways for monitoring-framework authors
  - A rigorous, transparently documented framework combining field surveys, laboratory analyses, and a standardized ecological-quality metric (PSYM) supports policy scrutiny and decision-making.
  - Structured data capture (tablet forms, predefined fields) and thorough QA (DEFRA JCoPR) enhance data reliability and comparability.
  - Clear delineation of pond boundaries, survey methods, and habitat sampling ensures reproducibility and diagnostic capability for degradation drivers.