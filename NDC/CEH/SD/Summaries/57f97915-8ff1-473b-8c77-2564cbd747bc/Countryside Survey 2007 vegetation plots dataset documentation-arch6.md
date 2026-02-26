# Countryside Survey 2007: vegetation plot data, Great Britain Dataset Documentation

## What this dataset contains
- Two CSV files from Countryside Survey vegetation plots (2007) for Great Britain:
  - Vegetation Plot - Plot Information 2007.csv
    - Columns: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, COUNTRY, ENV_ZONE_2007, EZ_DESC_07
  - Vegetation Plot - Species List 2007.csv
    - Columns: YEAR, SQUARE_ID, PLOT_ID, AMALG_PTYPE, BRC_NUMBER, BRC_NAMES, NEST_LEVEL, ZERO_COVER, FIRST_COVER, TOTAL_COVER
- Species nomenclature follows Stace, 1997 (New flora of the British Isles).
- Data ownership and rights: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; all rights reserved.
- Usage acknowledgement required on outputs: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and related copyright notice.

## How to use and interpret
- Join the two files on key identifiers (YEAR, SQUARE_ID, PLOT_ID) to link plot metadata with species lists and cover figures.
- Use ENV_ZONE_2007 and EZ_DESC_07 to analyze environmental zoning effects on vegetation.
- Interpret species presence and abundance via:
  - BRC_NUMBER and BRC_NAMES for species identity
  - ZERO_COVER, FIRST_COVER, TOTAL_COVER for cover percentages
  - NEST_LEVEL for first-recorded occurrence context
- Outputs may include vegetation composition profiles, environmental-zone based summaries, and plot-level statistics, suitable for self-serve exploration or reporting.
- Outputs should follow the provided acknowledgement requirement in all copies, publications, and presentations.

## Data quality and caveats
- Data date: 2007 Countryside Survey, Great Britain.
- Methodology and data handling are described in accompanying references (notably Maskell et al., 2008; Countryside Survey Vegetation Plots Handbook).
- Potential considerations when using: verify plot-level identifiers (PLOT_ID, SQUARE_ID) for correct joins; ensure consistency with environmental zone coding (ENV_ZONE_2007, EZ_DESC_07); be mindful of the field definitions for cover metrics (ZERO_COVER, FIRST_COVER, TOTAL_COVER).

## Access, licensing and attribution
- All uses must acknowledge Countryside Survey data and include the copyright notice.
- Relevant publications and references provide methodological context and background.

## Related publications and references
- Countryside Survey website: general overview and methodology
- Carey et al. (2008) Countryside Survey: UK Results from 2007
- Countryside Survey Environmental Zones
- Maskell et al. (2008) Countryside Survey: Vegetation Plots Handbook
- Countryside Survey data documentation and metadata resources