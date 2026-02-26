# Spatial distribution of FIOs in standing waters within UK Hydroscapes

- Purpose: Examine spatial distribution of fecal indicator organisms (FIOs) and their drivers in standing waters across UK Hydroscapes to inform water quality, ecology, and public health considerations for recreational use.

## Study areas and design

- Three Hydroscapes selected to represent contrasting landcovers:
  - Greater Glasgow (urban)
  - Norfolk (agricultural)
  - Cumbria (upland/pastoral)
- Within each Hydroscape: 18 water bodies (lakes) sampled to cover a gradient of size, productivity, hydrological connectivity, and ecological quality.
- Sampling periods: Spring, Summer, and Autumn in 2016 or 2017.

## Sampling and analysis methods

- Sampling timing: All samples collected 3 hours after sunrise for consistency with UAV exposure.
- Spatial sampling within lakes: Three discrete locations per lake, separated by ~100 m; samples from shallow water (<0.5 m) by wading.
- Subsampling design: At each location, three subsamples separated by ~5 m, yielding nine unique samples per water body per visit.
- Total samples: 1,278 unique samples across all lakes/visits.
- Water collection and preservation:
  - Approximately 30 cm depth
  - Sterile 180 ml bottles
  - Stored at 4°C
  - Processed within 6 hours of collection
- Microbiological analysis:
  - Filter three volumes (100 ml, 10 ml, 1 ml) through 0.45 μm membranes
  - Plated on MLGA agar; incubated at 37°C; read after 24 hours
  - Results expressed as colony forming units (CFU) per 100 ml
- Measured parameters:
  - E. coli concentrations (CFU per 100 ml)
  - Total heterotrophs concentrations (CFU per 100 ml)

## Data structure and variables

- Data source: Field data for standing waters in the UK.
- Key fields (as described in the appendix for the CSV):
  - Hydroscape: Landscape type (Greater Glasgow, Cumbria, Norfolk)
  - season: Spring, Summer, or Autumn
  - site: Focal water body name
  - sample: Spatially discrete sample code within a water body (1–3)
  - rep: Sub-sample identifier (a–c)
  - Ecoli: E. coli concentration (CFU per 100 ml)
  - Hetero: Total heterotrophs concentration (CFU per 100 ml)

## Appendix: field name descriptions

- Field names correspond to the dataset Disease_distribution_data_UK_standing_waters.csv and include:
  - Hydroscape, Description
  - season, Description
  - site, Description
  - sample, Description
  - rep, Description
  - Ecoli, Description
  - Hetero, Description

## GIS-focused considerations and potential uses

- Spatial analysis opportunities:
  - Map distribution of E. coli and heterotrophs across Hydroscapes to identify hotspots and gradients.
  - Compare microbial loads across landcover types (urban vs. agricultural vs. upland/pastoral).
  - Integrate with ancillary spatial data (hydrology, land use, rainfall) to model drivers.
- Data preparation for GIS:
  - Ensure spatial coordinates or centroids for each water body and sampling location are available.
  - Standardize field names and units (CFU per 100 ml) for cross-site comparability.
  - Link sample-level data to water body polygons and Hydroscape attributes for map-based visualization.
- Limitations and considerations:
  - Sampling occurs at discrete points within lakes; consider spatial interpolation cautiously.
  - Temporal coverage spans multiple seasons/years; account for seasonal variation in analyses.
  - Appendix indicates a consistent protocol, aiding reproducibility and cross-site comparisons.