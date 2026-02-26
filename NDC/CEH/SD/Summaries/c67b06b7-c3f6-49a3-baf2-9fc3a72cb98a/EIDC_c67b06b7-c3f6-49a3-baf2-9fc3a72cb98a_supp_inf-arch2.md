# Overview

- Field survey of living vegetation across 49 plots in 18 sites in Eastern Sabah, Malaysian Borneo (July–November 2017).
- Sites: 14 fragmented forest patches within RSPO-certified oil palm plantations (conservation set-asides) and 4 continuous forest sites for comparison.
- Targeted vegetation components: ground vegetation, tree seedlings, saplings, adult trees, and palms; plus lianas and coarse woody debris (CWD), with habitat and landscape context for each plot.
- Data are organized into six CSV files that cover vegetation, soils, and site/habitat context.

## Study design and sites

- Location: Sabah, Malaysian Borneo.
- Site composition: 14 fragmented sites in RSPO-certified oil palm plantations (conservation set-asides) and 4 continuous forest sites ( Danum Valley and Malua reserves).
- Fragmented sites vary by age since plantation establishment (8–26 years) and degree of fragmentation; continuous forests include fully protected primary forest and varying logging histories (once- and twice-logged, plus unlogged).
- Sites are spaced at least 1.5 km apart to reduce spatial autocorrelation; maximum site distance ~192 km.

## Plot design and sampling

- Within each site: 2–3 circular plots of 30 m radius (0.28 ha) for a total of 49 plots.
- Fragmented sites: plots begin 25 m from forest edge and are at least 25 m from edges; plots oriented to maximize habitat heterogeneity.
- Nested plot structure:
  - 30 m radius main plot: living trees and palms ≥25 cm DBH; CWD ≥25 cm diameter.
  - 20 m radius subplot: living trees and palms 10–<25 cm DBH; CWD 10–<25 cm.
  - 5 m radius subplot: living trees 2–<10 cm DBH.
  - Ground vegetation: eight 1×1 m quadrats located 25 m from plot center on randomized bearings.
- Data collected include diameters, species identifications, and, for a subset, height estimates and associated lianas.

## Data files and contents

- CWD.csv: coarse woody debris items; diameter, type (F/S/H), decay class, length/height, and subplot context.
- lianas.csv: liana DBH and association to the host tree; lianas are not identified taxonomically.
- seedlings_groundveg.csv: ground vegetation morphospecies data, abundance, ground cover, native/exotic status, life form, and voucher details.
- sites_habitat.csv: site-level habitat and landscape context (coordinates, elevation, forest type, disturbance, fragmentation metrics, fragmentation timing, and surrounding land cover data).
- soil.csv: soil chemistries and physical properties per plot (pH, phosphorus forms, nitrogen, carbon, C:N ratios, moisture).
- trees.csv: tree and palm stems with DBH, height (where available), species/genus, liana counts, and subplot context.

## Data collection and landscape context

- Fragmentation metrics (for fragmented sites) derived from UAV imagery within 0.1–2 km buffers around each plot:
  - Total forest area and an edge index (forest–oil palm boundary cells per forest area).
  - Straight-line distance to nearest forest–oil palm edge.
  - Years since fragmentation (time since first adjacent oil palm establishment).
- For continuous forests, forest area and edge metrics computed from Google Earth imagery.
- Additional site context: GPS-based coordinates, elevation, slope in four directions (N,E,S,W), leaf litter depth, and forest canopy cover via a spherical crown densiometer.

## Measurements and methods

- Trees and palms: DBH measured for individuals by size class; height estimated by eye for a subset; height validated with a subset using the tangent method.
- CWD: classified as standing, fallen, or hanging; diameter measurements at ends or stumps; decay class recorded.
- Lianas: DBH measured for lianas ≥10 cm that entered the crown of a tree ≥10 cm DBH; lianas linked to host trees.
- Ground vegetation: morphospecies identified to genus or species where possible; natives vs exotics determined; vouchers collected.
- Habitat and topography: leaf litter depth (cm) measured repeatedly within ground quadrats; canopy cover estimated in four directions; slope measured around plot center.
- Soil analyses: standardized chemistry (pH, total and available P, total N, total C, organic C, C:N ratios) and moisture content (gravimetric method).

## Data quality and notes

- Methodology follows established field protocols; height estimates and canopy cover measured by the same observer where applicable.
- Palms and lianas are not identified taxonomically and should be excluded from biodiversity/Community analyses.
- Height modeling: use stems with measured heights to fit height–DBH relationships; exclude irregular stems (e.g., multi-stemmed or leaning) from height model development.
- Forest cover from densiometer readings: convert to percent canopy with a specified transformation (multiply by 1.04, then subtract from 100).

## Usage notes for analysts monitoring environmental health

- The dataset provides standardized, multi-taxa vegetation and soil measurements across a landscape gradient of fragmentation, enabling temporal and spatial comparisons of environmental health and policy outcomes.
- Output formats include a structured, plot-level dataset with landscape context, suitable for cross-site comparisons, fragmentation analyses, and landscape-scale environmental health indicators.
- Care should be taken to exclude non-identifiable lianas and palms from biodiversity metrics; apply the specified canopy-cover conversion when estimating forest cover.
- When modeling tree heights, use only heights obtained directly or derived from robust height–DBH relationships, excluding irregular stems as recommended.