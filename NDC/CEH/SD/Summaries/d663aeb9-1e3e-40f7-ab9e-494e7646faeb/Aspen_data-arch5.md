# Metadata for Blonder et al., Spectral data for quaking aspen (Populus tremuloides) clones of different ploidy levels

## Overview
- A multi-method study of quaking aspen clones across SW Colorado (2016–2017) integrating ploidy data with ground-based and airborne spectral measurements.
- Network spans elevation 2730–3630 m, within Gunnison National Forest; sites chosen to represent diverse environmental conditions.
- Total ploidy measurements: 220 across plots and trees; effective sample sizes per site/analysis varied due to reuse of ploidy assignments across multiple plots/samples.
- Data are organized to enable linkage between genetic (ploidy) information and spectral reflectance data (leaf, bark, and canopy).

## Study design and sampling
- Sites located within ~37 km, near Almont, Crested Butte, and Gothic, CO; georeferenced with handheld GPS and laser rangefinder.
- Each site comprises multiple georeferenced plots within 1 km of the site center.
- Sampling approach allowed assignment of a single ploidy label to multiple plots/samples to reflect clonal structure.
- Ploidy assessment leveraged both microsatellite data and, at one site, flow cytometry for cross-validation.

## Genotyping and ploidy determination
- Microsatellite analysis conducted on n=210 samples (across Ben-1ha, Jolanta-1, Jolanta-2, Jolanta-3, Jolanta-4).
- A total of 12 unlinked microsatellites were tested; after quality checks, 9 informative markers used (two markers failed to amplify reliably; one was monomorphic).
- Ploidy called as triploid if three alleles observed at at least one marker; otherwise diploid.
- Reliability of microsatellite-based ploidy inference supported by prior work (high accuracy with 6–10 markers) and lack of linkage disequilibrium (rd = 0.008, p = 0.50).
- Flow cytometry used for n=10 samples at Burke site as an additional ploidy assessment, using Hordeum vulgare as a diploid standard.
- Provisions to demonstrate sexual reproduction within clones and to justify using clonal spatial interpolation instead of treating all samples as independent.

## Spectral data collection
- Ground-based leaf spectra: fresh leaves measured adaxially on 325–1075 nm range (1 nm resolution) with ASD FieldSpec handheld spectrometer; three replicates per leaf; measurements taken pre-drying.
- Ground-based bark spectra: laboratory measurements on ~5 cm² bark sections using identical spectrometer setup; samples kept moist and measured under controlled conditions.
- Airborne canopy spectra: July 2017, four sites surveyed with a UAV (Micasense RedEdge) at ~90–120 m AGL; five spectral bands (Blue 475, Green 560, Red 668, Red Edge 717, NIR 840 nm); ground reference calibration with a gray panel and downwelling irradiance sensor; flights adopted ~70–80% overlap; images processed with Pix4D Mapper and reflectance calibrated.

## Data quality control and preprocessing
- Ground spectra: removed about 15 spectra (<1%) with non-vegetation features; trimmed to 400–1075 nm; averaged triplicates into a single spectrum; applied Savitzky–Golay smoothing (order 1, window 21).
- UAV canopy spectra: resampled to 0.5 m resolution; canopy pixels masked using NDVI threshold (≥0.8) and mean reflectance threshold; extracted reflectance from pixels within a 4 m radius of focal trees; treated as replicates.
- Spatial data handling: ploidy values interpolated to adjacent samples using 1-nearest-neighbor interpolation; interpolation distance limited to ≤50 m based on prior evidence of clonal homogeneity; no interpolation beyond 50 m.
- Data organization across measurement types includes clear provenance and replication decisions to support reproducibility and dataset integration.

## Data processing and spatial integration
- Spatial interpolation rationale grounded in known clonal identity homogeneity at sub-50 m scales; proximity-based assignment ensures plausible ploidy labeling for spectral samples near known ploidy measurements.
- All data are aligned to a common geospatial framework (UTM Zone 13N) and associated with site/plot/tree identifiers to enable cross-modal linking.

## Data structure and files
- File S1. Georeferenced genetic information for all measurement types at all sites (CSV)
  - Columns include Site, Plot, Tree, Ploidy, Clone_name, Provenance, E_m, N_m, etc.
- File S2. Reflectance spectra measurements at each site (CSV)
  - Columns include Type, Site, Plot, Tree, Ploidy, Clone_name, Provenance, Spectral_band, Reflectance.
- File S3. Orthorectified and atmospherically corrected multispectral imagery (TIFF)
  - Channels ordered as blue, green, red, red-edge, NIR; georeferenced in UTM Zone 13N.

## Data governance considerations for data stewards
- Provenance and traceability: detailed methodology for ploidy determination (microsatellites, flow cytometry) and for spectral data collection and processing; explicit recording of marker performance (which markers amplified/not amplified or were monomorphic).
- Metadata completeness: site, plot, tree identifiers; ploidy, clone identifiers; measurement type (leaf, bark, canopy); data provenance for each record; geospatial coordinates with UTM references.
- Data quality controls: documented QC steps for both ground-based and UAV-derived spectra; removal criteria for non-vegetation spectra; replication handling and smoothing parameters.
- Interoperability and standards: multiple data types (genetic, leaf/bark spectra, canopy imagery) integrated with consistent coordinate reference system; careful note of processing steps to support reproducibility.
- Limitations and caveats: partial ploidy coverage (210/220 samples), some microsatellite markers failing, single-site flow cytometry validation, interpolation limited to 50 m, and NDVI-based canopy masking thresholds that may influence sample selection.

## References
- Agapow, P.-M. & Burt, A. (2001) Indices of multilocus linkage disequilibrium. Molecular Ecology Notes.
- Bennett, M. & Leitch, I. (2005) Plant DNA C-values database. Kew.
- Cole, C. T. (2005) Allelic and population variation of microsatellite loci in aspen. New Phytologist.
- Mock, K. E. et al. (2012) Widespread triploidy in western North American aspen. PLoS One.
- Mock, K. E. et al. (2008) Clonal dynamics in western North American aspen. Molecular Ecology.
- Smulders, M. J. M. et al. (2002) Trinucleotide repeat microsatellite markers for black poplar. Molecular Ecology Notes.
- Tuskan, G. A. et al. (2004) Characterization of microsatellites revealed by genomic sequencing of Populus trichocarpa. Canadian Journal of Forest Research.