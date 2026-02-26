# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

## Aim and Scope
- Classify every 1 km square in Great Britain into one of the land classes.
- Use automated methods based on machine-readable data to reproduce or improve the original Merlewood land classification.
- Maintain confidence in the original classification due to its widespread use and existing data bases; enable broad data use and future development.
- Conduct extensive methodological testing over 15 months to identify a robust, scalable approach.

## Data Used and Dataset Structure
- Data categories used for classification (available as 0.1 hectare units or automatable):
  - COASTAL (coastal cliff, rock, sand, mud, shingle, tidal)
  - ALTITUDE (height behind, distance to features, gradients, slopes)
  - MAPDATA (Sea, Woodland, Villages, roads, canals, water bodies, towns, railways, etc.)
  - DISTANCE (distance to south/west coasts)
  - ISLAND, CLIMATE (sunshine hours, snow days, January temps), GEOLOGY (detailed rock types), DRIFT (drift types like alluvium, moraines)
- Data sources and formats:
  - MOD 100 m Digital Terrain Model for altitude
  - OS digital map data via ARC/INFO for map attributes
  - 1 km grid square centroids used for environmental gradient extraction
- Original dataset and expansion:
  - Initial approach based on detailed square data from over 240 squares was impractical; expanded to use larger, automatable data sets
  - 1212 squares used for original ISA-based comparison
  - 76 indicator attributes identified to extend data coverage, enabling ~4800 additional squares to be considered

## Data Preparation and Dataset Construction
- Requirements for data: information either from existing datasets or recorded automatically for each square
- Data processing goals:
  - Retain relative distributions from the original sample
  - Ensure the feature set supports refinement of classifications while enabling full GB coverage
- Data issues addressed:
  - Differences in data balance and recording scale between original ISA and new data
  - Zeros and sparse data addressed to improve classification stability

## Classification Methods Explored
- Extended ISA versus original ISA (TwinSPAN vs Indicator Analysis)
  - Aimed to reproduce the original classifications with comparable detail
  - Differences in data balance, scale, and available square-level data led to shifts in resulting class boundaries
- Discriminant Function (DF)
  - Evaluated because of continuous-variable attributes and fast computation
  - Achieved partial correspondence with the original classification; several regional splits diverged
  - Various transformations tested; some regional misallocations persisted
- Other Multivariate Techniques
  - Various algorithms from phytosociology and related fields explored
  - Distance/likelihood approaches showed potential for inter-class relationship analysis but had issues with regional clustering
- Logistic Regression / Discriminant Function Hybrid (LR)
  - Applied to the first three levels (and compared against pure discriminant)
  - Initially produced 2-way correspondence with the original for a subset of squares; used for broader comparisons
- Indicators and Simulation Ordination
  - Simulated ordination approaches replicated the progression along environmental gradients
  - Generally produced good results for many classes but diverged for specific northern/southern patterns; largely superseded by LR approach
- Cross-tabulations and Environmental Gradient Alignment
  - Cross-tab analyses compared LR and DF against the original 1212-square classification
  - LR demonstrated stronger diagonal alignment with fewer outliers compared to head-to-head with the original
  - Environmental gradient correlations between classifications and the original were calculated to assess overall coherence

## Evaluation Criteria
- Geographical distribution of squares within each land class
- Dispersion measured by means and standard errors of locational variables
- Allocation fidelity of the original 1212 squares
- Proportional representation of land classes across GB
- Relationship between principal environmental gradient and land classes
- Proportion of field-sampled squares in various years (1978, 1984, 1990)
- Efficiency in predicting areas and cover features
- Ecological characteristics derived from environmental datasets and vegetation sampling

## Key Findings and Results
- Overall performance across methods:
  - Logistic Regression / Discriminant Function (LR) showed the strongest overall alignment with the original classification
  - Discriminant Function (DF) alone failed to identify coastal classes 7 and 8 in southern Britain, risking wholesale redefinition of coastal classes and extending class 25 northward
- Comparative advantages of LR
  - Better alignment with original classification across multiple metrics
  - More proportional sampling alignment to stratum size
  - Lower standard errors and reduced dispersion relative to the original
  - Improved handling of the expanded 4800-squares dataset and indicator-based attributes
  - Generated more stable, usable maps for policy and planning
- Limitations and caveats
  - DF alone could not capture certain coastal classes in the south; LR mitigates this by incorporating coastal distinctions
  - Some regional divergences remained, but overall LR reduced misclassifications and improved interpretability
- Correlation with vegetation data
  - Gradient correlations with vegetation quadrats showed LR and DF both closely tracking the environmental gradient identified by the original classification; DF slightly higher for some gradient correlations, LR offered better coastal class handling

## Output Products and Outputs
- Classification maps and data products
  - Maps of the original 32 ISA classes derived from the 1212-square dataset
  - Maps incorporating the 4800 squares identified from the 76 indicator attributes
  - Classification of all GB squares trained using the Discriminant Function on the original 1212 squares
- Tabular and descriptive outputs
  - Environmental means and attribute summaries (Tables of means across data types)
  - Altitude, drift, and coast-related dispersion metrics
  - Standard errors for gradient axis values
- Accessibility and formats
  - Maps and data available from ITE Merlewood on request
  - Supporting figures include scatter diagrams, cross-tabulations, and distribution maps

## Recommendations
- Primary recommendation: Use Logistic Regression / Discriminant Function (LR) for GB-wide classification
  - Why LR: DF alone misses southern coastal classes (7 & 8) and could require redefining coastal and northern classes; LR maintains coastal integrity and overall class balance
  - LR demonstrates closer alignment to the original classification across key metrics and lower error dispersion
  - LR provides better representation proportional to sampling strata and improved efficiency over the original and over indicator-based expansions
- Practical considerations
  - Maintain original coastal class definitions (with LR support) to avoid large-scale redefinition
  - Utilize LR outputs to produce defensible, policy-relevant maps with improved reusability and lower uncertainty
- Outputs to consider
  - Full GB classification maps trained from the original 1212 squares
  - Additional maps for the 4800-indicator-based squares to illustrate improvements and areas of divergence
  - Overlayable attribute maps (e.g., coastal features, altitude, drift, geology) for integrated analyses

## Ecological Correlation and Class Characteristics
- Environmental gradient coherence
  - Original vs LR vs DF show strong alignment along a major environmental gradient from southern/east lowlands to northern/west uplands
- Vegetation relationships
  - Correlations with vegetation assemblages (based on limited quadrat data) remained strong for all methods; LR and DF maintained high associations with environmental axes
- Soil and vegetation descriptions
  - Summary ecological characteristics (pH, typical plant communities) provided to aid interpretation of classes and potential management implications

## Challenges and Considerations for Data Support
- Data heterogeneity and availability
  - Integrating diverse data sources (coastal, altitude, map data, climate, geology) required careful harmonisation and data curation
- Representativeness and sampling
  - Ensuring proportional sampling relative to class sizes improved error estimation and inference for nationwide outputs
- Reproducibility and usability
  - Clear documentation of methods and data sources to enable reproduction and future updates as new data become available

## Appendices and References
- Appendix A: references to external studies using the Merlewood Land Classification system
- Appendix B: multivariate discrimination techniques (details of discriminant analysis approaches)
- Additional figures and tables illustrating cross-tabulations, gradient correlations, and standard errors (accessible via ITE Merlewood)