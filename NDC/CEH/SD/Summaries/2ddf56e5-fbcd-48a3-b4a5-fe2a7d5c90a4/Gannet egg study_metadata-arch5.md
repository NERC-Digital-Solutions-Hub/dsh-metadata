# Predatory Bird Monitoring Scheme – Egg Contaminant Data

## Overview
- Data generated as part of the Predatory Bird Monitoring Scheme (PBMS) for long-term temporal trend analysis.
- Contains contaminant measurements in homogenised egg contents from various seabird colonies; includes shell thickness indicator and multiple pollutants.
- Reports and deeper analyses are downloadable from the PBMS website.

## Data Content and Structure
- Key identifiers: Ref (unique alpha-numeric egg ID), Year (collection year), Site (colony location) with mapped coordinates.
- Sites covered: Ailsa Craig, Bass Rock, St Kilda, Grassholm, Scar Rocks, Hermness, Little Skellig (Ireland), Great Saltee (Ireland) with respective coordinates.
- Shell and contaminant metrics:
  - SHELL_INDEX: indication of eggshell thickness (unit: mg/mm, NA if not analysed).
  - SHELL_INDEX notes: ND (None Detected) or NA (Not Applicable) where appropriate.
  - HEOD, DDE, Hg: concentrations in homogenised egg contents (various units; Hg reported as dried weight; other units as specified per analyte).
  - PCBs: total PCB concentration and numerous congeners (e.g., PCB008, PCB018, PCB029, PCB031, PCB052, PCB077, PCB101, PCB105, PCB114, PCB118, PCB123, PCB126, PCB128, PCB138, PCB149, PCB153, PCB156, PCB157, PCB167, PCB169, PCB170, PCB180, PCB189, PCB194, PCB199, PCB201, PCB205, PCB206, among others).
  - Each analyte includes statuses: ND (None Detected) or NA (Not Analysed) where applicable; CAS Numbers and Units provided for many constituents.
- Data completeness: Multiple ND/NA entries indicate partial analyses across congeners; some fields include coordinates for precise site locations.

## Provenance and Access
- Source: Predatory Bird Monitoring Scheme.
- Usage: Long-term temporal trend analyses; related reports accessible via PBMS results page (http://pbms.ceh.ac.uk/results.htm).

## Data Quality, Standards, and Documentation
- Metadata scope includes Ref, Description, Year, Site (with coordinates), Shell Index, specific contaminants, units, and CAS Numbers where available.
- Observations for data governance:
  - Some analyses are not performed (NA) or not detected (ND), requiring clear documentation and handling in analyses.
  - Units may vary by analyte; ensure consistent unit harmonisation across datasets for comparability.
  - Site naming and coordinate data should be standardised and kept up to date.
- Documentation considerations for Data Stewards:
  - Maintain clear provenance and versioning of datasets.
  - Document data processing steps (e.g., quality assurance, transformation, handling of ND/NA values).

## Availability, Sharing, and Updates
- Datasets are intended for sharing within PBMS and related portals; updating procedures should ensure timely ingestion of new years/sites.
- Consider publishing summaries and trend reports alongside raw data to improve discoverability and usability.

## Key Challenges and Governance Considerations
- Incomplete understanding of user needs and priorities for specific contaminants or site prioritisation.
- Timeliness of data receipt from data creators and collaborators.
- Ensuring data creators meet metadata and standardisation requirements (including metadata for analytes, units, and CAS numbers).
- Interoperability across many systems and formats; handling large, multi-site datasets.
- Integration with outdated or bespoke databases requiring non-interoperable solutions.
- Embargoes or disclosure risks for sensitive site information; need clear policies for data availability.

## Actions for Data Stewards
- Enforce and document metadata standards: consistent fields for year, site, coordinates, analyte names, units, ND/NA status, and CAS numbers.
- Implement data ingestion pipelines that handle ND/NA consistently and flag gaps or anomalies.
- Ensure data is uploaded to and discoverable via relevant PBMS portals and catalogues; maintain versioning and provenance notes.
- Maintain stakeholder communication to clarify user needs and publish usable datasets with accompanying trend analyses when possible.
- Establish update workflows to keep datasets current and to track any embargoed or restricted information.