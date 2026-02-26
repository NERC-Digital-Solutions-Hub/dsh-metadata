# Explanatory Information: Species codes

- Purpose and scope
  - Provides mapping and crosswalks for ECN species codes to other taxonomic references (e.g., BRC concepts) and Latin names.
  - Enables interoperability across datasets by linking ECN codes to alternative taxonomic representations.

- Structure and content
  - Contains numerous rows translating ECN species codes (e.g., 1148, 2717, 1151, etc.) to multiple accepted names or concepts.
  - Each mapping often includes alternate names or synonyms (e.g., Rumex obtusifolius linked to Rumex sanguineus, or various Vas_ codes linked to taxon concepts).
  - Some entries map a single ECN code to multiple taxonomic concepts or to varietal/subspecies distinctions, reflecting nuanced taxonomic treatment.

- Examples of mappings
  - 1148, Rumex obtusifolius = Rumex sanguineus; 1148, Vas_1748 = Vas_1753
  - 2717, Rumex obtusifolius = Rumex seedling/sp.; 2717, Vas_1748 = Vas_4557
  - 1151, Rumex obtusifolius = Ruscus aculeatus; 1151, Vas_1748 = Vas_1760
  - 2271, Rumex obtusifolius = Saccogyna viticulosa; 2271, Vas_1748 = Bry_918
  - 1160, Rumex obtusifolius = Sagina subulata; 1160, Vas_1748 = Vas_1769
  - 3131, Rumex obtusifolius = Salix purpurea; 3131, Vas_1748 = Vas_1801
  - 1179, Rumex obtusifolius = Salix repens agg.; 1179, Vas_1748 = Vas_1802
  - 2634, Sorbus aucuparia (c) = Sorbus aucuparia (g); 2634, Vas_1960 = Vas_1960

- Governance and usage implications for Data Stewards
  - Maintain authoritative, canonical mappings and clearly document crosswalks between ECN codes, BRC concepts, and Latin names.
  - Apply consistent naming conventions in internal datasets while preserving crosswalks for interoperability.
  - Ensure the ECN_VF2/ECN_VF3 context supports these mappings (e.g., species presence data encoded with VEG_SPEC).
  - Track versioning of taxonomic mappings to support reproducibility over time.

- Practical application
  - Used to interpret and translate species codes embedded in dataset fields, enabling downstream analyses to align with external taxonomic references.

- Related documentation
  - Crosswalks and mappings are part of the ECN data documentation ecosystem, complemented by supporting CSV files and taxonomic references.

---

## Explanatory Information: Quality Codes

- Purpose
  - Defines a comprehensive set of quality indicators used to annotate field and laboratory observations within the ECN data.

- Coverage and organization
  - Field and sampling related codes (roughly 100–199 range) cover information gaps, sampling issues, environmental conditions, and non-standard events during data collection.
  - Codes addressing situational and management events (e.g., grazing, woodland management, construction, weather, fire) and operational notes.
  - Codes in the 200s address adverse conditions affecting sampling (weather, insects, light, flow, etc.) and data handling anomalies.
  - Codes in the 300–499 range include additional field/lab-specific notes (e.g., non-standard sampling date/time, data editing, sample preservation issues).
  - Codes 501–513 pertain to laboratory-related issues (e.g., no sample, sample lost, contamination, measurement constraints).
  - 999 is used for Unusual event, with accompanying quality text.

- Examples of category emphases
  - Field conditions and events: crop spraying, construction work, grazing, burning, pathways, road/track disturbance, rolling of survey areas, etc.
  - Environmental and sampling disruptions: weather extremes, water/ice conditions, snow, flood events, planting or management activities near the sampling site.
  - Data integrity and handling: partial loss, discarded samples, contaminated samples, measurement limitations, and non-standard sampling times/dates.
  - Taxonomic confidence and lab flags: levels of confidence in taxon identification (high/medium/low) and lab-specific data handling notes.

- Supporting notes
  - Quality notes for non-standard or unusual events are linked to non-standard quality notes via ECN_VF_qtext.csv, enabling richer documentation beyond the numeric code.
  - These quality codes are designed to support traceability, reproducibility, and data quality assessment within datasets comprising field observations, environmental measurements, and laboratory analyses.

- Implications for Data Stewards
  - Implement validation checks to ensure quality codes are applied consistently and aligned with the accompanying descriptive text.
  - Maintain and align the quality code taxonomy with the associated textual explanations to preserve interpretability.
  - Ensure provenance by linking quality codes to qtext entries where applicable, supporting transparent data quality reporting.
  - Use these codes to inform data cleaning, imputation, and uncertainty characterization in analyses.
  - Version control changes to quality codes and their descriptions to track updates over time.

- Example usage in practice
  - A record with a field observation may be annotated with codes describing sampling disruptions (e.g., 101 No sample taken; 201 Failing light; 202 Biting insects) and lab-related flags (e.g., 501 No sample in the lab; 513 Calculated value issues), enabling downstream metadata-driven filtering and quality-aware analyses.