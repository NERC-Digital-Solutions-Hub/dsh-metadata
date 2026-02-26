# Modelled surface nitrogen dioxide (NO2) for the grassland growing season in the UK and USA in 2018.

- Authors: Sharps, K.; Vieno, M.; Beck, R.; Hayes, F.
- Purpose: Provides a GIS-ready, map-based data product of modeled NO2 concentrations during the grassland growing season for the UK and USA in 2018, enabling spatial analysis and visualization for policy, client briefing, or public-facing maps.

## Data and modelling approach

- Modelling framework: EMEP-WRF global model, version 4.45, derived from the EMEP MSC-W model and driven by WRF meteorology.
- Meteorology: Hourly 3D meteorological data generated with WRF v4.2.2 for 2018; initialisation/nudging every six hours using GFS-FNL reanalysis data.
- Domain and resolution: Global domain with a horizontal resolution of 1° x 1°; 21 vertical layers, surface thickness ~40 m to top ~16 km.
- Emissions input: IIASA ECLIPSE v6a GAINS emissions for the year 2015.
- Temporal scope: Daily surface NO2 values produced per grid cell; seasonal average computed for the grassland growing season (mid-April to mid-July) for 2018.
- Output units and CRS: Surface NO2 in micrograms per cubic metre (ug/m^3) using the Geographic Coordinate System WGS84 (decimal degrees).

## Output data characteristics

- Spatial coverage: Global grid aggregated to 1° x 1° cells with attribution by country (USA or UK).
- Seasonal average: NO2 values reflect the grassland growing season mean for 2018 in USA and UK.

## Data structure and attributes

- Shapefile contains gridded data (1° x 1° resolution) with five attributes:
  - FID: Unique grid cell identifier
  - Lon: Longitude of grid cell centre (decimal degrees)
  - Lat: Latitude of grid cell centre (decimal degrees)
  - NAME: Country (USA or UK)
  - NO2_ug: Mean surface NO2 during the grassland growing season (mid-April to mid-July, 2018) in ug/m^3

## Quality control and validation

- QA/QC: EMEP model outputs undergo quality assurance and control before use.
- Validation context: A related study (Ge et al., 2021) evaluated global EMEP-WRF model performance against measurements for 2010 and 2015, showing the model captures overall spatial and seasonal variations in NO2 across major regions, including Europe and North America.

## GIS usage considerations

- Suitable for map-based visualization, thematic mapping, and spatial analysis of NO2 exposure during the grassland growing season.
- Easy to integrate into GIS workflows as a shapefile with explicit 1° grid resolution and clearly labeled attributes.
- Potential for comparative analyses with other spatial datasets (e.g., land cover, vegetation health, or emissions inventories).

## Limitations and caveats

- Grid resolution is relatively coarse (1° x 1°); finer-scale patterns are not captured.
- Based on model outputs using emissions data from 2015 and meteorology from 2018; not measured data.
- Represents the UK and USA only within the grassland growing season; applicability to other seasons or regions would require new modelling.

## References

- CLRTAP (2017) Mapping critical levels for vegetation. LRTAP Modelling and Mapping Manual.
- Ge, Y., et al. (2021) Evaluation of global EMEP MSC-W (rv4.34) WRF model outputs against measurements.
- Mills, G., et al. (2018) Ozone pollution and crop production impacts.
- Simpson, D., et al. (2012) The EMEP MSC-W chemical transport model technical description.
- Vieno, M., et al. (2016) Sensitivities of emissions reductions for UK PM2.5 mitigation.