# SOIL ANALYSIS OF RIGG FOOT, SOURHOPE

- Scope
  - Detailed soil and vegetation data for Rigg Foot, Sourhope, focusing on BLOCK 4 AUGER SAMPLES, BLOCK 5 SITE DETAILS and PROFILE, and ECOTRON SITE.
  - Includes sample IDs (MLURI barcodes), physical measurements (weight), chemical properties (%N, %C, C:N), major cations (Ca, Na, K, Mg), moisture metrics, soil loss on ignition, and pH (H2O and CaCl2).
  - Complementary vegetation surveys at plot and subplot levels, plus ECOTRON vegetation and soil data.

- GIS-facing data primitives (layers and attributes)
  - Site geometry and metadata
    - Blocks (BLOCK 4, BLOCK 5) and ECOTRON PLOT with associated grid references, altitude, slope, drainage status, soil series and parent material notes.
  - Soil horizons and profiles
    - Block 4 auger samples (4A–4F) with: weight (mg), %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH H2O, pH CaCl2.
    - Block 5 profile (FH, H, Ah, AB, Bg, BCg, Cg) with horizon-specific values for N, C, C:N, Ca, Na, K, Mg, moisture loss, LOI, pH H2O, pH CaCl2.
    - Augered sample analyses for 5A–5F and ECOTRON PLOT with the same suite of chemical/physical measurements.
  - Vegetation data
    - Block 4 plots (4A–4F) and Block 5 plots (5A–5F) with subplot-level species totals, presence/absence indicators, and counts across multiple species/groups.
    - ECOTRON PLOT vegetation survey with per-subplot totals and species indicators.
  - Temporal and data provenance
    - MLURI barcodes linked to each sample, indicating archival and analysis lineage; notes on LOI, moisture loss, and pH across horizons.
  - Treatments and context (where applicable)
    - Documented plot-level contexts (e.g., horizon layers, soil type descriptors) to support overlay of environmental variables (moisture regime, pH, texture inferred from horizon descriptions).

- Key soil and vegetation patterns (high-level observations)
  - Block 5 soil profile
    - Distinct horizon sequence (Ah to BCg to Cg) with increasing depth and mottling, indicating weathering and drainage variation.
    - Surface horizons show higher %C and LOI; soil C:N ratios generally around mid-teens; acidity indicated by low pH values (H2O around ~4–5; CaCl2 often around 3.5–4.5).
    - Calcium and Mg are present in notable but variable amounts across horizons; exchangeable cations and moisture loss show horizon- and block-level variability.
  - Block 4 auger samples
    - Consistent %N values around 0.5–0.6; %C values ~6–8; C:N ratios in mid-teens; Ca, K, Mg present in modest meq/100g ranges; pH values around 4.4–4.8 (H2O) with somewhat lower CaCl2 values.
    - Moisture loss and LOI values indicate organic-rich surface layers diminishing with depth.
  - ECOTRON SITE
    - Soil analysis shows low pH (H2O ~4.7) and relatively high LOI for surface layers; %N ~0.59; %C ~8.22; C:N ~13.83; Ca ~2.76 meq/100g; Mg ~1.7 meq/100g.
    - Vegetation data in ECOTRON plot reflects diverse but sparse subplots with presence/absence patterns across taxa.
  - Vegetation context
    - Plot-level totals indicate varying species richness across plots and subplots, with separate tallies for per-plot and per-subplot assessments, useful for mapping vegetation communities and diversity indices in GIS.
    - Data include dominant groups (e.g., grasses and forbs) and broader vegetation indicators, enabling classification into shallow-moisture and soil-type–associated communities.

- Data products and GIS applications
  - Spatial layers suitable for map-based dissemination
    - Horizon-level soil properties by plot/subplot and by horizon (N, C, C:N, Ca, Na, K, Mg, LOI, moisture loss, pH).
    - Soil profile delineations and boundary definitions for blocks 4, 5, and ECOTRON, with depth strata.
    - Vegetation layers: plot/subplot vegetation totals, species richness, and community classifications derived from survey data.
    - Site context: altitude, slope, drainage, soil series, and parent material overlays.
  - Potential analyses
    - Spatial correlation of soil chemistry with horizon depth and topographic position.
    - GIS-enabled comparison of vegetation communities with soil properties and horizon patterns.
    - Overlay with environmental layers (e.g., ECN/Micronet contexts) for cross-site gradient analyses and long-term monitoring.
  - Data integration notes
    - Data are tied to sample IDs (MLURI barcodes) and plots/subplots, enabling traceability.
    - Archival origin and analysis lineage noted, supporting reproducibility and cross-referencing with central data repositories.

- Practical considerations and challenges
  - Fragmented data sources across blocks and horizons; need for consistent data standards and harmonization for cross-block GIS analyses.
  - Some horizon and Na values are sparse or missing in certain samples; careful handling required for complete spatial modeling.
  - Rich, multi-resolution data (plot, subplot, horizon) offer powerful map-based capabilities but demand careful data structuring to maximize GIS utility.

- Takeaways for GIS specialists
  - The document provides a comprehensive, geospatially explicit dataset framework for soil biodiversity and grassland ecology at Sourhope, with robust horizon- and plot-level data suitable for high-resolution map products.
  - Combining horizon chemistry, soil profiles, and vegetation surveys enables detailed spatial analyses of soil-vegetation relationships and gradients across Block 4, Block 5, and ECOTRON sites.
  - Effective GIS use will require harmonizing sample IDs, horizon delimitations, and plant community classifications into consistent layers and attribute schemas across blocks.