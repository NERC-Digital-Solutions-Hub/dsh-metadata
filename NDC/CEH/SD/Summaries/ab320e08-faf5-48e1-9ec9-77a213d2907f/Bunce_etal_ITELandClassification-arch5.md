# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

- Objective: Classify every 1 km square in Great Britain into a land class, using automated methods that can reproduce the original Merlewood/I TE classification while enabling scalable, repeatable processing across all squares.
- Rationale: The original ISA-based classification was widely used; automation and expanded data inputs were required to classify all squares efficiently and consistently.

## Data and Datasets

- Data structure requirement:
  - Data categories used for classification (Section 2): COASTAL, ALTITUDE, MAPDATA, DISTANCE, ISLAND, CLIMATE, GEOLOGY, DRIFT.
  - Altitude data from MOD 100 m DTM; map data from OS 1:250,000; climate and geology information digitised or provided as attribute blocks.
  - Map units defined at 0.1 hectare; spatial scope covers all GB 1 km squares.
- Original vs expanded datasets:
  - Initial approach relied on detailed per-square data (over 240 fields) but practical limits necessitated automation.
  - Two data streams to expand: the original 1,212 classified squares and an expanded set of 4,800 squares identified by 76 indicator attributes (total 5,? squares used for testing).
- Data prerequisites and workflow:
  - Data could be obtained from existing datasets or recorded automatically.
  - Data processing used ISA (Indicator Analysis) as the baseline and later incorporated multivariate and regression approaches.
- Data periods and sampling:
  - Field sampling and vegetation data associated with 1978, 1984, and 1990 sampling cycles; inclusion of environmental gradients derived from map data.

## Classification Approaches Explored

- Baseline and replication:
  - ISA-based original classification using 1212 squares and 282 attributes.
- Multivariate and predictive methods tested:
  - Discriminant Function (DF) approach: tested similarity to the original classification; initial correspondence around 438/1212; issues with class balance and region-specific reallocation.
  - Logistic Regression (LR) and combinations (Logistic/Discriminant) approaches: extensive testing across levels; compared against original 1212-square classification and the 4,800 indicator-attribute squares.
  - Other multivariate techniques (e.g., TWINSPAN, other orderings) explored but largely rejected due to spatial misallocations (e.g., Midlands England dispersed into southern Scotland) or poor regional behavior.
  - Simulation ordination and indicator-based methods used to align with the original environmental gradient and to test sensitivity to indicators.
- Output formats and validation:
  - Cross-tabulations comparing original vs. derived classifications.
  - Environmental gradient correlations and dispersion metrics to assess coherence.
  - Distribution maps created for the LR/DF method only.

## Key Findings

- Classification consistency:
  - DF alone showed substantial divergence from the original in many areas (e.g., classes needing regional redefinition, coastal classes 7 & 8 not captured in the south).
  - LR/DF combination produced tighter clustering and generally better alignment with the original classifications, with reduced dispersion and lower standard errors in several cases.
- Regional and coastal classes:
  - The discriminant function failed to identify coastal classes 7 and 8 in the south, creating a strong argument for not relying on DF alone.
  - LR/DF avoided widespread misallocation seen with some other approaches and maintained more stable class definitions regionally.
- Proportional sampling and errors:
  - LR/DF provided sampling proportions closer to proportional to stratum size, improving the efficiency of error estimation and reducing dispersion relative to the original classification.
- Ecological validation:
  - Correlations between environmental gradients (derived from the dataset) and vegetation patterns remained high, with LR/DF showing strong but variable performance across gradients.
  - pH and soil-pit data, as well as vegetation cover comparisons, supported ecological plausibility of the LR/DF-derived classifications, though some outputs varied by class.

## Recommendations and Conclusions

- Primary recommendation:
  - Adopt the Logistic/Discriminant (LR/DF) approach for classifying all GB squares.
- Rationale:
  - DF alone misses coastal classes (7 & 8) in the south and would require redefining coastal classes, complicating reproducibility.
  - LR/DF achieves better alignment with the original classification overall, with the most favorable balance between proportional sampling, lower standard errors, and reduced dispersion.
  - LR/DF provides a robust path to classify all squares (including the 4,800-sample expansion) more consistently than the original approach.
- Important caveats:
  - While LR/DF improves many metrics, some discrepancies remain compared to the original classification, and a few coastal or border cases require careful interpretation.
  - The 4,800 additional squares identified via 76 attributes showed divergences from the original classification, highlighting the value of the LR/DF method but also the need for ongoing validation.
- Outputs and maps:
  - Distribution maps for the 32 (original ISA-derived) classes; maps for the LR/DF-trained classification; altitude means and standard errors; environmental means; overlays of selected attributes; field-survey square statistics.
  - Access to outputs (maps and data) was noted as available on request from ITE Merlewood.

## Outputs, Access, and Documentation

- Data products:
  - Original 32-class ISA maps derived from 1212 squares.
  - Original 1212 squares plus 4,800 squares identified via 76 attributes.
  - Classification of all squares trained using the Discriminant Function (and LR/DF as the recommended approach).
  - Distribution maps, altitude means, standard errors, and environmental mean tables.
- Accessibility:
  - Maps and data outputs available on request from ITE Merlewood.
  - Appendix materials and references provide supporting literature and methodological context.

## Ecological and Field Insights (Summarized)

- Vegetation and soil context:
  - Vegetation quadrats and soil pits linked to land classes; correlations between environmental gradients and vegetation patterns used as ecological validation.
  - LR/DF classifications demonstrated strong relationships with vegetation gradients, supporting ecological plausibility of the LR/DF-based mapping.
- Class-level ecological characteristics:
  - Various species groups ( grasses, clovers, bent grasses, moorland indicators) were described in relation to land classes, enabling interpretation of ecological meaning behind the LR/DF classifications.

## Data Stewardship Considerations

- Data governance and provenance:
  - Clear lineage: 1 km-square GB dataset, multiple data sources (coastal, altitude, mapdata, climate, geology, drift) and evolving attribute sets (282 → 76 key attributes).
  - Emphasis on reproducibility by replicating original ISA approach while enabling scalable automation.
- Data quality and metadata:
  - Documentation of data inputs, attribute meanings, and method choices (ISA replication vs. DF vs. LR/DF).
  - Handling of zeros and missing values during preprocessing to improve classification performance.
- Data sharing and versioning:
  - Availability of multiple outputs (original ISA-based maps, LR/DF maps, and cross-validated assessments) facilitates stakeholder comparison.
  - Recommendation to maintain versioned datasets, with clear notes on method choice (LR/DF) and any regional redefinitions of coastal classes.
- Future updates and governance:
  - The study indicates a path for ongoing updates as new data streams or sampling dates become available.
  - Consideration of revalidation with newer environmental data and potential expansion beyond 1 km squares for finer-scale analyses.