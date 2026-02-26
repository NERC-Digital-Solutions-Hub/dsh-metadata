# Metadata for Blonder et al., Spectral data for quaking aspen (Populus tremuloides) clones of different ploidy levels

## Overview and GIS relevance
- Provides georeferenced, multi-source spectral and genetic data across aspen sites to enable map-based analysis of ploidy patterns and spectral signatures.
- Data are structured for integration into GIS workflows: plot/tree-level coordinates, site metadata, and multiple raster/vector outputs (spectral data and imagery).

## Study area and sampling design
- Timeframe: summers 2016–2017.
- Location: southwestern Colorado, within Gunnison National Forest; sites span Almont, Crested Butte, and Gothic, with up to 37 km between sites.
- Elevation: 2730–3630 m.
- Sampling units: multiple georeferenced plots per site; total independent ploidy measurements: n = 220.
- Spatial layout: plots within 1 km of site centers; sample interpolation used to assign ploidy to nearby plots.
- Coverage: ground-based and airborne data collected across diverse forest types and substrates.

## Ploidy determination (genotypic analysis)
- Methods and data quality:
  - Microsatellite analysis for n = 210 samples using nine informative markers; triploidy defined by observing three alleles at a marker.
  - Flow cytometry for 10 samples at one site (Burke) to corroborate ploidy.
  - Prior work indicates high reliability (approx. 97% correct classification with 6–10 markers).
- Sampling caveats:
  - Ploidy assigned to multiple plots/samples due to cost constraints; intentional avoidance of pseudoreplication in analysis.
  - Genetic data support clonal identity and limited linkage disequilibrium, indicating sexual reproduction occurs among clones.

## Ground-based spectral data

### Leaf spectra
- Measurement: fresh leaves scanned on adaxial surface; spectral range 325–1075 nm (1 nm intervals).
- Replicates: three per leaf; measurements taken before drying.
- Calibration: standard white/black references; spectra pre-processed (calibration, S-G smoothing, averaging).

### Bark spectra
- Measurement: lab-based, ~5 cm² bark samples from ~2 mm depth; same spectral range and instrument as leaves.
- Replicates: three per sample; careful selection of homogeneous bark areas.

## Airborne canopy spectra
- Platform: unmanned aerial system (UAS) flights in July 2017 at four sites (not all sites).
- Sensor: Micasense RedEdge multispectral camera; bands in blue, green, red, red-edge, NIR.
- Flight parameters: ~70–80% image overlap, ~90–120 m AGL; calibration with a gray reflectance panel and downwelling radiation sensor.
- Processing: images stitched (Pix4D), reflectance calibrated; spatial alignment with ground data.

## Quality control and preprocessing
- Spectral data cleaning:
  - Removed ~15 spectra (<1%) with calibration or light-leak issues.
  - Excluded 325–399 nm due to low signal-to-noise; averaged triplicates into single spectra; applied Savitzky–Golay smoothing.
- UAV data processing:
  - Aggregated to 0.5 m resolution; canopy pixels isolated using NDVI threshold (>0.8) and a mean reflectance threshold (0.05–0.13, site-dependent).
  - Spectral samples extracted within 4 m radius of focal trees; treated as replicates.
- Spatial data handling:
  - Ploidy values interpolated to adjacent plots using 1-NN interpolation within 50 m; no interpolation beyond 50 m.
  - Clonal identity assumed homogeneous within the defined spatial scales.

## Data structure and files

- File S1: Georeferenced genetic information (CSV)
  - Columns: Site, Plot, Tree, Ploidy, Clone_name, Provenance, E_m, N_m (UTM Zone 13N coordinates)
- File S2: Reflectance spectra measurements (CSV)
  - Columns: Type (measurement method), Site, Plot, Tree, Ploidy, Clone_name, Provenance, Spectral_band (nm or canopy band label), Reflectance (0–1)
- File S3: Orthorectified multispectral imagery (TIFF)
  - Georeferenced to UTM Zone 13N; channels ordered as blue, green, red, red-edge, NIR; reflectance values 0–1

## Spatial and GIS considerations
- Coordinate system: Universal Transverse Mercator Zone 13N (UTM 13N) for all coordinates.
- Data layers:
  - Point-level ploidy and clone metadata for plot/tree mapping.
  - Ground-based spectra linked to site/plot/tree for spectral signature analysis.
  - UAV-derived 5-band imagery for landscape-scale spectral mapping and classifier development.
- Resolution and scale:
  - Ground measurements tied to plot-level locations; UAV imagery at 0.5 m resolution; sampling within 4 m radius around focal trees.
- Potential GIS uses:
  - Mapping ploidy distribution across landscapes.
  - Developing spectral classifiers to predict ploidy from leaf, bark, or canopy spectra.
  - Integrating genetic provenance with spectral phenotypes for habitat suitability or conservation planning.

## Reuse and references
- Data formats (CSV, TIFF) and metadata enable reproducible GIS analyses and cross-site comparisons.
- Cited methodological references underpin ploidy assessment reliability and microsatellite marker selection.

## Notes for practitioners
- Ensure consistent CRS (UTM Zone 13N) when integrating with other GIS layers.
- Consider proximity-based interpolation limitations (≤50 m) when aggregating ploidy to additional samples.
- Use File S3 imagery for region-wide spectral analyses and to link canopy reflectance with underlying genetic ploidy information.