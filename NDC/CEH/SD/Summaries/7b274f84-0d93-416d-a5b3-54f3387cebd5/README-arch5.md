# Data from: García-Díaz, P., et al. Management policies for invasive alien species: Addressing the impacts rather than the species. BioScience.

## Overview
- This is a literature review on the efficacy of invasive species control, conducted using a Web of Science search for "invasive species control efficacy."
- Timeframe and process: searches and screening occurred between 27 May 2020 and 10 July 2020, led by Pablo García-Díaz.
- Initial yield and filtering: 682 publications identified; exclusions applied to biofouling and ballast water (focus on preventing new IAS rather than controlling established populations) and laboratory-only experiments; aquarium, greenhouse, and mesocosm studies retained as they can inform IAS impacts and control-outcome relationships.
- Final curation: 373 publications deemed relevant to the topic and subjected to title, authors, journal, year, taxa, control type, and outcome data extraction.

## Data products and structure
- Data file: WOS-ControlSearchFinal.csv (CSV) containing the Web of Science search results that were screened by PG-D between 27/05/2020 and 10/07/2020.
- Each row represents one relevant study.
- Columns and their meanings:
  - Title: title of the study
  - Authors: authors of the study
  - Journal: journal of publication
  - Year: publication year
  - Taxa: taxa targeted by the control intervention
  - Type: control method
  - Outcomes - not including non-target & side effects: YES/NO for whether the study evaluated outcomes addressing IAS impacts
  - Outcomes - including non-target & side effects: YES/NO for whether the study evaluated non-target effects and other side effects

## Data provenance and availability
- The data are freely available.
- The extraction and organization were conducted by a single researcher (Pablo García-Díaz) with explicit inclusion/exclusion criteria and a defined screening workflow.
- Contact information for the corresponding author is provided for data inquiries.

## How this supports data stewardship
- Demonstrates the importance of structured metadata for literature datasets used in policy-relevant reviews (title, authors, journal, year, taxa, control type, outcome measures).
- Illustrates a reproducible data collection workflow: explicit search terms, screening criteria, and documentation of inclusion decisions.
- Highlights the need to record both efficacy outcomes and potential non-target/side effects to enable comprehensive downstream analyses.

## Limitations and challenges (relevant to data governance)
- Exclusion criteria limit scope to certain study types (e.g., ballast water, biofouling, and laboratory-only studies), which may bias conclusions about control efficacy.
- Single-curator data extraction may affect consistency; provenance and versioning are important for reproducibility.
- The dataset captures whether outcomes were evaluated but does not itself synthesize results; users must interpret heterogeneous study designs and metrics.

## Appendix: Data fields in WOS-ControlSearchFinal.csv
- Title
- Authors
- Journal
- Year
- Taxa
- Type
- Outcomes - not including non-target & side effects (YES/NO)
- Outcomes - including non-target & side effects (YES/NO)