# SUMMARY

## Context and Purpose
- Four years into the NERC Soil Biodiversity Thematic Programme at Sourhope (Macaulay Farm, Scottish Borders) focusing on above-ground productivity, plant community composition, and diversity in a long-term field experiment.
- Study examines three management processes with major botanical impacts: mowing, fertilisation (nitrogen and lime), and insecticide treatment; aims to understand both abundance and functional characteristics of plant communities.

## Site, Treatments, and Data Scope
- Location: Rigg Foot Experimental Site, Sourhope; 5 replicate blocks along downslope gradients; 6 main plots per block, subdivided into sub-plots with research groups using 0.5 m2 cells.
- Treatments (plot-level): Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime, Insecticide (Dursban 4 OPA); mowing to ~6 cm monthly May–Sept; insecticide applied after mowing; lime and nitrogen applied in spring; detailed yearly schedules in Appendices.
- Core data collected (1998–2002, with ongoing Phase I/II projects): 
  - Above-ground biomass (0.5 m2 sampling, pre-mow, dried and weighed).
  - Botanical surveys: baseline 1998; annual/biannual point analyses (0.5 m2 cell with 100-hole grid), bryophyte identification added in 2002.
  - Soil: pH (0–5 cm), soil moisture (theta probe) in 2002; additional soil and vegetative surveys (2000–2002).
  - Weather: on-site Automatic Weather Station since 1999; rainfall, radiation, and temperature data.

## Key Findings and Trends (2002)
- Biomass and productivity
  - Overall biomass productivity remained highest in plots with both nitrogen and lime, but 2002 saw declines across several treatments; Control 2 plots notably less productive than earlier years.
  - A general slope-related pattern: lower productivity on the upper blocks; Block 5 shows a larger decline than Block 1.
  - Normalised biomass (relative to Control 1) confirms the strongest gain with combined N & L; other treatments show varying declines.
- Soil chemistry and productivity
  - Lime raised soil pH significantly (toward ~7 in limed plots); nitrogen also raised pH but to a lesser extent.
  - Positive relationship between soil pH and biomass in the full dataset; however, within N- or Lime-only plots, the pH–biomass relationship weakens; with both N and Lime, the relationship may become nonlinear.
  - Negative relationship between soil moisture and pH; higher pH plots tended to be drier, which can influence productivity patterns.
- Plant community composition and diversity
  - Functional groups (CSR framework): stress-tolerators (S), competitive-stress-ruderals (CSR), and stress-ruderal/competitive-stress-ruderals (SR/CSR) dominated responses.
  - By 2002, CSR and SR/CSR groups expanded in N & L plots; stress-tolerant species increased in unfertilised plots.
  - Point Analysis: Festuca rubra and Poa pratensis (typical of improved pastures) were abundant in fertilised plots, while Festuca ovina and Anthoxanthum odoratum dominated unimproved plots.
  - Bryophytes (mosses and liverworts) increased across the site, particularly in unimproved plots; bryophyte hits rose from 6–11% (2000–2001) to ~20% in 2002.
  - Shannon diversity: 2002 index fell in N&L plots relative to baseline, while increases (to varying extents) occurred in other treatments; overall, diversity differences became statistically significant from 2000 onward.
- Insecticide effects
  - Insecticide plots show higher diversity in some contexts, but the link between reduced herbivory and diversity remains uncertain; observed patterns align with previous studies suggesting complex plant–herbivore interactions.
- Trampling effects
  - 2002 productivity drop in C2 plots partly attributed to trampling during 13CO2 pulses, indicating management-scale disturbances can markedly affect productivity.

## Spatial and Temporal GIS Considerations
- Spatial structure: block-based slope gradient affects productivity; clear spatial heterogeneity across the site that should be mapped (biomass, pH, moisture, species distribution).
- Multivariate drivers: interactions among management (N, Lime, Insecticide), soil chemistry (pH), moisture, and topography drive vegetation patterns; datasets support layered GIS analyses (map layers, time series).
- Temporal series: 1999–2002 biomass and biodiversity trends, plus annual point analyses; capacity to build time-series maps and change-detection visuals.
- Species and functional-group mapping: point-analysis results and PCA/loadings enable mapping of community-like clusters and treatment-associated assemblages.

## Data Products and GIS Implications
- Potential map layers
  - Biomass productivity per plot and per mowing event; year-over-year change maps.
  - Soil pH and moisture distribution maps by plot and across treatments, with correlations to biomass.
  - Species distribution rasters or presence/absence by treatment (focus on Festuca/Festuca rubra, Agrostis spp., Poa spp., bryophytes).
  - Functional-group distribution (S, CSR, SR/CSR) by plot and year.
  - Bryophyte density/abundance maps showing the broad rise across unimproved plots.
- Analytical visuals
  - PCA score plots and latent vector loadings interpreted as maps of key species groups.
  - Interaction plots showing pH–biomass relationships within and across treatments.
- Data quality and caveats
  - 2002 data gaps due to a weather-station malfunction; some 2002 periods were supplemented with Konza station data.
  - Amendments to plot activity logs and treatment schedules available in appendices; ensure metadata reflects 2002 missing intervals and data substitutions.

## Strengths and Limitations for GIS Use
- Strengths
  - Rich, multi-layered, longitudinal data across a well-replicated experimental design with explicit spatial arrangement (blocks, plots, sub-plots).
  - Combines abiotic (pH, moisture, weather) and biotic (biomass, species hits, bryophyte presence) datasets suitable for integrated spatial analyses.
- Limitations
  - Some years show treatment-wide declines and complex interactions that require careful modeling to separate treatment effects from site-level or climatic variation.
  - 2002 data gaps necessitate careful handling in time-series analyses; documentation and metadata are essential.

## Summary of Additional Notes
- The 2002 field work included major Phase II activities with labelled CO2 pulses and mobile labs; COVID-era-like access restrictions in 2001–2002 affected visits.
- Appendices provide detailed treatment schedules, species lists, weather data, and biomass rankings that underpin GIS data layers and analyses.

## Implications for GIS Practitioners
- Use this dataset to build multi-layer time-series maps showing how mowing, fertilisation, and insecticide treatments interact with soil chemistry and moisture to shape plant communities.
- Create spatial dashboards that visualize biomass productivity alongside soil pH, moisture, and bryophyte expansion to support policy, management, and public-facing visuals.
- Leverage CSR-based functional group classifications to map ecological strategies across treatments and over time, aiding interpretation of ecosystem function shifts.