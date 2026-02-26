# ECN Data Centre Vegetation Protocol and Metadata

- The Explanatory Information sections provide essential data dictionaries for the ECN vegetation dataset, focusing on:
  - Taxonomic and nomenclature mappings (species codes and aliases)
  - Data quality and metadata governance (quality codes and their interpretation)

## Explanatory Information: Species codes

- Purpose
  - Document cross-references between ECN species codes and alternative taxonomic names and synonyms.
  - Link ECN codes to other coding schemes (e.g., BRC, Vas_ identifiers) to support consistent species identification across datasets and sites.
- Key characteristics
  - Extensive mappings show that a single ECN code may be associated with multiple taxonomic names or synonyms (e.g., 2254 for Riccardia chamedryfolia linked to several names such as Riccardia multifida, Riccia sp., Rinodina interpolata, etc.).
  - Includes a mix of vascular plants, mosses, liverworts, lichens, and other life-forms, with many entries listing Latin names alongside common references or taxonomic aggregates (e.g., Rubus fruticosus agg., Rosa canina agg., Sorbus spp.).
  - Cross-references also appear to map to site-level identifiers and to broader taxonomic concepts (e.g., Rosa spp., Rubus spp., Viola spp.).
- Practical implications
  - Authors and data users must navigate multiple aliases to ensure consistent species identification over time and across sites.
  - The crosswalk supports data integration, reanalysis, and interoperability, but requires clear metadata and documented mappings to avoid misinterpretation.

## Explanatory Information: Quality Codes

- Purpose
  - Define a standardized set of data quality indicators used to annotate observational, field, hydrological, laboratory, and metadata issues.
- Key categories and examples
  - No information/lost data or samples (e.g., codes indicating data or samples are unavailable or lost).
  - Sampling/access problems (equipment out of action, unable to visit site, poor sample retention, partial sample loss).
  - Environmental and site disturbances (snow, insects, weather, flooding, construction, land-use change, mowing, grazing, windthrow, trampling).
  - Instrumentation and procedural issues (funnel/sampler problems, tube or clip issues, calibration, sample preservation problems).
  - Data processing and laboratory issues (data edited, unvalidated data, contamination, insufficient sample for measurement, equipment failure).
  - Hydrological and ecological context (non-standard sampling times, river/pond conditions, lake levels, water flow).
  - Confidence in taxon identification (taxonomy confidence levels: high, medium, low).
  - Unusual event (code 999) with accompanying quality text for detailed explanation.
- Practical implications
  - These codes enable rigorous data quality assessment and transparent data provenance.
  - The presence of a dedicated quality-text linkage (e.g., 999 indicating unusual events) highlights the need for supplementary metadata to interpret complex issues.
  - Ensures monitoring framework authors can communicate limitations and data caveats alongside results.

## Implications for Monitoring Framework Authors

- Metadata and provenance
  - The extensive species code mappings and quality codes underscore the importance of robust metadata to enable correct interpretation, data integration, and reuse.
- Taxonomy governance
  - Ongoing management of taxonomic aliases is crucial to maintain consistency over time and across sites; clear crosswalks are essential.
- Data quality governance
  - Quality codes should be coupled with accessible quality text to explain unusual circumstances, enabling transparent reporting and risk-aware decision-making.
- Data access and sharing
  - Given the complexity of mappings and the breadth of quality codes, comprehensive documentation and governance are necessary to reduce barriers to data access and proper reuse.
- Practical recommendations
  - Maintain and update crosswalk tables linking ECN codes to taxonomic synonyms and external coding schemes.
  - Ensure quality codes are always accompanied by human-readable explanations (quality text) and, where possible, linked to specific records or timepoints.
  - Incorporate these dictionaries into dashboards and reporting tools to promote clear communication of data limitations and data provenance.