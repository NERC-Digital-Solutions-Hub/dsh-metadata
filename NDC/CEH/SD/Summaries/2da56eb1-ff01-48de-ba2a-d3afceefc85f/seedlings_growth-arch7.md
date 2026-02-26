# Seedlings_growth.csv

## Overview
- Describes the AFEX fertilization experiment conducted within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, near Manaus, Brazil.
- Focuses on seedling measurements collected across fertilization treatments to understand plant responses to nutrient additions.

## Study area
- Location: KM41 reserve, within the BDFFP area, ~100 km from Manaus; coordinates around 02 24'S, 59 52'W.
- Climate: Humid, wet; mean temperature ~26.7°C; annual rainfall ~2200 mm; dry season July–September; peak rainfall March–April.
- Vegetation and soils: Dense Terra Firme rainforest; canopy heights 30–37 m (up to 55 m); clay soils (red-yellow podzols, yellow latosols) with high weathering, acidity, and low nutrients (WRB ferrasols).

## Amazon Fertilization Experiment (AFEX) design
- Treatments: Eight total (seven treatments plus a control) consisting of N, P, CATIONS, and combinations (N+P, N+CATIONS, P+CATIONS, N+P+CATIONS).
- Experimental layout: Full factorial design with four replicates per treatment, totaling 32 plots.
- Blocks and spacing: Four independent blocks, each at least 250 m apart.
- Plot details: Each plot sized 50 x 50 m; fertilization applied annually in three applications to reduce leaching/runoff; hand-spread within plots.
- Purpose: To assess how different nutrient additions influence seedling growth and health.

## Seedling sampling design
- Within-plot structure: In each 50 x 50 m plot, a central 30 x 30 m area contains four 1 x 1 m sub-plots.
- Replication and sampling: Four sub-plots per plot, leading to 16 sub-plots per treatment (across all four plots per treatment). Total sub-plots across all treatments: 128.
- Target individuals: Seedlings >20 cm tall with diameter at ground height (DGH) < 1 cm; palms and lianas excluded.
- Measurements per seedling: Height, diameter at ground height (DGH), total leaves, leaves with herbivory damage; mortality (0/1).
- Frequency: Data collected bimonthly for 12 months, yielding six sampling rounds per sub-plot (four during the rainy season, two during the dry season).

## Data spreadsheet (seedlings_growth.csv)
- Structure: 3409 rows, 13 columns.
- Columns and meanings:
  - CENSUS: Sampling number
  - MONTH: Month of sampling
  - DATA: Sampling date
  - TRT: Plot treatment (reference AFEX treatment)
  - BLOCK: Block number (1–4)
  - PLOT: Plot number (1–8 per block)
  - SUBPLOT: Subplot number (1–4)
  - INDIVIDUAL: Seedling tag
  - DGH: Diameter at ground height (mm)
  - HEIGHT: Height (cm)
  - TOTAL_LEAVES: Total leaves
  - LEAVES_WITH_HERBIVORY: Leaves with herbivory damage
  - MORTALITY: Death indicator (1 = dead, 0 = alive)

## GIS and data integration implications
- Spatial framework: Plot, sub-plot, and block identifiers enable spatial mapping of treatments and sampling effort within the KM41 area.
- Potential GIS products:
  - Map layers showing plot locations, treatment allocations, and replicate structure.
  - Temporal maps or animated visualizations of seedling metrics (DGH, HEIGHT, leaf damage) across months.
  - Overlay of environmental covariates (soil type, canopy height, topography) with fertilizer treatment effects.
- Data integration considerations:
  - Coordinate references for plot and subplot locations are not specified here; cross-linking with field GPS data is needed for precise GIS mapping.
  - Data cleaning and standardization necessary (units: DGH in mm; HEIGHT in cm; consistent date formats).
  - Handling data across multiple places (field notebooks, CSV) and aligning with the 128 sub-plots and 32 plots.

## References
- Chauvel A. 1982; Comita et al. 2007; Laurance et al. 1999; Lovejoy & Bierregaard 1990; Quesada et al. 2010, 2011; RADAMBRASIL 1978; Ranzani 1980.