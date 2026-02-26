# The Land Cover Map of Great Britain: an automated classification of Landsat Thematic Mapper data

- Purpose and scope
  - Presents the Land Cover Map of Great Britain (LCMGB), produced by supervised maximum likelihood classification of Landsat TM data.
  - Provides a 25 m grid with 25 land cover classes (cover types) and links to results from other surveys.
  - Combines summer and winter imagery to improve accuracy; reports the share of data derived from combined vs single-date analyses.
  - Describes class definitions, map resolution, depiction, and relationships to other surveys; notes on potential tailored aggregations for users.

- Data, methods and classification approach
  - Uses automated, supervised classification of Landsat TM imagery to produce land cover maps.
  - Class definitions were developed to be ecologically meaningful, nationally consistent, and mappable at the 25 m resolution; subclasses (e.g., crop types) are aggregated into broader target classes for reliability.
  - Two hierarchical classification scheme:
    - 25 target cover-types (full detail)
    - 17 key cover-types (aggregated, more consistently mappable; standard in Countryside Information System)
  - A crosswalk table (Table 1) links the 25 target classes to the 17 key classes.
  - Output formats include:
    - 25 m resolution: one value per 25 m cell (0–25 target class)
    - 1 km summary: for each target class, the percentage area within the 1 km cell
    - 17-class dataset available as 1 km summary data; non-standard/custom aggregations possible

- Spatial resolution and registration
  - Base mapping at 25 m grid with 25 distinct target classes; minimum mappable unit effectively around 1 ha (2-pixel features observed in practice).
  - Spatial registration to 1 km field maps showed an average displacement of about 0.8 pixels (20 m); most squares required no shift, with a minority needing small adjustments.
  - Overall, the positional accuracy is considered acceptable for most applications; differences in geometry can occur for boundary features or during post-processing.

- Classification accuracy and validation
  - Accuracy assessment relies on ground-truth data, acknowledging that ground truth itself is not a single definitive standard.
  - Comparisons with independent ground reference data (508 1 km squares) showed variations largely due to differing class definitions and boundaries between surveys.
  - Major error components include misclassification of mixed boundary pixels (about 40% of pixels border vector boundaries); excluding boundary pixels raises correspondence to about 71%.
  - When accounting for potential time-based changes between surveys, overall correspondence improves (approx. 76% with boundaries included; 82% without boundaries).
  - A realistic overall accuracy is estimated around 80–85% when allowing for definitional differences and temporal change.
  - The report emphasizes that accuracy is regionally variable, and discrepancies can reflect different definitions, sampling, and time lags.

- Land cover classes (structure and examples)
  - 25 target classes organized to reflect major ecological and land-use types (e.g., Sea/Estuary, Inland Water, Beach/Mudflat/Cliffs, Saltmarsh, Grassland categories, Marsh/Rough Grass, Bracken, Moorland, Bogs, Shrub Heath, Woodlands, Tilled Land, Suburban/Rural Development, Urban Development, Inland Bare Ground, Unclassified).
  - 17 key classes provide a simplified, consistent national product (A–Q in the key scheme) with a one-to-one crosswalk to many of the 25 target classes.
  - Subclasses (e.g., wheat, barley, oilseed rape under Arable; various grassland types) are aggregated for consistency, though users can digitally recombine as needed for specific objectives.
  - Some rare or regionally inconsistent classes (e.g., ruderal weeds) were not uniformly mapped; a 17-class simplification is recommended for consistency across Britain.

- How to use and interpret the data
  - Two standard digital products:
    - 25-class, 25 m resolution: per-cell target class value (0–25)
    - 1 km summary: per 1 km cell, percentage coverage for each target class
  - An additional 17-class product (1 km summary) offers a more robust, consistent national dataset when some rare 25-class categories are problematic.
  - The dataset supports GIS-style analyses and can be customized or aggregated for specific monitoring objectives.
  - Acknowledges that some users may prefer different aggregations (e.g., combining all grasslands into a single category) and that such customizations are feasible digitally, albeit with potential loss of some detail.

- Practical considerations and limitations
  - Temporal dynamics: land cover changes between the imagery dates can affect comparability with other surveys or time points.
  - Boundary handling: mixed pixels at class boundaries contribute to classification errors; attention needed when using boundary-rich areas.
  - Regional variability: spectral similarity among some classes and regional differences (lowland vs. upland). Some classes may require regional masks or contextual information to improve accuracy.
  - Unclassified areas: about 2% of Great Britain remains unclassified in the 25 m data due to cloud cover, lack of cloud-free scenes, or unusual cover types; unclassified areas are labeled as 0 in the 25 m data.
  - Metadata and data governance: the approach emphasizes well-documented class definitions, explicit crosswalks between classification schemes, and transparent data products to support governance and reuse in monitoring frameworks; the process acknowledges challenges around data availability, standardization, and changes in classification definitions over time.

- Implications for environmental health monitoring and policy
  - Provides a standardized, nationwide land-cover baseline at high spatial resolution suitable for policy evaluation, land-use planning, habitat assessments, and environmental health indicators.
  - The dual-level (25-class and 17-class) framework supports both detailed analyses and stable, comparable summaries across regions and time.
  - Clear class definitions, methodological transparency, and crosswalks facilitate reproducibility, comparability with other datasets, and integration into broader monitoring frameworks.
  - Recognizes the need to align data collection and classification with metadata quality, data sharing considerations, and data governance standards—critical for open monitoring outputs and stakeholder trust.

- Data sources and references
  - Ground-truth considerations and accuracy assessments discussed, with references to Congalton (1991) and various Fuller et al. studies (1987–1995) detailing methodology, accuracy, and comparisons to field surveys.
  - The report situates the LCMGB within a broader context of remote-sensing-based ecological monitoring and cross-survey comparability.