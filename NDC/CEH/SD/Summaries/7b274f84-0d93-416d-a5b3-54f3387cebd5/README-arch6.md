# Data from: García-Díaz, P., et al. Management policies for invasive alien species: Addressing the impacts rather than the species. BioScience.

## Overview
- Freely available dataset from a literature review focused on the efficacy of invasive species control methods and their broader impacts.
- Emphasizes addressing the impacts of control rather than the identity of the species.
- Source: García-Díaz et al., BioScience, 2020.

## Methods: data collection and screening
- Data derived from Web of Science search for the keyword phrase “invasive species control efficacy.”
- Retrieval window: 27 May 2020 – 10 July 2020.
- Initial yield: 682 publications identified.
- Exclusions: biofouling and ballast water (focused on preventing new IAS releases rather than controlling established populations); laboratory-only experiments excluded; aquarium, greenhouse, and mesocosm studies retained due to relevance for IAS impacts and control-outcome relationships.
- Final set: 373 publications deemed relevant to the topic.
- Curation: Pablo García-Díaz gathered data on title, authors, journal, year, taxa investigated, type of control method, and whether the paper evaluated outcomes.

## Data contents
- File: WOS-ControlSearchFinal.csv (CSV) containing one row per relevant study.
- Columns include:
  - Title
  - Authors
  - Journal
  - Year
  - Taxa (taxa targeted by the control intervention)
  - Type (control method)
  - Outcomes - not including non-target & side effects (YES/NO): whether the study evaluated the outcomes of the control intervention in terms IAS impacts
  - Outcomes - including non-target & side effects (YES/NO): whether the study evaluated non-target and other side effects
- The file includes explanations of each column.

## How this data supports data work
- Enables cross-study comparisons of control efficacy by method and targeted taxa.
- Supports synthesis and potential meta-analyses focused on the impacts of control interventions.
- Provides explicit indicators of whether outcomes were evaluated and whether non-target effects were considered, aiding assessment of evidence strength.

## Potential data products and reuse
- Dashboards or pivot-table style summaries to explore:
  - Efficacy by control type
  - Taxa targeted
  - Publication year trends
  - Proportions of studies reporting outcomes and non-target effects
- Integration with other data sources to inform policy evaluation and ecological impact assessments.

## Limitations and notes
- Based on Web of Science results and the defined inclusion/exclusion criteria.
- Excludes preventive measures for new invasions (biofouling, ballast water) and laboratory-only studies.
- Included context is applied, aquarium/greenhouse/mesocosm studies may bias toward certain experimental settings.