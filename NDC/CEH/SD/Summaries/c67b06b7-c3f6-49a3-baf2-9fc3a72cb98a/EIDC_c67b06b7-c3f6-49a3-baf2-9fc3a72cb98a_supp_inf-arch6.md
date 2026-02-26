# Overview

- Large, nested-plot vegetation survey in Sabah, Malaysian Borneo, conducted July–November 2017.
- Sampled living vegetation across 49 plots in 18 sites: 14 fragmented forest set-asides within RSPO-certified oil palm plantations and 4 sites in continuous primary/ logged forest for comparison.
- Measured lianas, coarse woody debris (CWD), and a suite of habitat/landscape variables for each plot.
- Data are organized into six CSV files describing CWD, lianas, ground vegetation seedlings, site habitat/topography, soil parameters, and tree measurements.

# Study design and sites

- 18 sites total: 14 fragmented sites within oil palm plantations and 4 continuous forest sites (two primary continuous, one once-logged, one twice-logged).
- Sites are at least 1.5 km apart to minimize spatial autocorrelation; maximum inter-site distance ~192 km.
- Dominant soils: orthic acrisols and dystric cambisols.
- Fragmented sites represent variation in fragmentation degree, time since fragmentation, and vegetation structure under RSPO policies.
- Continuous forest sites include highly protected areas (e.g., Danum Valley, Malua Reserve).

# Transect and plot design

- Each site contains 2–3 circular plots (radius 30 m; total plots N=49).
- Fragmented sites: first plot boundary 25 m from forest edge; plots ≥25 m from any edge and 100 m apart.
- Plot layout aimed to maximize habitat heterogeneity when possible (line transects perpendicular to forest edge in fragmented sites).
- Nested plot design:
  - Main plot (30 m radius): recorded live trees and palms ≥25 cm DBH; coarse woody debris ≥25 cm diameter.
  - Subplot (20 m radius): trees/palms 10–<25 cm DBH; CWD 10–<25 cm.
  - Inner subplot (5 m radius): trees 2–<10 cm DBH.
- Seedlings and ground vegetation sampled with eight 1×1 m quadrats per plot, located 25 m from plot center along eight random bearings.

# Measurements and data collection

- Living trees and palms: DBH measurements grouped by size class; genus/species identifications in field; height estimated by eye for a subset; height validation with clinometer on a subset.
- Coarse woody debris (CWD): ≥25 cm and ≥10 cm classifications; decay states (1–5) per Harmon et al.; measurements include diameter at ends, length, and height as needed; boundary-crossing items recorded to boundary.
- Lianas: DBH measured for lianas entering crowns of trees ≥10 cm DBH; associated tree recorded; trees not identified; not used for biodiversity analyses.
- Ground vegetation seedlings: eight 1×1 m quadrats per plot; all rooted individuals <2 cm DBH recorded; vouchers collected; morphospecies identified to genus or species; native/exotic status recorded.
- Habitat/topography: leaf litter depth (measured at five points per quadrat), forest cover via densiometer readings (N/E/S/W); plot GPS coordinates and elevation; slope in four directions (10 m from plot center).
- Fragmentation metrics (landscape context): UAV-derived measures within 0.1–2 km buffers around each plot for surrounding forest area and forest–oil palm edge density; distance to nearest forest edge; time since fragmentation (years since adjacent oil palm establishment).
- Soil parameters (per plot): pH; total P; available P; total N; total C; organic C; C:N ratios (total and organic); gravimetric soil moisture.

# Data files and key contents

- CWD.csv: coarse woody debris items recorded per item; fields include site, plot, date, Dbh measurements, type (F/S/H), decay class, length/height, and notes.
- lianas.csv: liana records per tree association; fields include site, plot, date, tree ID, tree DBH, liana DBH, associated tree species, and notes; not suitable for biodiversity analyses without identifications.
- seedlings_groundveg.csv: ground vegetation morphospecies data per 1×1 m quadrat; fields include site, plot, date, quadrat number, morphospecies code, counts, percent cover, voucher info, identification, genus, species, family, life form, and native/exotic status.
- sites_habitat.csv: plot-level site metadata and habitat/topography context; includes coordinates, elevation, planting dates near oil palm (for fragmentation), forest type, disturbance, fragmentation flag, survey dates, densiometer and slope readings, leaf litter, and landscape-scale forest metrics (Within multiple buffers: area, edge counts, edge index).
- soil.csv: plot-level soil chemistry and properties; fields include pH, total phosphorus, available phosphorus, total nitrogen, total carbon, organic carbon, C:N ratios, moisture, and related measurements.
- trees.csv: individual tree/palm stems (for carbon stock analyses); fields include site, plot, date, individual code, ID (Genus species or PALM/UNKNOWN), family, DBH, height, number of associated lianas, notes, measured distances/angles (subset), and subplot radius.

# Data quality and notes for use

- Biodiversity analyses: exclude palms and lianas from lianas.csv and use ground vegetation data with identified taxa; seedlings and climbers in ground vegetation are identified.
- Forest cover calculation: percent canopy cover = 100 minus [Forest_cover_X readings × 1.04], where Forest_cover_X are densiometer readings in four directions.
- Tree height modeling: use stems with measured heights to build a height–DBH model; exclude stems with irregularities (e.g., multi-stemmed or leaning trees); for heights inferred from clinometer data, sum top and base measurements or adjust if base is at eye level plus 1.5 m.
- Height data: some stems have height estimates only for a subset; plan to derive heights for others using the recommended height modeling approach.
- Data provenance: field measurements followed established protocols; heights and cover percentages were consistently measured by the same observer per variable; QC noted as careful data checks.

# Practical considerations for data integration and analysis

- Data structure uses consistent site/plot coding (F a P b) across all files; settings for site_code, Site_plot_code, and related identifiers should be harmonized when merging datasets.
- Landscape fragmentation metrics rely on UAV-derived surrounding-landscape classifications and buffer-based summaries; ensure alignment of buffer radii and edge definitions with analysis needs.
- Nested plot design enables multi-scale biodiversity and carbon stock analyses, but ensure consistent subplot radii when aggregating metrics (30 m, 20 m, 5 m).
- Temporal context: field data collected across several dates within 2017; use date fields to align measurements and account for temporal variation in analyses.