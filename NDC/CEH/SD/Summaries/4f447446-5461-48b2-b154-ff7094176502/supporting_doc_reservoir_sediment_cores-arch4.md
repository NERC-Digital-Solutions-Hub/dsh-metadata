# Collection, generation methods and quality control

- Overview: Describes the collection, preparation, analytical methods, and quality control for sediment core data from two reservoirs (Cowbury Dale Reservoir and Higher Swineshaw Reservoir) collected in 2018, including both elemental geochemistry (XRF) and organic/inorganic proxies (LOI, NIRS) and particle size measurements.

- Collection sites and sampling design:
  - Cowbury Dale Reservoir, Carrbrook, Tameside (06 August 2018) — OS Grid Reference SD 99745 01302
  - Higher Swineshaw Reservoir, Stalybridge, Tameside (11 December 2018) — OS Grid Reference SK 00493 99704
  - At each site: five cores along the reservoir long axis from inlet to dam wall; the deepest, undisturbed core used for analysis.
  - Core extraction method: gravity corer.

- Core processing and sampling:
  - Extruded cores sampled at 2.5 mm contiguous intervals.
  - Priority sample: deepest, continuous sediment interval selected for analysis.

- Analytical methods and quality control:
  - X-ray fluorescence (XRF) geochemistry:
    - Instrument: XEPOS 3 Energy-dispersive XRF.
    - Conditions: samples ground, pressed, measured in helium with Pd and Co excitation; silicon drift detector.
    - Calibration and QA: daily standardization; validated with 18 certified reference materials.
  - Loss on ignition (LOI) and organic matter correction:
    - LOI determined by a two-step process (105°C overnight drying; 450°C for 4.5 hours).
    - LOI values cross-calibrated with Near Infrared Spectrometry (NIRS) predictions.
    - NIRS: BRUKER MPA FT-NIR spectrometer (3,598–12,493 nm) with 4 nm interval scans; cross-calibrated using training set of >500 direct LOI measurements.
    - Reported LOI via XRF and NIRS show strong correlation (r2 = 0.86) for rapid, non-destructive LOI estimates.
  - Particle size analysis:
    - Instrument: Coulter LS 13 320 Laser Diffraction Particle Size Analyser.
    - Pre-treatment: remove organics with H2O2; disperse with Na6O18P6; sonicate.
    - Measurements: three repeats per sample; outliers removed to minimize intra-sample noise.
    - Output: D50 (median particle diameter) in millimeters.
    - Quality: regular calibration with known distributions.
  - Data handling and structure:
    - Depth in core: depth (cm).
    - LOI (XRF estimated): loi_xrf (%).
    - LOI (NIRS): nir_loi (%).
    - Elemental analysis: concentrations of a broad suite of elements; units reported as mg/g or µg/g depending on concentration.
    - Elements explicitly mentioned include Mg, K, Cl, Co, Sr, Al, Ca, Ti, Ni, Y, Si, Fe, V, P, S, Ge, Ag, Te, Ce, Pb, Cu, Se, Zr, In, Cs, W, Cr, Zn, Br, Nb, Sn, Ba, Au, Mn, Ga, Rb, Mo, Sb, La, Hg, among others.
    - Data notes: missing values indicated by blank spaces; elemental units vary by concentration.

- Data structure and units:
  - Depth: cm.
  - loi_xrf: % (XRF-estimated LOI).
  - nir_loi: % (NIRS-derived LOI).
  - Elemental concentrations: various elements with units mg/g or µg/g.
  - Metadata richness includes sampling dates, locations, grid references, and core selection criteria.

- References and methodological context:
  - Key methodological references for XRF calibration, LOI-NIRS cross-calibration, and grain-size statistics (e.g., Gradistat) cited to underpin QA/QC and analytical approaches.

- Data quality and usability considerations for data leaders:
  - Robust QA/QC: daily XRF standardization, certified reference material validation, and cross-calibrated LOI measurements.
  - Non-destructive LOI estimation via NIRS provides rapid screening with validated correlation to direct LOI.
  - Comprehensive metadata supports traceability (site details, dates, grid references, core selection rationale).
  - Wide suite of elemental measurements with clear notes on units and missing data; potential need for unit standardization when integrating with other datasets.
  - Exemplary documentation of sampling design, preparation steps, and calibration/validation procedures to enable reproducibility and cross-network collaboration.