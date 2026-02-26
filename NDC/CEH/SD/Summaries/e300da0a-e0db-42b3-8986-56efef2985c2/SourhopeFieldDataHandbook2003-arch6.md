# SOURHOPE FIELD DATA HANDBOOK 2003

## Overview
- Presents soil and vegetation data from Sourhope field sites used in the Soil Biodiversity Programme, with detailed records by blocks (notably Blocks 4 and 5) and an Ecotron plot.
- Data types include soil profiles (horizons and description), horizon-specific laboratory analyses, auger-derived soil chemistry, vegetation surveys by plot/subplot, and climate context.
- Designed to support multi-block, multi-treatment research on soil–vegetation interactions and responses to environmental perturbations.

## Data Architecture and Key Entities
- Core data components:
  - Soil profiles by block with horizon designations (e.g., LF, FH, H, Ah, AB, Bg, BCg, Cg) and descriptive texture/structure notes.
  - Laboratory soil analyses by horizon and by auger samples (e.g., %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH H2O, pH CaCl2).
  - Auger sampling data (4A–4F for Block 4; 5A–5F for Block 5) with site replicates, chemical/physical metrics, and pH measurements.
  - Vegetation surveys by plot with species counts and totals; linkage to horizon context and block-level descriptors.
  - ECOTRON plot data (soil analysis and vegetation survey) for comparative perturbation experiments.
- Data identifiers:
  - MLURI barcodes for each horizon and sample (e.g., FH 603951; Ah 603953; 4A 603918; ECOTRON 603930).
  - Depths and horizon labels standardized across blocks (LF, FH, H, Ah, AB, Bg, BCg, Cg, etc.).
- Contextual site details:
  - Block 5 soil series: Brown forest soil with gleying; parent igneous/andesite materials; site altitude and slope context.

## Block 4 Data Highlights
- Soil profile (0–95 m depth) shows a progression from fibrous surface horizons (LF, FH) through dark Ah with sandy silt loam texture to Abg and Bg/ Cg horizons, indicating organic-rich upper layers and horizon differentiation.
- Key horizon descriptors:
  - LF and FH: fibrous, moist, sparse mineral grains, extensive fine roots.
  - H: black matrix with amorphous texture; weak blocky structure.
  - Ah: dark reddish-brown, sandy silt loam; friable; many fine roots; volcanic/igneous stone content noted.
  - Abg/B sg/C gx: progressively more structured horizons with mottling and angular blocky/platy structure; presence of igneous stones.
- Soil chemistry (horizon-wise):
  - %N ranges broadly across horizons; %C high in surface horizons (Ah) and declines with depth.
  - C:N ratios typically in mid-teens to low 20s at surface horizons, decreasing with depth.
  - Exchangeable Ca, Mg, K show horizon and block-to-block variability; Ca generally higher in upper horizons, Mg and K vary by horizon.
  - pH(H2O) generally acidic (roughly 4.5–5.0 across horizons); pH CaCl2 consistently lower.
  - %Moisture loss and LOI values highest in surface horizons, declining with depth.
- Auger samples (4A–4F) corroborate horizon trends:
  - %N and %C present with relatively high C at some horizons; C:N around 12–14 in several samples.
  - Ca and Mg vary across auger points; Na often minimal or not reported; K and Mg present in modest amounts.
  - pH measurements reflect acidic to slightly more acidic conditions in some auger points.
- Vegetation data (Block 4):
  - Plot-level totals show diverse taxa presence/absence with varying dominance across plots (A–D; B–F).
  - Indicator taxa and community composition described, aligned with upland grassland contexts.

## Block 5 Data Highlights
- Soil profile (0–100 cm) across horizons LF, FH, H, Ah, AB, Bg, BCg, Cg.
- Horizon descriptors reflect progressive enrichment in clay and mottling with depth; presence of igneous stones; organized horizon structure (massive to angular blocky).
- Soil chemistry (Block 5):
  - %N and %C recorded per horizon; C:N ratios span roughly mid-teens to low 20s, higher in surface horizons.
  - Exchangeable Ca shows notable values across horizons; Na generally low; K and Mg present with block-to-block variability.
  - %Moisture loss and LOI indicate substantial organic content in surface horizons and reduction with depth.
  - pH(H2O) and pH(CaCl2) show acidic to moderately acidic conditions; CaCl2 pH values typically near 3.8–4.1 in affected horizons.
- Auger samples (5A–5F) corroborate Block 5 horizon data:
  - %N and %C show consistent litter-derived signals; C:N ratios typically around 12–14 in many auger samples.
  - Ca, Mg, K, and Na exhibit horizon- and sample-specific variability; moisture loss and LOI reflect organic matter content.
  - pH measurements mirror Block 4 patterns with acidic readings in many horizons.
- Vegetation data (Block 5):
  - Plot-level species totals and presence-absence patterns show community composition across plots 5A, 5B, 5C, 5D, 5E, 5F, indicating habitat heterogeneity and horizon-linked vegetation differences.

## ECOTRON Plot Data
- Soil analysis (ECOTRON PLOT 1):
  - Wt (soil mass) ~6.1 mg; %N ~0.59; %C ~8.22; C:N ~13.83; Ca ~2.76 meq/100g; Mg ~1.7 meq/100g; moisture loss ~4.79%; LOI ~17.42%; pH H2O ~4.79; pH CaCl2 ~3.82.
- Vegetation survey (ECOTRON PLOT):
  - Plot A–F with various species totals and indicators; overall richness varies by sub-plot, consistent with perturbation experimental design.

## Climate Context and Data Resources
- The Sourhope site is a core ECN site; climate context supports interpretation of soil–vegetation dynamics and perturbation responses.
- Climate data include monthly mean temperatures (1993–2003) from the Sourhope weather station; climate described as humid, underpinning interpretation of soil and vegetation processes.

## Data Management, Archiving, and Access
- Field and laboratory data collected with standardized procedures; soil samples archived for long-term storage.
- Documentation and appendices (e.g., Appendix A, profile data, analysis outputs) accompany the dataset; use of Twinspan and NVC references indicates structured processing and classification workflows.
- Data identifiers (MLURI barcodes) provide traceable linkage between horizons, auger samples, and analyses.

## Practical Implications for Data Support
- Opportunities to build dashboards and data products showing:
  - Plot- and block-level soil properties by horizon (e.g., %N, %C, C:N, Ca, Mg, K, moisture loss, LOI) with horizon context.
  - Horizon-specific pH trends (H2O and CaCl2) and their spatial variability across blocks.
  - Vegetation composition and diversity contextualized by horizon and soil chemistry, enabling soil–vegetation relationship analyses.
  - ECOTRON perturbation context overlays (soil chemistry and vegetation responses) to support comparative analyses with established blocks.
  - Temporal markers and data completeness notes (e.g., sampling coverage by establishment year) to aid interpretation of provisional vs. established-year results.

## Data Gaps and Considerations
- Some horizons or blocks have incomplete Na reporting; partial sampling in establishment year affects full-site interpretation.
- Block-to-block variability and anomalous blocks (e.g., in Ca, Na, Mg) require careful contextual interpretation when comparing across plots and treatments.
- Horizon boundaries and granular descriptions indicate heterogeneity that should be accounted for in analyses and dashboards.