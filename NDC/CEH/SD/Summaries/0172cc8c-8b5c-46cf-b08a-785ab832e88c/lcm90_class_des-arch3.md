# The Land Cover Map of Great Britain (LCMGB)

- An extract describing the Land Cover Map of Great Britain (LCMGB), produced in 1995 from supervised maximum likelihood classifications of Landsat Thematic Mapper data.
- Coverage: 25 m grid; 25 target land cover types plus an unclassified category; data also available as a 1 km summary; a secondary 17 “key” class aggregation (A–Q) provides a more consistent national product.
- Purpose for monitoring: provides standardized land cover measures to scrutinize and inform environmental health policy, with outputs suitable for dashboards, reports, and GIS analyses.

## Data, Methods and Resolution

- Data source: Landsat TM imagery; combination of summer and winter images improves classification accuracy (88% of Britain from combined data; 12% from single-date data; cloud-free coverage 0.4% on both dates; offshore islands 0.1%).
- Spatial resolution: 25 m grid for the full 25-class dataset; 1 km summary data available (per 1 km cell, the percentage of each class is shown).
- Classification approach: supervised maximum likelihood classification; accuracy checks rely on ground-truth data; acknowledges inherent subjectivity in class definitions and generalization.
- Registration: Landsat-derived rasters aligned to 1 km field maps; average positional shift about 20 m (0.8 pixels); most squares required no shift or only minor adjustments.

## Classification Scheme and Outputs

- 25 target classes: a detailed, ecologically meaningful set derived from a synthesis of field knowledge and other surveys.
- 17 key classes: a simplified aggregation (A–Q) to improve consistency across regions where rare classes are inconsistently mapped; Table 1 maps the 17 key classes to the 25 target classes.
- Outputs and formats:
  - 25-class dataset (standard): 25 m resolution; each cell labeled 0–25, where 0 = Unclassified.
  - 1 km summary data: for each target class, a layer showing the percentage of that class within each 1 km cell (e.g., 1,600 25-m cells per 1 km cell; 320 cells of a given class yield 20% in that layer).
  - 17-class dataset: available as 1 km summary data; can be produced as customized outputs if needed.
- Class descriptions cover broad categories (e.g., Sea/Estuary, Inland Water, Coastal Bare Ground, Saltmarsh, Pasture/Meadow/Amenity Grass, Mown/Grazed Turf, Meadow/Verge/Semi-natural, Ruderal Weed, Bracken, Moorland Grass, Dense Shrub Heath, Deciduous Woodland, Coniferous Woodland, Tilled Land, Urban/Suburban Development, Inland Bare Ground, etc.) and note regional differences (lowland vs. upland), spectral separability, and management effects on appearance.

## Accuracy, Uncertainty and Validation

- General accuracy: realistic assessment around 80–85% when accounting for definition differences and temporal change; exact ground truth is seldom available, and “truth” is gradient rather than discrete.
- Factors influencing accuracy:
  - Boundary pixels: up to ~40% of pixels lie on or near class boundaries; excluding boundaries raises correspondence to ~71%.
  - Mixed pixels and geometry: misclassification vs. misregistration can be difficult to disentangle in dissected landscapes.
  - Temporal changes: data from different dates may reflect actual land-cover changes (e.g., pasture ploughed later).
  - Definition differences: hydrological vs. botanical definitions of certain vegetation (e.g., bogs) cause mismatches between reference surveys.
- Validation findings:
  - Ground reference comparisons across 508 1 km squares show varying correspondence depending on detail level and class definitions.
  - When allowing for different definitions and a time lag, correspondence suggests an overall realistic accuracy around 80–85%.

## Data Availability, Formats and Use

- Standard products:
  - 25-class dataset at 25 m resolution (0–25 target classes; 0 = Unclassified).
  - 1 km summary data (per target class, percentage within each 1 km cell).
- Optional/custom outputs:
  - Customized data can be provided as a subset of the 25 classes or aggregated into the 17 key classes.
- Practical use notes:
  - The 25-class dataset is comprehensive but may be overly detailed for some national-scale monitoring; the 17-class aggregation offers more consistent national mapping.
  - Minimum mappable area: effectively around 1 ha; practice may show smaller features (2-pixel areas) in some cases.
  - Regional generalization: regional upland vs. lowland masks are used to generalize classifications; local GIS context (altitude, climate, latitude/longitude) can improve regional separation.

## Implications for Policy Monitoring and Governance

- Provides a reproducible baseline and monitoring framework for land-cover change analyses across Great Britain.
- Enables policy evaluation of land use, habitat distribution, and ecosystem extent over large scales and long periods.
- Requires careful interpretation due to classification uncertainties, boundary effects, and regional variations; users should consider aggregation levels (25 vs 17 classes) and temporal alignment when measuring change.
- Metadata and data governance considerations:
  - Awareness that some rare classes are inconsistently mapped; aggregation to 17 key classes may be preferable for national consistency.
  - Ground-truth quality and definitions are variable; users should document chosen class schemes and align with monitoring objectives.
  - Availability of both 25 m and 1 km data supports multi-scale monitoring and integration into GIS-based dashboards.

## Limitations and Regional Variability

- Some rare classes (e.g., Ruderal Weed) not consistently mapped across all regions; potential for regional bias.
- Differences in class definitions between hydrological and botanical interpretations can affect cross-study comparability.
- The unclassified category (0 in 25 m data) accounts for about 2% of Britain and is due to cloud, data gaps, or unusual cover types; users must account for unclassified areas in analyses.

## References (Context)

- Summarizes methodologies and validation studies related to land-cover classification, accuracy assessment, and Landsat TM-based mapping approaches referenced in the document.