# Dataset Originator

- ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview

- The UK Environmental Change Network (ECN) dataset is hosted by the ECN Data Centre and is part of a broader program sponsored by UK government departments and agencies to understand environmental change.
- Dataset focuses on bat transect surveys conducted across ECN sites, using bat detectors to map bat activity and behavior.

## Dataset Ownership and Sponsorship

- Dataset Owners: The ECN programme is funded by a consortium of UK government departments and agencies (e.g., Defra, Natural England, Environment Agency, Scottish/ Welsh governments, NERC councils, etc.).
- Usage acknowledgment: ECN asks users to acknowledge data usage and to send one reprint of any publication citing the data.

## Protocol and Data Quality

- ECN provides standard operating procedures to ensure cross-site comparability (reference to accompanying ba.pdf for data collection details).
- Methodology: bat detection, transect walks four times per year (specific four three-week periods); surveys not conducted in heavy rain or strong winds.
- Limitations: methodology limits precise inference about relationships between bat populations and environmental change; mitigated by linking ECN data to other monitoring programs.
- Quality: users should rely on accompanying quality information when using the data.

## Data Model and Access

- Data Download structure includes:
  - SITECODE: unique ECN site code
  - SDATE: sampling date
  - TRANSECT: transect identifier
  - BATLOC_ID: bat location (unique per survey date)
  - FIELDNAME: variable measured (species codes)
  - VALUE: measured value
  - ACTS: bat seen
  - ACTH: bat heard
  - ACTF: bat feeding buzz heard
- Contact for data access or questions: ecn@ceh.ac.uk

## Supporting Documentation

- ECN_BA2.csv: details about how the survey was conducted (e.g., detector type, frequency settings, and QA steps).
- ECN_BA3.csv: habitat observed on transects (habitat codes).
- ECN_BA_qtext.csv: site managers’ quality text describing circumstances affecting data quality.
- Additional explanatory information is available in the ECN site and habitat code references.

## Site and Species Explanatory Information

- Explanatory Information – Site Codes
  - T01 to T11 with site names (e.g., Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, etc.) and their geographic coordinates.
  - A link to a broader ECN site catalogue is provided for more details.
- Explanatory Information – Species Codes
  - Abbreviations mapped to Latin and common names (e.g., Pp = Pipistrellus pipistrellus, Bb = Barbastella barbastellus, Nn = Nyctalus noctula, etc.), including “XX” for No bats found and “UU” for Unidentified bat.
- Explanatory Information – Habitat Codes and Habitat Types
  - Habitat Codes HAB1, HAB2, HAB3 used to record habitat context near sighting locations.
  - Habitat Types 1–43 with detailed descriptions (e.g., hedgerows, treelines, stone walls, water features, various woodland types, grasslands at multiple intensities, arable land, built areas, quarries, bare soil, etc.).

## Practical Considerations for Data Leaders

- The dataset embodies a structured data pipeline with clearly defined fields, site metadata, species codes, and habitat context, enabling reproducible analyses and cross-site comparisons.
- Key governance points: multi-organization sponsorship, explicit data usage acknowledgments, and requests for publications reprints to demonstrate dataset value.
- Data discoverability and interoperability are supported by standardized protocols, extensive metadata (site, species, habitat codes), and accompanying documentation (BA2, BA3, qtext).
- Potential integration opportunities: link ECN bat data with other ECN environmental datasets to study species-environment relationships, while leveraging the quality notes to assess suitability for specific analyses.
- Users should account for methodological limitations when interpreting population-environment relationships and utilize quality information to filter or weight data appropriately.