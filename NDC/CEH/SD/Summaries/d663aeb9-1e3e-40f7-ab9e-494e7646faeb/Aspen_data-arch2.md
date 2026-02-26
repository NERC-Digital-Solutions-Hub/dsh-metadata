# Metadata for Blonder et al., Spectral data for quaking aspen (Populus tremuloides) clones of different ploidy levels

## Aim and scope
- Establish a network of aspen forest sites across a wide range of elevation and environmental conditions ( southwestern Colorado; 2730–3630 m; ~37 km span) to study quaking aspen clones of different ploidy levels.
- Collect genotypic (ploidy) and spectral data (ground-based leaves, bark; airborne canopy) to enable standardized environmental monitoring and comparison across environmental gradients.
- Create structured datasets suitable for monitoring environmental health and policy-relevant outputs over time.

## Study design and site characteristics
- Summers 2016–2017: network of sites near Almont, Crested Butte, and Gothic, CO; all within Gunnison National Forest.
- Site selection: representative range of environmental conditions; multiple georeferenced plots per site; plots within 1 km of site center.
- Sampling depth: 220 total ploidy measurements; effective sample sizes varied within plots due to shared ploidy assignments; no formal pseudoreplication concerns as analyses focused on classifier predictive ability and used resampling to control for size.
- Elevation range: 2730–3630 m; forest types range from tall stands to alpine scree stands; diverse soil and rock substrates.

## Genotyping and ploidy determination
- Ploidy measured for 210 samples via microsatellite analysis; an additional 10 samples assessed by flow cytometry (at one site).
- Microsatellite panel: nine informative markers (out of an initial larger set) with markers largely derived from Populus species; two markers failed to amplify or were monomorphic, leaving nine informative loci.
- Protocol: DNA extraction, two multiplex PCRs, touchdown PCR cycling, capillary electrophoresis, and scoring with GeneMapper.
- Ploidy calling: triploid if at least one marker shows three alleles; diploid if all markers show at most two alleles.
- Reliability: upheld by literature reporting high accuracy (97% across 296 individuals) for similar marker sets in P. tremuloides; no evidence of linkage disequilibrium in dataset, indicating sexual reproduction persists among clones.
- Flow cytometry approach: 1 cm² leaf sections measured against diploid Hordeum vulgare as standard; triploids identified by ~50% higher fluorescence relative to diploid standard.

## Spectral data collection and types
- Ground-based leaf spectra: 325–1075 nm (1 nm intervals) with three replicate measurements per leaf, measured on adaxial leaf surface before drying.
- Ground-based bark spectra: lab measurements on ~5 cm² bark sections after field collection; standardized preparation and identical spectral range as leaves.
- Airborne canopy spectra: July 2017, ~4 sites, 500 m long transects; UAV platform with Micasense RedEdge; five bands (blue, green, red, red edge, NIR); ground-based calibration with a gray reference panel and downwelling irradiance sensor; flights at ~70–80% image overlap; processed to orthorectified reflectance imagery.

## Data processing, quality control, and standardization
- Ground and canopy spectra QA/QC:
  - Removed ~15 spectra (<1%) with artifacts (e.g., no chlorophyll peak) indicating calibration/light-leak issues.
  - Excluded 325–399 nm due to low signal-to-noise; averaged three leaf replicates into a single spectrum; applied Savitzky–Golay smoothing.
- UAV data processing:
  - Downsampled imagery to 0.5 m resolution to minimize small-scale heterogeneity (shrubs, rocks).
  - Canopy masking using NDVI threshold (≥ 0.8) and mean reflectance threshold (0.05–0.13, site-dependent); extracted spectral information from a 4 m radius around focal trees; treated as replicates.
- Spatial data handling:
  - Ploidy data interpolated to adjacent plots using nearest-neighbor (k = 1) but never beyond 50 m; guided by evidence of clonal identity homogeneity at sub-50 m scales.
  - Spatial interpolation and data treatment decisions justified by prior work showing clonal stability and phenotype consistency at these scales.
- Data structure and accessibility:
  - File S1: georeferenced genetic information (CSV) with fields for site, plot, tree, ploidy, clone name, provenance, and coordinates (E/N in UTM Zone 13N).
  - File S2: reflectance spectra (CSV) with fields for site, plot, tree, ploidy, clone, provenance, spectral band or wavelength, and reflectance value.
  - File S3: orthorectified, atmospherically corrected multispectral imagery (TIFF) with blue, green, red, red-edge, NIR channels; geo-referenced in UTM Zone 13N.

## Data structure and accessibility
- File S1: Georeferenced genetic information across all measurement types; includes ploidy (diploid/triploid) and provenance of ploidy determination.
- File S2: Spectral measurements by type and sample, with corresponding metadata for site, plot, tree, and ploidy.
- File S3: Co-registered multispectral imagery (orthorectified) for selected sites; channels ordered as blue, green, red, red-edge, NIR.
- Datasets are organized to support cross-file integration for environmental monitoring analyses, trend tracking, and policy-relevant reporting.

## References and methodological context
- Prior work underpinning ploidy assessment reliability (Mock et al. 2008, 2012) and clonal dynamics (Mock et al. 2008).
- Microsatellite marker resources (Smulders et al. 2002; Tuskan et al. 2004).
- General methods for flow cytometry-based ploidy estimation and spectral data processing referenced in the metadata.

## Relevance to environmental monitoring practice
- Demonstrates a standardized, multi-modal data collection and processing pipeline integrating genotypic information with spectral signatures across environmental gradients.
- Produces structured, interoperable datasets (ground-based and UAV-derived) suitable for monitoring forest health, detecting spectral–genotypic associations, and informing management decisions.
- Addresses data value and accessibility challenges by storing data in clearly defined files with metadata-rich records and by documenting QA/QC and interpolation strategies to enable reuse and integration with other environmental datasets.