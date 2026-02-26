# Metadata for Blonder et al., Spectral data for quaking aspen (Populus tremuloides) clones of different ploidy levels

## Aims and scope
- Documents a dataset linking spectral measurements (leaf, bark, and canopy) to ploidy levels in quaking aspen clones across environmental gradients.
- Combines ground-based measurements and airborne multispectral imagery with genotypic ploidy determinations (microsatellites, flow cytometry) to enable analysis of spectral signals associated with ploidy.

## Study design and sampling
- Timeframe and location: Summers 2016–2017; four aspen sites in southwestern Colorado within Gunnison National Forest, spanning elevation 2730–3630 m.
- Spatial layout: Sites within ~37 km of each other, with multiple georeferenced plots per site (each plot within 1 km of site center).
- Sampling intensity: n = 220 ploidy measurements collected; effective sample sizes per site/analysis varied due to assigning a single ploidy level to multiple plots/samples for cost reasons.
- Rationale: Sampling aimed to cover a locally representative range of environmental conditions; pseudoreplication concerns mitigated by focusing on classifier predictive ability and using resampling to control for sample size.

## Genotypic analysis and ploidy determination
- Primary method: Microsatellite analysis for 210 samples using nine informative markers (out of an initial suite; some markers failed to amplify reliably).
- Ploidy calling: Triploid if three alleles observed at any marker; diploid if only up to two alleles observed for each marker.
- Validation: Flow cytometry performed on 10 samples at the Burke site as supplementary confirmation.
- Methodological basis: Marker selection and interpretation draw on prior work showing high reliability (≈97% correct classification across 296 individuals) due to high genetic diversity in P. tremuloides.
- Data provenance: Ploidy assignments drawn from combined data across co-authors’ independent projects; no evidence of linkage disequilibrium (r_d = 0.008, p = 0.50).

## Spectral data collection

### Ground-based leaf spectra
- Procedure: Fresh leaves measured on the adaxial surface prior to drying; three replicate spectra per leaf.
- Equipment and range: Field spectrometer (ASD Handheld 2) covering 325–1075 nm (1 nm intervals); calibrated with white and dark references.
- Handling: Leaves kept moist prior to measurement; leaf measurement performed before drying in silica.

### Ground-based bark spectra
- Procedure: Bark samples (~5 cm2, ~2 mm depth) collected from stems and measured in the lab.
- Range and replicates: 325–1075 nm with three spectral replicates per sample.
- Sample selection: Homogeneous, smooth bark areas avoided damaged regions; samples stored in moisture-retaining conditions prior to measurement.

### Airborne canopy spectra
- Flight details: July 2017 over four sites; ~500 m transects; UAS (Tarot, T560 Sport) with a Micasense RedEdge camera.
- Spectral bands: Blue (475 ± 20 nm), Green (560 ± 20 nm), Red (668 ± 21 nm), Red Edge (717 ± 10 nm), NIR (840 ± 40 nm).
- Flight parameters: ~90–120 m AGL; 70–80% front/side overlap; downwelling radiation sensor and gray reference panel used for calibration; Pix4D Mapper for image stitching.
- Data processing: Reflectance calibrated against downwelling data and gray reference; canopy pixels isolated via NDVI and reflectance thresholds; spectral data extracted from pixels within a 4 m radius of focal trees.
- Site coverage: Flights conducted at four sites; Burke and Jolanta-4 not flown; eastern edge of Jolanta-3 not flown due to constraints.

## Quality control and data processing
- Spectral QC: Excluded n ≈ 15 spectra (<1%) lacking characteristic vegetation features; truncated data to 400–1075 nm (removed 325–399 nm due to low SNR); triplicate spectra averaged per sample; Savitzky-Golay smoothing (order 1, window 21).
- UAV data QC: Aggregated imagery to 0.5 m to reduce fine-scale noise; canopy masks created using NDVI threshold (≥ 0.8) and mean reflectance threshold (0.05–0.13; site-dependent); spectral samples treated as replicates within a plot.
- Spatial handling: Ploidy values interpolated to adjacent spectral samples using k-nearest-neighbor (k = 1) to assign the nearest known ploidy; interpolation constrained to within 50 m to reflect observed clonal homogeneity; no interpolation beyond 50 m.
- Data integrity: Interpolation guided by prior evidence of clonal identity homogeneity at <50 m scales and visual phenotypic consistency.

## Data structure and accessibility
- File S1: Georeferenced genetic information for all measurement types; columns include Site, Plot, Tree, Ploidy, Clone_name, Provenance, E_m, N_m.
- File S2: Reflectance spectra measurements; columns include Type, Site, Plot, Tree, Ploidy, Clone_name, Provenance, Spectral_band (nm for non-canopy; B/G/R/red-edge/NIR for canopy), Reflectance (0–1).
- File S3: Orthorectified and atmospherically corrected multispectral imagery (TIFF); channels ordered blue, green, red, red-edge, NIR; georeferenced in UTM Zone 13N.
- Supplement: Metadata references and methodology details supporting data provenance and reuse.

## Challenges and considerations for monitoring frameworks
- Data availability and access: Ground- and canopy-based datasets require careful integration across methods and sites; some data (e.g., specific markers) may fail to amplify, reducing marker set.
- Metadata completeness: Comprehensive metadata is provided (provenance, coordinates, sampling scheme), enabling reproducibility and audit trails.
- Data transformation: Spectral data required cleaning, normalization, and thresholding to enable cross-method comparability; spatial interpolation introduces assumptions about clonal homogeneity.
- Data governance and sharing: While not framed as an open-data policy, the dataset is accompanied by structured supplementary files and clear provenance, illustrating best practices for data sharing and reproducibility.
- Communication of complexity: The study involves multi-scale, multi-source data with nuanced interpretation (ploidy-linked spectral signals across environmental gradients), highlighting the need for clear visualization and reporting in monitoring frameworks. 

## References
- Agapow, P.-M. & Burt, A. (2001) Indices of multilocus linkage disequilibrium. Molecular Ecology Notes.
- Bennet, M. & Leitch, I. (2005) Plant DNA C-values database. Kew.
- Cole, C. T. (2005) Allelic and population variation of microsatellite loci in aspen. New Phytologist.
- Mock, K. E. et al. (2012) Widespread triploidy in western North American aspen. PLoS One.
- Mock, K. E. et al. (2008) Clonal dynamics in western North American aspen. Molecular Ecology.
- Smulders, M. J. M. et al. (2002) Trinucleotide repeat microsatellite markers for black poplar. Molecular Ecology Notes.
- Tuskan, G. A. et al. (2004) Characterization of microsatellites in Populus trichocarpa. Canadian Journal of Forest Research.