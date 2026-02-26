# Collection, generation methods and quality control

- Study sites and sampling
  - Reservoir sediment cores collected from two reservoirs: Cowbury Dale Reservoir (Carrbrook, Tameside) and Higher Swineshaw Reservoir (Stalybridge, Tameside).
  - Collection dates: 06 August 2018 (Cowbury Dale) and 11 December 2018 (Higher Swineshaw).
  - At each site, five cores were taken along the long axis from inlet to dam wall; the deepest, undisturbed core was selected for analysis.
  - Sampling method: gravity corer (Boyle, 1995); cores extruded and sampled at 2.5 mm contiguous intervals.

- Analytical methods and measurements
  - Sediment geochemistry
    - X-ray fluorescence (XRF) analysis using XEPOS 3 Energy-dispersive XRF.
    - Sample preparation: light grinding, pressing; measurements conducted in a helium atmosphere with Pd and Co excitation; high-resolution silicon drift detector.
    - Quality control: daily standardization and verification using 18 certified reference materials.
    - LOI (loss on ignition) correction: LOI determined via heating (105°C overnight to remove moisture; 450°C for 4.5 h to combust organics) and cross-checked/estimated by XRF data.
  - Organic content estimation
    - LOI measured by near-infrared spectrometry (NIRS) cross-calibrated with direct LOI measurements.
    - NIRS method: BRUKER MPA FT-NIR spectrometer; scans from 3,598 to 12,493 nm at 4 nm intervals for each 1-cm depth sample.
    - Cross-calibration: strong correlation (r2 = 86%) between the first derivative of the entire NIR spectra and LOI (n>500 samples).
    - LOI concentration predicted from NIRS data, providing rapid, non-destructive estimates.
  - Particle size
    - Particle size distribution measured by Coulter LS 13 320 laser diffraction.
    - Sample preparation: organic matter digested with H2O2; dispersion with Na6O18P6; sonication.
    - Replicates: three repeats per sample with outlier removal.
    - Output: D50 (median particle diameter) in micrometers; instrument calibrated with known distributions (regular checks).
  - Data structure and elemental analysis
    - Depth in core: unit = cm.
    - LOI (XRF estimated): variable loi_xrf, unit %.
    - LOI (NIRS): variable nir_loi, unit %.
    - Elemental analysis: data reported as d50 element-specific concentrations; units cereal are mg/g and µg/g depending on concentration.
    - Elements listed include Mg, K, Co, Sr, Al, Ca, Ti, Ni, Y, Si, Fe, V, P, S, Ge, Ag, Te, Ce, Pb, Cr, Zn, Br, Nb, Sn, Ba, Au, Mn, Ga, Rb, Mo, Sb, La, Hg.
    - Missing values are indicated by blank spaces.
  - Data provenance and reproducibility
    - Methods and instrument calibration described; standardized procedures and cross-calibrations documented to ensure comparability across cores and sites.

- Data quality, assurance and reporting
  - Robust QA/QC: daily XRF standardizations; use of 18 certified reference materials; cross-calibration of LOI with NIRS to improve robustness of organic content estimates.
  - Replication and noise reduction: triplicate measurements for particle size with outlier removal; use of laboratory calibrations for accuracy in elemental measurements.
  - Clear metadata and data structure: explicit depth, units, and element-specific conventions; notes on missing values and dual units where applicable.
  - References and methodological context provided for reproducibility and comparison with other sediment core studies.