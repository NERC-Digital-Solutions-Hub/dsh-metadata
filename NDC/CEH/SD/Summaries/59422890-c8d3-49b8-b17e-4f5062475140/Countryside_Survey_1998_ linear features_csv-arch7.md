# Dataset Documentation

- Purpose
  - Provides national estimates of landscape linear feature stock for 1998, calculated using the 2007 ITE Land Classification.
  - Data expressed as total lengths (in 000s km) for each linear feature type by Land Class, with 95% confidence intervals (Lower and Upper estimates) and Land Class area.

- Data content and structure
  - YEAR: Year of Survey
  - LAND_CLASS: ITE Land Class (text)
  - FEATURENO: Linear feature code
  - FEATURE: Linear feature description
  - LOWER_ESTIMATE: Lower 95% confidence interval of feature length (000s km)
  - MEAN_ESTIMATE: Mean length estimate (000s km)
  - UPPER_ESTIMATE: Upper 95% confidence interval of feature length (000s km)
  - LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha)
  - Feature codes included:
    - _1: Hedge
    - _3: Wall
    - _4: Line of trees/shrubs/relict hedge/fence
    - _5: Line of trees/shrubs/relict hedge
    - _6: Bank/grass strip
    - _7: Fence
    - TOTAL: Total length of linear features

- Key methodological notes
  - Reporting uses a hierarchical, six-feature class system with no double counting.
  - Hedge features take precedence when co-occurring with walls or fences; estimates for walls/fences do not include lengths that occur with a hedge.
  - Hedges may be beside walls and/or fences; reporting of stock for walls/fences excludes hedge-associated lengths.

- Data interpretation and quality notes
  - Lengths are reported in 000s of kilometers by Land Class and feature type.
  - Some MEAN_ESTIMATE values may be negative due to the statistical model; treat negative values as zero.
  - Data were collected from the 1998 field survey and linked to the 2007 ITE Land Classification.

- Use limitations and attribution
  - All uses of Countryside Survey data must acknowledge the source.
  - Acknowledge: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; data copyright reserved.

- Access and references
  - Countryside Survey Website: http://www.countrysidesurvey.org.uk/
  - Related publications and technical reports (background and methodology) including:
    - Carey et al. 2008 (UK results from 2007)
    - Haines-Young et al. 2000 (habitats accounting methodology)
    - Scott 2007 (Statistical Report for national estimates)
    - Bunce et al. 1996, 2007 (ITE Land Classification references)
  - Additional methodology and data documentation available via linked reports and metadata in the Countryside Survey resources.