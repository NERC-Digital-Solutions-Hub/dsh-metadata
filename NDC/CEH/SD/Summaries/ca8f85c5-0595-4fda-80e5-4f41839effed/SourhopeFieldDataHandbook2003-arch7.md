# SOIL ANALYSIS OF RIGG FOOT, SOURHOPE

## Overview
- Multi-block soil and vegetation data from Sourhope (Block 4, Block 5) with additional ECOTRON plots.
- Contains horizon-level soil chemistry, moisture indicators, and soil profile descriptions, plus vegetation surveys by plot/subplot.
- Data are geolocated and organized for GIS use (plot-level, horizon-level, and ECOTRON subdivisions).

## Data structure and key content

### Block 4: Auger samples and vegetation (Block 4)
- Auger samples labeled 4A–4F with corresponding MLURI barcodes.
- Variables per sample:
  - Wt (mg)
  - %N
  - %C
  - C:N ratio
  - Ca, Na, K, Mg (meq/100 g)
  - %Moisture loss and %Loss on Ignition (LOI)
  - pH(H2O) and pH(CaCl2)
- Example ranges (approximate from the data):
  - N: ~0.51–0.58%; C: ~6.80–8.02%; C:N: ~12.6–14.3
  - Ca: ~1.01–2.96 meq/100 g; Na: ~0.12–0.15; K: ~0.58–0.81; Mg: ~0.58–1.59
  - %Moisture loss: ~4.29–5.15%; LOI: ~14.6–17.96%
  - pH(H2O): ~4.45–4.82; pHCaCl2: ~3.64–4.05
- Vegetation survey data present for Plot 4A–4F (values shown as per-subplot and plot totals; many entries are coded with presence/absence indicators and species counts).

### Block 5: Site details, soil profile, auger samples, and vegetation
- Site details: Block 5, grid NT8544019520; altitude ~315 m; slope ~5°; imperfect drainage; Brown forest soil with gleying; parent igneous/andesite materials.
- Soil profile (0–100 cm) with horizon sequence FH, H, Ah, AB, Bg, BCg, Cg; depth ranges and descriptive notes (moisture, structure, root presence, mottles, color, and boundary characteristics).
- Block 5 auger samples: 5A–5F with MLURI barcodes.
  - Variables include Wt (mg), %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH(H2O), pHCaCl2.
  - Notable variation across horizons and samples (e.g., Ca ranging from a few tenths to several meq/100 g; Mg from ~1.5 to ~3.5 meq/100 g; pH values generally acidic).
- Vegetation data (Block 5) by plot (e.g., Plot 5A, 5B, 5C, 5D, 5E, 5F) with subplots Ac, Ao, At, Br, Cp, Cxp, Dc, Df, Fo, Fr, Gs, Hm, Je, Lm, Lzm, Mc, Ns, Pe, Pp, Pt, Ra, Rr, Rs, Tr, Vc; species totals and occurrences recorded per subplot/plot.
- ECOTRON site data (ECOTRON PLOT 1)
  - Soil analysis: Wt 6.089 mg; %N 0.59; %C 8.22; C:N 13.83; Ca 2.76; Na 0.15; K 0.62; Mg 1.7; %Moisture loss 4.79; %LOI 17.42; pH(H2O) 4.79; pHCaCl2 3.82.
  - Vegetation survey: presence/absence and counts across Ac, Ao, At, Br, Cp, Cxp, Dc, Df, Fo, Fr, Gs, Hm, Je, Lm, Lzm, Mc, Ns, Pe, P, etc. with species totals by subplot and plot.
- ECOTRON SOIL SITE (a) and (b) sections provide horizon-level soil chemistry and vegetation counts for additional ECOTRON subdivisions, including MLURI barcodes, horizon names, and per-subplot species data.

### Spatial references and identifiers
- Block 5 site reference: grid NT8544019520.
- Block 4 auger samples linked to MLURI barcodes (4A–4F) for traceability.
- Block 5 horizon data tied to profiles FH, H, Ah, AB, Bg, BCg, Cg with depth intervals.
- ECOTRON PLOT 1 identified by MLURI barcode 603930 and associated soil/vegetation measurements.
- Vegetation data described with plot/subplot codes (e.g., Plot 4A, Plot 5A) and species totals.

## GIS implications and usage

- Multi-scale spatial structure:
  - Block-level context (Block 4, Block 5) with detailed horizon-level soil chemistry per auger sample, enabling spatial interpolation or zoned mapping of soil fertility indicators.
  - Plot- and subplot-level data allow high-resolution mapping of soil properties alongside vegetation composition.
  - ECOTRON plots add controlled-environment context for comparing field and experimental conditions.
- Potential map layers and analyses:
  - Soil chemical layers by horizon (N, C, C:N, Ca, Mg, K, Na, pH, LOI) across blocks and plots.
  - pH and base cation gradients (Ca, Mg, K) with depth and horizon depth, highlighting acidity and fertility patterns.
  - Vegetation presence/absence and species totals by plot/subplot, enabling habitat-type mapping and relation to soil gradients.
  - Overlay of treatments or experimental contexts (where applicable in Block 4/5 data) with soil and vegetation outcomes.
- Data integration considerations:
  - Horizon-specific data require careful alignment to spatial polygons representing plots and horizons.
  - Some entries contain missing values (noted as blanks or placeholder symbols); handle with appropriate imputation or exclusion in analyses.
  - Ensure consistent unit interpretation across records (meq/100 g for cations, LOI as a percentage, LOI and moisture loss as proxies for organic matter and moisture status).

## Notable observations for GIS stakeholders

- Soils exhibit acidic surface horizons with varying Ca and Mg across horizons and blocks; C and N contents and C:N ratios vary by horizon, influencing fertility gradients.
- Horizon sequences FH to Cg show systematic color and structure changes, with loamy textures and mottling in deeper horizons (Bg/BCg/Cg) in Block 5.
- Vegetation data accompany the soil profiles, enabling spatial correlation analyses between soil chemistry and plant communities across blocks and plots.
- ECOTRON data provide a controlled-context counterpart (soil chemistry and vegetation) to support comparative GIS analyses of field vs. experimental conditions.

## Takeaways for GIS work

- The dataset offers rigorously designed, geolocated, multi-scale soil and vegetation information suitable for creating map-based visualizations of soil gradients, plant communities, and treatment effects across Sourhope Blocks 4 and 5 and ECOTRON plots.
- When building GIS products, account for horizon and block variability, align plots/subplots to their spatial coordinates, and integrate historical context (drainage, land use) to interpret spatial patterns accurately.