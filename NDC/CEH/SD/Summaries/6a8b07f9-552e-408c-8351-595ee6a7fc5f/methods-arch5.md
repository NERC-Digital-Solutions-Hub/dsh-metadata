# Biomass maps of Mabalane, Gurue, and Maruppa, Mozambique

## Data overview
- Dataset represents aboveground woody biomass (tC/ha) for three study areas in Mozambique: Mabalane, Gurue, and Maruppa.
- Structure: three GeoTIFF layers stacked as band 1 = 2007, band 2 = 2010, band 3 = 2014; each pixel holds biomass value.
- No-data value is -18.0; negative biomass values may occur due to noise.
- Individual layers can be extracted for year-specific analyses.

## Data structure and content
- Three-layer geotiff per dataset (one per year) with the biomass values in tC/ha.
- Wireframe of layers allows year-specific analyses while maintaining a consistent spatial extent.

## Methods and processing
- Method follows Ryan et al. (2012, 2014) and is updated for PALSAR-2.
- Data sources: three ALOS PALSAR scenes per year (2007, 2010, 2014) using HV backscatter in power units.
- Acquisition: late dry season, from two tracks; calibrated, terrain-corrected, and speckle-filtered with a 3x3 GammaMAP filter (SNAP v2.0); output at 15 m pixel.
- Per-year scenes are georeferenced to a mosaicked, pansharpened Landsat 8 image (Sept 2014) using ENVI v4.8; tie points are manually selected around the image for georeferencing.
- Tie-point accuracy is reported in Table 1 (mean/max RMS errors, number of tie points per scene; RMS errors range roughly from ~0.6 to ~1.9 pixels across years and scenes).
- Biomass layer values are converted from sigma0 to carbon density using Ryan et al. (2012) equation; note this calibration is not local to the study area.
- Limitations acknowledged: accuracy not validated with local plot data; maps may be inaccurate in flooded/wet areas and in urban areas; recommended masking these areas.
- Noise considerations: suggested to resample to 30–60 m to suppress noise.

## Quality, limitations, and caveats
- Local calibration is not performed; accuracy relies on referenced equations and external validations.
- Wetlands, flooded areas, and urban areas may produce biased biomass estimates; mask these regions.
- Significant uncertainties due to cross-sensor calibration, terrain effects, and lack of local plot-based validation.
- Accuracy estimates exist in Ryan et al. (2012) and should be consulted for site-specific expectations.
- The dataset is historical (2007, 2010, 2014); no ongoing update mechanism described.

## Provenance, attribution, and licensing
- Data produced from ALOS PALSAR and Landsat 8 imagery; requires acknowledgment of image providers:
  - JAXA (ALOS PALSAR data) under Research Agreement PI No. 1152
  - ESA (ALOS data via Category-1 Proposals 7493 and 18624)
  - ESPA acknowledgement is required separately
- Users must cite the cited Ryan et al. (2012, 2014) methodology references when applicable.

## Access, reuse, and data governance
- The three-year biomass product allows year-specific analyses by extracting the corresponding layer.
- For reuse, acknowledge JAXA/ESA/ESPA per above and cite the Ryan et al. references.
- Metadata should document:
  - Data structure (three-layer GeoTIFF with years 2007, 2010, 2014)
  - Unit and data units (tC/ha)
  - No-data handling (-18.0)
  - Processing chain (calibration, terrain correction, despeckling, georeferencing)
  - Known limitations (non-local calibration, wetland/urban masking recommendations)

## References
- Ryan, C. M. et al. Quantifying small-scale deforestation and forest degradation in African woodlands using radar imagery. Glob. Chang. Biol. 2012.
- Ryan, C. M., Berry, N. J. & Joshi, N. Quantifying the causes of deforestation and degradation and creating transparent REDD+ baselines: A method and case study from central Mozambique. Appl. Geogr. 2014.