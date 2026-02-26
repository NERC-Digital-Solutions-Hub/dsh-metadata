# Glastir Monitoring & Evaluation Programme FIELD HANDBOOK Freshwater, Version 2013.02

## Purpose and scope (for data stewardship)

- Documents nationwide pond surveys in Wales to support the Glastir Monitoring & Evaluation Programme (GMEP).
- Data aim: record pond and aquatic biodiversity and environment to assess ecological quality and inform management.
- Data are captured across multiple linked datasets (invertebrates, macrophytes, chemistry, environment) and stored centrally for analysis and reporting.

## Survey design and sampling framework

- Sampling units: 1 km survey squares distributed across strata; half of squares targeted at Glastir priority areas.
- Exclusion criteria: random squares with >75% urban land or >90% sea are excluded.
- Spatial referencing: squares identified with 10 km easting/northing coordinates and Land Classification (ITE) codes.
- Ponds identified within each square; random SURVEY POND selected for condition assessment when ponds exist.

## Pond definition and boundary treatment

- Pond: standing water 25 m² to 2 ha, typically holding water for at least four months/year (outer winter water level used for area).
- Boundary rules: outer boundary defined by winter water level; survey may extend outside square to capture full pond area.
- Age and boundary tracing: new ponds recorded (up to ~10 years); sketches and marker boards used to relocate sites.

## Data capture and electronic recording

- Field forms used on PC tablets:
  - Pond Checklist (water chemistry and macroinvertebrate survey)
  - Pond Attributes (pond characteristics, environment)
  - Pond Plants (macrophyte abundance and vegetation cover)
  - Pond Invertebrates (macroinvertebrate list and abundance)
- Required information on forms: square number, pond reference, survey date, location details, and all measurements.
- Data are entered electronically; all forms include pond location details to ensure correct site attribution.
- Photos: one or two photos per pond with a marker board including pond, square, and date.

## Field procedures and health & safety

- Roles: Surveyor A (water sampling and macroinvertebrates) and Surveyor B (photography and plant survey, attribute data entry).
- Water chemistry measurements at site: pH, conductivity, turbidity; field sampling of 50 ml filtered samples for SRP, TON, total alkalinity.
- Safety: assessment of hazards (access, water conditions, bedding, vegetation); high-risk conditions halt sampling.
- Sampling sequence and data capture flow are documented to ensure reproducibility and traceability.

## Sampling methods and components

- Habitat survey for macroinvertebrates: identify main habitats, divide 3-minute net sampling equally among habitats, plus 1-minute visual search.
- Macroinvertebrate sampling: standard 25 cm² net (900 µm mesh); avoid excessive sediment; record amphibians and fish encountered; preserve samples in formalin and label with site info; transport in dedicated pots with proper sealing.
- Macrophyte (macrophyte) survey: walk and wade within outer boundary; identify all wetland plants to species when possible; record abundance using categories (dominant, abundant, frequent, occasional, rare); estimate total cover by submerged, floating, and emergent groups; record shade from overhanging vegetation; photograph and record boundary features; rare species flagged for confirmation and potentially require licenced verification.
- Macrophyte data handling: two-part data entry forms; standard nomenclature; some specimens may be sent for verification; guidance for collecting problematic taxa (e.g., Callitriche, Potamogeton, Ranunculus, Charophytes) and for rare species confirmation.

## Laboratory analyses and data products

- Chemistry analyses conducted at UK Centre for Ecology & Hydrology (Lancaster) using accredited methods:
  - Phosphate (PO4-P) by colorimetric method
  - Total dissolved nitrogen (TDN) and total nitrogen (TN)
  - Alkalinity via automated titration
- Biological quality assessment via PSYM (Predictive System for Multimetrics) to derive an overall pond quality score by comparing observed metrics to an undegraded reference state.
- Quality assurance aligned with DEFRA Joint Codes of Practice (JCoPR) for robust, auditable science.
- Data structures (tables) used for storage and sharing:
  - GMEP_POND_INVERTS_2013_16.csv: pond invertebrate species lists and counts
  - GMEP_POND_MACROPHYTES_2013_16.csv: macrophyte species and category within pond boundary
  - GMEP_POND_MACROPHYTES_SUMMARY_2013_16.csv: cover percentages, shade, IBI/PSYM, and survey adequacy
  - GMEP_POND_ENV_SURVEY_2013_16.csv: pond environmental attributes
  - GMEP_POND_CHEMISTRY_2013_16.csv: headwater chemical determinands and values
- Data units and identifiers are standardized; -9999 denotes missing data.

## Data governance, quality assurance, and interoperability

- Data are governed by PSYM methodology (Howard, 2002) and integrated into a single ecological quality metric.
- QA follows JCoPR standards for science and process quality; procedures are auditable and repeatable.
- Data traceability: explicit linkage of square, pond, date, and unique IDs; photos and sketches accompany each pond entry to support site relocation and verification.
- Data sharing and stewardship considerations:
  - Centralized storage with clear metadata (square ID, pond ID, coordinates, year, LC code)
  - Clear naming conventions and field definitions to enable cross-study comparability
  - Documentation of sampling limitations (e.g., incomplete access, areas not surveyed) in the data records
- Potential data interoperability challenges:
  - Heterogeneous field formats and occasional non-interoperable units or categories
  - Handling missing or partial survey data due to safety or access constraints

## Practical implications for data stewards

- Ensure consistent use of identifiers (SQ_ID, pond reference) across all tables and forms.
- Maintain rigorous provenance: laboratory results linked to their corresponding field samples with complete metadata (date, site, determinand, units).
- Enforce standardized units and categories (e.g., abundance scales, PSYM/IBI classifications, land-use categories).
- Preserve specimen handling records for rare or difficult taxa; support workflows for verification while minimizing disturbance to rare species.
- Implement QA checks to verify completeness of pond checklists, plant/animal lists, and water chemistry records before submission.
- Track data lineage from field collection to laboratory analysis and final ecological quality assessment; ensure traceability for audits and reporting.

## References and collaborators

- Primary sources and supporting teams include O’Hare et al. (2013) field handbook, PSYM manual (Howard, 2002), and Glastir Monitoring & Evaluation Programme reports (Emmett et al., 2013–2017).
- Data and field teams are led by GMEP and Freshwater Habitats Trust personnel; UKCEH laboratories handle chemical analyses.