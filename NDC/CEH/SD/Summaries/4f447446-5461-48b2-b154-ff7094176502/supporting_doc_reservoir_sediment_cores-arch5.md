# Collection, generation methods and quality control

- Overview
  - Sediment cores collected from two reservoirs: Cowbury Dale Reservoir (Carrbrook, Tameside) on 06 August 2018 and Higher Swineshaw Reservoir (Stalybridge, Tameside) on 11 December 2018. OS Grid references provided for each site.
  - At each site, five cores were taken along the reservoir’s long axis from inlet to dam wall; the deepest, undisturbed core segment was used for analysis.
  - Cores sampled with a gravity corer; extrusion at 2.5 mm contiguous intervals.

- Sampling design and preparation
  - Depth-aligned sampling along the core, focusing on continuous sediment sections.
  - Cores ground lightly, pressed, and prepared for analysis in a helium atmosphere with Pd and Co excitation radiation.
  - Instrumentation and detectors include XEPOS 3 Energy-dispersive XRF and a high-resolution silicon drift detector.
  - Daily standardization and routine verification using 18 certified reference materials to ensure accuracy.

- Geochemical and organic content analyses
  - Loss on ignition (LOI) measured via two approaches:
    - Direct LOI: heating to 450°C for 4.5 hours after pre-drying at 105°C.
    - LOI estimated by near-infrared spectrometry (NIRS), cross-calibrated with direct LOI measurements; strong correlation (r2 = 0.86) demonstrated between NIR spectra and LOI.
  - NIRS reflectance measurements:
    - 1-cm depth samples from all cores scanned from 3598 to 12493 nm at 4 nm intervals using a BRUKER MPA FT-NIR spectrometer.
  - LOI concentrations reported as percentage; L-O-I values and NIRS-derived estimates aligned to provide rapid, non-destructive LOI estimates.

- Particle size analysis
  - Particle size distributions measured by laser granulometry (Coulter LS 13 320) over 0.375–2000 μm.
  - Sample digestion with H2O2 to remove organics, then dispersion in Na6O18P6 and analysis under ultrasonic conditions.
  - Three measurement repeats per sample; outliers removed to reduce intra-sample noise.
  - Size statistics calculated with standard methods (Folk and Ward), with results expressed as D50 (mm) median particle diameter.
  - Instrument calibration verified with known reference size distributions.

- Data structure, variables, and units
  - Depth in core: variable = depth; unit = cm.
  - LOI (XRF-estimated): variable = loi_xrf; unit = %.
  - LOI (NIRS): variable = nir_loi; unit = %.
  - Elemental analysis: each element reported as concentration with units either mg/g or µg/g; common elements include Mg, K, Cl, Co, Sr, Al, Ca, Ti, Ni, Y, Si, Fe, V, P, S, Ge, Ag, Te, Ce, Pb, Cu, Se, Zr, In, Cs, W, Cr, Zn, Br, Nb, Sn, Ba, Au, Mn, Ga, Rb, Mo, Sb, La, Hg.
  - Elemental dataset notes indicate missing values are blank; units may vary between mg/g and µg/g depending on concentration.
  - Particle size: D50 (mm) median particle diameter derived from laser granulometry.
  - Missing values are indicated by blank spaces in the dataset.

- Metadata, provenance, and documentation
  - Clear documentation of methodological steps, including sample collection location, dates, cores selected, and deepest undisturbed section used for analysis.
  - Detailed description of analytic procedures, calibration, and QA/QC procedures, including daily standardization and references to established methods.
  - References cited for methods and calibration approaches (e.g., Blott & Pye 2001; Boyle 1995; Boyle et al. 2015; Folk & Ward 1957; Schillereff et al. 2015).

- Quality assurance, calibration, and reproducibility
  - Regular instrument calibration and verification against certified references.
  - Cross-calibration of LOI by NIRS with direct LOI measurements to enable rapid, non-destructive estimation.
  - Repetition and outlier management in particle size measurements to improve data reliability.
  - Use of standardized protocols ensures alignment with common sediment core analysis practices.

- Data management implications for governance and sharing
  - The dataset comprises multiple data streams (depth, LOI, L-O-I, elemental concentrations, and particle size) with consistent depth-based alignment across cores.
  - Metadata should include site details, sampling dates, core selection criteria, analytical methods, calibration references, and QA/QC procedures to support discoverability and reuse.
  - Clear unit definitions and notes about differing units across elemental measurements facilitate interoperability and reduce misinterpretation.
  - Documented references and method provenance support traceability and reproducibility for future use and integration into larger datasets.

- References
  - Key literature underpinning methods and QA/QC, including Blott & Pye (Gradistat), Boyle (gravity corer closure), Boyle et al. (water content correction for μXRF), Folk & Ward (grain-size statistics), and Schillereff et al. (intercomparison of μXRF methods).