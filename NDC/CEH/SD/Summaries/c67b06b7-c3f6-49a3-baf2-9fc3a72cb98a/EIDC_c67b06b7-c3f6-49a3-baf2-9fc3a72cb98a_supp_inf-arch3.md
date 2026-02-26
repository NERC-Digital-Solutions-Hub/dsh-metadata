# Overview

- A field-based vegetation survey across 18 sites in Sabah, Malaysian Borneo (July–Nov 2017) comparing 14 fragmented forest set-asides within RSPO-certified oil palm plantations to 4 continuous forest sites for a fragmentation gradient.
- Nested plot design: 49 plots total in 18 sites, with 30 m radius main plots and two smaller subplots (20 m and 5 m radii) to sample different tree size classes; edge-inclusive sampling in fragmented sites.
- Comprehensive data collected on living vegetation (trees palms, seedlings/ground vegetation), coarse woody debris (CWD), lianas, habitat/topography, and soils across all plots.
- Data are organized into six CSV files, each describing different components of the field measurements (see below for contents and structure).

## Study sites and sampling design

- Eastern Sabah sampling across 18 sites: 14 fragmented forest set-asides in RSPO plantations and 4 continuous forest sites for comparison.
- Plot layout: 2–3 circular plots per site (0.28 ha each), with plots in fragmented sites placed 25 m from forest edge and ≥25 m from other edges; plots at least 1.5 km apart to reduce spatial autocorrelation.
- Fragmentation metrics derived from recent UAV imagery within 0.1–2 km buffers (forest vs oil palm), including:
  - Total surrounding forest area
  - Forest–oil palm edge count (edge index)
  - Distance to nearest forest–oil palm edge
  - Time since fragmentation (years since first adjacent oil palm establishment)

## Plot-level vegetation surveys and measurements

- Living trees and palms (≥25 cm DBH) surveyed in the 30 m radius plot; smaller size classes (10–25 cm DBH) in a 20 m radius subplot; saplings (2–10 cm DBH) in a 5 m radius subplot.
- Height estimates by eye for a subset, with validation on 5% of stems using a clinometer; full height modelling advised for missing values.
- Tree identification in the field to genus (and species where known); palms identified as PALM; some specimens unidentified.
- Coarse woody debris (CWD) measured ≥25 cm in the 30 m plot and ≥10 cm to <25 cm in the 20 m subplot, with decay state (5-class scale) and dimensions recorded.
- Lianas measured as DBH ≥10 cm entering crowns of recorded trees; associated tree recorded; non-woody lianas excluded.
- Ground vegetation (tree seedlings, shrubs, climbers, herbs, ferns, graminoids) surveyed in eight 1×1 m quadrats per plot, located 25 m from plot centre along eight random bearings; individuals counted and root systems used to distinguish clonal units; vouchers prepared for identification.

## Habitat, topography, and landscape context

- Leaf litter depth measured in quadrats; forest canopy cover estimated with a spherical crown densiometer in four directions.
- Plot centre GPS coordinates, elevation, and slope (measured in four directions up to 10 m).
- Additional habitat metrics gathered for each plot (distance to edge, canopy/understorey structure, and landscape-scale forest metrics as described above).

## Soil parameters

- Eight soil metrics measured per plot: pH, total phosphorus (TP), available phosphorus (AvP), total nitrogen (TN), total carbon (TC), organic carbon (OC), C:N ratios (total and organic), and gravimetric moisture.
- Soil sampling: five topsoil cores (0–20 cm), mixed per plot and analyzed after drying; standard soil chemical methods applied (Molybdenum-blue for P, Walkley-Black for OC, dry combustion for N and C).

## Data structure and file contents

- CWD.csv: itemized records of coarse woody debris with site, plot, date, diameters, type (F/S/H), decay class, length/height, and subplot context.
- lianas.csv: records of lianas entering crowns of recorded trees (Tree_individual_no, Tree_ID, DBH, height, associated tree, etc.). Note: Palms and lianas were not identified; exclude from biodiversity analyses.
- seedlings_groundveg.csv: morphospecies-level data for ground vegetation in quadrats, including abundance, ground cover, voucher info, identification, life form, and native/exotic status.
- sites_habitat.csv: per-plot metadata including coordinates, elevation, first planting dates near oil palm, fragmentation timing, forest type, disturbance, fragment status, survey dates, canopy and slope metrics, litter depth, distance to edge, landscape buffers, and derived forest-edge indices.
- soil.csv: plot-level soil properties (pH, TP, AvP, TN, TC, OC, CtoN ratios, moisture).
- trees.csv: tree stems data (plot, site, date, unique stem ID, taxonomic ID, DBH, height, associated lianas, notes, distance to trunk, angles, subplot radius).

## Data quality, processing, and notes

- Biodiversity caution: exclude palms and recorded lianas from biodiversity/community analyses; ground vegetation morphospecies are identified to genus/species where possible.
- Forest cover estimation: canopy percent derived from densiometer readings by converting to canopy opening and subtracting from 100; specifically multiply Forest_cover_X by 1.04 before subtraction.
- Tree height estimation: build height models from stems with measured heights; exclude irregular stems (e.g., multi-stemmed, leaning) from model development; for heights missing, use tangent method calculations and adjust for observer eye height where necessary.
- Data governance and sharing: methodology aligns with established protocols; identical observer consistently measures specific variables; data have been checked for errors.

## Relevance for monitoring and policy insight

- Provides standardized, multi-taxa measures of forest structure and composition across fragmentation gradients, including:
  - Canopy structure and edge effects
  - Tree size distributions and species composition
  - Liana load on trees and associated biotic interactions
  - Ground vegetation diversity and exotic/native status
  - Soil fertility and moisture status
  - Coarse woody debris as a carbon stock and habitat component
- Landscape-scale fragmentation metrics derived from UAV imagery enable linkage between local plot metrics and broader forest configuration.
- Data formats and metadata are designed to support reuse in policy-monitoring contexts, including RSPO-related conservation set-asides and broader biodiversity assessments.
- The dataset supports evaluation of environmental health indicators over time, informing decisions on monitoring frameworks, data governance, inter-organisational data sharing, and standardised reporting through reports, dashboards, or policy briefs.