# The Land Cover Map of Great Britain: an automated classification of Landsat Thematic Mapper data

- Purpose and scope
  - Aims to demonstrate environmental condition in a consistent, monitorable format to support scrutiny of environmental health and policy performance over time.
  - Produced by an established monitoring program using standardized, repeatable methodologies.

- Data and methodology
  - Data source: Landsat Thematic Mapper (TM) imagery.
  - Classification approach: supervised maximum likelihood classification.
  - Image strategy: combining summer and winter data to boost accuracy over single-date analyses.
  - Resolution and coverage: 25 m grid; map records 25 cover types (sea/inland water, beaches/bare ground, developed/arable land, and 18 semi-natural vegetation types).
  - Outputs: available as a 25-class dataset (25 m) and a 1 km summary; a 17-key (A–Q) dataset provides a more generalized, consistently mappable subset.

- Spatial resolution and data alignment
  - Minimum mappable unit is effectively around 1 ha in practice; features as small as 1 ha are generally detectable, with finer patterns (roads, fields, shelter belts) visible down to about 0.125 ha (2 TM pixels).
  - Geometric registration to 1 km field maps shows average displacement around 20 m (0.8 TM pixels); most squares require no shift or only 1-pixel shift.

- Classification accuracy and uncertainty
  - Ground-truth data for accuracy assessment is imperfect; boundaries and definitions introduce artificial generalization.
  - Comparisons with independent 1 km ground references indicate varying accuracies due to differing class definitions (hydrological vs botanical), with overall field–satellite correspondence around 67% (85% of field classes matching satellite when accounting for definition differences); excluding boundary pixels improves to ~71%.
  - Including time-based changes (e.g., pasture ploughed between dates) raises correspondence to ~76% (or ~82% excluding boundaries).
  - A realistic overall accuracy estimate is in the 80–85% range, acknowledging regional and field-definition variations.
  - Observations stress the difficulty of exact ground truth and the impact of generalization and mixed boundary pixels.

- Land cover classes: structure and guidance
  - Two standard class schemes:
    - 25 target classes (25 m grid): primary outputs for broad user needs.
    - 17 key classes (A–Q): a generalized, nationally consistent subset (Countryside Information System standard).
  - The 25-class dataset is available at 25 m resolution and as a 1 km summary (percentage of each target class within a 1 km cell).
  - The 17-class dataset is available as 1 km summary data; non-standard/custom outputs can be provided.
  - Classes are aggregates of many subclasses (e.g., wheat/barley/oilseed rape are under arable); designed to be ecologically meaningful and consistently recognizable across Britain.
  - Minimum mapped unit ~1 ha (real-world mappable area often closer to 1 ha); some rare or poorly represented classes may be mapped inconsistently across regions.
  - Regional masks differentiate lowland and upland types to improve consistency; some classes may be combined or separated in GIS depending on objectives and data quality.

- 25-class vs 17-key class mapping
  - Table 1 provides the correspondence between the 17-key (A–Q) classes and the 25 target (1–25) classes.
  - Examples (illustrative):
    - Sea/Estuary, Inland Water, Beach/Mudflat/Cliffs, Saltmarsh, Grass Heath, Mown/Grazed Turf, Meadow/Verge, Ruderal Weed, Open Shrub Heath/Moor, Moorland, Bogs (Lowland/Upland), Deciduous/Coniferous Woodlands, Urban/Rural Development, Inland Bare Ground, etc.
  - Some classes (e.g., ruderal weeds) are not consistently mapped across all regions due to training data limitations; users may opt for the 17-class aggregation for consistency.

- Data formats and usage
  - 25-class dataset (25 m): each 25 m cell carries a value 0–25 corresponding to the target class.
  - 1 km summary (25-class): in each 1 km cell, 25 layers show the percentage of each target class present (e.g., 20% of type 10 in a 1 km cell).
  - 17-class dataset: provided as 1 km summary; intended for consistent national usage, with an option for non-standard, customized datasets.
  - The classification descriptions are designed to be usable in GIS and adaptable for tailor-made outputs, acknowledging that some users require different aggregations.

- Practical considerations and best practices
  - Acknowledges that spectral signatures may not perfectly separate all subclasses; some aggregation is intentional to maintain reliability across Britain.
  - Because of mixed boundary pixels and geographic variation, map users should be aware of potential local discrepancies beyond the average accuracy.
  - Change over time can affect interpretation; comparisons should account for time lags between imagery dates.
  - The dataset is designed to be stored, shared, and uploaded to appropriate data portals, aligning with aims to increase data value and accessibility for secondary users.

- Accessibility and references
  - The Land Cover Map of Great Britain and its accompanying class descriptions are intended to support broad use, including policy monitoring, environmental assessments, and GIS-based analyses.
  - Foundational references include Fuller et al. (1994a, 1994b) and Wyatt et al. (1994), with methodological discussions on accuracy and class definitions.