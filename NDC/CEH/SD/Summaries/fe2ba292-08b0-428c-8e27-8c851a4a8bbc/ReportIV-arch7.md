Soil Biodiversity Thematic Programme: Sourhope Site Annual Report 2002

- Overview
  - Four years into the NERC Soil Biodiversity Thematic Programme, focused on a large field experiment at Sourhope, Scottish Borders.
  - Monitored changes in above-ground biomass (productivity), species composition, and relative abundance (diversity).
  - Three major management processes driving botanical changes: mowing, fertilisation (nitrogen and/or lime), and insecticide application; additional trampling on one subset.
  - Aimed to understand links between above- and below-ground communities and how management alters functional plant traits.

- Site layout and GIS-ready data structure
  - Rigg Foot Experimental Site: 5 replicate blocks along a downslope gradient.
  - Within each block: 6 main plots, subdivided into 10 sub-plots; 0.5 m x 0.5 m cells used for data collection.
  - Treatments allocated at random to plots; plot and cell-level data linked to specific research groups.
  - Treatments include: Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime, Insecticide (formerly Biocide).

- Treatments and data collection (yearly workflow)
  - Site management
    - Monthly mowing May–September to approximately 6 cm.
    - Insecticide (Dursban 4 OPA) applied after mowing on designated plots.
    - Fertilisation with nitrogen and/or lime applied in spring as per treatment.
  - Data collection routines
    - Automatic Weather Station on-site; daily/summary climate data from 1999 onward.
    - Above-ground productivity: annual 0.5 m2 cell samples in sub-plots S, T, U, V; samples dried and weighed.
    - Baseline and periodic botanical surveys: 0.5 m2 point quadrats (25-point baseline in 1998; 100-hole grid in 2000–2002); bryophyte identification enhanced in 2002.
    - Soil monitoring: soil pH at ~5 cm depth; soil moisture measured with theta probe (2002) across quadrant cells.
    - Additional small-scale surveys: vegetation cover in micro-squares, biomass dissections by species, and additional disturbance analyses (2000–2002).
  - Data repositories and access
    - Appendices and project reports provide treatment maps, species lists, weather, biomass time series, and point-analysis results.
    - Key references and appendices available via the Soil Biodiversity programme materials (e.g., website and CEH contacts).

- Key findings by theme (2002 results and patterns)
  - Mowing effect
    - Agrostis capillaris and A. vinealis declined by over 40% since 2000 across most treatments.
    - Festuca rubra expanded, especially in more fertile (lime and/or nitrogen) plots.
    - Mosses/bryophytes expanded across the site, aided by a ~6 cm sward height and lack of grazing; further reinforced in less fertile plots.
  - Fertilisation effect
    - Nitrogen and/or lime consistently increased productivity; plots with both N and lime showed the strongest productivity gains.
    - Some signs of diminishing returns in the highest-fertility plots (soil pH near 7.0; potential moisture limitation reducing growth during dry periods; chlorosis observed in lime-treated plots).
    - Functional shift: increased C-S-R (competitive-stress ruderal) species in N+L plots; stress-tolerant species favored in unimproved plots.
  - Insecticide effect
    - Diversity trends mirror earlier research suggesting complex plant-herbivore interactions; potential link between reduced herbivory and higher diversity is not conclusively proven, but changes in plant dominance patterns align with shifts in palatable species under altered herbivory pressure.
  - Trampling effect
    - In the C2 (trampling) plots, 2002 productivity decline linked to intense sample/13CO2 pulse activity; trampling likely suppressed growth in several plots.
  - Biodiversity and functional grouping (Point Analysis and PCA)
    - Two grass species (Festuca rubra and Poa pratensis) more common in improved plots; unimproved plots dominated by Festuca ovina and Agrostis spp.
    - Bryophytes (mosses/liverworts) increased in 2001–2002, especially in unimproved plots; bryophyte hits rose from 6.5% (2000) to ~20% (2002).
    - Shannon diversity rose in most treatments over time but fell in 2002 for N+L plots; diversification improved in insecticide-treated plots.
    - CSR functional-type analyses show a clear shift: N+L plots favor competitive and less-stressed types; unimproved plots favor stress-tolerators; SR/C-S-R groups decline with increased disturbance or lime use.
  - Spatial and temporal patterns
    - Across years, biomass generally increased from 1999 baseline but fell in 2002 relative to 2001 across several treatments.
    - A clear slope effect: Block 1 (low, bottom of slope) showed greater biomass increases in some years than Block 5 (upper, wetter, more acidic areas).
    - 2002 data indicate significant treatment-year interactions for biomass; lime- and nitrogen-related plots show distinct productivity patterns.

- GIS-ready insights and recommended map products
  - Spatial biomass maps by plot, block, and year (1999–2002), with normalisation to a common baseline (e.g., Control 1).
  - Change-detection maps showing relative biomass gains/losses year-over-year by treatment.
  - Map of soil pH and soil moisture by plot/cell, overlaid with biomass productivity to show correlations (e.g., pH–biomass gradient).
  - Species-hits distribution maps (dominant grasses and bryophytes) by treatment, year, and plot, including bryophyte expansion trends.
  - Functional-group distribution maps (stress-tolerators, competitive-stress ruderal groups) by plot/year.
  - PCA/ordination visualization outputs: spatially linked to plot locations to show treatment clustering and year-to-year shifts.
  - Trampling-influence overlays (C2 plots) showing productivity anomalies linked to disturbance events.
  - Data catalog: link plot-level data (biomass, point analysis hits, bryophyte counts, litter hits) to corresponding Appendices for quick reference.

- Data quality, gaps, and considerations for GIS use
  - Data heterogeneity: multiple data types (biomass, point hits, bryophytes, pH, moisture) collected at varying frequencies and resolutions; harmonise units and time frames for GIS analyses.
  - Weather data gaps in 2002 due to station issues; some 2002 figures substituted from Konza site data for missing periods.
  - Trampling data limited to specific C2 plots; interpret spatial effects with caution.
  - Bryophyte identification improved in 2002; ensure taxonomic resolution is consistent when comparing years.
  - Appendix-rich data availability: maps, species lists, treatment schedules, and detailed measurements available for integration into GIS workflows.

- Data sources and notable references
  - Site management and data collection details (Section 2; Appendices 1–8)
  - Weather and climatic data (Appendix 5)
  - Biomass and productivity time series (Appendix 6; 7)
  - Point Analysis results and bryophyte/species lists (Appendices 3, 8)
  - Discussion of mowing, fertilisation, insecticide, and trampling effects (Section 4)
  - Key literature cited (CSR functional types; plant responses to disturbance and nutrients)

- Practical implications for GIS projects
  - Build a relational data model linking plots, sub-plots, cells, treatments, and years to support multi-layer maps and time-series visualisations.
  - Use standardized spatial extents (plot and cell geometry) to enable consistent overlay across datasets (biomass, species hits, pH, moisture, litter).
  - Create interactive GIS visualisations to explore how management practices influence productivity, community composition, and functional trait distributions over time.
  - Consider incorporating the Appendix-embedded species lists and functional-group classifications to enrich map legends and analytics.