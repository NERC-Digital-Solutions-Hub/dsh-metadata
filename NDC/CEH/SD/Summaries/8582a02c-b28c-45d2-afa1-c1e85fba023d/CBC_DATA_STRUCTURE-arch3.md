# ECN Common Birds Census (CBC) Data Documentation

## Overview
- Documentation for ECN bird monitoring data focused on the Common Birds Census (CBC) methodology.
- Data are collected to understand environmental change impacts on bird populations and to inform policy and future monitoring decisions.
- ECN Data Centre manages dataset origin, with support from a consortium of UK government departments and agencies.

## Provenance and governance
- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (CEH) — http://data.ecn.ac.uk; ecn@ceh.ac.uk.
- Dataset Owners: UK government departments and agencies (e.g., Defra, Natural England, Environment Agency, Scottish Government, Welsh Government, Northern Ireland Environment Agency, NERC, etc.) contributing to site monitoring and network coordination.
- Acknowledgement and use: Users are asked to acknowledge ECN data usage and to send one reprint of any publication citing the ECN data.
- Protocols: ECN maintains standard operating procedures to ensure cross-site comparability; see accompanying bc.pdf for data collection explanations.
- Quality and governance: Data must be quality assured, cleaned, transformed, analyzed, and presented clearly; data sharing and governance processes are emphasized.

## Protocol and methodology
- Primary method: Common Birds Census (CBC) methodology; observations include bird detections by sight or sound during a series of visits across a defined plot in the breeding season; data are aggregated to estimate the number of territories (CLUST) and, for some species, nests (NEST).
- Scope and limitations: CBC is designed for national-scale surveys; site-based data have limited capacity to resolve precise relationships between population levels and environmental change. Users are advised to combine ECN data with broader monitoring data (e.g., BTO programs) to mitigate limitations.
- Historic and programmatic changes: CBC was the standard at lowland ECN sites until 1999, after which the Breeding Bird Survey (BBS) became dominant; some sites continued CBC for comparison. Pre-ECN data exist for certain sites (e.g., Wytham). Data date ranges vary by site.

## Data structure and fields
- Data download fields:
  - SITECODE: Unique ECN site code.
  - SYEAR: Sampling year.
  - BI_SPEC: Bird species code.
  - CLUST: Number of territories (clusters) found.
  - NEST: Number of nests (where applicable).
- Supporting documentation: ECN_cbc_qtext.csv (issues affecting data; includes SITECODE, SYEAR, BI_SPEC, DESCRIPTION).
- Explanatory information for interpretation accompanies site and species mappings.

## Site codes and site details
- Explanatory Information: Site codes map to specific ECN sites, with names, coordinates, and British Trust for Ornithology (BTO) land-use class (e.g., Farmland, Woodland, Special). Examples:
  - T01: Drayton (Farmland)
  - T03: Hillsborough (Woodland)
  - T05: North Wyke (Woodland)
  - T06: Rothamsted (Farmland)
  - T08: Wytham (Woodland)
  - T09: Alice Holt (Woodland)
  - T10: Porton Down (Special)
- Additional site information and broader ECN site details are available via the ECN catalogue.

## Bird species codes and mappings
- Extensive mapping of species codes to full names (e.g., BU for BLUE TIT, AV for AVOCET, BC for BLACKCAP, CC for CHIFFCHAFF, etc.).
- The dataset includes a wide range of species codes to support detailed biodiversity analyses and cross-site comparability.

## Usage guidance and limitations
- Suitability for monitoring: Data are useful for national-scale assessments but may require integration with broader datasets (e.g., BTO) for robust environmental-change linkage analyses.
- Metadata and data quality: Emphasis on using accompanying quality information; metadata completeness is essential for assessing data fit for purpose.
- Data governance: Encourages data sharing of underlying datasets where appropriate; stresses the need for data cleaning, transformation, and transparent reporting.

## Access, citation, and references
- Acknowledgement: Users should acknowledge ECN data usage; request for one reprint of publications citing the data.
- Related resources: Links to ECN site information and cross-referenced publications (e.g., Rennie et al., 2017) that document ECN bird data for 1995–2015.
- Supporting files and documentation: Includes ECN_cbc_qtext.csv for issue descriptions and reference to the bc.pdf protocol document.