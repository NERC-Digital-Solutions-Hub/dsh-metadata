# Plot-level forest structure, carbon density and tree species richness data from restoration sites in South and Southeast Asia

- Purpose and scope
  - Synthesis of plot-level data to compare naturally regenerating forests with actively restored (planted) forests.
  - Metrics include above-ground carbon density, basal area, and tree species richness.
  - Data span 13 landscapes across South and Southeast Asia, with plots surveyed from 0 to 50 years after disturbance and 0 to 30 years since planting.
  - Total dataset covers 91.6 hectares of restored forest across 451 plots.

- Data sources and coverage
  - Derived from published studies (15 papers) plus unpublished data from collaborators in the FOR-RESTOR network.
  - Landscapes include 12 landscapes from literature plus data additions for two landscapes and one additional unpublished landscape.
  - References and cross-study synthesis are compiled in Tables S4, S5, and S10.

- Variables and data extraction
  - Extracted from published studies (and collaborators): site condition, disturbance type, time since disturbance, time since planting, census date, restoration type, and forest structure/diversity metrics (basal area, above-ground carbon density, tree species richness).
  - Timeframe alignment: paired actively restored plots with naturally regenerating plots that have similar time since disturbance; when data were averaged in papers, used available means; in some cases, used proximate pairings reported in studies.
  - Disturbance categories prior to restoration: logging (clear fell and selective), agriculture, plantation, fire, mining, drainage.
  - Site condition at planting: Plantation, Forest, Open (includes grassland/shrub understory).
  - Exclusions: studies where treated and naturally regenerating plots were not comparable (e.g., natives planted into exotic plantations); two papers excluded from analysis for comparability reasons but included in tables.

- Data processing and study-specific assumptions
  - Time-related data often incomplete; authors document processing and assumptions (e.g., approximating census timing, equating time since disturbance to time since planting in some cases).
  - Examples of processing notes include:
    - Matching time since disturbance/planting for pairings (e.g., 10–20 years with specific study notes).
    - Assumptions to estimate plot age or census date when not explicitly reported.
  - Tables 1 and 2 (not shown here) detail processing steps, assumptions, and aggregation procedures used to build community-level summaries.

- Metrics and data structure
  - Primary metrics per plot: basal area (m2 per plot or per ha), above-ground carbon density (Mg C ha-1), and tree species richness (number of species per plot).
  - Plot characteristics: total plots = 451; total area = 91.6 ha.
  - Temporal scope: plots span 0–50 years since disturbance and 0–30 years since restoration planting.

- Analytical approaches
  - Three analyses conducted in a meta-analytic framework:
    1) Actively restored vs naturally regenerating plots
       - Use restoration response: log(active restoration m / natural regeneration m) for each metric m.
       - Linear mixed-effects models with mean time since disturbance as a fixed effect; study as a random effect; weighting by total area surveyed.
    2) Basal area change over time
       - Compare changes in basal area over time between actively restored and naturally regenerating plots, with old-growth data for reference when available.
       - Linear mixed-effects model: basal area ~ restoration type * time since disturbance + (time since disturbance | plot); weights by plot area.
       - Only three landscapes provided time-series data for this metric.
    3) Recovery completeness relative to old-growth
       - Use recovery-completeness log-response ratio: restored or regenerated m / old-growth m for each metric.
       - Linear mixed-effects model with time since disturbance and restoration type as fixed effects; study as random effect; weighted by area.
  - Software and provenance: analyses performed in R (versions 4.0.4 and 4.1.0).

- Data presentation and tables
  - Table S4: Studies included in the active restoration vs natural regeneration analysis.
  - Table S5: Summary values by study/landscape and by metric, including means and standard errors.
  - Table S10: Number of studies and plots contributing to each analysis (counts of studies, plots, and areas).

- Implications for GIS-oriented use
  - Provides a harmonized set of plot-level forest structure, carbon, and biodiversity metrics across multiple restoration landscapes, suitable for map-based visualization and spatial comparison.
  - Highlights heterogeneity across studies (different disturbance histories, site conditions, and measurement protocols) and the need to account for this in GIS analyses.
  - Useful for mapping recovery trajectories, comparing restoration approaches, and identifying landscapes with stronger carbon or biodiversity responses.
  - Cautions on data gaps and comparability due to varying reporting and approximations in study-specific processing.