# HEADWATERS

- Purpose and scope
  - National freshwater component of Countryside Survey 2007 (CS2007) conducted across GB, focusing on headwater streams in 425 CS2000 squares.
  - Re-surveys macroinvertebrate and aquatic plant communities, hydromorphology, water chemistry, and related environmental variables at headwater sites.
  - All 425 CS2000 squares revisited with a standardized 500 m stream reach for RHS (River Habitat Survey) and a 100 m aquatic-vegetation (MTR) survey; randomly selected 25% of ponds in CS2007 squares receive pond-specific surveys (physical, chemical, and macrophyte assessments).

- Key data products relevant to GIS
  - Spatial features and coordinates
    - CS square identifiers, GPS/NGR coordinates for sampling points (macroinvertebrate sampling points, RHS transversal points, pond survey locations).
    - RHS 500 m reach centered on macroinvertebrate sampling site; 100 m MTR macrophyte survey area centered on sampling location.
    - Photographs geotagged to sampling sites (macroinvertebrate area, RHS reach, MTR reach).
  - Data domains collected
    - Macroinvertebrate data (RIVPACS): site environmental data, sampling method, sample time, width, depth, velocity, substrate, bank vegetation, and photography records.
    - Hydromorphology and River Habitat Survey (RHS): detailed RHS indices via RAPID (3, 4-page entry with spot-checks, environmental attributes, bank/top vegetation, channel features, tree/shading, and overall habitat categories).
    - Water chemistry: field measurements (conductivity, pH) plus laboratory-filtered SRP, TON, alkalinity (with standardized bottle labeling and chain-of-custody).
    - Aquatic macrophytes (MTR): species presence/absence and percent cover for submerged, floating-leaved, and emergent plants over a 100 m reach; associated physical habitat data.
    - Pond condition: pond boundary mapping, area estimation, drawdown, turbidity, sediment and pond-base composition, pollution indicators, inflows/outflows, management, surrounding land use, amenity values, and pond macrophyte survey results.
  - Data capture tools and workflows
    - RAPID (River Habitat Survey field digital entry) for RHS data on a Tablet PC; in-field validation to ensure completeness.
    - IRIS (Aquatic plant survey field digital entry) for MTR plant data; in-field validation and sample handling guidance.
    - RIVPACS sample area forms for macroinvertebrate data capture; standardized environmental data fields.
  - Data quality and governance
    - On-site validation via RAPID/IRIS; “Check Data” validation sequence to identify missing or inconsistent fields.
    - Approx. 7% of headwater sites audited by CEH staff; regular team rotations to maintain sampling consistency.
    - Field survey checklists completed collaboratively to ensure all components (invertebrates, plants, RHS, water quality) are finished.
    - Rigorous sample labeling, transmittal, and transport protocols (TREM cards for fixatives; courier to CEH Dorset; monthly dispatch).

- Data collection framework and workflow (beginning, middle, end)
  - Pre-field and mapping
    - Pond mapping identified by mappers; survey ponds defined by outer boundary (winter water level) and area estimates; Pond Mapping Recording Sheet trackable.
  - Headwater (RHS) and macrophyte (MTR) surveys
    - 425 headwater squares re-surveyed with a 500 m sampling reach and 100 m plant survey length; 10 spot-checks (spot-checks 1, 6, and 10 require GPS coordinates) plus a central RHS 500 m reach.
    - Environmental variables and habitat data collected along the full sampling area; photographs taken to enable site relocation.
  - Sampling procedures and data capture
    - Macroinvertebrate sampling: three-minute pond-net kick-sweep plus mandatory manual search; careful handling to avoid over-collection and cross-contamination; field recording on RIVPACS forms.
    - Water chemistry: immediate field measurements (conductivity, pH); on-site filtration for SRP/TON/alkalinity; labeled sample tubes sent to CEH labs.
    - RHS data: Section A–Section P data entered in RAPID; validation checks performed on-site; 500 m RHS length-centered, survey valid even if full 500 m cannot be completed.
    - Macrophyte (MTR) survey: 100 m reach surveyed by wading; species identified in field with specimens sent to lab for confirmation; percentage cover estimated using standardized categories.
  - Pond condition surveying (CS2007)
    - Identify and map pond boundary, photograph, estimate pond area, drawdown height, and water presence; turbidity estimation; water chemistry sampling and measurements when feasible.
    - Environmental survey, macrophyte survey, and associated data recorded on pond-specific sheets; specimen handling and transport to Pond Conservation or CEH as appropriate.
  - Data consolidation and delivery
    - Data captured in field systems (RAPID, IRIS, RIVPACS forms); forms validated on-site; samples couriered to CEH Dorset; plant specimens posted to Pond Conservation.
    - Final data transported to central repositories with linked square/pond IDs to maintain traceability.

- GIS considerations and integration points
  - Spatial planning and relocation
    - Distinct sampling extents (500 m RHS reaches, 100 m MTR segments, 50 m plant survey reaches) require precise georeferencing and robust relocation markers (permanent landmarks, photographs with marker boards).
  - Multiresolution data integration
    - Overlay of macroinvertebrate, hydromorphology, plant community, and water-chemistry data with land-use and ecosystem context (surrounding land use, shading, channel morphology) for GIS analyses and visualization.
  - Data models and outputs
    - Structured data tied to square numbers and pond IDs, enabling per-square and per-pond GIS layers; site-level attributes allow spatial queries by reach length, habitat types (pool/run/riffle/slack), substrate composition, and bank vegetation.
  - Quality control and auditability
    - On-site validation, standardized field sheets, and data export workflows enhance GIS-ready data quality and reproducibility; field notes and photos support spatial verification and re-location.

- Practical considerations for GIS-enabled use
  - Data standardization
    - Consistent geospatial identifiers (CS square numbers, pond codes) and GPS/NGR coordinates linked to sampling points; standardized measurement scales for width, depth, velocity, substrate, and vegetation cover.
  - Temporal aspects
    - Sampling occurs within CS2007 field season with documented dates; site-level changes over time can be mapped and analyzed against RHS indices, RIVPACS outputs, and land-use changes.
  - Accessibility and documentation
    - Comprehensive field manuals and forms (RIVPACS Sample Area Form, RHS RAPID, MTR IRIS, pond condition sheets) provide structured metadata for GIS databases and downstream analytics.

- Endnotes and references (GIS relevance)
  - Data sources are anchored to CEH-led field manuals and the 2003 RHS framework; standardized forms and software (RAPID, IRIS) ensure consistent data capture and QA for GIS integration.
  - The approach supports map-based data products for policy, client, and public audiences, aligning with GIS specialists’ aims to create explorable, map-centric datasets that reflect headwater and pond conditions nationwide.