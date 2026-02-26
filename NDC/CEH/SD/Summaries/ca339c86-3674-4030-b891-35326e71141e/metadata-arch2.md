# Global plant climate envelopes

## Aim
- Produce a bioclimatic envelope for each species recorded in GBIF (1901–2018) based on occurrence records and historical climate, with a correction for collection effort using Enhanced Vegetation Index (EVI).

## Data Sources
- GBIF plant occurrence records (1901–2018; ~212 million initially)
- ECMWF reanalysis climate reconstructions: CERA-20C and ERA-Interim for 1901–2018 (monthly means; precipitation and solar radiation from monthly means of daily forecasts)
- EVI proxy for plant density (2001–2015)
- Botanic Gardens Conservation International (BGCI) garden locations for georeferencing checks
- The Plant List (for accepted taxonomic names)
- Exclusion of Antarctica and Arctic islands due to data quality

## Methodology
- Data filtering and cleaning
  - Retain records for species with accepted names; remove marine/fossil records
  - Exclude records within 0.02° of botanic gardens; similarly filter country centroids
  - Consider top 100 recording institutions; ultimately retain original data after checks
  - GBIF data include both native and alien records to capture potential climate tolerances
- Climate data preparation
  - Use aggregated monthly ECMWF datasets; replace final 39 years (1979–2018) with ERA-Interim for higher spatial resolution
  - Exclude Antarctica/islands for quality
- Envelope extraction
  - For each GBIF record, assume presence at the site for at least one year prior
  - Extract climate variables for the record month and preceding 11 months (12-month profile)
  - Average across the 12 months per variable; for temperature also compute min and max
  - Bin records per species into 1,000 bins per climate variable to form envelopes
- Bias correction
  - Correct for GBIF spatial/taxonomic biases using global abundance proxy (EVI)
  - Weight bin profiles by the ratio of global collection distribution to plant abundance proxy
  - Average across climate bins, weighted by the number of records, to obtain per-species envelope values

## Dataset Description
- A single CSV file containing the average envelope value per species for each ECMWF parameter:
  - tmin, tmax, tmean, trng
  - stl1–stl4 (soil temperature levels)
  - swvl1–swvl4 (volumetric soil water layers)
  - ssr (surface net solar radiation)
  - tp (total precipitation)
- Includes a unique SppID, taxonomic information (phylum to genus), and numrecords (records informing the envelope)

## Output and Accessibility
- Provides per-species climate envelope values suitable for monitoring environmental conditions and species’ climate tolerances over time
- Associated paper and code available (Zenodo link)
- References and data sources detailed in the metadata

## Considerations for Analysts Monitoring the Environment
- Addresses sampling biases in GBIF via EVI-based weighting to improve envelope accuracy
- Envelopes reflect climates species could tolerate, including occurrences beyond native ranges
- Limitations include residual spatial bias, lack of native/non-native distinction, and assumptions about year-long site presence prior to observation