# Reflectance of charcoal from tropical rainforest plots in southern Amazonia, Brazil and southwestern Amazonia, Peru

## Data overview
- Dataset reflectance.csv containing charcoal reflectance measurements.
- Samples collected from soil surface in tropical rainforest plots (0.25 ha) at Feliz Natal, Brazil (n=75) and Pucallpa, Peru (n=14) in 2015.
- Total of 89 charcoal pieces measured; each sample measured 24–90 repetitions.
- Related to CAPES Brazil project (PVE177-2012), NERC project on past fires and carbon dynamics, Charcoal reflectance project (NE/N011570/1, 1628035), SilvaCarbon, and UNEMAT PhD project.

## Collection methods
- Charcoal pieces collected from the forest floor soil surface (0–5 cm depth).
- Organic material/soil removed with hydrogen peroxide digestion to clean samples.
- Samples embedded in resin and polished.
- Reflectance measured photometrically from the sample surface at the cell-wall junction.
- Instrumentation: TIDAS-MSP 200 microspectrometer, x50 objective (x32 eyepiece), MSP200 v3.27 software.
- Measurements conducted at Exeter Fire Lab.

## Nature and units of recorded values
- Reflectance values reported as percentages (%).

## Quality control
- Failed or non-convergent runs were discarded and not included in the dataset.

## Details of data structure
- Data stored in a comma-separated value file (reflectance.csv) with columns:
  - Site: Area where charcoal was sampled
  - Parcel: parcel identifier within the Site
  - Charcoal: code for the charcoal sample
  - Reflectance: reflectance value of the charcoal in %

## Geographic scope and samples
- Two study sites: Feliz Natal, southern Brazil, and Pucallpa, Peru.
- Total charcoal pieces: 89
- Samples per site: 75 at Feliz Natal, 14 at Pucallpa
- Depth context: soil surface 0–5 cm

## Relevance for GIS and data products
- Provides spatially referenced reflectance measurements by Site/Parcel, suitable for map-based data products.
- Potential to integrate with other GIS layers (e.g., fire history, soil types, vegetation) to analyze spatial patterns of charcoal reflectance.
- Note: Coordinates or geolocations are not specified in the summary; linking to GIS layers may require additional localization of Site/Parcel identifiers.
- Units standardized as percent reflectance, facilitating consistent comparison across samples.

## References
- Belcher, C. M., New, S. L., Santín, C., Doerr, S. H., Dewhirst, R. A., Grosvenor, M. J., & Hudspith, V. A. (2018). What can charcoal reflectance tell us about energy release in wildfires and the properties of pyrogenic carbon? Frontiers in Earth Science, 6, 169.
- Belcher, C. M., & Hudspith, V. A. (2016). The formation of charcoal reflectance and its potential use in post-fire assessments. International Journal of Wildland Fire, 25(7), 775-779.
- Crawford, A., Feldpausch, T., Marimon, B.H., de Oliveira, E., Belcher, C. (in press). Effect of tree wood density on energy release and charcoal reflectance under constant heat exposure. International Journal of Wildland Fire.
- New, S. (2020). Charcoal Reflectance: A Quantitative Approach to Understanding the Impact of Fire on an Ecosystem. University of Exeter. https://ore.exeter.ac.uk/repository/handle/10871/120478