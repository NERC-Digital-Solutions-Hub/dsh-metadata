# SUMMARY

- Overview
  - Four years into the NERC Soil Biodiversity Thematic Programme at Sourhope (Scottish Borders) focused on monitoring above-ground biomass ( productivity ), plant species composition, and relative abundance (diversity) under a controlled grazing-exclusion regime.
  - Major drivers of botanical change identified: mowing, fertilisation (nitrogen and/or lime), and insecticide treatment; these interact with site-wide disturbance, moisture, and soil chemistry to shape community structure.

- Site design and GIS-relevant layout
  - Rigg Foot Experimental Site: 5 replicate blocks along a downslope gradient.
  - Within each block: 6 main plots, subdivided into 10 sub-plots; 0.5 m x 0.5 m cells used for micro-sampling.
  - Treatments (plot-level): Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime, Insecticide (formerly Biocide).
  - Management: monthly mowing to 6 cm May–September; insecticide (Dursban 4) applied after mowing on insecticide plots; lime and/or nitrogen added in spring as per schedule.
  - Geographic data gathered include plot locations, block structure, and year-by-year treatment assignments enabling spatial mapping of responses.

- Data collected and time frame
  - Climate and site weather: on-site Automatic Weather Station (rainfall, temperature, radiation, soil moisture proxies) since 1999; notable 2002 features include variable rainfall and a milder winter.
  - Above-ground biomass: annual biomass estimates per plot, derived from random 0.5 m2 cells within sub-plots, n = multiple harvests per summer (1999–2002); biomass data normalized to controls for cross-year comparison.
  - Plant surveys: baseline (1998) and annual July/August point-analysis surveys (2000–2002) using a 25-point quadrat within each plot cell to record species presence at each point; bryophytes identified to species in 2002; additional plots and micro-surveys (litter, cover) conducted.
  - Soil chemistry and moisture: soil pH measured at ~5 cm depth; theta-probe moisture measurements in 2002; pH also tracked in the plot centers and in cells used for point analysis.
  - Data volume: total site soil samples 11,621 since start; extensive dataset across biomass, species, bryophyte data, and weather (Appendices detail yearly counts and datasets).

- Key findings by functional drivers
  - Mowing effect
    - Dominant shift: Festuca spp. increases relative abundance; Agrostis spp. declines (approx. 40% reduction across years).
    - Mosses/bryophytes expand, possibly due to consistent sward height (~6 cm) and reduced disturbance from grazing.
    - Moss expansion more pronounced in unimproved plots; grazing exclusion and mowing homogenize disturbance and promote bryophytes.
  - Fertilisation effect
    - Nitrogen and/or lime yield higher productivity; plots with both N and lime show the strongest biomass increases.
    - Potential productivity peak in plots with both N and lime (soil pH ~7.0); high lime applications linked to drier soils and signs of plant stress (chlorosis) in 2002.
    - Relationship between soil pH and biomass: positive overall, with non-linear patterns when both N and lime are applied.
    - Functional shift: more competitive (CSR) traits expand under fertilised conditions; stress-tolerant (S) types prosper in unimproved plots.
  - Insecticide effect
    - Shannon diversity index highest in insecticide-treated plots, suggesting reduced herbivory may favor a broader set of species, though attribution to herbivory control remains tentative.
    - Trends align with prior insect-plant interaction work; diversity gains likely tied to changes in which plant species can persist under altered herbivory pressure.
  - Trampling effect
    - First-year trampling in C2 plots (2002) coincided with notable productivity reductions, likely due to intense sample collection/13CO2 pulse activities rather than a treatment per se.

- Spatial and temporal patterns
  - Biomass and productivity trends show an overall increase from 1999 baseline, but 2002 biomass declined relative to 2001 across most treatments; Block 5 (upper slope) exhibited the largest declines, with a consistent bottom-up gradient in productivity linked to slope position.
  - Principal Components Analysis (PCA) of point-analysis data clearly separates improved (fertilised/limed) vs unimproved plots; lime-treated plots cluster distinctly, with some nitrogen-treated samples resembling limed plots, while several nitrogen plots align more closely with controls and insecticide plots.
  - Bryophyte hits rose across treatments over 2000–2002, particularly in unimproved plots; vascular plant hits show shifts in dominance among Festuca vs Agrostis species, with Festuca rubra increasing in fertile plots.
  - Functional-group analysis (S, CSR, SR/CSR) indicates that post-treatment communities increasingly comprise stress-tolerant and competitive-stress categories, with significant treatment differences emerging by 2000–2002.

- Data products and GIS-ready insights
  - Potential map layers and visuals
    - Treatment map: plot-level layer showing Control, Nitrogen, Lime, Nitrogen+Lime, Insecticide.
    - Biomass time series maps: annual biomass per plot and per block (1999–2002), with normalization to controls for cross-year comparison.
    - Soil chemistry and moisture surfaces: pH at plot/cell level, moisture proxies (theta probe) by cell for 2002 and baseline references.
    - Species distribution layers: point-analysis results by year, including dominant grasses (Festuca spp., Agrostis spp.), bryophyte distributions, and key for CSR/S/SR categories.
    - Diversity and functional-group maps: Shannon diversity indices by plot/year; proportion of S, CSR, SR/CSR hits per plot/year.
    - Space-time evolution: PCA-based clustering visuals separating improved vs unimproved plots; temporal trajectories of key species and bryophytes.
  - Data readiness and standards
    - Large, multi-resolution dataset combining plot-, sub-plot-, and cell-level data with annual snapshots; important to align with GIS-ready formats (geo-locations, plot IDs, year, treatment, and measured variables).
    - Appendices provide detailed species lists, site activity, and measurement schedules that can support reproducible mapping and longitudinal analyses.

- Implications for GIS-based data products
  - The dataset enables robust map-based storytelling of how management decisions drive spatially structured plant community responses.
  - GIS products can support hypothesis testing on disturbance regimes, nutrient status, and biotic interactions by overlaying treatment layers with biomass, pH, moisture, and diversity metrics.
  - Temporal mapping (1999–2002) can visualize trajectories of productivity and community composition across the downslope gradient and slope-position blocks.

- Notes on data interpretation and caveats
  - Insecticide effects on diversity are inferred from Shannon indices; causality with herbivore suppression remains cautiously interpreted.
  - 2002 trampling/flux events (e.g., 13CO2 pulses) likely influenced C2 plot productivity; account for sampling-induced effects in spatial analyses.
  - Plant functional-type dynamics (CSR/S/SR) are tied to soil chemistry and disturbance regimes; spatially explicit data can illuminate where particular functional groups dominate over time.

- References and appendices (context for GIS data layering)
  - Appendices include species lists, treatment summaries, weather data, and biomass snapshots by plot; Appendix 5–8 provide raw data points, enabling the construction of multi-layer GIS datasets and time-series layers.