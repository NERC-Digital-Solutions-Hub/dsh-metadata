# Countryside Survey vegetation species, recorded from plots in 2020 and 2021

- A dataset from the Countryside Survey (UKCEH-CS) covering vegetation plots surveyed in 2020 and 2021, part of the rolling Countryside Survey program initiated in 2019.
- Countryside Survey is a long-running, ecosystem-based audit of the countryside’s natural resources, allowing comparison across time and space to detect changes in soils, vegetation, headwater streams, habitats, and landscape features.

## Study design and rolling program

- Rolling survey design: repeats occur once a five-year cycle or 500 squares are completed; aims to maximize site visits while monitoring year-on-year changes.
- Sample framework: 500 x 1km squares across GB, stratified by the Land Classification of Great Britain; about 100 squares visited annually.
- Selection criteria: includes the 1978 set of 256 squares for longest time series; additional squares added based on earlier survey years; exclusions applied to squares with >75% urban land or >90% sea.
- Multi-metric approach: coordinates data collection across soils and vegetation at multiple scales to support ecosystem-level insights.

## Data collection and quality assurance

- Data collection: field surveys conducted by trained botanical survey teams following standard protocols (Smart et al., 2020), with initial training and ongoing supervision to ensure consistency.
- Quality assurance: 10% of plots re-surveyed by QA assessors; QA processes and analyses conducted by the same assessor since 1990 for consistency and validation.
- Validation: independent validation of plot locations and their assignment to JNCC habitat classifications.
- Confidentiality: distribution maps are not scaled to protect data confidentiality.

## The data files

- Vegetation plots information file
  - UKCEHCS_VEGETATION_PLOTS_2020_21.csv
  - Key columns include: YEAR, SQUARE_ID (1km square), PLOT_ID, PLOT_TYPE, PLOT_BH (BAP Broad Habitat), PLOT_PH (BAP Priority Habitat), COUNTRY (England/Scotland/Wales), COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07 (Land Classification), LC07_NUM (numeric code), and related environmental descriptors.
- Vegetation species list file
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2020_21.csv
  - Key columns include: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, BRC_NUMBER (species identifier), nest-level data (NEST_LEVEL), ZERO_COVER, FIRST_COVER, TOTAL_COVER (percent cover), and notes on nest/site structure.
  - Species nomenclature follows Stace (1997): New flora of the British Isles.
- Plot and species data are organized to support linking each plot to its recorded species composition and cover metrics.

## Data use, access and confidentiality

- Data structure supports analysis of plant diversity, community composition, and cover across years and space.
- Nomenclature and classifications align with established references (Stace 1997; Jackson 2000 for habitat classifications; Bunce et al. 2007 land classification; UKBAP descriptors).
- Data presented with attention to confidentiality in spatial distribution.

## Related methods and references

- Field methods and field handbook: UK-SCAPE Field Survey Field Handbook 2020 Vegetation Plots (Smart et al., 2020).
- Statistical and methodological context: Countryside Survey technical reports and peer-reviewed analyses (Scott 2008; Norton et al. 2012).
- Classification and habitat frameworks: ITE Land Classification of Great Britain (Bunce et al., 2007); Biodiversity Broad Habitat Classification (Jackson, 2000); UKBAP Priority Habitat descriptions (Maddock, 2008).

## Practical notes for data users

- The dataset provides longitudinal vegetation data suitable for temporal trend analyses across GB at national and sub-national scales.
- Use the plot and species files together to reconstruct plot-level species assemblages and their changes over 2020–2021.
- Reference field handbook and methodological documentation for data processing steps, QA procedures, and habitat classifications to ensure consistent analysis and interpretation.