# Explanatory Information: Species codes

- Purpose for monitoring-framework authors
  - Establishes a standardized approach to species coding and taxonomy mapping to enable cross-site comparability, interoperability, and robust data governance.
  - Provides guidance on interpreting coded species data within long-term environmental monitoring datasets.

- Key components
  - Comprehensive mapping between ECN-coded species and:
    - Latin (scientific) names
    - Cross-references to Biological Records Centre (BRC) concepts
    - VESPAN coding system and synonyms
  - Extensive crosswalks to aid analysts in linking ECN codes to accepted taxonomic concepts and broader taxonomy (e.g., multiple Latin names, synonyms, and higher-ridelity concepts).
  - Explicit documentation of coding evolution and synonymy to support retrospective analyses and data harmonization.

- Practical implications for framework design
  - Include a centralized species-code crosswalk (ECN_VF2, ECN_VF3) and a crosswalk to BRC concepts to support consistent species interpretation across years and sites.
  - Preserve provenance information for each code, including origin, site ownership, and acknowledgment requirements when data are reused.
  - Provide usage notes detailing how to apply species codes in analyses, with attention to synonyms and cross-references.

- Data governance considerations
  - Encourage clear documentation of taxonomic decisions, updates to coding schemes, and any reclassifications to maintain transparency and reproducibility.
  - Emphasize open data practices while protecting metadata completeness and the integrity of code mappings.

# Explanatory Information: Quality Codes

- Purpose for monitoring-framework authors
  - Defines a standardized set of quality flags to accompany field and laboratory observations, facilitating transparent assessment of data reliability.

- Key components
  - Numeric quality codes with descriptive text (examples)
    - 100: No information available - data lost
    - 101–119: Various reasons for missing or compromised data (no sample, equipment issues, debris, contamination, etc.)
    - 120–135: Contextual problems affecting data (weather, land-use changes, obstructions, sampling disturbances)
    - 140–149, 150–159: Procedural or environmental disturbances (grazing, management actions, sampling interference)
    - 160–169, 170–179: Equipment or sampling-site issues (pitfall traps, pumps, hydrological conditions)
    - 200–235: Adverse conditions and recording issues (insects, light, flow, etc.)
    - 501–507: Laboratory-related limitations (no sample, loss, contamination, insufficient material)
    - 508–513: Laboratory/measurement-related constraints and data-calculation caveats
    - 999: Unusual event – see the quality text
  - These codes cover field, lab, and environmental factors that can compromise data quality or interpretation.

- Practical implications for framework design
  - Incorporate a formal quality-coding scheme with clear definitions and a mapping to data-likelihood or reliability levels.
  - Attach quality codes to observations to enable downstream users to filter, weight, or impute data appropriately.
  - Provide a corresponding “quality text” or explanatory notes (qtext) to capture nuanced reasons behind quality flags.

- Data governance considerations
  - Ensure that quality codes are consistently applied across sites and years, with documented guidance for auditors and data managers.
  - Link quality codes to metadata fields and provenance to support traceability of data quality issues.

# Practical guidance for authors of Monitoring Frameworks

- Use standardized taxonomic coding and crosswalks
  - Adopt established mappings (e.g., ECN_VF2, ECN_VF3) and crosswalks to BRC concepts to enable cross-dataset analyses.
  - Preserve synonyms and taxonomic updates to support longitudinal analyses.

- Embed robust metadata and provenance
  - Document origins of all codes, site ownership, and usage requirements; require acknowledgment when data are reused.
  - Provide usage notes detailing interpretation of codes and any caveats related to taxonomy or quality.

- Integrate clear data-quality governance
  - Implement a formal quality-code schema with explicit definitions and a mechanism for attaching quality flags to observations.
  - Include a textual quality context (qtext) where needed to supplement numeric codes.

- Facilitate data sharing and replication
  - Align with open data principles while maintaining rigorous metadata completeness and traceability of coding schemes.
  - Encourage publication of accompanying documentation that explains code mappings, quality flags, and their impact on analyses.

# Endnotes

- The materials support cross-site data integration by providing detailed species-code mappings, taxonomy crosswalks, and a comprehensive quality-codes framework suitable for long-term environmental monitoring datasets.