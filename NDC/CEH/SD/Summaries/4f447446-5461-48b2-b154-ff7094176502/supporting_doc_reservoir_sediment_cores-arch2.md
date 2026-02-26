# Collection, generation methods and quality control

- Study sites and sampling
  - Reservoirs: Cowbury Dale Reservoir (Carrbrook, Tameside) and Higher Swineshaw Reservoir (Stalybridge, Tameside).
  - Sampling: at each site, five cores taken along the reservoir’s long axis from inlet to dam wall; deepest, uninterrupted core selected for analysis.
  - Method: gravity corer used to extract extruded cores; sampling interval 2.5 mm along each core.

- Laboratory methods and measurements
  - Sediment geochemistry (XRF)
    - Instrument: XEPOS 3 Energy-dispersive XRF.
    - Procedure: samples lightly ground, pressed, measured in a He atmosphere with Pd/Co excitation; high-resolution silicon drift detector.
    - Quality control: daily standardization; verification with 18 certified reference materials.
    - LOI (loss on ignition) correction: LOI values derived from XRF data after correcting for organic content.
  - Loss on ignition (LOI) and organic content
    - Direct LOI measurements: LOI by heating at 105°C overnight, then 450°C for 4.5 hours.
    - Cross-calibration with NIRS: LOI predicted from Near Infrared Spectrometry (NIRS) reflectance data.
    - NIRS specifics: BRUKER MPA FT-NIR, 3,598–12,493 nm, scanning 1-cm depth samples at 4 nm intervals; cross-calibrated using a training set of direct LOI measurements (n > 500) with a strong correlation (r2 = 86%).
  - Particle size analysis
    - Instrument: Coulter LS 13 320 Laser Diffraction Particle Size Analyser.
    - Sample preparation: organic component removed with H2O2; dispersion in Na6O18P6 and sonication.
    - Replicates: three repeats with outlier elimination to reduce intra-sample noise.
    - Output: D50 (median particle diameter) in micrometers.
    - Calibration: regular calibration checks with known size distributions.

- Data structure, nature and units
  - Depth in core: depth (cm).
  - Loss on Ignition (XRF estimated): loi_xrf (%).
  - Near infrared Spectrometry LOI: nir_loi (%).
  - Elemental analysis: multiple elements with units mg/g or µg/g; included elements cover a wide range (e.g., Al, Ca, Ti, Ni, Sr, Si, Fe, P, S, Ge, Ag, Te, Ce, Pb, Cu, Se, Zr, In, Cs, W, Cr, Zn, Br, Nb, Sn, Ba, Au, Mn, Ga, Rb, Mo, Sb, La, Hg, etc.).
  - Notation: missing values are blank; units for elemental analysis may be mg/g or µg/g depending on concentration.
  - Depth and elemental data are provided per depth increment across the sampled cores.

- References and methodological context
  - Key sources for methods and calibration approaches are cited, including: Gradistat for grain-size statistics; gravity corer design; μXRF core scanning calibration comparisons; and foundational grain-size and sediment geochemistry literature.

- Relevance to environmental monitoring and data use
  - Standardized, repeatable methods for core collection, geochemical analysis, LOI correction, and particle-size measurement support consistent environmental health and policy monitoring.
  - Use of dual LOI estimation (direct LOI and NIRS-assisted prediction) enhances rapid, non-destructive assessments while maintaining calibration to direct measurements.
  - Comprehensive elemental data across multiple reservoirs enables cross-site comparisons and long-term trend analyses when integrated with broader datasets.

- Considerations for data reuse and value enhancement
  - Aim to increase dataset value by integrating with additional relevant datasets (e.g., hydrology, pollution sources, historical records) to enrich environmental interpretation.
  - Facilitates broader accessibility of underlying data used to produce final outputs, aligning with open-usage and reproducibility goals.