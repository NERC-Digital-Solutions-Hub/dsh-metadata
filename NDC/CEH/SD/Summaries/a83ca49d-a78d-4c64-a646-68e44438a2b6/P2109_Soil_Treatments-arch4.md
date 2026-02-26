# Background

## Overview
- The NERC Soil Biodiversity Thematic Programme (established 1999) focused on intensive study of a large field experiment at Sourhope, Scottish Borders, to understand soil biota diversity and the functional roles of soil organisms in ecological processes.
- 24 research projects investigated soil structure, processes (e.g., carbon and nitrogen cycles), micro- and macro-fauna, and their ecological roles.

## Dataset Details
- Data set: P2109_VIEW_SOIL_TREATMENTS.csv, covering soil plot treatments from 1999–2001 with additional data for 2001–2004.
- Purpose: Data can be used with other experimental datasets from Sourhope as explanatory variables.
- Key columns: TREATMENT_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT_TYPE, DOSAGE.
- Primary reference: Scott et al., 2003 (SOURHOPE FIELD DATA HANDBOOK 2003). Supporting information accessible via EIDC catalogue record.

## Treatments: Site and Plot Level
- Site-level treatment: vegetation cutting schedules across years 1999–2002 with multiple cuts per year and notes on mower downtime.
- Plot-level treatments (six types):
  1. Control 1 – No treatment
  2. Control 2 – No treatment
  3. Nitrogen – NH4NO3 fertilizer; annual rate 24 g m-2 (total 5.76 kg plot-1; 240 kg ha-1); two yearly applications
  4. Lime – CaCO3; annual rate 600 g m-2 (144 kg plot-1; 6000 kg ha-1); one dose per year
  5. Nitrogen and Lime – combination of Nitrogen and Lime as above
  6. Insecticide – Dursban 4 OPA; 0.15 ml m-2 per application; repeated after mowing across specified years
- Insecticide applications occurred several times per year (exact dates listed per year in the dataset).

## Data Governance, Quality, and Access
- Data subject to quality assurance procedures, but NERC cannot warrant accuracy or fitness for a particular use; no liability for outcomes from use of these data.
- Data are provided for user access with caveats on reliability; documentation includes a detailed treatment handbook and supporting information via the EIDC catalogue.

## Data Management Implications for Data Leaders
- Demonstrates a structured data asset with explicit experimental design (site vs. plot-level treatments) and rich metadata (plot and cell identifiers, treatment timing, dosage).
- Highlights the importance of:
  - Clear data lineage and provenance (links to Scott et al., 2003 and the SOURHOPE FIELD DATA HANDBOOK).
  - Metadata quality (descriptions for each field like BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT_TYPE, DOSAGE).
  - Discoverability and interoperability (CSV format, cross-referencing with other datasets as explanatory variables).
  - Governance considerations and explicit disclaimers about data accuracy and liability.
- Indicates potential data gaps (periods with mower downtime; explicit notes in site-level treatment dates) that affect analyses and require careful handling.
- Useful as a case study for coordinating data across long-term field experiments and integrating data into broader data ecosystems or networks of practice.