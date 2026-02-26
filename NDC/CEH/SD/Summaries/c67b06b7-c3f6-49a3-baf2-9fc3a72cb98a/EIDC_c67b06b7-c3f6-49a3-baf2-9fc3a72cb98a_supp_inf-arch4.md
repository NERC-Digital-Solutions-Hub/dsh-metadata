# Overview

- Study aims and scope
  - Field sampling of living vegetation (ground vegetation, tree seedlings, saplings, adult trees, and palms) across 18 sites in Eastern Sabah, Malaysian Borneo (July–November 2017).
  - Comparison between 14 fragmented forest sites within RSPO-certified oil palm plantations and 4 sites in a large continuous forest for baseline comparison.
  - Additional measurements of lianas, coarse woody debris (CWD), and habitat/topographic variables per plot.
  - Data organized into six CSV files for broad accessibility and cross-linking.

- Study design and site context
  - Nested plot design: at each site, 2–3 circular plots of 30 m radius (0.28 ha), totaling 49 plots.
  - Fragmented sites: plots placed to capture edge effects (first plot 25 m from edge; subsequent plots ≥25 m from edges; 100 m spacing where possible).
  - Continuous forest sites: two primary continuous forest sites, plus variably logged sites for context.
  - Landscape fragmentation metrics derived from UAV imagery within 0.1–2 km buffers around each plot, including forest area, edge index, distance to nearest forest–oil palm edge, and years since fragmentation.

- Vegetation and soil measurements (plot-level)
  - Living trees and palms: dbh measurements in three concentric subplots (30 m plot, 20 m subplot for 10–25 cm dbh, 5 m subplot for 2–10 cm dbh); height estimated for a subset; taxonomic identification to genus or species where possible.
  - Coarse woody debris: recorded for ≥25 cm diameter in the main plot and ≥10 cm to <25 cm in the 20 m subplot; debris classified by decay class and orientation; length/height measured as applicable.
  - Lianas: dbh measured for lianas entering crowns of trees ≥10 cm dbh; association to the host tree recorded; lianas not identified to species.
  - Ground vegetation: eight 1×1 m quadrats per plot for seedlings and ground flora; all rooted individuals counted and identified to genus when possible; native vs exotic status assigned.
  - Habitat/topography: leaf litter depth, canopy cover (densiometer readings in four directions), GPS-based location/elevation, slope in four cardinal directions.
  - Soils: eight parameters per plot (pH, total P, available P, total N, total C, organic C, C:N ratios, soil moisture).

- Data files and contents
  - CWD.csv: coarse woody debris items with item-level details (site, plot, date, diameters, type, decay, length/height, notes, subplot radius).
  - lianas.csv: liana records linked to host trees (site, plot, date, tree ID, host tree dbh/height, liana dbh, and counts).
  - seedlings_groundveg.csv: ground vegetation morphospecies per quadrat (site, plot, date, quadrat, orientation, morphospecies code, counts, ground cover, voucher data, identification, life form, native/exotic).
  - sites_habitat.csv: per-plot metadata (location, elevation, fragmentation dates, forest type, disturbance, fragment status, survey date, forest cover readings, slope measures, litter depths, proximity to edges, and surrounding forest/edge metrics at multiple buffers).
  - soil.csv: plot-level soil chemistry and moisture data (pH, TP, AvP, TN, TC, OC, CtoN totals, moisture, CtoN organic).
  - trees.csv: individual tree stems (site, plot, date, unique ID, species, family, dbh, height, associated lianas, notes, distance and angle measurements for height estimation, subplot radius).

- Data handling and analysis notes
  - Biodiversity considerations: palms and lianas collected in lianas.csv were not identified to species and should be excluded from biodiversity analyses relying on species-level identifications.
  - Forest cover calculation: canopy cover percentage estimated from densiometer data by converting raw readings (Forest_cover_X) to canopy cover as 100 minus (reading × 1.04).
  - Height estimation guidance: where heights are missing, heights can be modeled from available stem dbh–height relationships using established methods; for clinometer-derived heights, use the tangent method and add eye-height (1.5 m) when base height is uncertain.
  - Quality control: data collection followed standardized protocols; height estimates and ground vegetation cover were consistently recorded by the same observer for each variable; data checked for errors.

- Practical considerations for data use
  - The six CSV files are designed for easy integration and cross-linking (e.g., linking trees.csv and lianas.csv via tree IDs; joining seedling/ground vegetation with plot metadata in sites_habitat.csv).
  - The dataset captures both local plot-scale forest structure and landscape-scale fragmentation context, enabling analyses of how fragmentation and edge effects influence vegetation structure, biodiversity, soil properties, and carbon-relevant metrics.
  - Sampled sites span a gradient from highly fragmented RSPO-set-asides to continuous primary forest, with explicit documentation of disturbance history and edge conditions to support robust comparative analyses.

- References and methodological context
  - Field protocols and methodological references include standard tropical forest census manuals, liana censusing standards, and ecophysiological measurement practices, ensuring methodological alignment with established tropical forest data collection.