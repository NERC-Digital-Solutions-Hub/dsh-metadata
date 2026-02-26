# Supporting Document for 'A systematic review of common measurement methods of global soil protease activity between 1970-2020' dataset

## Overview
- This document accompanies a systematic review of soil protease activity measurement methods (1970–2020) and describes the dataset collected for meta-analysis.
- Proteases are key in soil nitrogen cycling; understanding global measurement methods and enabling cross-study comparisons require standardized protocols and rich metadata.
- The work aims to identify variance in soil protease activity and the methods used to measure it, informing standardization and future monitoring.

## Methodology and Scope
- Systematic review conducted in March 2020.
- Primary data sources: Web of Science; secondary search in ScienceDirect for specific assay substrates.
- Inclusion criteria focused on studies measuring soil protease activity; 680 studies met criteria (PRISMA diagram in Fig. S1).
- Data export criteria defined a priori; data extracted to support meta-analysis.

## Dataset Structure and Content
- Dataset comprises two raw data files: Fluorimetric_methods.csv and Colorimetric_methods.csv (same structure, separated by measurement type).
- Variables are described in Table S6; cells marked 'not stated' indicate missing information in the source study.
- Core data fields include:
  - Identification: ID, author, date, title, DOI.
  - Location and soil context: soil_type (FAO/WRB classifications), location, altitude, mean annual temperature (MAT), mean annual precipitation (MAP), soil_depth, pH (mean and_sd), ph_reps.
  - Soil properties: soil organic carbon (SOC) content and units, clay content and related reps.
  - Protease measurements: protease_mean, protease_sd, protease_reps, protease_unit, protease_method details, description.
  - Methodology details: substrate used (e.g., casein, gelatin, p-nitroanilide, etc.), substrate_conc, assay_buffer and its concentration, assay_ph, assay_time, assay_temp, termination method, wavelength (for fluorimetric methods; excitation/emission values).
  - Metadata about source: method_cited, citation details.
- Dataset layout notes:
  - Two files reflect different assay modalities (fluorimetric vs. colorimetric) but share a consistent variable structure.
  - All data are raw extractions from individual studies.

## Metadata and Data Quality
- Variables include detailed environmental metadata (climate, soil properties, depth) to facilitate robust cross-study comparisons.
- Data are pulled directly from studies and annotated with units; where not reported, fields are left as missing or marked not stated.
- Table S3 specifies selection criteria (e.g., protease activity measured in soil, consideration of assay condition effects) and exclusions (e.g., unobtainable studies, lack of controls).
- Table S4 defines data export criteria for meta-analysis.
- Figure S1 provides the PRISMA diagram documenting study identification and screening.

## Data Governance, Sharing, and Usability
- The dataset emphasizes transparency and traceability, enabling replication and further synthesis.
- Sharing underlying data is highlighted as essential for openness, although barriers can exist (e.g., metadata completeness, standardization, data governance requirements).
- The dataset’s rich metadata supports governance decisions about data stewardship, provenance, and interoperability across monitoring programs.

## Implications for Monitoring Frameworks
- Highlights the need for standardized measurement protocols to enable valid comparisons of soil protease activity across regions and time.
- Demonstrates the value of comprehensive metadata schemas (soil type, climate, depth, pH, SOC, texture) for environmental health monitoring.
- Provides a model for how to structure monitoring datasets to support meta-analyses and evidence-based decision-making.
- Underlines practical governance considerations:
  - Mandating complete metadata capture for all measurements.
  - Aligning soil classifications (e.g., FAO, WRB) and units across datasets.
  - Ensuring data provenance, versioning, and accessible data sharing to reduce silos.

## Challenges and Considerations for Practice
- Heterogeneity in methods (fluorimetric vs. colorimetric; substrates; assay conditions) can obscure comparability.
- Incomplete metadata and missing data fields impede cross-study synthesis.
- Data transformation and standardization efforts are often required to render disparate datasets usable.
- Barriers to data sharing (e.g., privacy, governance constraints) can affect the availability of underlying data.

## Practical Takeaways for Policy and Monitoring Authors
- When designing monitoring frameworks, adopt standardized assay protocols and substrate choices where feasible.
- Implement a minimum, well-defined metadata set for all measurements, including soil type, climate, depth, pH, SOC, and key assay parameters (substrate, concentration, buffer, pH, time, temperature).
- Use consistent soil classifications and clearly report units and measurement methods.
- Encourage open data practices, provide data dictionaries, and document data provenance to facilitate meta-analyses and cross-program comparability.
- Plan for data governance that supports data sharing while maintaining quality assurance, data cleaning, and clear documentation.

## References and Supporting Elements
- Supporting materials include Table S1–S6, supplementary PRISMA figure (Fig. S1), and dataset descriptions (Tables S2–S6).
- Annexed references include standard soil manuals and soil resource classifications (e.g., Booker Tropical Soil Manual, FAO World Reference Base).