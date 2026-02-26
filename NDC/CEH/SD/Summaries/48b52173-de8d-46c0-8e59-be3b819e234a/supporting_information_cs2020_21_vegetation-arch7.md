# Countryside Survey vegetation species, recorded from plots in 2020 and 2021

## Overview
- A dataset from the Countryside Survey (UKCEH-CS) detailing vegetation plots and species observed in 2020–2021 across GB.
- Part of a rolling monitoring program designed to detect spatial and temporal changes in soils, vegetation, habitats, and landscape features.

## Survey design and rolling program
- Rolling program adopted in 2019: repeats on a five-year cycle or after 500 squares completed.
- Approximately 100 of the 1km squares are visited each year, maximizing site coverage while enabling year-on-year trend detection.
- Sampling frames built on a 1km grid stratified by the Land Classification of Great Britain (ITE/Bunce et al., 2007).
- Exclusion criteria: remove squares with >75% urban land or >90% sea.

## Sampling framework and square selection
- Core long-term time series: the 1978 selected squares (256) are retained for repeat sampling to maximise historical continuity.
- Additional 1km squares added from the earliest years (1990) to extend the time series.
- A total of 500 x 1km squares are surveyed over five years, with stratification to support national and sub-national indicators.

## Data collection and quality assurance
- Field surveys conducted by trained botanical survey teams following Smart et al. (2020) protocols.
- Intensive pre-surveys and ongoing supervision to ensure consistency and data quality.
- 10% of plots re-surveyed for quality assurance; independent validation of plot locations and habitat classifications (JNCC broad and priority habitats).
- QA processes managed by the same assessor across survey years starting in 1990.

## Datasets included (Vegetation plots and species lists)
- UKCEHCS_VEGETATION_PLOTS_2020_21.csv
  - Plot-level information, including: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, X, XX, PLOT_BH (Broad Habitat), PLOT_PH (Priority Habitat), COUNTRY, COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07, LC07_NUM.
- UKCEHCS_VEGETATION_PLOT_SPECIES_2020_21.csv
  - Species list and plot association information: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, BRC_NUMBER (species identifier), nest levels (NEST_LEVEL), coverage metrics (ZERO_COVER, FIRST_COVER, TOTAL_COVER), and related fields.
- Nomenclature follows Stace (1997) New flora of the British Isles.

## Key GIS-relevant details
- Spatial scope: 1km squares across Great Britain, with plot-level data nested within squares.
- Rich attribute set for mapping and analysis: habitat classifications (BAP Broad/Priority Habitats), environmental zones, land classification codes, and county-level geography.
- Multi-layer potential: integration with soils, vegetation metrics, and landscape features for ecosystem-scale visualizations.

## Data quality and standards
- Data collected under standardized field protocols (Smart et al., 2020) with rigorous training and quality assurance.
- Independent validation against habitat classifications ensures reliability for GIS mapping and policy-oriented analyses.

## References and further reading (selected)
- Bunce et al. 1996, 1996, 2007 — ITE Land Classification of Great Britain; methodology and classification framework.
- Jackson 2000; Maddock 2008 — habitat definitions and biodiversity classifications.
- Carey et al. 2008; Norton et al. 2012; Scott 2008; Smart et al. 2020 — methodologies, field manuals, and key analyses from Countryside Survey.
- Countryside Survey project site and supporting materials.