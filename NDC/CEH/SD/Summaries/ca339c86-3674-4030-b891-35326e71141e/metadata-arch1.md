# Global plant climate envelopes

## Overview
- Aims to produce a bioclimatic envelope for every species recorded in GBIF over 1901–2018, based on occurrence data and historical climate.
- Envelopes are adjusted for collection effort using the Enhanced Vegetation Index (EVI) from MODIS to reduce sampling bias.
- Data supports understanding of the climates that species could tolerate, including environments beyond native ranges.

## Data sources
- GBIF occurrence records (1901–2018) for plant species with accepted names.
- ECMWF reanalysis climate reconstructions: CERA-20C and ERA-Interim for 1901–2018 (monthly means of daily data; precipitation and solar radiation from monthly means of daily forecast accumulations).
- Global Vegetation Index proxy for plant density: EVI (2001–2015), used to correct sampling biases.
- Botanic Gardens Conservation International (BGCI) locations to identify garden observations for exclusion.
- The Plant List (2013) for accepted species names.
- Exclusions: Antarctica and Arctic islands (including Greenland) due to data quality concerns.

## Methodology and data processing
- Species filtering: use only species with accepted names; remove marine species and fossils.
- Data cleaning: remove records georeferenced to botanic gardens (0.02 decimal degree buffer) and similarly around country centroids; evaluated top recording institutions but retained original data due to similar results.
- Climate timeline: combine CERA-20C and ERA-Interim; replace final 39 years (1979–2018) with ERA-Interim for higher spatial resolution, maintaining 1901–2018 coverage.
- Per-record climate extraction: assume each GBIF record’s site hosted the species for at least one year prior; extract climate variables for the record’s month and the preceding 11 months; average across the 12 months (except temperature, where both mean and range are computed).
- Bias correction: weight species’ climate profiles by the ratio of global species distribution to the EVI proxy of plant abundance to reduce observation bias from uneven sampling.
- Envelope construction: bin all records per species into 1,000 bins for each climate variable; generate 12-month climate profiles per species; weight bins by record counts to derive an average envelope value per climate variable.
- Output format is a single CSV with per-species envelopes and metadata.

## Dataset content and variables
- Output: a single CSV file containing the average plant climate envelope per species for 14 ECMWF-related parameters.
- Variables included (per 14 climate parameters):
  - tmin, tmax, tmean, trng
  - stl1, stl2, stl3, stl4 (soil temperature levels)
  - swvl1, swvl2, swvl3, swvl4 (volumetric soil water layers)
  - ssr (surface net solar radiation)
  - tp (total precipitation)
- Additional per-species fields:
  - SppID (unique species identifier)
  - taxonomic information: phylum, class, order, family, genus
  - numrecords (number of GBIF records informing the envelope)
- Temperature values include both central tendency (mean) and extremes (min/max) where applicable; other variables are represented by their average envelopes.

## Practical notes and interpretation
- GBIF data are spatially and taxonomically biased (e.g., overrepresentation in Western Europe, Eastern North America, Australia; underrepresentation in tropics). Bias corrections using EVI address this but some residual biases may remain.
- GBIF includes native and introduced occurrences; envelopes capture climates species can tolerate, including introductions to new environments, which is informative for understanding potential range shifts.
- The work emphasizes tolerance envelopes rather than strict native ranges, aligning with analyses of climate adaptability.
- Reproducibility: the associated paper (Harris et al., 2022) and code are available via a Zenodo link.

## References
- BGCI. 2019. GardenSearch online database.
- Dee, D. P., et al. 2011. The ERA-Interim reanalysis: Configuration and performance.
- GBIF. 2019. Global Biodiversity Information Facility.
- Gibson, H., & Weiss, D. 2015. Oxford MAP EVI gap-filled dataset.
- Huete, A., Justice, C., & van Leeuwen, W. 1999. MODIS Vegetation Index (MOD13) Algorithm.
- Laloyaux, P., et al. 2018. CERA-20C: A Coupled Reanalysis of the Twentieth Century.
- TPL. 2013. The Plant List Version 1.1.