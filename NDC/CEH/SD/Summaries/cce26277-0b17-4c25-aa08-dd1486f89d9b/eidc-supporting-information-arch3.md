# Hydraulic mobility of aquatic insect (Trichoptera) bioconstructions and incorporated sediments

- Purpose: Quantify how caddisfly (Trichoptera) case construction affects sediment transport and bed stability in rivers using controlled flume experiments.
- Study design:
  - Three species: two tubular-case builders and one domed-case builder.
  - Comparisons: empty caddisfly cases vs. disaggregated sediment after case removal.
  - Experimental setup: cases and sediment placed center-field in a flume; hydraulic force increased across 11 discharge steps; sediment erosion measured via staged photography.
  - Timeline: field collection (June and August 2019); flume experiments (August–September 2019).

- Data products and contents (S1–S4):
  - S1_Velocimetry_data:
    - Raw and post-processed three-direction velocity data (U, V, W) with means and standard deviations.
    - Quality metrics: correlation, signal-to-noise ratio (SNR).
    - Derived metrics: turbulent kinetic energy (TKE) and bed shear stress (Tb).
    - Key variables include Date, Discharge_step, Umean_raw/Umean/Ustd_raw/Ustd, Vmean_raw/Vmean/Vstd_raw/Vstd, Wmean_raw/Wmean/Wstd_raw/Wstd, U_corr, U_SNR, V_corr, V_SNR, W_corr, W_SNR, TKE, Tb.
  - S2_Case-grain-size-distribution_data:
    - Grain-size distributions for each caddisfly case (by species/individual).
    - Variables: Sample_ID, Sed_mass, Sieved_mass, Loss_mass, Loss_percent; sieve size references; mass values (g).
  - S3_Entrainment_data:
    - Percentage of sediment entrained during each discharge step (1–11).
    - Variables: Sample_ID, State (Case or loose sediment), Discharge_step, Value (cumulative % transported).
  - S4_Case-and-entrainment-threshold_data:
    - Case characteristics (mass, axes a, b_D50, c) and entrainment/movement thresholds.
    - Variables: Case/Sediment ID, State, Mass, a, b_D50, c, E_10 (critical entrainment threshold), E_90 (movement threshold).

- Measurement and processing details:
  - Methods: Acoustic Doppler velocimetry (ADV) for hydraulic conditions; post-processing to obtain clean velocity fields and turbulence metrics; visual/photographic assessment for entrainment.
  - Case characterization: dry mass and geometric axes to relate morphology to hydraulic response.
  - Entrainment assessment: based on imagery to determine percent sediment transported.

- Relevance for monitoring frameworks:
  - Demonstrates a multi-indicator approach to environmental health monitoring: hydraulic forcing (bed shear stress), sediment entrainment, sediment size distribution, and bioconstruction geometry.
  - Emphasizes thorough metadata and variable definitions to enable data reuse, comparability, and transparency in monitoring evaluations.
  - Provides policy-relevant measures for river habitat assessment and the influence of bioconstructions on sediment dynamics and bed stability.

- Data quality and governance notes:
  - Explicit variable definitions and units within each data file enhance data quality and governance.
  - Includes data quality indicators for velocimetry (SNR, correlation) and clearly documented processing steps.
  - While the document describes the data and its structure, it implies the importance of data sharing and standardized metadata to support future monitoring and decision-making. Potential governance considerations include ensuring ongoing access, metadata completeness, and harmonization with other datasets for broader monitoring use.