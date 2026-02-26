# Otter Liver Tissue Dataset Metadata

## Overview
- Metadata/schema for a dataset linking otter carcass findings to liver tissue chemical analyses.
- Includes unique identifiers from multiple projects (CEH Ref from Predatory Bird Monitoring Scheme; UWC Ref from Cardiff University Otter Project), temporal and spatial data, biological attributes, and a comprehensive panel of liver element concentrations.

## Core fields and data standards
- Identifiers:
  - CEH Ref: Unique numeric identifier (Predatory Bird Monitoring Scheme)
  - UWC Ref: Unique numeric identifier (Cardiff University Otter Project)
- Temporal data:
  - Month Found
  - Year Found
- Location data:
  - County (England or Wales)
  - X-coordinate
  - Y-coordinate
- Biological data:
  - Sex (Female or Male)
  - AgeClass (Juvenile, Sub-adult, Adult)
  - Condition coefficient (K): Calculated as per Kruuk and Conroy (1991)
- Sample/analysis details:
  - % Dry matter: Determined by drying a 0.5 g liver subsample at 70°C for 48 hours
- Chemical analyses (all on dry weight, mg/kg):
  - Al, Mn, Fe, Co, Ni, Cu, Zn, Se, Sr, Mo, Cd, Sb, Pb, Hg, Cr, As, V, Ag
- Data quality indicators:
  - ND = Non detected
  - NA = Not analysed
- Data handling and sharing notes:
  - Data may be documented with the work performed on each dataset
  - Availability and limitations (disclosure risks, embargoes, proprietary issues) should be identified

## Data quality and processing
- Quality assurance, cleaning, and transformation of datasets prior to sharing
- Ensure consistency in metadata and units across all records
- Maintain traceability to the original data sources and calculation methods (e.g., K coefficient method)

## Data access, sharing, and governance
- Datasets are uploaded to relevant portals and catalogued within data holdings
- Clear documentation of work done on datasets to aid reuse
- Manage sharing limitations and update mechanisms to ensure current data remain discoverable and usable
- Consider data provenance and cross-referencing between CEH Ref and UWC Ref identifiers

## Challenges relevant to Data Stewards
- Incomplete understanding of user needs and priorities
- Timeliness of data delivery from data creators
- Achieving consistent data standards and complete metadata from contributors
- Interoperability across multiple systems and diverse file formats
- Handling large datasets and transfer difficulties
- Dealing with legacy or outdated databases requiring bespoke, non-interoperable solutions