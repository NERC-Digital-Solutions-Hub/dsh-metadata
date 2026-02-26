# The response of plants, carabid beetles and birds to 30 years of native reforestation in the Scottish Highlands

## Aim and context
- Assess ecosystem responses to native reforestation in the Scottish Highlands, focusing on restoration of Caledonian pinewood habitats.
- Examine how reforestation, grazing exclusion, and their interactions influence ecosystem functions and structure over time.
- Use standardized monitoring to support evaluation of environmental health and policy performance related to woodland restoration.

## Study design and sites
- Location: Central Scottish Highlands (Glen Affric and Glen Moriston) with adjacent landscapes of mature Caledonian pinewood, conifer plantations, heathland, and regenerating native forest.
- Sites: 14 fenced reforestation sites established 1990–2012, with sampling in 2018.
- Treatments and controls:
  - Forest status: Reforestation, Unforested, Mature forest.
  - Grazing status: Grazed, Ungrazed.
  - All combinations represented except Reforestation × Grazed (grazing pressure prevents establishment in the reforestation plots).
  - Three sites include associated mature forest plots (two grazed and two ungrazed per site, totaling five grazed and five ungrazed mature forest plots).
- Plot design: 10 × 10 m plots within each treatment category; plots within sites spaced 30–400 m apart.
- Plot counts and structure are captured in a dedicated data framework (52 plots across all treatments).

## Measurements and methods
Data collected to monitor ecosystem functioning and structure across treatments, using standardized approaches:

- Aboveground tree carbon
  - Measure diameter at breast height (dbh) for all trees (or stems for multi-stemmed individuals; dbh > 2.5 cm).
  - Apply species- and genus-specific allometric equations to estimate aboveground biomass.
  - Convert biomass to carbon using species- and group-specific carbon fractions (approximately 49–50%).
- Topsoil carbon and nitrogen (0–10 cm)
  - Collect three cores per plot; homogenize for analysis of total carbon and nitrogen; determine bulk density.
  - Lab analyses follow ISO standards; compute soil carbon and nitrogen stocks per unit area.
- Decomposition rate
  - Tea Bag Index: bury six pairs of teabags (green and rooibos) per plot at 8 cm depth; use 54–67 days incubation.
  - Dry, weigh to estimate final mass and derive decomposition rate constant (k).
- Soil invertebrate feeding
  - Bait lamina sticks (six per plot) with cellulose/s Wheat bran/activated charcoal substrate; insert in soil and monitor feeding over 30 days.
  - Record perforation-level feeding and compute proportional feeding indicators and overall stick-feeding (Eaten).
- Tree regeneration
  - In each plot, count young trees in DBH < 2.5 cm across height categories: <50 cm, 50–<100 cm, 100–<150 cm, ≥150 cm, by species.
- Ground-layer and moss height
  - Three 1 × 1 m quadrats per plot; measure ground-layer vegetation height and moss depth at five points per quadrat.
- Shrub and moss metrics
  - Shrub layer height: mean height across measurements per plot.
  - Moss depth: mean depth across measurements per plot.

## Data structure and outputs
- Data are organized into CSV files with clear metadata and field definitions:
  - plot_locations.csv: plot IDs, site associations, forest/grazing treatments, year established, grid references.
  - aboveground_carbon.csv: plot-level aboveground carbon (kg/m2).
  - topsoil_C_N.csv: topsoil carbon and nitrogen (%), bulk density, and derived carbon/nitrogen stocks (kg/m2).
  - decomposition_rate.csv: Tea Bag Index results (k) per plot and teabag.
  - soil_invert_feeding.csv: bait lamina feeding data (per perforation) and derived proportions.
  - seedling_regeneration.csv: seedling counts by species and height category.
  - shrub_height.csv: mean shrub height per plot.
  - moss_height.csv: mean moss depth per plot.
- Each file contains identifiers for Site, Plot type, and Treatment to facilitate cross-site comparability and meta-analyses.
- Appendix 1 details author roles across experimental design, fieldwork, and data collection, supporting provenance and reproducibility.

## Data quality, standardization and storage
- Methods are adapted from established studies (e.g., Warner et al., 2021) to ensure standardized, repeatable data collection across sites.
- Field plots are embedded in a hierarchical sampling design to enable comparison across reforestation, unforested, and mature forest states, with and without grazing.
- Datasets are stored and uploaded to appropriate data portals to enable long-term monitoring, transparency, and reuse.

## Relevance for environmental monitoring and policy
- Provides a standardized, long-term framework for evaluating native forest restoration outcomes, including carbon stocks, soil properties, decomposition, invertebrate activity, regeneration, and understory structure.
- Supports evidence-based assessment of restoration policy effectiveness for Caledonian pinewood habitats and deer/grazing management.
- The structure and open data availability facilitate integration with other environmental datasets (climate, herbivore pressure, biodiversity, etc.) to enhance the utility and value of the monitoring effort.