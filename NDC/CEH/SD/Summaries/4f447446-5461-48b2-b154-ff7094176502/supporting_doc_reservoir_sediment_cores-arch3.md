# Collection, generation methods and quality control

## Sampling design and collection
- Reservoirs: Cowbury Dale Reservoir (Carrbrook, Tameside) and Higher Swineshaw Reservoir (Stalybridge, Tameside).
- At each site: five cores collected along the long axis from inlet to dam wall.
- Core selection: deepest segment with no obvious breaks chosen for analysis.
- Collection method: gravity corer (Boyle, 1995).
- Sampling: extruded cores sampled at 2.5 mm contiguous intervals.

## Analytical methods
- Sediment geochemistry: X-ray fluorescence (XRF) using XEPOS 3 Energy-dispersive XRF; samples measured in a He atmosphere with Pd and Co excitation and a silicon drift detector.
- LOI (loss on ignition): determined by LOI at 105°C overnight, then 450°C for 4.5 hours to combust organic matter; LOI cross-calibrated with near-infrared spectrometry (NIRS).
- NIRS: BRUKER MPA FT-NIR spectrometer; 3598–12,493 nm; cross-calibrated against direct LOI measurements using a training set (>500 samples); LOI concentration predicted from NIRS data (robust, rapid, non-destructive estimates).
- Elemental and particle size analyses: 
  - Elemental composition: reported as d50 values with elements listed (Mg, K, Co, Sr, Al, Ca, Ti, Ni, Y, Si, Fe, V, P, S, Ge, Ag, Te, Ce, Pb, etc.).
  - Particle size: laser diffraction (Coulter LS 13 320) after H2O2 digestion of organics; samples dispersed and sonicated; three repeats; outliers removed; results presented as D50 (mm).
- Instrument calibration and standards: daily standardization for XRF with 18 certified reference materials; regular calibration checks for the Coulter instrument; three repeats per sample to reduce intra-sample variability.

## Data structure, units and handling
- Depth in core: depth (cm).
- LOI (XRF estimated): loi_xrf (%).
- L-O-I (NIRS-derived): nir_loi (%).
- Elemental data: d50 labeled as 'element' with units mg/g or µg/g; includes elements such as Mg, K, Co, Sr, Al, Ca, Ti, Ni, Y, Si, Fe, V, P, S, Ge, Ag, Te, Ce, Pb, Cu, Se, Zr, In, Cs, W, Cr, Zn, Br, Nb, Sn, Ba, Au, Mn, Ga, Rb, Mo, Sb, La, Hg; missing values represented by blank spaces.
- Units: LOI and NIRS LOI in percent; elemental units in mg/g or µg/g; d50 in mm.
- Notes: some entries include explicit element lists; L-O-I and LOI values may be cross-referenced with NIRS-derived estimates.
- Data provenance and transparency: extensive method detail provided, including core selection criteria, sampling intervals, and measurement conditions; missing values and unit conventions are documented.

## Quality assurance and calibration
- XRF quality: daily standardization procedures; accuracy verified with 18 certified reference materials.
- LOI and NIRS: strong cross-calibration between direct LOI measurements and NIRS predictions; reported strong correlation (r2 = 86%) between the first derivative of the entire NIR spectra and LOI training set.
- Reproducibility: three replicates per particle-size measurement; outlier removal to minimize intra-sample noise.
- Calibration for particle size: Coulter LS 13 320 calibrated with known distributions; digestion and dispersion steps standardized to ensure comparability.

## References
- Blott SJ, Pye K. 2001. Gradistat: A grain size distribution and statistics package for the analysis of unconsolidated sediments. Earth Surface Processes and Landforms 26: 1237-1248.
- Boyle JF. 1995. A simple closure mechanism for a compact, large diameter, gravity corer. Journal of Paleolimnology 13: 85-87.
- Boyle JF, Chiverrell RC, Schillereff D. 2015. Approaches to water content correction and calibration for μXRF core scanning: comparing X-ray scattering with simple regression of elemental concentrations. In Micro-XRF Studies of Sediment Cores. Springer; 373-390.
- Folk RL, Ward WC. 1957. Brazos River bar: a study in the significance of grain size parameters. Journal of Sedimentary Research 27: 3-26.
- Schillereff DN, Chiverrell RC, Boyle JF, Croudace IW. 2015. An intercomparison of μXRF scanning analytical methods. In Developments in Palaeoenvironmental Research: Micro-XRF Studies of Sediment Cores, Rothwell RG, Croudace IW (eds). Springer: Dordrecht; 110-120.