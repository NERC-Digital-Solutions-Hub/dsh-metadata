# The Land Cover Map of Great Britain

- Purpose and scope
  - Describes the Land Cover Map of Great Britain (LCMGB) produced from supervised maximum likelihood classifications of Landsat Thematic Mapper data.
  - Uses a 25 m grid to map 25 land cover types plus an unclassified category; combines summer and winter imagery to improve classification accuracy.

- Data products and resolutions
  - 25 target cover-types (25-class dataset): each 25 m cell is assigned a value 0–25 corresponding to a target class (with 0 = Unclassified).
  - 1 km summary data: for each 1 km cell, 25 layers exist, each representing the percentage of that target cover-type within the cell (e.g., layer 10 would record the percent of that 1 km cell occupied by target class 10).
  - 17 key cover-types (A–Q): an aggregated, more consistently mappable set derived from the 25 target classes; provided as an alternative dataset but the 25-target set remains standard.
  - Availability: both 25 m and 1 km summary resolutions; 17 key dataset is available as an option but the 25-class dataset is standard.

- Spatial resolution and registration
  - Minimum accurately mappable unit is effectively around 1 ha; features as small as 1 ha are identifiable, with some finer structure visible (e.g., roads, fields) down to 0.125 ha (2 pixels) after removing isolated pixels.
  - Landsat-derived maps registered to 1 km field maps show an average displacement of about 0.8 pixels (20 m); most squares align with 0–1 pixel shifts, with a few requiring more.

- Classification accuracy and caveats
  - Ground-truth data are limited; various reference surveys use different definitions, affecting direct comparability.
  - Overall correspondence between field data and LCMGB: approximately 67–71% when boundary pixels are included (lower due to mixed pixels and boundary issues); about 71% when boundaries are excluded; with time-based changes considered, correspondence rises to ~76–82%.
  - A realistic assessment of overall Land Cover Map accuracy is likely 80–85%.
  - The largest source of error is misclassification of mixed boundary pixels (often >40% of pixels border vector boundaries). Distinguishing misclassification from misregistration is challenging.
  - Comparisons with ground data depend on definition differences (e.g., bog definitions hydrological vs. botanical); discrepancies reflect methodological differences rather than pure mapping error.

- Land cover class descriptions (conceptual overview)
  - The classification aggregates many botanical subtypes into ecologically meaningful, consistently identifiable 25 target classes; subclasses (e.g., different grains in arable) are collapsed for mapping practicality.
  - Classes are defined to be mappable above the practical minimum area and to remain interpretable across Britain; some rarer classes may be inconsistently mapped (e.g., ruderal weeds).
  - Important grouping notes:
    - Coastal and inland water, sea/estuary vs. inland water distinctions.
    - Coastal bare ground, saltmarsh, and various grass/veg communities (pasture, meadow, and semi-natural swards with management distinctions).
    - Grasslands divided into mown/grazed turf and meadow/verge/semi-natural swards to reflect management and spectral differences.
    - Heaths and moorlands (lowland and upland variants) including bare/shrub mixes and mosses.
    - Shrub and woodland classes (deciduous and coniferous; mixed woodlands; scrub/orchard).
    - Wetlands (bogs, lowland and upland) with distinct herbaceous vs. shrub-dominated signatures.
    - Distinctions between agricultural/managed land (tilled land, arable) and developed land (suburban/rural development, continuous urban, inland bare ground).
  - The document provides explicit, detailed definitions for each class (e.g., what constitutes beach/coastal bare ground, saltmarsh, rough pasture, bracken, felled forest, etc.) and notes on regional variations and spectral separability.

- Practical guidance for GIS use
  - Two-tier output structure allows both broad national-scale analyses (17 key types) and finer detail (25 target types).
  - Results can be aggregated or reclassified in GIS to suit specific objectives; non-standard classifications or tailored outputs are feasible, with the caveat that some subdivisions may not be consistently separable spectrally.
  - Acknowledges regional inconsistencies and suggests regional masks (e.g., upland vs. lowland) to improve consistency in some analyses.
  - The dataset is designed to support map-based data visualizations and to enable exploration of spatial patterns and land cover composition for policy, client, or public audiences.

- References and context
  - Details, accuracy evaluations, and class definitions are anchored in Fuller et al. (1994a, 1994b), Wyatt et al. (1994), and related methodological studies on remote sensing classification and land cover definitions.
  - The document discusses the intended use, limitations, and interpretation of the LC MGB outputs, with emphasis on how classifications relate to ground truth and other surveys.