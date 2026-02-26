# Collection, generation methods and quality control

- Site and sampling
  - Sediment cores collected from two reservoirs in Tameside, UK: Cowbury Dale Reservoir (Carrbrook) and Higher Swineshaw Reservoir (Stalybridge)
  - Dates: Cowbury Dale core collected 06 August 2018; Higher Swineshaw core collected 11 December 2018
  - At each site, five cores taken along the long axis from inlet to dam wall; deepest, undisturbed core chosen for analysis
  - Cores extruded and sampled at 2.5 mm contiguous intervals; depth in core recorded in cm

- Analytical workflow and data generation
  - X-ray fluorescence (XRF) analysis
    - Instrument: XEPOS 3 Energy-dispersive XRF
    - Sample handling: ground, pressed, measured under He with Pd and Co excitation; daily standardization; accuracy checks with 18 certified reference materials
    - Corrections: light elements corrected for organic content
  - Loss on ignition (LOI) and organic content
    - LOI measured by near-infrared spectrometry (NIRS) cross-calibrated with direct LOI measurements
    - Direct LOI: ashing at 450°C for 4.5 hours
    - NIRS: scan of each 1-cm depth sample (3,598–12,493 nm) with BRUKER MPA FT-NIR; LOI predicted from NIRS with strong cross-correlation (r2 ≈ 86%)
    - LOI and NIRS LOI values used to correct light-element estimates in XRF analyses
  - Particle size analysis
    - Instrument: Coulter LS 13 320 Laser Diffraction Particle Size Analyzer
    - Pre-treatment: organic matter digested with H2O2; samples dispersed in Na6O18P6; sonicated
    - Replicates: three repeats with outliers removed; results expressed as D50 (median particle diameter, in mm)
    - Calibration: regular checks with known size distributions
  - Data integration and structure
    - Depth in core (cm)
    - LOI_xrf: LOI estimated from XRF data (%)
    - nir_loi: LOI from NIRS (%)
    - Elemental analysis: concentrations for multiple elements (units vary; mg/g or µg/g as appropriate)

- Data structure, units, and coverage
  - Elemental datasets include a wide range of elements (major and trace, including Mg, K, Ca, Si, Fe, P, S, and various trace metals)
  - Units may be mg/g or µg/g depending on concentration
  - Missing values are indicated by blank spaces

- Quality control and validation
  - XRF accuracy verified via daily standardization and 18 certified reference materials
  - LOI estimates cross-validated with direct LOI measurements; LOI–NIRS cross-calibration shows strong correlation (r2 ≈ 0.86)
  - Particle size measurements repeated (three replicates) with outlier removal; calibration against known distributions
  - Comprehensive metadata for traceability, including sampling details and method references

- References and methodology context
  - Cited methodological sources include standard grain-size analysis, gravity corer sampling, μXRF calibration approaches, and LOI/NIRS cross-calibration studies (Blott & Pye, 2001; Boyle, 1995; Boyle et al., 2015; Folk & Ward, 1957; Schillereff et al., 2015)

- Practical notes for data use
  - The dataset supports multi-proxy sediment characterization, enabling cross-comparison of organic content, mineral/sediment composition, and particle-size distributions along sediment cores
  - The LOI and NIRS cross-calibration approach provides rapid, non-destructive estimates of organic content to supplement XRF-derived elemental data
  - Users should account for unit variations and missing values when integrating across samples or datasets