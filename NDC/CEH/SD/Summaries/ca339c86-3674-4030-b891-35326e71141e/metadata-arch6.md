# Global plant climate envelopes

## Overview
- Aims to produce a bioclimatic envelope for each GBIF-recorded plant species for 1901–2018 using occurrence data and historical climate.
- Envelopes are adjusted for collection effort using MODIS Enhanced Vegetation Index (EVI) to reduce sampling biases.
- Outputs a single, ready-to-use data product intended to support exploration of species’ climate tolerances and potential responses to climate change.

## Data Sources
- Plant occurrence records from GBIF (1901–2018), filtered for species with accepted names in The Plant List.
- Climate reconstructions: ECMWF CERA-20C and ERA-Interim (monthly means of daily data) for 1901–2018; ERA-Interim data extended to 2018 for higher spatial resolution (1979–2018 subset reused).
- Climate variables include temperature, precipitation, solar radiation, and soil moisture/temperature layers.
- Global vegetation proxy: mean global Enhanced Vegetation Index (EVI) from MODIS (2001–2015) to correct for plant density and observation bias.
- Exclusions: Antarctica and Arctic islands (e.g., Greenland) due to data quality concerns.

## Aim
- Derive a single species-specific climate envelope per climate variable that captures the range of conditions the species could tolerate, using historical occurrence data and climate context while correcting for sampling bias.

## Methodology
- Data preparation:
  - Start with ~212 million GBIF records; filtered to ~215,000 species and just over 100 million records after quality filters.
  - Remove botanic garden records (0.02° buffer) and similarly check centroid records; assess top recording institutions but retain original data after comparison.
  - Acknowledge GBIF’s lack of native/alien differentiation; consider introductions informative for potential tolerance in novel climates.
- Climate profiling:
  - For each GBIF record, extract climate data for the record’s month/location and the preceding 11 months (12-month profile per variable).
  - Average across the 12 months per climate variable; for temperature also compute min and max.
- Envelope construction:
  - Bin records per species into 1,000 bins for each climate variable to create envelope profiles.
  - Apply bias corrections to account for uneven sampling across space.
- Bias correction and weighting:
  - Weight binned species profiles by the ratio of global distribution of plant collections to a proxy of plant abundance (EVI).
  - Use EVI to downweight overrepresented regions (e.g., Western Europe, Eastern USA, Australia) and upweight underrepresented regions (tropics).
  - Average across climate bins, weighted by the number of records, to produce an overall value per species for each climate variable.
- Outputs and code:
  - Full methods and code available in associated resources (Zenodo DOI provided).

## Dataset Description
- A single CSV file containing the average value of the climate envelope per species for the following ECMWF parameters:
  - tmin, tmax, tmean, trng (temperature-derived metrics)
  - stl1–stl4 (soil temperature levels 1–4)
  - swvl1–swvl4 (volumetric soil water layers 1–4)
  - ssr (surface net solar radiation)
  - tp (total precipitation)
- Metadata included for each species:
  - SppID, taxonomic information (phylum, class, order, family, genus), and the number of occurrence records informing the envelope (numrecords).
- Temperature variables include derived statistics (min/max for tmin/tmax/tmean as applicable). Antarctica and Arctic islands excluded from processing.

## Outputs and Access
- The dataset provides per-species climate envelopes suitable for downstream analyses, such as species distribution modelling and climate-change impact assessments.
- Associated paper and code resources referenced for full methodological details and replication.

## References
- BGCI. (2019). GardenSearch online database.
- Dee, D. P. et al. (2011). ERA-Interim reanalysis: Configuration and performance.
- GBIF. (2019). Global Biodiversity Information Facility.
- Gibson, H., & Weiss, D. (2015). Oxford MAP EVI: MODIS gap-filled vegetation index.
- Huete, A., Justice, C., & van Leeuwen, W. (1999). MODIS Vegetation Index (MOD13) Algorithm.
- Laloyaux, P. et al. (2018). CERA-20C: A coupled reanalysis of the twentieth century.
- TPL. (2013). The Plant List Version 1.1.