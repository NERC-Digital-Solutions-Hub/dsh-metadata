# Countryside Survey vegetation plots 2022-23

## Overview
- Part of the Countryside Survey (UKCEH-CS), a rolling monitoring program of the UK's countryside initiated in 2019 to track change across multiple ecosystem components.
- Focuses on vegetation plots and associated habitat data collected during 2022 and 2023, with the aim of producing robust national and subnational indicators over time.
- Data are collected using standardized protocols to enable comparisons with previous surveys and to support policy-relevant analyses.

## Design and Sampling
- Rolling five-year cycle: 500 x 1km squares are surveyed per cycle, with around 100 squares visited each year.
- Sampling strata based on the Land Classification of Great Britain to capture landscape variation (topography, geology, climate, etc.).
- Longest-running time series prioritized: 1978 survey squares retained to maximize historical continuity; additional squares from the 1990 cohort added to maintain longitudinal coverage.
- Exclusion criteria: any square with more than 75% urban land or more than 90% sea (per LCM2007 and census data) is excluded.
- Rationale: maximize site visits across GB while monitoring year-to-year change and broader spatial variation in a cost-effective way.

## Data Collection and Quality Assurance
- Data collected by trained field surveyors following Smart et al. (2020) field protocols; intensive pre-surveys and ongoing supervision ensure methodological consistency.
- 10% of plots re-surveyed for quality assurance; QA analyses conducted by the same assessor each survey year since 1990.
- Independent validation of plot locations and alignment with JNCC broad and priority habitat classifications.
- Data capture includes both plot-level information and species lists, with rigorous documentation and provenance.

## Data Products and Metadata
- Two CSV data files for 2022-23:
  - Vegetation plots file (UKCEHCS_VEGETATION_PLOTS_2022_23.csv): plot location, 1km square ID, plot ID, plot type, habitat classifications (BAP Broad Habitat; BAP Priority Habitat), country, county, environmental zone, Land Classification, and related metadata.
  - Vegetation plot species file (UKCEHCS_VEGETATION_PLOT_SPECIES_2022_23.csv): species-level data per plot, including species name, nest level, percent cover (across different nest levels), and total cover; nomenclature follows Stace (1997).
- Consistent with field handbook guidance (UK-SCAPE Field Survey Field Handbook 2020) and employs the ITE/JNCC habitat classifications for cross-walking habitat types.
- Nomenclature and metadata are designed to support reproducibility and cross-survey comparability.

## Data Access, Use, and Temporal Context
- Designed to support national and subnational indicators for GB countryside stock and change, enabling analysis of spatial and temporal trends across cycles.
- The rolling program buffers against climate-year extremes, improving reliability of year-to-year comparisons while preserving long-term trends.
- First rolling cycle began in 2019; 2022-23 data contribute to ongoing monitoring and policy-relevant assessments.

## Data Quality, Standards, and Governance
- High methodological standards through training, standard protocols, and continuous QA/validation.
- Data provenance is clearly documented via field handbook references and methodological literature.
- Metadata and data dictionaries correspond to the described CSV columns, with explicit mappings to habitat classifications and land classifications to support interoperability.

## Limitations and Considerations for Data Leaders
- Potential gaps at finer spatial or thematic granularity due to the survey design and exclusion criteria.
- Data accessibility and discoverability rely on repository practices and documentation; ongoing emphasis on clear metadata and data lineage is important for broader reuse.
- Some variation in habitat classifications and nomenclature across sources requires careful cross-walking when integrating with other datasets.

## Key References and Resources
- Smart et al. 2020: UK-SCAPE Field Survey Field Handbook 2020 – Vegetation Plots.
- Bunce et al. 2007: ITE Land Classification of Great Britain 2007.
- Stace 1997: New Flora of the British Isles.
- Additional methodological and historical context available in Countryside Survey project documentation and related CEH/NERC publications.