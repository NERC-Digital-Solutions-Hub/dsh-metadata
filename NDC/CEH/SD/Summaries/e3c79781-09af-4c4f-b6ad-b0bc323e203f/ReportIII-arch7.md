# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

## Overview
- Field experiment at Sourhope Farm, Scottish Borders, under the NERC Soil Biodiversity Thematic Programme.
- Focus on monitoring a large, replicated plot experiment (1999–2001) to contextualize detailed end-user studies.
- Treatments include Control (two plots), Nitrogen (N), Lime (L), Nitrogen + Lime (N+L), and Biocide.
- Data types collected: Automatic Weather Station data, above-ground biomass, soil pH, and botanical composition via Point Quadrat surveys.
- Notable disruptions in 2001 due to Foot and Mouth Disease (FMD) restrictions and a change in site officer; otherwise key management activities continued.

## Data and Methods
- Measurements and dates summarized for cross-year comparisons (1999–2001).
- Above-ground biomass: five summer harvests per year (May–Sept); biomass totals per plot calculated and log-transformed for analysis.
- Botanical composition: Point Quadrat surveys in July 2001 using a 100 x 100 grid per cell; species hits recorded and later analyzed with PCA.
- Species coding and survey procedures documented; cross-survey consistency checked (no significant assessor differences).
- Data analysis: split-plot ANOVA to test treatment effects; inter-year ANOVA for treatment changes; PCA to explore species associations with treatments.
- Weather data from the on-site automatic weather station; rainfall, radiation, and soil moisture tracked by year.

## Key Results

### 2.1 Automatic Weather Station
- 2001 weather began with rainfall near long-term average after a very wet prior year.
- Radiation levels similar to previous years; slightly cooler average temperatures.
- Soil moisture content higher in 2001 than in earlier years.

### 2.2 Above-ground Biomass
- Consistent treatment hierarchy in biomass production across the sampling period; peaks in July/August.
- 2001 biomass higher than previous years, likely due to a change in personnel and the switch from manual cutting to mechanical shears.
- Normalising all treatments to C1 reveals sustained positive impact of nitrogen and, to a lesser extent, lime on productivity.
- ANOVA on log-transformed biomass shows:
  - Significant differences between improved (N and/or L) vs. unimproved plots.
  - Significant interaction between treatment and year.
  - No significant differences between blocks.

### 2.3 Soil pH
- Lime addition continues to raise surface soil pH (0–5 cm depth):
  - Limed plots averaged pH 6.19.
  - Nitrogen + Lime plots averaged pH 6.38.
- Nitrogen alone also raises pH, but to a lesser degree.
- Control plots show little change since baseline (August 1998).

### 2.4 Botanical Composition
- July 2001 Point Quadrat protocol mirrored 2000; no significant difference between surveyors.
- Total number of hits in 2001 increased by 58% versus 2000, suggesting greater vegetation density, possibly from reduced grazing since 1998.
- Treatment effects on species composition:
  - Agrostis capillaris declined across all treatments in 2001 (no longer the most abundant in all plots).
  - Festuca species (ovina and rubra) increased across treatments; most frequent in N+Biocide and N+L plots, respectively.
  - Improved plots (N and/or L) show more perennials associated with improved pastures (Festuca rubra, Poa pratensis); untreated plots dominated by species typical of less fertile pastures (Anthoxanthum odoratum, Nardus stricta).
- Diversity changes:
  - Unimproved plots (Control, Biocide) had 24 species; N+L plots had 18 species, suggesting possible initial decline in diversity with higher fertility.
- PCA results:
  - Clear separation between improved (N and/or L) vs unimproved plots.
  - Latter plots with bryophytes and species such as Agrostis vinealis and Nardus stricta cluster together.
  - Increased frequency of Festuca rubra in limed plots linked to community shifts.
- Biomass and species abundance relationships:
  - Positive correlations: Festuca rubra and Poa pratensis hits rise with higher biomass.
  - Negative correlations: Anthoxanthum odoratum, Nardus stricta, bryophytes decline as biomass increases.
  - Increased litter in N and/or Lime treatments indicates faster vegetation turnover with higher soil fertility.

## Site Heterogeneity

### 3.1 Variation in surface soil pH and plant community composition
- Spatial heterogeneity noted: columns E and F on the slope show comparatively more acidic plots.
- Underlying differences persist, with lower pH in Nitrogen and/or Lime treated plots in these columns.
- This emphasizes spatially structured heterogeneity in pH and community composition across the site.

### 3.2 Variation in vegetation Biomass
- Total biomass shows outlier plots with unusually low biomass across treatments (examples: several Control, Nitrogen, Lime, Biocide plots).
- Higher biomass densities tend to be in more central site plots (e.g., Nitrogen + Lime in 2E, Lime 2C, Biocide 2D, Control 1 2B).
- Strong positive correlation observed between surface soil pH and biomass.
- No significant differences in biomass across predefined blocks, indicating spatial patchiness rather than block-level effects.

## GIS and Data-Product Implications
- The dataset supports spatially explicit maps of:
  - Biomass productivity by plot and sub-plot over time (1999–2001).
  - Surface soil pH distribution and changes due to lime and nitrogen treatments.
  - Species composition and diversity indicators (point-quadrat hits by species per plot).
  - Treatment effect maps to illustrate the impact of N and/or lime on productivity and vegetation structure.
- Data layers to consider:
  - Plot-level biomass (annual and cumulative 1999–2001).
  - pH (baseline vs. 2001 measurements, by depth if available).
  - Species abundance surfaces from Point Quadrats and PCA loadings.
  - Spatial heterogeneity indicators (column-based and central vs. edge effects).
- Temporal dimension: multi-year comparisons (1999–2001) enabling trend analyses and change detection.
- Caveats for GIS work:
  - FMD-related access restrictions in 2001 affecting sampling cadence and potential data gaps.
  - A shift in mowing method (manual vs. mechanical) in 2001 affecting biomass estimates; normalization against a reference plot (C1) recommended for temporal analyses.
  - Spatial heterogeneity across the site (not just plot treatments) should be incorporated into any spatial models or interpolation approaches.
- Practical outputs:
  - Interactive map showing treatment effects over time.
  - Spatially explicit PCA biplots or species distribution maps linked to plot locations.
  - GIS-ready tables of biomass, pH, and species hits by plot with year and treatment attributes.

## Additional Notes
- Documentation includes detailed tables (Tables 1–6) and figures (Figs 1–9) supporting analysis; species codes are provided for map-based labeling.
- Acknowledgements note personnel changes and field constraints that influenced data collection in 2001.