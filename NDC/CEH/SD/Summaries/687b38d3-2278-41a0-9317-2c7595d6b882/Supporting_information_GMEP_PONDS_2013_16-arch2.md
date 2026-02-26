# Glastir Monitoring & Evaluation Programme FIELD HANDBOOK Freshwater

- Purpose: Provide a standardized, data-driven framework to monitor pond ecosystems in Wales, enabling assessment of environmental health and policy performance over time.
- Audience: Field teams and analysts responsible for data collection, quality assurance, and integration into monitoring databases.

## Sampling design and survey scope

- Survey framework: 1 km squares across Wales stratified by Land Classification; sampling effort allocated proportionally to stratum size, with half of squares targeted at Glastir priority areas.
- Exclusions: Squares with >75% urban land or >90% sea are excluded.
- Pond sampling within squares: Randomly selected survey pond per square (SURVEY POND) for condition assessment; pond identification and location details gathered from mappers.
- Data capture: Field data entered via tablet forms; datasets stored in central portals.

## Pond selection and boundary concepts

- Pond definition (Axis II): standing water from 25 m² to 2 ha, usually water for at least four months/year.
- Boundary treatment: Outer pond boundary defined by the upper winter water level; pond surveys include boundaries outside the square when necessary.
- Boundary identification cues: shifts from aquatic to terrestrial vegetation, water marks, willow root bundles, slope breaks, or outflow levels.

## Field workflow and forms

- Preliminary steps: Field mappers identify all ponds in a square; select SURVEY POND; surveyors receive location details.
- Main forms used on tablet:
  - Pond checklist: water chemistry and macroinvertebrate survey details.
  - Pond attributes: pond characteristics and environmental information.
  - Pond plant survey: macrophyte abundance and vegetation cover.
- Photos: One or two images per pond with a marker board (Pond survey reference) for future relocation.

## Habitat and survey planning

- Habitat mapping: Identify main pond habitats (e.g., sedges, submerged, emergent, inflows) to guide sampling.
- Macrophyte and macroinvertebrate focus: Ensure comprehensive representation by sampling multiple habitats (avg 5–10 per pond; larger ponds may have more).

## Water chemistry and field measurements

- Measurements at each pond: Conductivity, pH (field); SRP, TON, alkalinity (filtered samples).
- Sampling protocol: Collect water from a representative area not disturbed by sediment; avoid inflows for sampling.
- Equipment: Hanna Combi pH/EC meter; 1 L bottles for chemistry; 50 mL bottles for SRP/TON/alkalinity with on-site filtration.
- Data handling: Label samples with project, square, pond, date; store in padded envelopes; record turbidity category (clear to turbid) and all readings on Pond Checklist.

## Pond attributes and mapping

- Data capture: Pond area, boundary, surrounding features, inflows/outflows, and sampling transects.
- Sketching and measurement: Draw pond outline on waterproof paper, include scale, north arrow, and identifiers (Project, Axis II, Waterbody type, Square, Pond, Date).
- Documentation: Photograph pond with marker board; record boundary and notable features along the perimeter.

## Macrophyte (wetland plant) survey

- Aims: Record all wetland plant species within the outer boundary; estimate total cover by submerged, floating-leaved, and emergent categories; record shade from overhanging vegetation.
- Identification: Field identification to species level where possible; use identification keys; collect specimens for difficult taxa (e.g., Callitriche, Potamogeton, Ranunculus) with care to minimize impact.
- Rare species: Mark with asterisk; confirm rare species with care; sometimes digital photographs used for confirmation.
- Specimen handling: Pressed or preserved (pickle) specimens; label with pond and square details; return specimens to Freshwater Habitats Trust.
- Data entry: Enter species and abundance into macrophyte forms; three abundance scales: D 91–100%, A 51–90%, F 21–50%, O 6–20%, R 0–5%.
- Data outputs: Total aquatic vegetation percent cover; separate metrics for submerged, floating-leaved, emergent; pond overhang and margin shade.

## Macrophyte data management and references

- Data structure: Two sheets for plant data; taxonomy aligned to standard flora references; table includes species, category, abundance, and geographic coding (E/N coordinates, year, LC).
- Abundance and cover: Input total cover percentages by group; calculate percentage cover per category and overall macrophyte coverage.
- PSYM/IBI considerations: PSYM assessment for ecological quality (Howard 2002) linked to macrophyte metrics; IBI-like indices (IBI, PSYM) supported by PSYM software.

## Macroinvertebrate survey

- Aim: Build a thorough species list within the limited 3-minute netting window plus 1 minute of visual search.
- Habitat sampling: Sample all main pond habitats (approx. 5–10 per pond); habitats chosen based on vegetation structure and substrate.
- Sampling method: 25 cm² pond net with 900 µm mesh; time is divided equally among habitats; kick-sampling for shallow or sheltered areas; avoid deep sediment piles.
- Additional search: An extra 1 minute of searching on surface, under rocks/logs to catch missed species.
- Specimen handling: Preserve samples in 40% formalin (approx. 50–100 mL per bag) and label; store in 1.3 L pots; label both inside and outside containers; transport with TREM-labeled boxes.
- Safety and ethics: Return aquatic fauna encountered to pond when possible; note presence of fish or amphibians during sampling.

## Data handling and field logistics

- Transit and storage: Macroinvertebrate samples stored in labeled containers; transport in secure boxes; field emergency and transport information documented (TREM).
- Field checklist: Ensure Pond checklist, pond attributes, macrophyte survey, and macroinvertebrate surveys are complete; documents stored and linked to site.
- Training and QA: Field teams use standardized procedures; QA guided by DEFRA Joint Codes of Practice (JCoPR) for quality and reproducibility.

## Laboratory protocols and analytical methods

- Water chemistry analysis (lab): PO4-P measured colorimetrically; TDN and TN measured with chemiluminescence; alkalinity determined via automatic titration with standard reagents.
- Analytical facilities: UK Centre for Ecology and Hydrology (UKCEH) Lancaster; accredited methods.
- PSYM and biological quality: PSYM used to derive a single ecological quality score from metrics derived from plant and invertebrate surveys; used alongside environmental data for overall assessment.

## Data structure and output formats

- Primary data tables:
  - GMEP_POND_INVERTS_2013_16.csv: pond invertebrate species lists with counts by square/year.
  - GMEP_POND_MACROPHYTES_2013_16.csv: macrophyte species within pond boundary; abundance and category.
  - GMEP_POND_MACROPHYTES_SUMMARY_2013_16.csv: aggregate metrics (e.g., aquatic vegetation Cover %, submerged/ floating-leaved/emergent species, shade, PSYM, IBI).
  - GMEP_POND_ENV_SURVEY_2013_16.csv: environmental attributes (field variables, descriptions, and values).
  - GMEP_POND_CHEMISTRY_2013_16.csv: pond water chemistry (SAMPLE_DATE, determinations, units, LC, coordinates).
- Data modeling: Datasets are designed to be compatible with central monitoring portals; PSYM outputs are used to classify ecological quality.
- Confidence and traceability: Detailed labeling (square, pond, date) and sample metadata enable traceability and correct attribution of records.

## Quality assurance and standards

- QA framework: DEFRA Joint Codes of Practice (JCoPR) followed for scientific quality and reproducibility.
- Data standards: Consistent field methods, standardized data forms, and uniform coding for units, coordinates, and classifications.
- Documentation and references: Field handbook and supporting literature cited; data products linked to established monitoring programs (GMEP, PSYM, ITE Land Classification).

## Challenges and opportunities for analysts

- Value enhancement: Integrate pond data with broader environmental datasets to avoid “single use” datasets and improve interpretability for policy analysis.
- Data accessibility: Ensure underlying data (raw survey forms, specimen records, and lab results) are accessible to researchers and stakeholders for validation and secondary analyses.