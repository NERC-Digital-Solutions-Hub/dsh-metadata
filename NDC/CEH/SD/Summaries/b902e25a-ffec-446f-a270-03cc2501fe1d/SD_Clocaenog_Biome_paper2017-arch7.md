# Shrubland primary production and soil respiration diverge along European climate gradient

- Objective
  - Examine how shrubland primary production (aNPP) and soil respiration (Rs) respond to climate variation across a European gradient, using data from climate manipulation experiments.

- Study context and sites
  - Seven shrublands across Europe: United Kingdom (UK), The Netherlands (NL), Denmark (DK-B, DK-M), Hungary (HU), Spain (SP), and Italy (IT).
  - Part of the INCREASE network (Integrated Network on Climate REsearch Activities on Shrubland Ecosystems).
  - Climate manipulations began between 1999 and 2006, including nighttime warming and extended drought treatments.
  - Experimental design per site: plots of 4 m x 5 m with three plots for nighttime warming, three for drought, and three untreated controls (n = 9 plots per site, except variable across some sites).

- Experimental design details
  - Warming achieved with horizontally moving curtains triggered by dawn light sensors; curtains removed at sunrise.
  - Drought imposed by curtains to reduce nighttime precipitation reaching the vegetation (15–50% reduction in annual precipitation in drought plots).
  - Drought timing varied by growing season and site; curtains removed at high wind speeds (>10 m/s) to prevent damage.
  - Measurements spanned 1998–2012.

- Measurements and methodologies
  - Standing aboveground biomass (SB) and aboveground net primary productivity (aNPP)
    - SB estimated with the pin-point method (minimum 300 measurement points per site).
    - aNPP calculated from SB increments plus litterfall; site-specific rules applied (e.g., HU and UK adjustments due to deciduous/perennial vegetation).
    - aNPP converted to carbon by multiplying biomass by 0.5.
  - Litterfall
    - Collected monthly or at longer intervals using litter collectors; samples dried and weighed.
  - Soil respiration (Rs)
    - Measured with permanently installed soil collars (10 cm diameter; 3–13 cm edge above soil).
    - Vegetation inside collars removed to measure autotrophic and heterotrophic respiration.
    - Techniques varied by site: gas chromatography or portable infrared gas analysers; measurement frequencies ranged from monthly to biweekly or campaign-based.
    - Winter measurements paused to protect equipment; Rs up-scaled to annual values.
  - Climate data
    - Mean annual precipitation (MAP) and mean annual temperature (MAT) from Kröel-Dulay et al. (2015).
    - Gaussen Index (GI) of aridity calculated as GI = MAP / (2 × MAT), adjusted for treatment effects on MAP and MAT.

- Data products and structure
  - CLM_Biome_paper_annual.csv
    - 8 columns, 316 rows
    - Variables: Year, Country (UK, NL, DK-B, DK-M, HU, SP, IT), Treatment (Control, Drought, Warming), ANPP_gCm2 (g C m^-2 yr^-1), ANPP_gbiomass (g biomass m^-2), Biomass_gCm2 (g C m^-2), Biomass_gbiomass (g biomass m^-2), Rs_gCm2 (g C m^-2)
    - Notes: ANPP values derived from biomass with a 0.5 conversion factor; some years have missing measurements.
  - CLM_Biome_paper_aNPP_Rs.csv
    - 7 columns, 29 rows
    - Variables: Variable (aNPP or Rs), Country, Treatment, Gaussen_index_of_aridity, Treatment_difference_Gaussen_index, Mean_change_from_control_percent, SE_change_from_control_percent
    - Purpose: summarizes aridity-adjusted treatment effects and overall percent changes relative to control for drought and warming plots.

- Analytical approach and outputs
  - Climate treatment effects quantified as the average difference in aNPP and Rs between treatment and control plots.
  - Gaussen Index used to contextualize aridity and to compare treatment effects under aridity constraints.
  - Data enable cross-site, map-based visualization of how carbon gain (aNPP) and soil CO2 efflux (Rs) respond along the European climate gradient.

- Data usage considerations for GIS
  - Spatially distributed across multiple countries with different measurement protocols; harmonization notes apply (e.g., varying collar counts, measurement frequencies, and equipment).
  - Useful for map-based analyses of carbon flux components (aNPP, biomass, Rs) under warming and drought scenarios.
  - Aridity context via GI provides a consistent climate metric to relate site-specific responses to broader climate gradients.
  - Missing data by year/site are indicated; users should account for non-continuous time series in analyses and visualizations.

- Related literature
  - Foundational and methodological references supporting climate manipulation experiments, biomass estimation, soil respiration measurement, and aridity indices.
  - Key related works include Beier et al. (2004), Sowerby et al. (2008), Lellei-Kovács et al. (2011), de Dato et al. (2010), Kröel-Dulay et al. (2015), Penuelas et al. (2007), among others.

- Accessibility and provenance
  - Data underpin the paper by Reinsch et al. (2017) and are linked to the broader CLM/Biome research context; two primary CSV datasets accompany the publication for reuse and visualization.