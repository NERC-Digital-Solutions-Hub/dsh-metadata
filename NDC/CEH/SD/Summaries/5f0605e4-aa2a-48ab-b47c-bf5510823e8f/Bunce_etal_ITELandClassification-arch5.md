# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

## Purpose and scope
- Objective: classify every 1 km square in Great Britain into land classes using automated, machine-readable data to reproduce the original ISA-based classification and enable broad reuse.
- Rationale: manual classification would take ~20 man-years; hence a reproducible, data-driven method was pursued to support extensive downstream studies and policy analyses.

## Structure and content of the data used
- Data requirements: data could be sourced from existing datasets or recorded automatically; the project moved from detailed per-square field data to scalable, digitised attributes.
- Key data components (variables) used in classifications:
  - COASTAL (coastal environments)
  - ALTITUDE (hill/valley metrics, aspect, gradient)
  - MAPDATA (OS-derived features: roads, towns, waterways, etc.)
  - DISTANCE (distance to south/west coasts)
  - ISLAND (island status)
  - CLIMATE (sunshine hours, snow, January temp)
  - GEOLOGY (lithology categories)
  - DRIFT (drift/soil/geomorphological deposits)
- Data sources and formats:
  - Mapdata and coast data from OS digital data (1:250,000 scale)
  - Altitude data from MOD 100 m Digital Terrain Model
  - Climate data digitised onto grids
  - Geographic data stored in ARC/INFO format
  - 1 km grid squares with values represented as 0.1 hectare units for mapdata
- Scale and scope: aim to classify all GB squares; initial ISA-inspired approach used data from a core set of squares (1212) with 282 attributes, later expanded to include approximately 4800 additional squares using 76 indicator attributes.

## Classification approaches explored
- Baseline and motivation:
  - Attempt to replicate original ISA classification as closely as possible to preserve user confidence and continuity of many prior studies.
  - Several multivariate approaches were tested due to impracticality of re-collecting field data for all squares.
- Approaches tested and key findings:
  - Discriminant Function (DF)
    - Pros: continuous variables; fast; provided outputs that summarized relationships between classes.
    - Cons: could reallocate original sites and produced imbalanced class sizes in some regions; failed to identify coastal classes 7 and 8 in the south, necessitating redefinition of coastal classes.
    - Overall correspondence with original: moderate (438/1212 match for some configurations; regional imbalances noted).
  - Logistic Regression / Discriminant Function (LR/DF)
    - Found to offer better overall correspondence with the original classification across many regions.
    - Provided more balanced class representation and lower standard errors in several important metrics.
  - Other multivariate techniques (e.g., simulations on ordination axes, other algorithms from phytosociology)
    - Some offered insights but caused geographic dispersion of certain classes (e.g., Midlands Scotland vs southern England) or failed regional coherence; largely rejected for final approach.
- Cross-comparisons and validation:
  - Cross-tabulations against the original 1212-square classification showed improved alignment with LR/DF, though some divergence remained for specific classes.
  - Environmental gradient analyses (ordination on original vs new classifications) indicated close coherence for LR/DF relative to the original.

## Key results and comparisons
- Overall recommendation from analysis:
  - Logistic Regression combined with Discriminant Function (LR/DF) is recommended for classification of all GB squares.
  - Primary reasons:
    - DF alone failed to identify coastal classes in the south, risking substantial redefinition of coastal classes.
    - LR/DF produced the best balance between proportional representation and correspondence to the original classification.
    - LR/DF yielded lower standard errors and less dispersion than the original (with improvements also when using indicator-attribute-expanded data).
- Specific performance highlights:
  - Correspondence with original classification: LR/DF shows higher overall alignment than original alone and other tested methods.
  - Coastal classes (7 & 8): LR/DF preserves coastal structure without forcing major redefinition; DF alone would require redefinition of coastal classes.
  - Field data and sampling: proportional sampling improved correspondence and error estimates as sample size increased (LR/DF maintains better alignment with proportional sampling).
  - Environmental gradients and vegetation correlation: correlations with vegetation gradients were strongest for the DF approach, with LR showing competitive performance; LR/DF still favored for classification stability and coastal representation.
- Outputs and data products:
  - Distribution maps of land classes using LR/DF for all squares.
  - Access to multiple data products on request:
    - Original 32 ISA-derived classes from 1212 squares
    - Original 1212 squares plus 4800 squares from 76 attributes
    - Classification of all squares trained with the Discriminant Function
  - Altitude means and standard errors, environmental gradient scores, and regional dispersion metrics.

## Implications for data governance and stewardship
- Data standardisation and interoperability:
  - Emphasis on using machine-readable, digitised attribute sets (coastal, altitude, mapdata, etc.) to enable scalable classification across all GB squares.
  - Adoption of consistent data formats (ARC/INFO) and standardized attribute definitions to support reuse and integration with other datasets.
- Provenance, metadata, and versioning:
  - Clear documentation of data sources (OS, MOD DTMs, climate maps), processing steps, and classification methods to enable auditability and reproducibility.
  - Explicit reporting of the limitations (e.g., data balance issues, regional disparities, zeros in data) and how they were mitigated (e.g., removal of zeros, region-specific transformations).
- Data quality and uncertainty:
  - Use of standard errors and dispersion metrics to quantify uncertainty in class assignments, with the LR/DF method delivering tighter clustering and lower errors in many cases.
  - Recognition that some ecological and vegetation correlations vary by method, suggesting the need to document method-specific strengths when communicating results to data users.
- Sharing, reuse, and data products:
  - Availability of multiple data products and maps on request; potential for broader dissemination through data portals and catalogues.
  - Documentation of overlay attributes and possible attribute-combination scenarios to support end-user applications (e.g., coastal feature overlays, environmental means).
- Data maintenance and updates:
  - Framework supports updating classifications as new data become available (expanded attributes, refined data sources), aligning with governance needs for living datasets.
  - Emphasis on maintaining a publishing mindset to ensure datasets remain usable, discoverable, and up to date.

## Conclusions and recommendations
- Final recommendation: Use Logistic Regression combined with Discriminant Function (LR/DF) for the classification of all GB squares.
  - Strong justification: coastal classes retained without major redefinition; improved proportional representation; generally lower standard errors and dispersion than the original; demonstrated value over the expanded indicator-attribute approach.
- Practical implications for data custodians:
  - Prioritise LR/DF as the default classification workflow for nationwide GB land classification.
  - Provide access to multiple outputs (32-class ISA baseline, expanded 4800-sample set, full-square LR-trained classification) to support diverse user needs.
  - Continue to document data sources, attribute definitions, methods, and uncertainty to support reproducibility and governance.
- Overall impact: established a scalable, transparent, and governance-friendly framework for GB land classification that preserves historical continuity while improving statistical robustness and suitability for large-scale applications.

## Appendices and supplementary information
- Appendix A: References to studies using the Merlewood Land Classification system and related efforts.
- Appendix B: Multivariate discrimination methods (details on DF, logistic regression, and other approaches) and their comparative performance.
- Additional outputs:
  - Environmental means and population of coastal features
  - Overlaying of individual attributes (example with sea cliffs and chalk)
  - Field survey square statistics and error terms
  - Correlation figures relating environmental gradients to vegetation and land classes