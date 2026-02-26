# Soil Biodiversity Thematic Programme: Sourhope

- Four years into the NERC Soil Biodiversity Thematic Programme, focused on intensive study at the Sourhope field site (Macaulay Land Use Research Institute, Scottish Borders). The site monitors above-ground biomass (productivity), plant species composition, and relative abundance (diversity) under five treatments across a block-plot design.

## Site, treatments, and spatial layout (GIS-relevant)

- Experimental design: 5 replicate blocks along downslope environmental gradients; each block contains 6 main plots, subdivided into 10 sub-plots, with 0.5 m x 0.5 m cells used by research groups (S, T, U, V for data collection).
- Treatments (plot-level): 
  - Control 1 and Control 2 (no treatment)
  - Nitrogen (N)
  - Lime (L)
  - Nitrogen & Lime (N&L)
  - Insecticide (Dursban 4; previously Biocide)
- Site management: mowing of entire site to ~6 cm from May–Sept; lime and/or nitrogen applied in spring; insecticide applied after mowing.
- Data collection cells: baseline and annual point analyses use 0.5 m2 cells within subplots; additional subsampling and smaller plots for biomass, litter, bryophytes, and species lists.

## Data collected (GIS-ready data types)

- Climate and site weather: on-site Automatic Weather Station with long-term records (1999–2002), including rainfall, radiation, and temperatures.
- Above-ground biomass: annual biomass estimates per plot, derived from 0.5 m2 cell clippings dried and weighed (May–Sept sampling across five cuts per year).
- Soil properties: soil pH (measured at ~5 cm depth) across plots; 2002 soil moisture (theta probe) in point-analysis cells; spatially referenced to plots and cells.
- Vegetation surveys:
  - Point Analysis surveys (2000–2002): 100-hole grid over 0.5 m2 cell; species presence at 25 grid points per quadrat; bryophyte identification expanded in 2002.
  - Species lists: vascular plants and bryophytes identified (Appendix 3 lists numerous species by code).
  - Litter and biomass components: additional biomass samples and litter hits across years.
- Functional grouping: plants categorized into Stress Tolerators (S), Competitive-Stress-Ruderal (CSR), and SR/CSR groups; tracked over time to assess functional shifts.
- Temporal dimension: data collected annually (1998 baseline, 1999–2002) with year-to-year comparisons; 2002 includes a notable data gap due to weather-station issues (July–Nov missing data period partially substituted).

## Key findings (spatially informed patterns)

- Mowing effect (site-level disturbance regime):
  - Agrostis capillaris and Agrostis vinealis declined by over 40% since 2000; Festuca rubra expanded, especially in fertile (N/L) plots.
  - Bryophyte expansion (mosses) observed broadly, linked to consistent mowing height and reduced grazing; more pronounced where vascular productivity is lower.
- Fertilisation effect:
  - Nitrogen and/or lime increase productivity; the strongest biomass is in plots with both N and lime.
  - Possible productivity peak in N+L plots around 2002; higher soil pH (~7.0) linked to lime; potential moisture stress in very lime-fertilised plots.
  - Functional shift: N+L plots show a rise in competitive, less stress-tolerant species; unimproved plots favor stress-tolerant species.
- Insecticide effect:
  - Plant diversity patterns (Shannon index) show improvements in some plots with insecticide, but causal links to reduced herbivory are not definitive; patterns align with literature suggesting herbivore pressure can influence diversity.
  - 2002 data indicate bryophytes increase where insecticide or less-fertile conditions prevail; relationships are complex and context-dependent.
- Trampling and new sampling (C2 plots in 2002):
  - Productivity in newly sampled C2 plots fell relative to C1, likely due to trampling during intense sampling activity (e.g., 13CO2 pulses).
- Biodiversity composition and functional groups (2000–2002):
  - PCA and diversity indices show clear treatment differentiation; lime- and nitrogen-treated plots cluster separately from controls and insecticide-only plots.
  - SR/C-S-R and CSR groups shift across treatments; by 2002, significant differences among treatments in all three functional groupings.
- Spatial pattern on the slope:
  - Biomass productivity generally higher lower on the slope in some years, with block-position effects observed (e.g., Block 1 vs Block 5 differences).

## GIS applications and data products

- Spatial layers and analyses to generate:
  - Plot-level biomass over time (1999–2002), with year-by-year comparisons and treatment-normalized values.
  - Sub-plot and cell-level data: 0.5 m2 cells (S, T, U, V) for point analyses and bryophyte/vascular species occurrences.
  - Species distribution maps by treatment and year; bryophyte vs vascular plant distribution trends.
  - Soil maps: pH at multiple depths (with lime-treated plots showing higher pH), soil moisture patterns (2002 measurements linked to treatment and pH).
  - Functional-group distribution: S, CSR, SR/CSR shares per plot and year.
  - Weather and microclimate overlays tied to biomass and diversity outcomes.
  - PCA and latent vector loadings visualization to illustrate species groupings by treatment.
- Potential data products for policy, clients, and public audiences:
  - Interactive maps of productivity and biodiversity under different management regimes.
  - Time-series dashboards for biomass, soil chemistry, and species diversity across treatments.
  - Reports and GIS-ready datasets for cross-site comparisons and baseline-to-change analyses.

## Data quality and limitations (GIS considerations)

- Data fragmentation: multiple datasets across years, treatments, and survey methods; standardization needed for integration.
- Data coverage gaps: 2002 weather data gaps (July–Nov) due to station issues; some plots/subplots have limited sampling in certain years.
- Complexity of linking above- and below-ground processes requires careful interpretation when building map-based data products.
- Bryophyte identification improved in 2002; species-level mapping may require harmonization with earlier years.

## Endnotes and references (data sources)

- DetailedAppendices (1–8) provide site maps, treatment summaries, species lists, weather data, biomass time series, and PCA results that underpin GIS data products and visualization.