# Shrubland primary production and soil respiration diverge along European climate gradient

- Study across seven European shrublands (UK, NL, DK-B, DK-M, HU, SP, IT) within the INCREASE network, measuring standing aboveground biomass, litterfall, and soil respiration from 1998–2012.
- Experimental climate manipulations included nighttime warming and extended drought, implemented with moving curtains; treatments began at different years by site (1999–2006).
- Goals include understanding how shrubland primary production and soil respiration respond to warming and drought along a European climate gradient.

## Experimental design and sites

- Seven shrubland sites across the UK, NL, DK (two sites), HU, SP, IT; climate manipulations started 1999–2006 depending on site.
- Plot layout: at most sites, 4 m x 5 m plots with three plots per treatment (nighttime warming, extended drought, control); total n = 9 plots per site.
- Warming curtains triggered at dawn and retracted at sunrise; drought curtains reduced nighttime precipitation during rain events.
- Drought intensity reduced site precipitation entering plots by ~15–50% and lowered soil moisture; curtains removed at high wind speeds to prevent damage.

## Measurements and calculations

- Standing aboveground biomass (SB) and aboveground net primary productivity (aNPP)
  - SB estimated with the pin-point method; minimum ~300 measurement points per site.
  - Litterfall measured with random litter collectors; dried and weighed to derive biomass flux.
  - aNPP derived from SB increments plus litterfall (site-specific calculation rules; varies by site due to phenology).
  - aNPP converted to carbon by multiplying by 0.5 (typical C content in plant biomass).
- Soil respiration (Rs)
  - Measured with permanently installed soil collars; vegetation removed inside collars to capture autotrophic and heterotrophic respiration.
  - Sites used different measurement instruments (gas-tight lids with syringes, portable infrared gas analyzers, open/closed chambers) and differing collar numbers per plot.
  - Measurements paused in winter or under poor weather; annual Rs up-scaling performed.
- Data processing
  - Rs and aNPP values standardized to annual scales; units generally g C m-2 yr-1 or g C m-2 for annual measures.

## Climate data and aridity context

- Mean annual precipitation (MAP) and mean annual temperature (MAT) used to characterize sites; data drawn from Kröel-Dulay et al. 2015.
- Gaussen Index (GI) of aridity calculated as GI = MAP / (2 * MAT); MAP and MAT adjusted for drought and warming treatment effects when comparing control vs. treatments.

## Data and datasets (for reuse and governance)

- Two datasets underpin the paper:
  - CLM_Biome_paper_annual.csv
    - 8 columns, 316 rows.
    - Variables include Year, Country (UK, NL, DK-B, DK-M, HU, SP, IT), Treatment (Control, Drought, Warming), ANPP_gCm2, ANPP_gbiomass, Biomass_gCm2, Biomass_gbiomass, Rs_gCm2.
    - ANPP and Biomass reported as g C m-2 and g biomass m-2; ANPP values derived from biomass and litterfall, with carbon conversion factor 0.5.
  - CLM_Biome_paper_aNPP_Rs.csv
    - 7 columns, 29 rows.
    - Variables include Variable (ANPP or Rs), Country, Treatment, Gaussen_index_of_aridity (GI), Treatment_difference_Gaussen_index, Mean_change_from_control (%), SE_change_from_control (%).
    - Provides aridity-adjusted comparisons and percentage changes relative to control for drought and warming.
- Data coverage
  - Years: 1998–2012; measurements across all sites but some years have missing data (empty cells).
  - Treatments: Control, Drought, Warming; sites have differing sampling frequencies.

## Data quality, provenance, and governance considerations

- Methods and site-specific procedures are well-documented, enabling cross-site comparability, but:
  - Missing data (empty cells) and differing measurement intervals across sites require careful handling.
  - Variation in measurement instruments and collar numbers across sites affects comparability of Rs data; documentation needed for reproducibility.
- Provisions for data stewardship
  - Clear documentation of data collection methods, treatment implementations, and conversion factors (e.g., 0.5 for C content) supports data reuse.
  - Provisions for recording treatment impacts via GI-adjusted aridity metrics and treatment differences.
  - Potential for updating the datasets with future re-analyses if additional years or sites are added.

## Relevance for data stewardship and reuse

- The study demonstrates how long-term, multi-site climate manipulation experiments can be harmonized into comparable datasets with explicit metadata on treatments, site conditions, and measurement methods.
- The provided dataset schemas (annual biomass, aNPP, Rs, and aridity-adjusted treatment metrics) support secondary analyses of climate-ecosystem interactions, cross-site comparisons, and methodological assessments of respiration and productivity modeling.
- For future reuse, ensure alignment of units, clearly documented data transformations, and explicit handling of missing values.

## Related publications and context

- Core links to Beier et al. (2004), de Dato et al. (2010), Jonasson (1988), Kröel-Dulay et al. (2015), Lellei-Kovács et al. (2011), Mikkelsen et al. (2008), Penuelas et al. (2007), and Sowerby et al. (2008) for broader methodological and ecological context.
- Reinsch et al. (2017) Scientific Reports (paper under discussion) focusing on divergence of shrubland primary production and soil respiration along climate gradient.