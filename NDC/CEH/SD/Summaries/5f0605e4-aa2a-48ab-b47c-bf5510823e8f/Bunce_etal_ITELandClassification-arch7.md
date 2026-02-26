# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

- Objective: classify every 1 km square in Great Britain into land classes, using automated, map-based data to reproduce the original Merlewood land classification and support extensive GIS-based applications.

## Data architecture and inputs
- Data categories used for classification (mapped to 1 km squares):
  - COASTAL: coastal cliff, coastal rock, coastal sand, coastal mud, coastal shingle, tidal
  - ALTITUDE: height of hill, distance to hill, gradient, slope, mean altitude, etc.
  - MAPDATA: sea, woodland, villages, A roads, minor roads, canals, inland water, towns, motorways, B roads, railways, rivers (0.1 hectare resolution)
  - DISTANCE: distance to south coast and to west coast (in km)
  - ISLAND: island membership
  - CLIMATE: mean sunshine hours, mean snow days, mean January temp
  - GEOLOGY: detailed rock groupings (12–15 categories)
  - DRIFT: various drift types (alluvium, raised beaches, moraines, loess, glacial deposits, etc.)
- Data sources and resolution:
  - Altitude data from MOD 100m DTM
  - Mapdata and coast information from OS digital data (1:250,000)
  - Climate contours digitised for nearest center point in each 1 km square
- Data requirement: automated or existing data sources that allow full-coverage UK square-by-square classification.

## Classification approaches explored
- Baseline: reproduce the original ISA (Indicator Analysis) approach as closely as possible for continuity and comparability.
- Other multivariate and predictive approaches tested:
  - Discriminant Function (DF)
  - Logistic Regression (LR) and combinations (Logistic/Discriminant)
  - Other multivariate techniques (from phytosociology) and simulation ordination
- Key evaluation criteria for methods:
  - Geographical distribution and dispersion of land classes
  - Consistency with original 1212-square classifications
  - Proportional representation of classes across GB
  - Relationship to the principal environmental gradient
  - Proportion of field-sampled squares and efficiency in predicting land cover
  - Ecological characteristics of classes across data sets

## Key findings and comparisons
- Original ISA versus automated approaches:
  - Direct replication of the original 32-class ISA on the full GB was not feasible with available digitised data; differences in data balance, data scale, and availability of square-level field details led to divergent results.
- Discriminant Function (DF) findings:
  - Initial DF analyses yielded good correspondence for some divisions but performed poorly for coastal classes 7 and 8, and for a class (25) extending into southern Britain, suggesting redefinition would be required.
  - Overall, reduced alignment with the original classification and problematic regional balance limited DF utility.
- Logistic Regression (LR) and Logistic/Discriminant (LR/DF) findings:
  - LR and LR/DF produced higher correspondence with the original classification than DF alone.
  - LR/DF provided the best overall balance between preserving original class structure and improving practical map-based usability.
  - LR-based approaches yielded tighter clustering and better stability in class positions relative to the environmental gradient.
- Validation metrics:
  - Correlations with the principal environmental gradient: original vs Discriminant ~0.995; original vs LR ~0.997.
  - LR/DF demonstrated lower standard errors and dispersion than the original classification.
  - Simulated indicator-based approaches and some alternatives offered improvements at regional levels but introduced regional misallocations (e.g., northern Scotland vs southern England in some schemes).
- Outputs and representations:
  - Distribution maps presented for the LR/DF method only.
  - Comparisons included cross-tabulations with the original classifications, distance to coasts, altitude means, and environmental gradient representations.
  - The LR/DF approach reduced large-scale misclassifications and produced more coherent geographic clustering.

## Outputs and data products for GIS use
- Primary map products:
  - Distribution maps for the GB land classification derived from LR/DF (primary recommended product)
  - The original 32 ISA classes from 1212 squares and the 1212-plus-4800-squares variant with 76 attributes (available on request)
  - Classification trained on the original 1212 squares using the Discriminant Function
- Additional analytical outputs:
  - Environmental means and standard errors by class (altitude, drift-free classes, etc.)
  - Overlaying of individual attributes (e.g., coastal features with other attributes)
  - Coastal feature distributions (maps and statistics for major coastal environments)
  - Overlay of land classes with vegetation and soil data (ecological correlations)
  - Land cover estimates for GB based on 1978 data and LR/DF techniques
  - Ecological characteristics of classes derived from soil pit data, vegetation quadrats, and climate/soil descriptors
- Reusable data layers:
  - Coarse-to-fine environmental gradients
  - Spatial dispersion metrics (distance to coasts, altitude dispersion, etc.)
  - Potential for overlay with other GIS datasets (e.g., remote sensing classifications, habitat maps)

## Recommendations and conclusions
- Primary recommendation: use Logistic Regression with Discriminant Function (LR/DF) for GB-wide land classification.
  - Reasons:
    - DF fails to identify southern coastal classes 7 & 8, requiring redefinition of coastal classes and misplacing class 25 into southern Britain
    - LR/DF yields closer alignment to the original classification and better proportional sampling relative to class sizes
    - LR/DF generally provides lower standard errors and dispersion than the original classification, improving reliability for policy and planning use
    - LR/DF outperforms alternative approaches in key performance areas, while the indicator-based approaches produced divergent and regionally inconsistent results
- Practical implications for GIS users:
  - The recommended LR/DF-based maps offer more reliable, spatially coherent representations for policy analysis, planning, and environmental assessments
  - Use of LR/DF outputs improves consistency with the established body of land-class-derived studies and datasets
  - Availability of multiple output formats (original ISA classes, LR/DF-derived classifications, and augmented data) supports diverse GIS workflows and analyses

## Additional notes and references
- Extensive appendix and references document prior studies and applications of the Merlewood Land Classification system and its use with remote sensing, habitat studies, forestry, and environmental planning.
- The report also discusses the potential and limitations of combining multiple attributes and the value of proportional sampling for estimating GB land cover.