# SOIL ANALYSIS OF RIGG FOOT, SOURHOPE

- Purpose and scope
  - Document soil and vegetation measurements at Rigg Foot, Sourhope to support GIS-enabled analyses and map-based data products.
  - Includes auger samples, soil profile descriptions, chemical/physical analyses, and vegetation surveys across blocks 4 and 5, plus ecotron plots.

- Block 4: AUGER SAMPLES
  - Sample identifiers: MLURI Barcodes 4A–4F for six auger samples.
  - Measured variables (per sample 4A–4F): weight (mg); %N; %C; C:N ratio; Ca, Na, K, Mg (meq/100g); %Moisture loss; %Loss on Ignition; pH(H2O) and pH(CaCl2).
  - Observations: consistent %N around 0.51–0.58; %C ~6.8–8.02; pH typically acidic (H2O ~4.45–4.82; CaCl2 ~3.64–4.53); wide range in Ca, Mg, and minor variations in moisture/ignition.
  - Data utility: horizon-level soil chemistry for mapping across Block 4; suitable for integration with plot-level GIS attributes.

- Block 4: VEGETATION SURVEY
  - Plot-level vegetation data for Block 4, Plot 4A and adjacent subplots (Ac, Ao, At, Br, etc.) including species totals and presence/absence indicators.
  - Notable patterns: Dominant species and total counts vary by subplot; data structured to support habitat/classification mapping and species distribution analyses.
  - Data utility: enables GIS-based vegetation mapping by plot/subplot and correlation with soil properties.

- BLOCK 5: SITE DETAILS AND PROFILE
  - Site details (Block 5): Grid reference NT8544019520; altitude ~315 m; slope 5°; imperfect drainage; major soil subgroup: Brown forest soil with gleying; parent material: andesite-derived.
  - Soil profile (Block 5): Depths and horizons described from surface to deeper layers (LF, FH, H, Ah, AB, Bg, BCg, Cg) with detailed soil descriptions and boundary characteristics.
  - Profile descriptions (examples): 
    - Ah horizon: Very dark brown, sandy silt loam with friable structure and abundant roots.
    - AB/ Bg horizons: Gray to reddish-brown colors with mottles; multiple horizons show transition from organic-rich to mineral layers.
    - Cg horizons: Clay loam to deeper mineral horizons with abundant stones; limited rooting.
  - Data utility: comprehensive horizon-level geology/soil texture context for spatial soil mapping and interpretation of soil-forming processes.

- BLOCK 5: AUGER SAMPLES AND ANALYSIS
  - Auger sample set: Barcodes 5A–5F for multiple horizon- and site-wide auger analyses.
  - Measured variables (per sample 5A–5F): weight; %N; %C; C:N; Ca, Na, K, Mg (meq/100g); %Moisture loss; %Loss on Ignition; pH(H2O) and pH(CaCl2).
  - Observations: wide range in chemical properties by horizon; typical acidic pH; variable Ca/Mg/K across horizons and samples.
  - Data utility: supports horizon- and block-level soil property mapping; enables cross-block comparison of fertility indicators.

- BLOCK 5: VEGETATION SURVEY
  - Plot-level vegetation data for Block 5 plots (5A, 5B, 5C, 5D, 5E, 5F) including subplots (Ac, Ao, At, Br, Cp, Cxp, Dc, Df, Fo, Fr, Gs, Hm, Je, Lm, Lzm, Mc, Ns, Pe, Pp, Pt, Ra, Rr, Rs, Tr, Vc).
  - Observations: species totals per subplot; variation in species richness and composition across plots/subplots.
  - Data utility: supports spatial biodiversity mapping and habitat classification across Block 5.

- ECOTRON SOIL SITE
  - ECOTRON PLOT soil analysis: Barcodes with results for a single ECOTRON plot (Wt, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH(H2O), pH(CaCl2)).
  - ECOTRON vegetation survey: per-subplot species presence/absence and totals; data suitable for comparing managed subplot responses to soil conditions.
  - Data utility: supports integrated GIS analyses within the ECOTRON framework and cross-site comparisons.

- GIS and data integration implications
  - Horizon- and block-level soil properties (N, C, C:N, Ca, Na, K, Mg, moisture loss, LOI, pH) can be mapped by block and horizon for detailed soil property rasters.
  - Vegetation data by plot/subplot enables habitat mapping, species distribution models, and change-detection potential when paired with temporal data.
  - Sample IDs (MLURI barcodes) facilitate traceability and data linking across soil chemistries, physical properties, and vegetation observations.
  - Data gaps identified by missing entries (represented as ".") should be flagged in GIS workflows and data quality checks.

- Relevance for GIS specialists
  - Rich, multi-layered dataset combining horizon-level soil chemistry/physical properties with plot-level vegetation surveys.
  - Clear structure for creating map products: horizon-based soil maps, block-level fertility gradients, and vegetation/habitat distribution maps across Sourhope.
  - Suitable as a foundation for spatial analyses of environmental gradients, soil-plant interactions, and treatment-like effects across different blocks and ecotone contexts.

- Data accessibility and notes
  - Data are organized by block (4 and 5) with corresponding auger, soil profile, and vegetation data, plus ECOTRON subset.
  - Barcodes and detailed horizon descriptions support data linkage and reproducibility.
  - Some entries contain missing values; plan for data cleaning and imputation if used for rigorous GIS modeling.