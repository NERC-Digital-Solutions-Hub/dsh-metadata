# Metadata for Blonder et al., Spectral data for quaking aspen (Populus tremuloides) clones of different ploidy levels

## Overview
- Describes the field and laboratory methods used to collect genotypic and spectral data from quaking aspen clones with different ploidy levels across southwestern Colorado (2016–2017).
- Aims to enable analysis of relationships between ploidy, genotype, and spectral properties at leaf, bark, and canopy scales, including Ground and UAV-derived imagery.
- Provides data structure details and quality controls to support reproducibility and reuse.

## Site selection and sampling design
- Network of aspen sites spanning a wide range of elevation and environmental conditions in Gunnison National Forest, CO.
- Elevation range: 2730–3630 m; spatial layout within ~37 km; sites near Almont, Crested Butte, and Gothic.
- Each site contains multiple georeferenced plots within 1 km of the site center; total of 220 independent ploidy measurements.
- Unique ploidy measurements were assigned to multiple plots/samples within plots due to cost constraints; effective sample sizes per site/analysis varied.
- No formal pseudoreplication concerns; analyses focused on classifier predictive ability; used resampling to control for sample size.

## Genotypic analysis (ploidy determination)
- Leaves collected from trees using rope-assisted methods or pruning; leaves dried in silica desiccant.
- Ploidy determined for 210 samples at multiple sites using microsatellite analysis.
- DNA extraction and microsatellite genotyping using 12 markers across two multiplex PCRs; markers include WPMS, ORPM, and PMGC sets.
- Some markers failed or were monomorphic, resulting in nine informative markers.
- Triploidy defined as three alleles observed at least at one of the nine markers; otherwise diploidy inferred.
- Reliability context: prior work showed ~97% correct classification with 6–10 markers; no evidence of linkage disequilibrium, indicating sexual reproduction occurs among clones.
- Additional ploidy measurements for n=10 samples at the Burke site using flow cytometry (nuclei stained and measured; comparison to diploid barley standard).

## Ground-based leaf spectra
- Leaf measurements taken on the adaxial surface (avoiding main vein) of fresh leaves before drying.
- Instrument: ASD handheld spectrometer (400–1075 nm range preserved after preprocessing); three replicates per leaf.
- Samples stored in moist conditions prior to measurement to maintain integrity.

## Ground-based bark spectra
- Bark samples (~5 cm^2 area, ~2 mm depth) collected from standing trees at ~1.3 m height.
- Lab measurements using the same field spectrometer and protocol as leaves.
- Three spectral replicates per sample; samples kept moist prior to measurement.

## Airborne canopy spectra
- July 2017: multispectral imagery over ~4 sites (~500 m each) using a UAV (Micasense RedEdge) with a five-band sensor.
- Flight parameters: ~90–120 m AGL, ~6–7 cm pixel resolution (treetop-focused), 70–80% front/side overlap.
- Wavelength bands: blue (475 ± 20 nm), green (560 ± 20 nm), red (668 ± 21 nm), red edge (717 ± 10 nm), NIR (840 ± 40 nm).
- Calibration: captured ground gray reference panel and downwelling radiation for reflectance conversion; data processed with Pix4D Mapper.
- Note: not all sites flown ( Burke, Jolanta-4 excluded; eastern Jolanta-3 edge excluded).

## Quality control and preprocessing
- Ground spectra: removed ~15 spectra (<1%) with non-vegetation features; restricted to 400–1075 nm, excluding 325–399 nm due to low signal-to-noise; averaged replicates to a single spectrum; Savitzky–Golay smoothing.
- UAV spectra: aggregated to 0.5 m resolution; masked canopy pixels using NDVI threshold (≥0.8) and mean reflectance threshold (0.05–0.13); extracted reflectance from pixels within a 4 m radius of focal trees.
- Spatial handling: ploidy values interpolated to samples near known ploidy via k-nearest-neighbor with k=1; ensured interpolation did not exceed 50 m; grounded in observed clonal homogeneity at small scales (<50 m).

## Data structure and accessibility
- File S1: Georeferenced genetic information (CSV)
  - Columns: Site, Plot, Tree, Ploidy (diploid/triploid), Clone_name, Provenance, E_m, N_m (UTM 13N coordinates)
- File S2: Reflectance spectra (CSV)
  - Columns: Type (measurement method), Site, Plot, Tree, Ploidy, Clone_name, Provenance, Spectral_band (nm or band label), Reflectance (0–1)
- File S3: Orthorectified multispectral imagery (TIFF)
  - Channels: blue, green, red, red-edge, NIR; values 0–1; georeferenced in UTM 13N
- All data references and sampling metadata are provided to support reproducibility and reuse.

## References and context
- Key microsatellite markers and methods cited (Mock et al., Smulders et al., Tuskan et al., etc.).
- Validation context for ploidy inference and the expectation of high reliability in triploidy/diploidy calls.

## How the data support analysis (analyst perspective)
- Enables investigation of associations between ploidy level and spectral signatures across scales (leaf, bark, canopy) and across diverse environmental conditions.
- Supports development of classifiers linking spectral features to ploidy, with explicit metadata for provenance and measurement type.
- Provides a framework for fusing ground-based and UAV-derived spectral data, with preprocessing steps and quality controls documented to ensure comparability.
- The dataset acknowledges and documents limitations (e.g., incomplete marker amplification, selective site coverage for UAV data) and describes methods to mitigate potential biases (resampling, limited interpolation distance).