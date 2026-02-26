# REPORT III
RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

## Overview
- Intensive field study at Sourhope Farm (Scottish Borders) as part of the NERC Soil Biodiversity Thematic Programme.
- Documents monitoring across 1999–2001 to provide context for detailed studies and enable year-to-year comparisons.
- Site management affected in 2001 by Foot and Mouth Disease restrictions and a change of site officer; some sampling proceeded under a formal protocol and a 2001 Site Management Plan.

## Data collected and main measurements
- Automatic Weather Station (2001): headline measures show rainfall near long-term average; radiation stable; average temperatures slightly lower; higher soil moisture than previous years.
- Above-ground biomass (1999–2001):
  - Clear treatment hierarchy; peak biomass in July/August.
  - 2001 biomass higher than prior years, likely due to personnel changes and switch from manual cutting to mechanical shears.
  - Biomass data normalized against C1 within each year; analyses show significant differences between improved (N and/or Lime) vs. non-improved plots; significant year × treatment interaction; no significant blocks effect.
- Soil pH (top 5 cm):
  - Lime treatment raises pH to 6.19 (limed plots) and 6.38 in Nitrogen & Lime plots.
  - Nitrogen alone also raises pH but less so; control plots near baseline 1998 values.
- Botanical composition (Point Analysis, July 2001 vs July 2000):
  - Higher total hits in 2001 (58% more) across treatments; surveyor differences not significant.
  - Treatment differences: Agrostis capillaris declines with treatment; Festuca spp. increases across treatments; improved plots show more Festuca rubra and Poa pratensis; unimproved plots retain species like Agrostis vinealis, Nardus stricta, Anthoxanthum odoratum.
  - Diversity: 24 species in unimproved treatments vs 18 in Nitrogen & Lime plots (possible early onset of reduced diversity in improved plots).
  - PCA shows distinct separation of nitrogen- and/or lime-treated plots from control/biocide plots; biomass correlates with shifts toward Festuca rubra and Poa pratensis.
  - Biomass correlates with species composition: higher biomass linked to F. rubra and P. pratensis; lower abundance of A. odoratum, N. stricta, bryophytes with increased biomass.
  - Increased litter in plots receiving nitrogen and/or lime, indicating faster vegetation turnover with higher soil fertility.
  
## Site heterogeneity and spatial patterns
- Variation in surface soil pH and plant communities:
  - Columns E and F exhibit comparatively more acidic plots; underlying spatial heterogeneity linked to slope orientation and plot composition (notably many Control or Biocide plots in those columns).
- Variation in vegetation biomass:
  - Outlier plots with low biomass across treatments (e.g., specific A/B plots) and higher biomass in centrally located plots (e.g., Nitrogen and Lime plot 2E; Lime plot 2C; Biocide plot 2D; Control 1 plot 2B).
  - Strong positive correlation between surface soil pH and biomass.
  - No significant biomass differences between experimental blocks.

## GIS-relevant insights and potential data products
- Spatial structure:
  - Experimental design comprises 5 blocks, each containing plots with six treatments, plus sub-plots (S, T, U, V) per plot; data are suitable for multi-layer GIS representations (plots, sub-plots, blocks).
- Potential map layers:
  - Biomass: map annual and cumulative above-ground biomass by plot/sub-plot; identify treatment effects spatially.
  - Soil pH: pH map by plot (top 5 cm) with lime and nitrogen effects highlighted; detect spatial heterogeneity (columns E/F).
  - Botanical composition: species abundance maps per plot or per sub-plot; PCA-based or cluster-based plant community maps showing shifts by treatment.
  - Climate/soil moisture: interpolate weather station data to support context maps of growing conditions.
- Analysis-ready relationships:
  - pH–biomass relationship maps (positive association) for assessing fertility-driven productivity.
  - Species-driven biomass indicators: maps showing areas where Festuca rubra and Poa pratensis dominate and correlate with higher biomass.
  - Temporal GIS view: 1999–2001 time series of biomass by treatment to assess dynamics, including the 2001 shift due to management changes.
- Spatial statistics and modeling:
  - Assess spatial autocorrelation (Moran’s I, variograms) of pH and biomass.
  - Spatial regression or geostatistical models linking pH, biomass, and species composition across the field.
  - Identify and map there-within-field heterogeneity patterns (e.g., slope-related effects, column-based variation).

## Data provenance, quality, and limitations
- Baseline data and site description available in Baseline Data Survey (1998).
- 1999–2001 measurements documented with explicit schedules (Table 1) and a published annual workflow (e.g., mowing, sampling dates, and methods).
- Inter-surveyor reliability tested for Point Quadrat surveys; no significant surveyor bias found (NS p-value).
- Field disruptions in 2001 due to FMD restrictions; some activities were delayed or adjusted per protocol; one biocide application missed.
- Data normalization and statistical analyses (e.g., ANOVA on log-transformed biomass) support comparisons across treatments and years; blocks showed no significant effect in the main biomass analyses.

## End notes and context
- The Sourhope field experiment provides rich, plot-level data on how nitrogen, lime, and their combination influence biomass, soil chemistry, and plant community composition under grassland management.
- Spatial heterogeneity within the site and clear treatment-driven vegetation shifts offer substantial value for GIS-based visualization, mapping, and spatial analysis of agricultural and ecological productivity.