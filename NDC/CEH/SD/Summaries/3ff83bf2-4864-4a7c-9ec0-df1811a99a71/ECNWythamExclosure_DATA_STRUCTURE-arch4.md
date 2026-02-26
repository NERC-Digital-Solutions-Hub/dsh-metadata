# Explanatory Information: Species codes

## Overview of species code mappings

- The document provides detailed crosswalks between ECN (Environmental Change Network) species codes and multiple taxonomic concepts, including Latin names and common names.
- Each ECN code (e.g., 1209, 1210, 1220, etc.) is linked to one or more scientific names and, in some cases, alternative taxon concepts or synonyms.
- Cross-references extend to wider taxonomy systems (e.g., BRC concepts), facilitating interoperability across datasets and networks.
- The mappings illustrate the complexity of taxonomic identification in long-term environmental datasets, where a single code may correspond to several related taxa or naming conventions.
- The high level goal is to support data discovery, consistent interpretation, and integration of multi-site vegetation data by standardizing taxon references and providing clear crosswalks.

## Implications for data governance and interoperability

- Rich, explicit taxon crosswalks enable reliable data reuse and cross-dataset analyses by ensuring consistent taxon identification across partners.
- The presence of standardised codes, cross-referenced taxonomic concepts, and common naming schemas supports data harmonization within an enterprise data strategy.
- Documented mappings aid analysts in reconciling historical and current taxonomic references, reducing ambiguity during data ingestion and analysis.
- The structure exemplifies best practices for data stewardship: maintain stable codes, provide crosswalks, and connect taxonomy to broader references.

## Explanatory Information: Quality Codes

- The quality codes provide structured metadata about data quality and the conditions under which data were collected or processed.
- Categories include:
  - 100-series: No information available or data lost.
  - 101–105, 107–118, 121–123, 125–139, 141–151, 160–177, 179–187, 188–196, 200–209, 210–236, 237–238: Various field/collection issues and environmental disturbances (e.g., equipment issues, sample loss, snow in samples, insects, disturbance, flooding, mowing, etc.).
  - 126–127: River/lake conditions affecting sampling (frozen or dry).
  - 128–135, 136–147: Operational and site conditions affecting sample collection (fauna in traps, condensation, relocation accuracy, disturbances, management activities, etc.).
  - 239–241: Taxon identification confidence levels (e.g., medium or low confidence in taxon identification).
  - 501–507: Laboratory processing issues (e.g., no sample, sample lost, contamination, insufficient material).
  - 999: Unusual event (flagged for special handling and requires accompanying quality text).
- The codes are designed to be used with descriptive metadata (e.g., FROM_DATE, TO_DATE, DATETYPE, DESCRIPTION) to explain the context of the issue.
- The system supports nuanced data quality filtering, error tracing, and robust documentation for data consumers.

## Practical takeaways for data leaders

- Ensure taxon codes are paired with clear, cross-referenced taxonomic mappings to support interoperability across datasets and organizations.
- Maintain comprehensive quality metadata for each observation, enabling users to filter data by collection conditions, processing status, and confidence in identifications.
- Use the 999 code to flag unusual events or anomalies and provide detailed explanatory text to facilitate correct interpretation.
- Leverage the taxonomy crosswalks (e.g., ECN codes linked to BRC concepts) to support cross-network analyses and data harmonization initiatives.
- Document data provenance and quality considerations alongside the dataset to demonstrate data value, readiness for reuse, and justification for ongoing investments in the data program.