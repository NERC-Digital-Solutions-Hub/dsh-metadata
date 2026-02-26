# Management policies for invasive alien species: Addressing the impacts rather than the species.

- Overview
  - Aims to inform management policies by focusing on the impacts of invasive alien species (IAS) rather than the species themselves.
  - The study aggregates evidence on IAS control efficacy to understand how interventions affect IAS impacts.

- Methods and study selection
  - Literature search conducted in Web of Science for the term “invasive species control efficacy.”
  - Search window: 27 May 2020 to 10 July 2020; led by Pablo García-Díaz.
  - Initial results: 682 publications identified.
  - Exclusions: biofouling and ballast water studies (focused on preventing introduction rather than controlling established populations); laboratory-only experiments excluded.
  - Inclusions retained: aquarium, greenhouse, and mesocosm experiments as they can inform IAS impacts and control-outcome relationships.
  - Final screening: 373 publications deemed relevant for the topic.

- Dataset contents and structure
  - File: WOS-ControlSearchFinal.csv
    - A comma-separated-value file containing the results of the Web of Science search for “invasive species control efficacy.”
    - Each row represents one relevant study.
    - Columns and meaning:
      - Title: study title.
      - Authors: study authors.
      - Journal: journal of publication.
      - Year: year of publication.
      - Taxa: taxa targeted by the control intervention.
      - Type: control method.
      - Outcomes - not including non-target & side effects: YES/NO on whether the study evaluated outcomes addressing IAS impacts.
      - Outcomes - including non-target & side effects: YES/NO on whether the study evaluated effects on non-target species or other side effects.

- Implications for GIS and data visualization
  - The dataset provides rich metadata that can be used to create map-based visualizations, such as:
    - Geographic or jurisdictional distribution of studies (if location data are linked or added).
    - Spatial patterns by taxa groups or control methods.
    - Layers showing whether studies assessed impacts vs. only control efficacy, and whether non-target effects were considered.
  - Useful for transparency and quality assessment of evidence guiding policy, enabling researchers to map evidence gaps and data availability.

- Limitations and considerations
  - Based solely on Web of Science results within a specific time frame.
  - Excludes lab-only studies and certain types of interventions (biofouling, ballast water).
  - The dataset records whether outcomes were evaluated but does not itself provide spatial coordinates or detailed outcome metrics; may require augmentation for full GIS use.
  - Temporal coverage is limited to publications up to 2020 (as per the submission window).