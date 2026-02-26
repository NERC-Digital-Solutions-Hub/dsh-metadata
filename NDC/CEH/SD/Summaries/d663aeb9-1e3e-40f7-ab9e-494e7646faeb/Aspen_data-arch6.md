# Metadata for Blonder et al., Spectral data for quaking aspen (Populus tremuloides) clones of different ploidy levels

## Overview
- Study conducted summers 2016–2017 across a network of aspen forest sites in southwestern Colorado (Gunnison National Forest) to capture ploidy diversity and associated spectral data.
- Sites span elevation 2730–3630 m, within ~37 km, near Almont, Crested Butte, and Gothic.
- Each site contains multiple georeferenced plots within 1 km of the site center; total of 220 independent ploidy measurements collected.
- Unique ploidy assignments were applied to multiple plots/samples within plots due to cost constraints; effective sample sizes per site/analysis were variable.
- Emphasis on classifier predictive ability rather than formal statistical significance; pseudoreplication concerns mitigated by resampling and focusing on data usefulness for downstream analyses.

## Study design and sampling
- Plots located within 1 km of site centers; diverse forest types and substrates sampled.
- Leaves collected from canopy using slingshot/rope or pruners; samples dried for ploidy analysis.
- Ground- and canopy-level spectral data collected to enable linking spectral signatures with ploidy.

## Genotypic analysis and ploidy determination
- Ploidy measured for n = 220 samples; n = 210 samples analyzed by microsatellite markers.
- Microsatellite analysis used nine informative markers (out of an initial set; some markers failed).
  - Markers: ORPM 206 and PMGC 2571 failed to amplify reliably; ORPM 028 was monomorphic.
  - Nine informative markers used to determine ploidy: triploid if three alleles observed for at least one marker; diploid otherwise.
- Flow cytometry conducted on n = 10 samples (Burke site) using leaf tissue and Hordeum vulgare as a diploid standard; triploids identified as samples with ~50% higher fluorescence than the diploid standard.
- Previous work cited indicates high reliability for ploidy assessment with 6–10 microsatellites (about 97% correct classification across 296 individuals); no evidence of linkage disequilibrium among markers (rd = 0.008, p = 0.50).

## Spectral data collection

### Ground-based leaf spectra
- Measurements taken on the adaxial leaf surface before drying.
- Instrument: ASD Handheld 2 field spectrometer (325–1075 nm, 1 nm steps); three replicates per leaf.
- Calibration with white/black references prior to measurement.

### Ground-based bark spectra
- Bark samples (~5 cm2 area, ~2 mm depth) collected from stems at ~1.3 m height and measured in the lab.
- Samples kept moist and measured with the same instrument and wavelength range as leaves.
- Three spectral replicates per sample.

### Airborne canopy spectra
- July 2017: multispectral imaging over four sites (~500 m long) using a UAV (Tarot T560 Sport) with a Micasense RedEdge camera.
- Five spectral bands captured: Blue (475 ± 20 nm), Green (560 ± 20 nm), Red (668 ± 21 nm), Red Edge (717 ± 10 nm), NIR (840 ± 40 nm).
- Flights at 70–80% front/side overlap; ground reference calibration with a gray panel; incident radiation measured continuously.
- Data processed with Pix4D Mapper; reflectance calibrated against downwelling radiation and gray reference.
- Not all sites flown due to weather/permit constraints (Burke, Jolanta-4, and edge of Jolanta-3 excluded).

## Quality control and preprocessing
- Excluded n = 15 spectra (<1%) showing non-vegetation features (e.g., no chlorophyll peak).
- Spectral range trimmed to 400–1075 nm (325–399 nm removed for low SNR).
- Replicates averaged per sample; spectra smoothed with Savitzky–Golay filter (order 1, window 21).
- UAV imagery: aggregated to 0.5 m resolution; canopy pixels isolated via NDVI threshold (≥0.8) and mean reflectance threshold (0.05–0.13, site-dependent).
- Spectral values extracted from pixels within 4 m of focal trees; treated as replicates.

## Data processing, interpolation, and structure
- Ploidy values spatially interpolated to adjacent samples using k-nearest neighbors (k = 1); distance limited to 50 m to avoid extrapolation beyond clonal consistency.
- Each plot may have multiple spectral samples (ground-based leaves, ground-based bark, and/or canopy pixels) around the ploidy measurement locations.
- Data structure:
  - File S1: Georeferenced genetic information (CSV) with Site, Plot, Tree, Ploidy, Clone_name, Provenance, E_m, N_m.
  - File S2: Reflectance spectra (CSV) with Type, Site, Plot, Tree, Ploidy, Clone_name, Provenance, Spectral_band, Reflectance.
  - File S3: Orthorectified, atmospherically corrected multispectral imagery (TIFF) with 5 bands (Blue, Green, Red, Red-edge, NIR) georeferenced in UTM Zone 13N.

## Reliability, limitations, and notes
- Ploidy reliability draws on Mock et al. and earlier work: high accuracy when using 6–10 microsatellites; robust due to high genetic diversity and lack of strong linkage.
- Some microsatellite markers failed or were non-informative; nine markers used for ploidy inference.
- Interpolation limited to 50 m and based on clonal identity assumptions; results intended for classifier development and data exploration rather than absolute spatial inference.

## Data availability and references
- Data files S1–S3 provided with detailed metadata and spectral measurements.
- References include foundational work on microsatellite markers and ploidy assessment in Populus tremuloides and related Populus species.