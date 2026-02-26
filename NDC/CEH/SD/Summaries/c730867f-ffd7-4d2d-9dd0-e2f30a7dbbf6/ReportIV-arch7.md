# Soil Biodiversity Thematic Programme: Sourhope Site Summary

- Purpose and scope
  - Four years into the NERC Soil Biodiversity Thematic Programme at Sourhope, a large field experiment investigates above-ground productivity, plant species composition, and relative abundance (diversity).
  - Focus on links between above- and below-ground processes, with botanical monitoring integrated alongside soil biota studies.

- Site layout and data architecture
  - Rigg Foot Experimental Site, Sourhope: 5 replicate blocks on a downslope gradient.
  - Each block contains 6 main plots, which are subdivided into 10 sub-plots; a 0.5 m x 0.5 m cell system is used to allocate plots to research groups.
  - Treatments mapped to plots; data collected at multiple resolutions (plot, sub-plot, and 0.5 m2 cells).
  - Treatments include both plot-level and site-level management tasks, with ongoing monthly mowing and targeted additions of nutrients or insecticide.

- Treatments and management
  - Site-level: mowing all vegetation to ~6 cm monthly (May–Sept).
  - Plot-level treatments (six main categories): Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime (N&L), Insecticide (formerly Biocide; Dursban 4 OPA).
  - Nutrient additions: Nitrogen (NH4NO3) and Lime (CaCO3) applied on spring schedules, with annual rates specified per treatment.
  - Insecticide applied after mowing on designated plots.
  - Data collection begins in 1999, with baseline and ongoing monitoring.

- Data collection and metrics
  - Above-ground productivity: regular biomass sampling from randomly selected 0.5 m2 cells, dried and weighed after mowing events (1999–2002).
  - Weather and site climate: continuous on-site Automatic Weather Station data (rainfall, radiation, temperature).
  - Botanical surveys and species identification: baseline (1998) and repeated Point Analysis surveys (2000–2002) using a 0.5 m2 cell with a 25-point grid; bryophyte identification expanded in 2002.
  - Soil properties: soil pH measured at ~5 cm depth across plots (and in central cells for point analyses) and soil moisture measured with a theta probe in 2002.
  - Additional small-scale surveys: biomass sorting by species, litter, mosses and liverworts counts, and various targeted vegetation cover assessments.
  - Data volumes and access: 11,621 soil samples by 2002; extensive appendices detailing treatments, species lists, weather, biomass, and point-analysis results.

- Key results and patterns (by theme)
  - Mowing effects
    - Dominant grasses shift: Festuca rubra expands in more fertile, lime/N-treated plots; Agrostis spp. (A. capillaris, A. vinealis) decline across most treatments, suggesting mowing homogenizes competition.
    - Bryophyte expansion: mosses increase across the site, especially under mowing with reduced disturbance; potential link to sward height maintenance (~6 cm).
  - Fertilisation effects
    - Productivity: nitrogen and lime increase above-ground biomass; plots with both N and Lime show the strongest productivity, though signs of potential plateau or stress at high pH and/or lower soil moisture.
    - Soil pH and moisture: liming raises soil pH toward ~7; higher pH correlates with certain shifts in biomass; moisture declines in fertilized plots, potentially contributing to stress under drought.
    - Functional group shifts: higher abundance of competitive (C-S-R) and related groups in N&L plots; stress-tolerant species dominate unimproved plots; overall functional composition shifts with fertility and disturbance regime.
  - Insecticide effects
    - Diversity responses: literature-supported expectation that insect herbivory can influence plant diversity; observed patterns suggest possible indirect benefits to some palatable species when herbivory is reduced, though causality is not firmly established.
  - Trampling and disturbance
    - C2 plots (insecticide context with sampling pulses) show reduced productivity potentially due to trampling during 13CO2 pulse experiments.
  - Community composition and diversity
    - Point Analysis: improved plots show higher frequencies of Festuca rubra and Poa pratensis; unimproved plots show greater Bryophyte hits and dominance by Agrostis spp. relative to lime-only or nitrogen-treated plots.
    - PCA of point data cleanly separates improved vs unimproved plots; lime-treated plots cluster with fertilized plots in several respects.
    - Shannon diversity indices: 2002 data show a 15% decline in diversity in N&L plots, while other treatments show stable or increased diversity.
  - Functional groups and CSR framework
    - Three main functional groupings (stress tolerators S, competitive-stress-ruderals CSR, and SR/CSR) account for a majority of species hits.
    - Over time (2000–2002), a shift toward C-S-R and SR/C-S-R in fertilized plots, with unimproved plots favoring stress-tolerant species.
  - Site-wide trends and limitations
    - Overall biomass production increased across treatments since 1999, but 2002 saw reductions in several plots; block position on slope influences productivity.
    - Bryophyte contribution to biomass increases in unimproved plots; disturbance removal and nutrient cycling changes influence long-term community dynamics.

- Data analysis approaches
  - Split-plot ANOVA to evaluate treatment, year, and interaction effects on shoot biomass (1999–2002).
  - Correlation analyses between soil pH, moisture, and biomass to explore physiological drivers.
  - Principal Components Analysis (PCA) on 2002 point-analysis data to differentiate treatments and identify key species contributing to treatment groups.
  - Layered interpretation of CSR functional-group dynamics to link plant strategy with environmental changes (pH, nutrients, disturbance).

- GIS and data product implications
  - Spatial mapping opportunities
    - Visualize treatment layouts, slope gradient, and block-level variability to understand spatial drivers of productivity and species composition.
    - Map biomass productivity across plots over time to identify hotspots of response to N, Lime, and N&L treatments.
    - Map soil pH and moisture gradients alongside vegetation data to explore spatial correlations with productivity and diversity.
  - Data integration considerations
    - Multiple resolutions: plot-level, sub-plot level, and 0.5 m2 cell data; require harmonization for GIS analyses and time-series visualization.
    - Temporal alignment: annual mowing events, treatment application dates, and multi-year surveys (baseline 1998; surveys 2000–2002) necessitate careful temporal layering.
    - Taxonomic resolution: ability to differentiate bryophytes and vascular plants; include CSR-functional grouping layers for enhanced ecological interpretation.
  - Potential GIS products
    - Time-series maps of above-ground biomass by treatment and block.
    - Spatial gradients of soil pH and moisture with overlay of plant functional-group distributions.
    - Species-hits maps from Point Analysis to show shifts in dominant species under each treatment.
    - Interactive dashboards linking mowing regime, fertilizer regime, insecticide application, and biodiversity indices.

- Data accessibility and references
  - Rich appendices accompany the report, including species lists (vascular plants and bryophytes), treatment summaries, weather data, biomass time series, and multivariate analyses.
  - Core literature cited includes Grime CSR theory, ecological plant strategies, and prior grazing/mowing studies, providing context for observed shifts in community composition and function.

- Practical notes for GIS use
  - When building map-based data products, align spatial units to the 0.5 m2 cell framework where feasible, and maintain links to plot and block identifiers for temporal analyses.
  - Document treatment boundaries and changes (e.g., 1999–2002 lime/nitrogen schedules, insecticide applications) to enable reproducible spatial analyses.
  - Consider including derived rasters for soil pH, soil moisture, and biomass productivity, along with attribute tables for species hits and functional-group classifications.