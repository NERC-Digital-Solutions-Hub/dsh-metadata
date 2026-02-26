# NERC Soil Biodiversity Thematic Programme: Sourhope Field Experiment – Summary

## Overview
- Four years since establishment of the NERC Soil Biodiversity Thematic Programme at the Sourhope field site.
- Main focus: monitor above-ground biomass production, plant species composition, and relative abundance (diversity) in response to management treatments.
- Three key management processes driving botanical changes: mowing, fertilisation (nitrogen and lime), and insecticide application.

## Study Design and Treatments
- Location: Rigg Foot Experimental Site, Sourhope; 5 replicate blocks along a downslope gradient.
- Structure: each block contains 6 main plots subdivided into 10 sub-plots; data collected from 0.5 m x 0.5 m cells within sub-plots S, T, U, V.
- Treatments (plot-level): Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime, Insecticide (formerly Biocide).
- Site management:
  - Mowing: monthly May–September to about 6 cm across the whole site.
  - Insecticide: Dursban 4 (chlorpyrifos) applied to Insecticide plots after mowing.
  - Fertilisation: Nitrogen and/or Lime applied in spring to designated plots.
- Data collection milestones:
  - Automatic Weather Station for weather data since Feb 1999.
  - Above-ground productivity: random 0.5 m2 cell sampled prior to each mow; biomass dried and weighed.
  - Baseline vegetation survey (July 1998) using a 0.5 m2 25-point quadrat.
  - Annual Point Analysis surveys (July/August) in 2000, 2001, 2002 using a 100-hole frame to record species at 25 fixed points; bryophytes identified to species level in 2002.
  - Soil monitoring: soil pH (at ~5 cm depth) and soil moisture (theta probe) at specified intervals; additional small-scale surveys for vegetation cover, litter, and biomass across various sub-samples.
- Research activity:
  - Phase I projects largely completed by 2002; Phase II projects conducted fieldwork with mobile labs for trace gas measurements.

## Data Collection and Methods
- Biomass measurements: harvests from five mowing occasions per summer (1999–2002), dried and summed per plot; data log-transformed for analysis.
- Statistical analyses: Split-plot ANOVA to test effects of Treatment, Year, and their interaction; consideration of block and subplot factors.
- Soil and moisture: soil pH measured in 2002 to reflect treatment effects; soil moisture measured in 2002 corners of each point-analysis cell; relationships explored between pH, moisture, and productivity.
- Vegetation analyses:
  - Point Analysis: 2000–2002 surveys to determine species frequency; bryophytes tracked; changes in dominance among grasses (Festuca vs Agrostis) and other taxa assessed.
  - Diversity: Shannon Diversity Index calculated across years (baseline 1998 and surveys 2000–2002).
  - Functional groups: plants categorized using CSR framework (C = competitors, S = stress-tolerators, R = ruderals) with intermediate forms; analysis of changes in functional group composition by treatment and year.
- Multivariate analysis: Principal Components Analysis (PCA) on 2002 point-analysis data after ranking species within treatments to explore community-level differences.

## Results at a Glance
- Biomass and productivity:
  - Sustained positive effect of fertilisation on above-ground biomass; plots receiving Nitrogen and Lime (especially together) show the highest productivity.
  - 2002 total biomass declined relative to 2001 across most treatments, with reductions ranging from about 14% to 31%; slope position also influenced productivity, with lower blocks typically showing larger declines.
  - Control plots (especially Control 2) tended to be less productive than fertilised plots over the study period.
- Relationships with soil conditions:
  - Lime markedly increased soil pH to about 7.0 in the upper soil profile; nitrogen increased pH modestly.
  - A strong negative correlation between soil moisture and soil pH observed; higher pH associated with drier conditions.
  - Positive associations between higher pH and biomass productivity across all plots; within some treatments (notably those with both N and Lime) the relationship was more complex and could be negative, suggesting non-linear dynamics as pH rises.
- Plant community composition and diversity:
  - Mowing effects: significant decline in Agrostis capillaris and Agrostis vinealis across most treatments, suggesting reduced suitability under a uniform mowing regime; Festuca rubra expanded in fertilised plots, highlighting a shift toward more fertile, competitive taxa.
  - Bryophyte expansion: bryophyte hits increased site-wide, with Rhytidiadelphus squarrosus becoming more abundant; mosses contributed a growing share of total hits, especially in unimproved plots.
  - Improved vs unimproved plots: Point-analysis clearly separated plots by management, with Festuca rubra and Poa pratensis more common in fertilised/improved plots; Festuca ovina and Anthoxanthum odoratum more common in unimproved plots.
  - Diversity trends: Shannon Diversity Index increased in most treatments after 1998 but showed a notable 15% decline in the Nitrogen & Lime (N&L) plots by 2002 relative to baseline; other treatments saw modest increases or smaller declines.
  - Functional groups: by 2002, significant treatment effects on CSR-related groups. CSR and SR/CSR tended to dominate in N&L plots, stress-tolerators (S) benefited in unimproved plots, and SR/CSR were reduced in lime- and insecticide-treated plots.
- Insecticide effects:
  - The link between reduced herbivory and increased plant diversity remains uncertain; results align with some prior work where herbivore suppression can increase diversity, but interpretation is cautious due to insufficient data on the exact insect-control impacts.
- Trampling effects:
  - In C2 plots (introduced in 2002), productivity declines attributed to trampling during intense sampling periods linked to 13CO2 pulse experiments.

## Spatial and Temporal Data Implications for GIS
- Spatial layout and resolution:
  - Data are organized across a 5-block by 6-plot grid with 0.5 m2 cells, enabling high-resolution mapping of biomass, species hits, and bryophyte distribution within and across plots.
- Layers to consider for map-based products:
  - Biomass productivity by plot and by 0.5 m2 cell, year-by-year (1999–2002).
  - Soil properties: pH (5 cm depth) and soil moisture, with treatment and block context.
  - Species distribution: frequency of key grasses (Festuca spp., Agrostis spp.), other vascular plants, and bryophytes; differentiate improved vs unimproved plots.
  - Functional groups: spatial distribution of CSR, S, C-S-R, SR/CSR groups across treatments and years.
  - Disturbance and management: mowing regime, lime/N, insecticide treatments represented as overlay layers.
- Temporal analysis:
  - Time series of biomass, pH, moisture, and diversity indices (1998 baseline; 2000–2002 surveys) to track trajectories under different management regimes.
- Data quality considerations:
  - A noted data gap in 2002 due to weather-station issues (approx. 6 weeks lost), with some corrections using nearby station data; this should be annotated in GIS products for transparency.

## Appendices and Data Resources
- Site map and treatment allocations (Appendix 1).
- Detailed treatment protocols (Appendix 2).
- Species lists for 2002 (Appendix 3).
- Site activity summaries and weather data (Appendices 4–5).
- Biomass, rank data, and point-analysis results (Appendices 6–8).
- Full data tables include biomass per plot, bryophyte occurrences, and 2002 PCA loadings.

## Practical Takeaways for GIS-Based Data Products
- Build multi-layered map products that integrate biomass productivity, soil chemistry/moisture, and species distribution across treatments and years.
- Use CSR-based functional group classifications to illustrate shifts in ecological strategies under different nutrient and disturbance regimes.
- Provide interactive time sliders to visualize year-over-year changes in species composition, bryophyte expansion, and diversity.
- Ensure data provenance and metadata accompany GIS outputs, including treatment codes, block layouts, and notes on data gaps (e.g., 2002 weather station outage and data substitutions).