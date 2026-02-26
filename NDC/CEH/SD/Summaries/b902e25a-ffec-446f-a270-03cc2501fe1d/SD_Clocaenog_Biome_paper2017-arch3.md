Shrubland primary production and soil respiration diverge along European climate gradient

## Authors
- Sabine Reinsch; Eva Koller; Alwyn Sowerby; Giovanbattista de Dato; Marc Estiarte; Gabriele Guidolotti; Edit Kovács-Láng; György Kröel-Dulay; Eszter Lellei-Kovács; Klaus S. Larsen; Dario Liberati; Roma Ogaya; Josep Peñuelas; Johannes Ransijn; David A. Robinson; Inger K. Schmidt; Andrew R. Smith; Albert Tietema; Jeffrey S. Dukes; Claus Beier; Bridget A. Emmett
- Affiliations span UK, Ireland, Denmark, Netherlands, Hungary, Spain, Italy, Spain, Norway, Germany, Denmark, and the United States (various ecological and forestry institutes and universities)

## Experimental design
- Location: seven European shrublands (UK, NL, DK-B, DK-M, HU, SP, IT) as part of the INCREASE climate change network
- Timeframe: 1998–2012
- Treatments: control, drought, and warming (nighttime warming) with three plots per treatment per site (total n = 9 plots per site)
- Setup: 4 m x 5 m plots; nighttime warming achieved with moving curtains; drought via rainfall exclusion; curtains retracted under high wind
- Climate manipulations began at different sites (1999–2006 depending on site)

## Measurements and methods

### 3.1 Standing aboveground biomass (SB) and aboveground net primary productivity (aNPP)
- SB: estimated annually using the pin-point method with at least 300 measurement points per site
- Biomass: derived from SB and related measurements; litterfall collected monthly or per site schedule
- aNPP: calculated from SB increments plus litterfall; site-specific rules applied (e.g., HU deciduous dynamics; UK perennial dominance)
- Conversion: aNPP and biomass reported in g C m^-2 y^-1 and g biomass m^-2; carbon content assumed as 50% of biomass

### 3.2 soil respiration (Rs)
- Soil collars: permanent collars (10 cm diameter; 3–13 cm edge exposed) to measure vegetation-free soil respiration (autotrophic + heterotrophic)
- Measurements: varied by site (number of collars per plot; measurement technique differences across sites)
  - NL: gas-tight lid with syringe; SP, IT, DK-M, UK: portable infrared gas analyser with closed chamber
  - HU: open gas exchange system with soil respiration chamber
- Temporal pattern: monthly to biweekly campaigns; paused in winter/poor weather
- Upscaling: Rs scaled to annual values

### 4. Climate data and aridity
- Climate inputs: mean annual precipitation (MAP) and mean annual temperature (MAT) from Kröel-Dulay et al. (2015) with adjustments for drought and warming effects
- Aridity index: Gaussen Index (GI) calculated as GI = MAP / (2 × MAT); adjustments made for treatment-induced changes

## Effects of climate treatments
- Comparative assessment: ecosystem carbon gain (aNPP) and Rs differences calculated as averages relative to untreated controls for drought and warming
- Purpose: quantify sensitivity of shrubland productivity and soil carbon efflux to warming and drought across a European climate gradient

## Data structure and availability

### 5. Details of data structure
- Two datasets underpin the paper

### 5.1 CLM_Biome_paper_annual.csv
- 8 columns, 316 rows
- Variables include:
  - Year (A)
  - Country (UK, NL, DK-B, DK-M, HU, SP, IT) (B)
  - Treatment (Control, Drought, Warming) (C)
  - ANPP_gCm2 (D) and ANPP_gbiomass (E)
  - Biomass_gCm2 (F) and Biomass_gbiomass (G)
  - Rs_gCm2 (H)
- Notes: ANPP and biomass reported as g C m^-2; units derived from biomass × 0.5

### 5.2 CLM_Biome_paper_aNPP_Rs.csv
- 7 columns, 29 rows
- Variables include:
  - Variable (A): aNPP or Rs
  - Country (B)
  - Treatment (C)
  - Gaussen_index_of_aridity (D)
  - Treatment_difference_Gaussen_index (E)
  - Mean_change_from_control_percent (F)
  - SE_change_from_control_percent (G)

## Related publications
- Beier et al. 2004; de Dato et al. 2010; Jonasson 1988; Kröel-Dulay et al. 2015; Lellei-Kovács et al. 2011; Mikkelsen et al. 2008; Penuelas et al. 2007
- Reinsch et al. (2017) Shrubland primary production and soil respiration diverge along European climate gradient (Scientific Reports, in press at the time)