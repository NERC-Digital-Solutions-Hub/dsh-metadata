# ECN Data Centre dataset description

- The ECN dataset uses extensive explanatory information to support cross-site comparability and interpretation of environmental data, including detailed species and quality coding.

## Explanatory Information: Species codes

- Provides large cross-referenced mappings between coded species and scientific names, including numerous synonyms, subspecies, and alternate nomenclature.
- Uses VESPAN/BRC coding for plant species with comprehensive cross-references to support interpretation and analyses.
- Example patterns show multiple-to-one mappings (e.g., Rumex obtusifolius linked to various Rumex names; Scapania degenii linked to several Scapania names), illustrating the depth and breadth of taxonomic linkage.
- The species code system is designed to enable accurate identification and comparability of species presence/absence data across sites and years.

## Explanatory Information: Quality Codes

- Defines a wide range of data quality codes, primarily numeric (e.g., 100, 101, 102, … 999), describing issues affecting data integrity.
- Categories cover:
  - Field and sampling issues: no information available, sample lost, partial loss, weather or environmental conditions affecting sampling, non-standard sampling times, grazing disturbances, etc.
  - In-field operational notes: equipment problems, sample handling abnormalities, plot relocation or disturbance events.
  - Laboratory-related issues: no sample in laboratory, partial loss, contamination, measurement limitations, and related QC concerns.
- Some codes denote specific contextual events (e.g., 121 Change of land use in vicinity; 135 Disturbance in plot; 141 Grazing by animals; 200+ Adverse conditions affecting sampling).
- 999 is used for unusual events; these require further explanation via the accompanying quality text.
- Quality codes are linked to qualitative explanations stored in ECN_VF_qtext.csv, providing detailed descriptions for each code.

## Analytical implications for Analysts

- When using ECN data, consult the quality metadata (ECN_VF_qtext.csv) to assess data reliability and choose appropriate filters or weights.
- Ensure correct interpretation of species data by referencing the comprehensive VESPAN/BRC cross-references; account for taxonomic updates and synonyms when aggregating species.
- For data integration across sites/years, align datasets using the standardized SITECODE/SYEAR/plot-level and cell-level encodings and reflect any quality-related caveats indicated by the quality codes.
- Acknowledgement of provenance and adherence to ECN data-use guidelines (including citation and sharing reprints) remain important.