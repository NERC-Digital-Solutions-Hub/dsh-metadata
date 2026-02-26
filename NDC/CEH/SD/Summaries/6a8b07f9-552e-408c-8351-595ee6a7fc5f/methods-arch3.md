# Biomass maps of Mabalane, Gurue, and Maruppa, Mozambique

- A dataset describing aboveground woody biomass (tC/ha) for three study areas in Mozambique: Mabalane, Gurue, and Maruppa.
- Three yearly layers per area: 2007, 2010, and 2014; each pixel represents biomass; -18.00000 indicates no data; negative values may occur due to noise.
- Data can be extracted by year from the three-layer stack for year-specific analyses.

## Data Structure

- Geotiff format with three layers per year corresponding to 2007, 2010, and 2014.
- Each layer is a biomass map of the study area at 15 m pixel size.
- The biomass layer is converted from sigma0 to carbon density (tC/ha) using Ryan et al. 2012 equation (not locally calibrated; data from central/northern Mozambique).

## Methods and Quality Control

- Input imagery: three ALOS PALSAR scenes per year (HV backscatter, power units) from late dry season; two tracks.
- Processing steps: calibration, terrain correction, despeckling (3x3 GammaMAP) in SNAP v2.0; mosaicked and pan-sharpened with Landsat 8 (Sept 2014) using manually selected tie points for georeferencing.
- Accuracy references (RMS errors and tie-point counts) are provided for each year/image (detailed in Table 1 of the source).
- Coregistration: attempted but deemed not necessary; georeferencing primarily relies on Landsat mosaic reference points.
- Limitations noted: biomass estimates may be inaccurate in flooded/wet areas; urban areas should be masked; consider increasing pixel size (e.g., 30–60 m) to suppress noise.
- Accuracy caveat: local validation with plot data is recommended to assess map accuracy.

## Data Usage and Considerations for Monitoring Frameworks

- Data provenance and transparency: acknowledges JAXA and ESA for providing ALOS PALSAR data; ESPA acknowledgment required.
- Data quality and governance: underlying data come with metadata and processing steps; data users should verify suitability against local conditions and consider masking unreliable areas (flooded, urban).
- Reproducibility: workflow described (sensor selection, processing steps, and reference dataset) enables replication and temporal comparison.
- Data sharing and metadata: the document emphasizes detailed method reporting; users should document usage of these maps and ensure proper attribution.

## Data Source Acknowledgments

- ALOS PALSAR data provided by JAXA (through Research Agreement and PI No. 1152); ESA provided ALOS data via Category-1 Proposals 7493 and 18624.
- ESPA acknowledgment required.

## References

- Ryan, C. M. et al. Quantifying small-scale deforestation and forest degradation in African woodlands using radar imagery. Glob. Chang. Biol. 2012.
- Ryan, C. M., Berry, N. J., & Joshi, N. Quantifying the causes of deforestation and degradation and creating transparent REDD+ baselines: A method and case study from central Mozambique. Appl. Geogr. 2014.