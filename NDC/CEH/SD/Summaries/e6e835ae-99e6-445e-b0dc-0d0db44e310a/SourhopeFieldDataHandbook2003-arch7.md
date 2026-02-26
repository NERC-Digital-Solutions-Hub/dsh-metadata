# SOIL ANALYSIS OF RIGG FOOT, SOURHOPE : BLOCK 4 AUGER SAMPLES

## Overview
- Detailed soil chemical data from Block 4 auger samples (4A–4F) and Block 5 soil profiles, plus Ecotron plot data and associated vegetation surveys.
- Data suitable for GIS-based mapping of soil chemistry by horizon and plot, and for linking soil attributes to vegetation patterns.

## Data Coverage and Structure

- Block 4 Auger Samples (4A–4F)
  - Measurements: weight (mg), %N, %C, C:N ratio, Ca, Na, K, Mg (meq/100g), %Moisture loss, %Loss on Ignition, pH (H2O), pH CaCl2.
  - Values (example ranges): %N 0.51–0.58; %C 6.80–8.02; C:N 12.62–14.26; Ca 1.01–2.96 meq/100g; Mg 0.58–1.59 meq/100g; K 0.58–0.81 meq/100g; pH H2O 4.45–4.82; pH CaCl2 3.64–4.05.
  - Notes: Data provided per auger sample, with some parameters missing in places (noted as blanks).

- Block 5 Site and Profiles
  - Site details: grid NT8544019520; altitude 315 m; slope description 5 degrees; soil drainage imperfect; major soil subgroup Brown forest soil with gleying; parent material undifferentiated intermediate igneous and andesite.
  - Soil profile (Block 5): Horizons labeled FH, H, Ah, AB, Bg, BCg, Cg with depths 0–100 cm and horizon-specific chemistries.
  - Profile data: %N and %C vary by horizon (e.g., FH N 2.05%, C 33.81%; H N 2.17%, C 31.06%; Ah N 0.65%, C 9.36%; Bg N 0.06%, C 0.72%; BCg N 0.04%, C 0.43%; Cg N 0.01%, C 0.12%); C:N ratios range ~10–16; pH H2O 4.34–5.2; pH CaCl2 3.53–4.48.
  - Cations: Ca (meq/100g) ranges from 0.35 to 11.91 across horizons; K and Mg vary by horizon; Na generally low or not reported in several horizons.
  - Moisture and LOI: %Moisture loss 2.79–9.43; %Loss on Ignition 4.83–67.00; notable high LOI in FH horizon (67.00%).

- Ecotron Plot
  - Soil: Wt 6.089 mg; %N 0.59; %C 8.22; C:N 13.83; Ca 2.76 meq/100g; Na 0.15; K 0.62; Mg 1.7 meq/100g; %Moisture loss 4.79; %LOI 17.42; pH H2O 4.79; pH CaCl2 3.82.
  - Vegetation: survey data available per sub-plot with species totals and counts by category.

## Vegetation Data (GIS-relevant)

- Block-wise vegetation surveys accompanying soil data (e.g., plot 4A–4F, 5A–5F; ECOTRON plot).
- Species totals and presence/absence indicators per plot/subplot; data suitable for mapping community types (e.g., NVC-like groupings) and indicator species.
- Some plots show richer species counts downslope; results support generating vegetation-chemistry interaction maps.

## GIS-ready Attributes and Suggested Layers

- Soil horizon layers
  - Horizon-based chemistry: %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH H2O, pH CaCl2 by horizon (FH, H, Ah, AB, Bg, BCg, Cg).
  - Depth: total profile to 100 cm (Block 5) and horizon boundaries.
- Plot and block attributes
  - Block identifiers (Block 4, Block 5), plot IDs (e.g., 4A–4F, 5A–5F), horizon-level data aggregated to plots.
  - Elevation/altitude, grid references, slope descriptors.
- Vegetation layers
  - Vegetation community classifications by plot (NVC-like groups and subcommunities).
  - Indicator species and species totals by plot/subplot.
- Ecotron/experimental layers
  - ECOTRON plot attributes, including soil chemistry and vegetation survey results.
- Overlays
  - Grazing/cutting regime history and management actions (where available) to contextualize results.

## Data Quality, Limitations, and Caveats

- Block 4 data: auger samples 4A–4F with several missing values; not all chemical attributes reported for every sample.
- Block 5 data: detailed horizon-level data (FH to Cg) with multiple horizons and depth ranges; some horizons show heavy stone content and variable pH; missing Na values in several horizons.
- Ecotron data: limited to a single plot; representative but not exhaustive.
- Temporal scope: snapshot data for blocks; integration with ongoing long-term datasets (ECN/Micronet) advised for trend analyses.
- Interpretation caution: variability across horizons and blocks; some anomalies noted in horizon chemistry and pH values.

## Data Context and Sources

- Part of the Sourhope field site data collection (Soil Biodiversity Programme, 1998–2003) with accompanying vegetation surveys and multivariate analyses.
- ECOTRON and Micronet involvement for long-term environmental monitoring.
- Data referenced by MLURI barcodes and block-specific analyses for auger samples and soil profiles.

## Practical GIS Use Cases

- Create horizon-specific soil chemistry maps by block/plot for visualization of spatial gradients.
- Build 3D soil models by integrating horizon depths with chemistry and pH layers.
- Map vegetation communities and indicator species in relation to soil chemistry and horizon depth.
- Link Ecotron soil and vegetation data to broader environmental monitoring layers for integrated analyses.