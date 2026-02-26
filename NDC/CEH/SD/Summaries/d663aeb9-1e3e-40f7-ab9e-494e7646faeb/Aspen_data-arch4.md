# Metadata for Blonder et al., Spectral data for quaking aspen (Populus tremuloides) clones of different ploidy levels

## Purpose and study design
- Establish a dataset linking spectral data with ploidy levels (diploid vs. triploid) across a network of aspen sites in southwestern Colorado.
- Summers 2016-2017: 4 sites with diverse elevation and environment within Gunnison National Forest; sites chosen to span representative conditions (2730–3630 m).
- Each site contained multiple georeferenced plots within a 1 km radius; total independent ploidy measurements: n = 220.
- Acknowledge variable effective sample sizes because ploidy was not measured for every stem/leaf; unique ploidy assigned to multiple plots/samples when needed.

## Ploidy determination (genotypic analysis)
- Samples: healthy, mature leaves collected from trees; ploidy measured for n = 220 samples (210 via microsatellite analysis; 10 via flow cytometry at one site).
- Microsatellite genotyping: 12 unlinked markers used; 9 informative markers retained after reliability checks (ORPM 206 and PMGC 2571 failed amplification; ORPM 028 monomorphic).
- Ploidy calling: triploid if three alleles observed for at least one marker; diploid otherwise. Prior work reports high accuracy (≈97%) using 6–10 markers in this species.
- Flow cytometry: used as an additional ploidy assessment for 10 samples at the Burke site.
- Quality notes: no evidence of linkage disequilibrium among markers; substantial sexual reproduction indicated; high genetic diversity supports ploidy inference from markers.

## Spectral data collection

### Ground-based leaf spectra
- Collection: fresh leaves measured on the adaxial surface before drying; three replicate spectra per leaf.
- Instrument: field spectrometer (ASD Handheld 2), 325–1075 nm, 1 nm interval; calibration against white/black references.

### Ground-based bark spectra
- Collection: bark samples (~5 cm2, ~2 mm depth) cut from trees (~1.3 m height) and stored in moist conditions prior to measurement.
- Processing: lab-based spectral measurements over the same 325–1075 nm range with three replicates per sample.

### Airborne canopy spectra
- Flights: July 2017, four sites (~500 m each); two sites (Burke, Jolanta-4) and eastern edge of Jolanta-3 not flown due to weather/permits.
- Sensor: Micasense RedEdge multispectral camera on a UAV (Terra or similar platform); bands: blue (475 ± 20 nm), green (560 ± 20 nm), red (668 ± 21 nm), red-edge (717 ± 10 nm), NIR (840 ± 40 nm).
- Calibration: ground gray reference panel and downwelling radiation for reflectance conversion.
- Flight geometry: ~70–80% front/side overlap; altitude controlled for consistent imaging.

## Data processing, quality control, and interpolation

### Quality control
- Preprocessing: remove ~1% spectra with non-vegetation features; exclude 325–399 nm due to low signal-to-noise; average triplicates into a single spectrum; apply Savitzky–Golay smoothing (order 1, window 21).
- UAV imagery: aggregate to 0.5 m resolution; mask canopy using NDVI threshold (>0.8) and mean reflectance threshold; extract spectral values from pixels within 4 m of focal trees.
- Spatial interpolation: assign ploidy to adjacent plots using k-nearest neighbors (k = 1); interpolation limited to distances <= 50 m; no extrapolation beyond 50 m to preserve cluster identity.

### Data structure and file contents
- File S1: Georeferenced genetic information for all measurements (CSV)
  - Columns: Site, Plot, Tree, Ploidy ( diploid/triploid ), Clone_name, Provenance, E_m (UTM 13N easting), N_m (UTM 13N northing)
- File S2: Reflectance spectra (CSV)
  - Columns: Type (method), Site, Plot, Tree, Ploidy, Clone_name, Provenance, Spectral_band (nm for non-canopy; B/G/R/Red-edge/NIR for canopy), Reflectance (0–1)
- File S3: Orthorectified multispectral imagery (TIFF)
  - 5 channels in order: blue, green, red, red-edge, NIR; georeferenced to UTM 13N
  - Coverage for Ben-1ha, Jolanta-1, Jolanta-2, Jolanta-3

## Data availability and limitations
- Spatial coverage: ground measurements across multiple plots; UAV data available for four sites, with some locations missing flights; interpolation applied within 50 m of known ploidy data.
- Data types: integrates genotypic ploidy data with ground-based and airborne spectral measurements across a consistent wavelength range.
- Limitations: reliance on a subset of informative microsatellite markers for ploidy (some markers failed); some spectra and plots not represented due to logistical constraints; interpolation introduces assumptions about spatial homogeneity of ploidy within short distances.
- Data governance: dataset organized in clearly labeled files with metadata for traceability and reuse; designed to support cross-site comparisons and integration with other data products.

## References
- Mock et al. (2008, 2012) on ploidy reliability and clonal dynamics in Populus tremuloides
- Smulders et al. (2002); Tuskan et al. (2004) on microsatellite markers for Populus species
- Bennett & Leitch (2005) plant DNA C-values database
- Cole (2005) PCR methodology for microsatellite analysis