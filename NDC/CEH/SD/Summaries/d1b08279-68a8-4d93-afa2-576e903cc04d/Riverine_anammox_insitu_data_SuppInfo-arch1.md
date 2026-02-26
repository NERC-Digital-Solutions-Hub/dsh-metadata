# Dataset containing results from field measurements of riverine nitrogen transformations

- Purpose and scope
  - Contains field measurements of riverine nitrogen transformations in the Hampshire Avon catchment.
  - Measures nitrate reduction using 15N-labelled nitrate tracers in permeable sediments (sands, chalks) via push-pull sampling, and in intact cores for clays.
  - Quantifies ambient denitrification and anammox using isotope pairing and mass spectrometry, with related production rates (P29, P30) and fractionation metrics (ra, p14, A14, D14).

- Dataset structure
  - 13 data columns and 67 rows (including headers).
  - Data quality flags: BDL (below detection limit) and ND (not collected).
  - Key columns include: Sample Label, Site (Clay/Sand/Chalk; specific river sites with coordinates), Depth (cm), Injection (µM), Fe(II), O2 (µM), O2sat (%), Nitrate (µM), Nitrite (µM), Ammonium (µM), SRP (µM), pH, D14, P29, P30, p14, A14, ra.

- Site and sampling details
  - Rivers located in the Hampshire Avon catchment; site designations indicate sediment type: Clay (greensand/Clay), Sand, Chalk.
  - Precise site coordinates provided for several sites (e.g., Clay 1 and Clay 2 on the River Sem; Sand 1/2; Chalk 1/2 with corresponding lat/long).
  - Depth refers to the screen mid-point below the riverbed surface.
  - Background porewater samples collected before 15N-injection to measure nutrients, oxygen, pH, Fe(II).
  - Porewater samples filtered, preserved, and stored appropriately; analyses performed within 6 months.

- Measurements and analytical methods
  - Fe(II): Measured after porewater filtration via UV/Vis spectrophotometry with phenanthroline; LOD ~1 µM; precision ±1%.
  - Oxygen (O2): Measured in porewater with a fast-response microelectrode; calibration with zero and known O2 solutions; contamination correction ~10 µM; LOD ~10 µM; precision ~2%.
  - O2 saturation (O2sat): Calculated relative to air-equilibrated water using temperature-based solubility.
  - Nitrate/Nitrite: NOx and nitrite determined by automated colorimetry (Griess); NOx reduced to nitrite inline for nitrate analysis; LOD ~0.4 µM; precision ~1%.
  - Ammonium (NH4+): Indophenol blue method; LOD ~0.8 µM; precision ~3%.
  - Soluble reactive phosphorus (SRP): Molybdenum blue colorimetry; LOD ~0.1 µM; precision ~1%.
  - pH: Measured in porewater after oxygen measurement.

- Isotopic measurements and rate calculations
  - 15N-nitrate injections used to trace nitrate reduction; production of 29N2 and 30N2 quantified by mass spectrometry.
  - N2 concentration calculations follow established isotope-pairing formulations.
  - Rates: P29 (29N2) and P30 (30N2) decay rates estimated by linear fits to time-series data.
  - Ambient non-tracer processes (p14) computed to represent production of 14N2 not from the 15N tracer.
  - Anammox fraction (ra) determined by comparing 15N enrichment in N2 and N2O pools; D14 (ambient denitrification) and A14 (ambient anammox) derived from p14 and ra.

- Data quality and metadata
  - Data include field blanks and analytical blanks; background measurements assist in distinguishing ambient processes from tracer-derived signals.
  - Site and sediment-type metadata (Clay, Sand, Chalk) enable cross-site comparisons.
  - Data reflect measurements from August 2013; shallow sediments where tracer plumes could be contained within the riverbed surface.

- Limitations and considerations for analysts
  - Data are limited to the Hampshire Avon catchment and to the conditions/time of sampling (August 2013); limited to selected sites with indicated sediment types.
  - Some measurements are below detection limits (BDL) or not collected (ND), requiring careful handling in analyses.
  - Rate calculations depend on isotope pairing assumptions and mass-spectrometry calibrations; consult referenced methods for detailed uncertainty quantification.

- References
  - Lansdown, K. et al. Fine-Scale in Situ Measurement of Riverbed Nitrate Production and Consumption in an Armored Permeable Riverbed. Environ. Sci. Technol. 2014.
  - Nielsen, L. P. Denitrification in sediment determined from nitrogen isotope pairing. FEMS Microbiol. Ecol. 1992.
  - Risgaard-Petersen, N. et al. Application of the isotope pairing technique in sediments where anammox and denitrification coexist. Limnol. Oceanogr. Methods 2003.
  - Thamdrup, B. & Dalsgaard, T. The fate of ammonium in anoxic manganese oxide-rich marine sediment. Geochim. Cosmochim. Acta 2000.
  - Trimmer, M. et al. Direct measurement of anaerobic ammonium oxidation (anammox) and denitrification in intact sediment cores. MEPS 2006.