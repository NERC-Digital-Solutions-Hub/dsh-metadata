# The response of plants, carabid beetles and birds to 30 years of native reforestation in the Scottish Highlands

## Overview
- Multisite study assessing ecosystem responses to native reforestation in the Scottish Highlands, focusing on plant communities, soil functioning, and associated biota.
- Data collected in 2018 across 14 fenced reforestation sites and matched unmanaged/unforested areas, with a subset including mature Caledonian pinewood for reference.
- Data are organized into multiple datasets documenting aboveground carbon, soil carbon and nitrogen, decomposition, soil invertebrate feeding, seedling regeneration, and vegetation structure.

## Study design and scope
- Location: Glen Affric and Glen Moriston, central Scottish Highlands.
- Treatments: 
  - Forest status: reforestation, unforested, mature forest (where present).
  - Grazing status: grazed, ungrazed.
  - All combinations represented except reforestation × grazed (deer grazing pressure prevents this pairing in the landscape).
- Plot design: 10 × 10 m plots within each treatment combination; 14 reforestation sites plus associated unforested areas and 5 mature forest plots (across 2–3 sites).
- Sampling framework: Hierarchical design with:
  - Reforestation plots matched to nearest unforested grazed and nearest unforested ungrazed plots for comparison.
  - Mature forest plots included where available, with paired grazed/ungrazed plots.
  - Plot distances ranged from 30 to 400 m within sites.
- Data collection year: 2018, with methods adapted from prior studies (Warner et al., 2021).

## Data collected and key variables
- Aboveground tree carbon: measured using DBH for each tree/stem; species-specific allometric equations applied; biomass converted to carbon using standard concentrations.
- Topsoil carbon and nitrogen: samples from top 10 cm; three cores per plot for carbon, nitrogen, and bulk density; ISO-based CN analysis.
- Decomposition rate: Tea Bag Index (k) calculated from buried green tea and rooibos tea bags (6 pairs per plot) after 54–67 days.
- Soil invertebrate feeding: bait lamina sticks deployed in plots; feeding evidence recorded per perforation and per stick, with a summary proportion and overall Eaten indicator.
- Tree regeneration: all seedlings with dbh < 2.5 cm counted in height categories per species.
- Ground-layer and moss height: three 1 × 1 m quadrats per plot to measure mean shrub layer height and moss depth.
- Additional plant community metrics include seedling density by species/height category and shrub/moss depth measurements.

## Data structure and file descriptions
- plot_locations.csv: coordinates and plot metadata; site and plot identifiers; forest and grazing statuses; planting year and plot type.
- aboveground_carbon.csv: per-plot total aboveground tree carbon (kg/m2).
- topsoil_C_N.csv: topsoil carbon and nitrogen metrics, including bulk density and derived stocks (kg/m2).
- decomposition_rate.csv: decomposition rate constant (k) per teabag per plot.
- soil_invert_feeding.csv: bait lamina results per plot, including per-bait perforation feeding and overall Eaten status.
- seedling_regeneration.csv: seedling counts by species and height category per plot.
- shrub_height.csv: mean shrub layer height per plot.
- moss_height.csv: mean moss layer depth per plot.

## Data processing, methods, and standards
- Aboveground biomass: dbh-based allometric equations for Betula, Salix, Alnus, Sorbus, and others; phosphorus-free constants; carbon content assumed (broadleaves 49%, conifers 50%).
- Topsoil analyses: ISO 10694 and ISO 13878 protocols for carbon and nitrogen; CN analyser used; bulk density derived from dried, sieved samples.
- Decomposition: Tea Bag Index procedure with standardized post-collection drying and weighing.
- Soil invertebrate feeding: standardized bait lamina protocol with fixed substrate; exposure and perforation readings used to compute feeding activity.
- Tree regeneration and ground-layer data: standardized height categories and vegetation height metrics.
- Data dictionaries and structure: explicit field names and units provided for each CSV; references to prior methodological work (Warner et al. 2021; Muukkonen & Mäkipää 2006; Zianis et al. 2005; ISO standards).

## Data quality, limitations, and considerations
- Some plots could not provide soil cores for all treatments, resulting in reduced sample sizes (e.g., n = 12 for certain soil measurements in specific categories).
- Natural heterogeneity in drainage and topography affected establishment success and plot-level outcomes.
- The dataset emphasizes cross-site comparability through a paired, matched design but still reflects site-specific contexts (e.g., deer pressure, historical land use).

## Metadata, governance, and accessibility
- Comprehensive documentation accompanies the data (plot-level IDs, site coordinates, treatment categories, and measurement timelines).
- Data are organized into clearly named CSV files with accompanying methodological notes; references to foundational studies and standard protocols are provided to ensure reproducibility.
- Appendices document roles of authors involved in experimental design, fieldwork, and data collection, supporting transparency of data provenance.

## Implications for data leadership and data strategy
- Demonstrates the importance of a well-documented, hierarchical, multi-variable data architecture to compare restoration outcomes across treatment combinations and reference conditions.
- Highlights need for standardized ontologies, consistent measurement protocols, and metadata that enable future data discovery, reuse, and integration with external datasets.
- Illustrates handling of data gaps and site heterogeneity, including explicit reporting of sample sizes and limitations to inform robust inference and governance.
- Provides a model for long-term data stewardship in landscape-scale ecological projects, with clear data products (carbon stocks, soil health indicators, decomposition rates, biodiversity proxies) that can inform policy, monitoring programs, and adaptive management.