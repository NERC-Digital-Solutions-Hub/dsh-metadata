REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

# Overview
- Intensive field experiment at Sourhope Farm (Scottish Borders) under the NERC Soil Biodiversity Thematic Programme.
- Focus on monitoring and analysing how different nutrient and management treatments affect biomass, soil chemistry, and plant community composition.
- Treatments include Control, Nitrogen, Lime, Nitrogen & Lime, and Biocide; two Control plots (C1, C2) used in analyses.
- Data collected include above-ground biomass (multiple harvests), soil surface pH (0–5 cm), botanical composition (Point Quadrat), and weather data from an Automatic Weather Station.
- Timeframe: measurements and observations spanning 1999–2001, with context from the Baseline Data Survey (1998).

# Experimental setup and data collection (relevant to GIS)
- Plot layout and treatments
  - 5 treatments across blocks, with two Control plots (C1, C2).
  - Subplots per plot designated as S, T, U, V for biomass sampling; five blocks provide replication.
- Measurements and sampling
  - Above-ground biomass: five summer cuts per year (May–September); clipping to ~6 cm, 0.5 m2 subplots, oven-dried and weighed.
  - Botanical survey: Point Quadrat method in July 2001 (grid of 100 cells per cell; ~25 pins per cell recorded species touches).
  - Soil pH: upper 5 cm sampled in Oct 2001; pH measured in distilled water.
  - Weather: data from site Automatic Weather Station (rainfall, radiation, temperature, soil moisture).
- Temporal coverage and data handling
  - 1999–2001 data presented with a focus on links to other years and comparability.
  - Normalisation of biomass data to the C1 treatment to identify treatment effects across years.
- Data quality and QA
  - Two surveyors contributed to the 2001 botanical survey with no significant differences between their results.
  - Use of Genstat 5 for ANOVA and PCA analyses to validate treatment effects and sample consistency.

# Key findings

## 2.1 Automatic Weather Station
- 2001 rainfall near long-term average after a very wet previous year.
- Radiation roughly constant; mean temperatures slightly lower; soil moisture content somewhat higher than in earlier years.

## 2.2 Above-ground biomass
- Clear hierarchy of biomass across treatments throughout 1999–2001.
- Peak biomass consistently in July or August.
- 2001 biomass higher than 2000, likely due to personnel changes and switch from manual cutting to mechanical shears.
- When normalised to C1, nitrogen and/or lime treatments show greater biomass, with the Nitrogen + Lime treatment being most effective.
- Statistical results:
  - Significant differences between improved (N and/or L) vs non-improved plots (ANOVA on ln-transformed data).
  - Significant interaction between treatment and year (but no significant block effect).

## 2.3 Soil pH
- Lime addition continued to raise surface soil pH (top 5 cm):
  - Limed plots: ~6.19
  - Nitrogen & Lime plots: ~6.38
- Nitrogen alone also raised pH, but less markedly.
- Control plots showed no significant pH change since baseline (1998).

## 2.4 Botanical composition
- 2001 Point Quadrat results: similar survey structure to 2000; surveyors showed no significant difference in results.
- Biodiversity and species composition:
  - Agrostis capillaris declined across all treatments in 2001; remained most abundant only in Control and Limed plots.
  - Festuca species (ovina, rubra) increased across all treatments; most frequent in Nitrogen and Biocide (F. ovina) and Nitrogen & Lime (F. rubra) plots.
  - Species associated with improved pastures (Festuca rubra, Poa pratensis) more apparent in fertilised plots, especially Nitrogen + Lime.
  - Species linked to poorer pastures (Anthoxanthum odoratum, Nardus stricta) more common in untreated Control plots.
  - Species richness: 24 species in unimproved treatments (Control/Biocide) vs 18 in Nitrogen + Lime plots, suggesting possible early biodiversity decline in more improved plots.
- Multivariate analysis (PCA)
  - Clear separation between plots treated with nitrogen and/or lime vs unimproved plots.
  - Improved plots show more extreme positions in PCA space, linked with higher abundance of Festuca rubra, Poa pratensis, etc.
- Biomass correlations with species abundance
  - Positive correlation: Festuca rubra and Poa pratensis with higher biomass.
  - Negative correlation: Anthoxanthum odoratum, Nardus stricta, bryophytes (Rhytidiadelphus squarrosus) with higher biomass.
  - Increased litter frequency in nitrogen- and/or lime-treated plots, indicating faster vegetation turnover with higher soil fertility.

# Site heterogeneity and spatial patterns

## 3.1 Variation in surface soil pH and plant community composition
- Spatial heterogeneity observed: columns E and F show relatively more acidic conditions, largely influenced by treatment mix (more Controls/Biocide in those columns).
- Underlying spatial pattern suggests pH-driven differences in community composition across the site.

## 3.2 Variation in vegetation biomass
- Biomass distribution shows outliers with low biomass at several plots, while higher biomass generally concentrates in central site plots (e.g., Nitrogen & Lime plot 2E; Lime plot 2C; Biocide plot 2D; Control 1 plot 2B).
- Positive correlation between surface soil pH and biomass.
- No significant differences in biomass across blocks (statistical result provided in Appendix).

# Implications for GIS data products
- Data layers to create
  - Biomass by plot, year, and sub-plot (0.5 m2 basis) for temporal mapping and trend analysis.
  - Soil surface pH (0–5 cm) by plot and year to map fertility gradients and treatment effects.
  - Botanical composition maps (species abundance and diversity indices) by plot/year; focus on dominant species shifts (Festuca rubra, Poa pratensis, Agrostis capillaris, etc.).
  - Biodiversity indicators derived from Point Quadrat data (species counts, hits per species, diversity indices).
  - Weather overlays (rainfall, temperature, soil moisture) linked to each plot for environmental context.
- Spatial and temporal capabilities
  - GIS-ready representation of the plot/block/subplot layout, including treatment assignments and column-level heterogeneity.
  - Time-enabled layers to compare 1999–2001 changes and assess treatment-by-year interactions.
- Data standards and QA
  - Ensure consistent units (biomass, pH, species hit counts) and normalization references (e.g., biomass relative to C1).
  - Document surveyor contributions and cross-check with Genstat PCA/ANOVA results to validate spatial patterns.
- Practical use
  - Map-based visualization of how nitrogen and lime inputs shift productivity and plant communities.
  - Identify regions of erosion of biodiversity in highly fertilised plots and potential habitat implications.
  - Support policy or farm-management decisions regarding liming and fertilization strategies in semi-natural pastures.

# Notable events and considerations
- Foot and Mouth Disease (FMD) restrictions in 2001 limited site visits February–May; field sampling adapted under veterinary guidelines, but core management activities (liming, pH measurements, biomass collection, etc.) continued as planned.
- Change of site Officer in Charge in May 2001; one biocide application (May) was missed, others completed as per plan.

# Conclusions
- Nitrogen and/or Lime treatments consistently increase above-ground biomass, with Nitrogen + Lime often yielding the strongest response.
- Lime raises soil pH substantially; soil fertility improvements correlate with shifts toward species associated with improved pastures, albeit with signs of reduced species richness in the most improved plots.
- There is clear spatial heterogeneity across the Sourhope site, influencing biomass and plant composition; central plots generally exhibit higher biomass, with local pH variations linked to community differences.
- The collected data are well-suited for GIS-based mapping and analysis, enabling spatially explicit visualization of treatment effects, soil conditions, and plant community dynamics over time.