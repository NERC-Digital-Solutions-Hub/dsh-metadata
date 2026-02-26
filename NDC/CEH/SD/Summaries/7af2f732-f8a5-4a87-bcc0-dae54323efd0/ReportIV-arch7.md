# Soil Biodiversity Thematic Programme: Sourhope Site Summary

- Four-year monitoring at the Sourhope field site (Macaulay Land Use Research Institute, Sourhope, Scottish Borders) focusing on above-ground biomass production (productivity), plant species composition and relative abundance (diversity).

- Key management processes driving botanical change:
  - Mowing: regular cutting to ~6 cm height (since 1999) after fencing off grazing; promotes Festuca spp. over Agrostis spp.; associated with bryophyte expansion in unfertilised plots.
  - Fertilisation: nitrogen and/or lime increases productivity; lime strongly raises soil pH (to ~7.0 in summer 2002); possible moisture reduction and chlorosis in highly limed plots.
  - Insecticide (Dursban 4): possible increase in plant diversity through reduced herbivory, though evidence is circumstantial; observed shifts in species composition and functional groups.

- Site design and treatments (GIS-relevant layout):
  - Experimental design: 5 replicated blocks along downslope gradient; each block contains 6 main plots with randomized treatments; plots subdivided into 10 sub-plots; 0.5 m x 0.5 m sampling cells (S, T, U, V) used for data collection.
  - Treatments (plot-level): Control 1 (no treatment), Control 2 (no treatment), Nitrogen, Lime, Nitrogen & Lime, Insecticide.
  - Management tasks: annual mowing of entire site; application of lime, nitrogen, and/or lime; insecticide applied after mowing on designated plots.

- Data collection and GIS-relevant data layers:
  - Weather: on-site Automatic Weather Station (rainfall, temperature, radiation, moisture, etc.) from 1999 onward.
  - Above-ground productivity: annual biomass estimates per 0.5 m2 cell, aggregated per plot and per year (1999–2002).
  - Plant biodiversity data: point analysis surveys in 1998 baseline and 2000–2002 repeat surveys; 0.5 m2 sampling cell per sub-plot; 100-hole point frame per cell; species identifications including bryophytes to species level in 2002.
  - Soil properties: soil pH (5 cm depth), soil moisture (theta probe data in 2002 corners of analysis cells).
  - Species lists: extensive vascular plants and bryophytes identified; appendix includes full species lists and abundances by treatment and year.
  - Functional grouping: species categorized into stress-tolerators (S), competitive-stress-ruderal (CSR), and SR/CSR (and SR/C-S-R) to assess functional shifts.
  - Spatial patterns: observed along slope blocks with block-level and plot-level variation; C2 plots (first-year data collection) show trampling effects.

- Major results (highlights by theme):
  - Biomass productivity (1999–2002):
    - Long-term increase in biomass across all treatments relative to 1999 baseline.
    - Nitrogen and Lime treatments together give the highest productivity; unfertilised plots show relative declines over time.
    - 2002 saw a general decrease in biomass within several treatments compared with 2001; Block 1 (bottom of slope) showed larger relative declines than Block 5 (upper slope).
  - Relationship with soil chemistry and moisture:
    - Lime markedly increases soil pH (to ~7.0 in upper soil profile); nitrogen also raises pH but less strongly.
    - Positive general relationship between soil pH and above-ground biomass when considering all plots; the relationship is treatment-specific (positive in some fertilised plots, weaker or negative when both nitrogen and lime are applied).
    - Negative correlation between soil moisture and pH; drier, limed plots tend to have higher pH and higher productivity in some treatments.
  - Point Analysis and species composition:
    - Improved pastures dominated by Festuca rubra and Poa pratensis found more in Nitrogen and Lime plots; unimproved plots dominated by Festuca ovina and Anthoxanthum odoratum.
    - Bryophytes (mosses) increased across the site, particularly in unimproved plots, and are more prevalent with mowing and absence of grazing; bryophyte hits rose from 6–7% (2000) to ~20% (2002).
    - Agrostis capillaris and Agrostis vinealis declined by over 40% since 2000, across all treatments, possibly due to mowing/homogeneous cutting rather than a specific treatment effect.
    - Shannon diversity indices: declines in nitrogen & lime plots by 2002; other treatments show stability or modest increases.
    - Functional groups: S (stress-tolerators) expanded in unimproved plots; CSR and SR/CSR groups dominated in nitrogen-and-lime plots; SR/CSR groups reduced in lime- and insecticide-treated plots over time.
  - Other observed patterns:
    - Mosses and bryophytes increasingly contribute to biomass in several plots, particularly unimproved plots.
    - Litter hits increased in 2001–2002, especially in fertilised plots.
    - Trampling effects likely influenced 2002 biomass declines in C2 plots due to intense activity around 13CO2 pulses.

- Key implications for mapping and data use:
  - Spatial layers to map:
    - Plot-level treatments and block locations (5 blocks x 6 plots).
    - 0.5 m2 cell sampling points within sub-plots for biomass and species data.
    - Temporal layers for biomass (1999–2002), soil pH, soil moisture, and Shannon diversity by plot.
    - Species and functional-group distributions (S, CSR, SR/CSR) by treatment and year.
    - Bryophyte distribution and relative abundance over time.
  - Potential GIS analyses:
    - Temporal trend analysis of biomass across treatments and along slope, visualized as per-plot time series.
    - Correlation maps among soil pH, moisture, and biomass to identify treatment-specific responses.
    - PCA-based clustering of plots by species composition and treatment to illustrate divergence between improved vs unimproved plots.
    - Spatial pattern of bryophyte expansion relative to mowing regime and grazing exclusion.
  - Data considerations and limitations:
    - Some 2002 data gaps due to weather station issues; in 2002, data substitutions were made from a nearby station for missing periods.
    - C2 trampling effects noted; interpretation of 2002 biomass declines should consider this anthropogenic factor.

- References and supplementary material:
  - Appendices provide detailed species lists, site layouts, biomass time series, PCA loadings, and treatment-by-year summaries.
  - Core references underpinning the functional-group framework (CSR) and plant–insect interactions, useful for contextual GIS interpretation.

- Relevance for GIS specialists:
  - The project delivers a rich, multi-layered dataset ideal for map-based data products: treatment and block layouts, longitudinal biomass and biodiversity data, soil chemistry and moisture, and functional-group dynamics.
  - Enables creation of interactive maps and dashboards to explore how mowing, fertilisation, and insecticide influence productivity, species diversity, and functional composition over time and across the spatial gradient of the site.