# Global plant climate envelopes

## Overview
- A dataset and methodology to create bioclimatic envelopes for plant species based on GBIF occurrence records (1901–2018) and historical ECMWF climate reconstructions.
- Aims to produce, for each species, the climate envelope they could tolerate across the past century, adjusted for sampling effort using MODIS Enhanced Vegetation Index (EVI).
- Data prepared for integration with phylogenetic models; metadata and code are provided in associated publications and repositories.

## Data sources and aims
- Data sources:
  - GBIF occurrence records (1901–2018) for plant species.
  - ECMWF climate reconstructions (CERA-20C and ERA-Interim) for 1901–2018.
  - EVI proxy for plant density (MODIS, processed by Gibson & Weiss; Huete et al. 1999).
  - Botanic Gardens Conservation International (BGCI) locations used to filter out garden observations.
  - The Plant List (for accepted names) to filter records and remove fossils/marine species.
- Aims:
  - Build a bioclimatic envelope for each GBIF-recorded species for the past century, incorporating climate at the time of observation and the preceding 11 months.
  - Correct for collection effort biases to better reflect species’ climate tolerances.

## Methodology and data processing
- Occurrence data handling:
  - Filter GBIF data to accepted names in The Plant List; remove marine/fossil records.
  - Exclude records within 0.02 degree of botanic gardens to minimize garden-originated observations.
  - Antarctica and Arctic islands excluded due to data quality concerns.
  - Consider both native and introduced occurrences to capture tolerances to new climates.
- Climate data handling:
  - Use monthly means of daily means from ECMWF reconstructions for 11 climatic variables; for precipitation and solar radiation, use monthly means of daily forecast accumulations.
  - Fill timeline 1901–2018 by combining CERA-20C/ERA-Interim data; replace final 39 years (1979–2018) with ERA-Interim for higher spatial resolution.
- Bias correction and weighting:
  - Correct GBIF biases by weighting species’ climate profiles with the ratio of global distribution of plant collections to a proxy of plant abundance (EVI).
  - Weighting reduces overrepresentation from intensively surveyed regions (e.g., Western Europe, Eastern America, Australia) and addresses tropical data gaps.
- Envelope extraction:
  - For each GBIF record, extract climate variables for the month of observation and the previous 11 months, then average across the 12 months (except for temperature where min/max are also computed).
  - For each species, bin records into 1,000 bins per climate variable to form envelope profiles.
  - After binning, derive per-species envelopes by averaging across climate bins, weighted by the number of records.
- Documentation and reproducibility:
  - Full methodological details and code are available in the associated paper and Zenodo repository.
  - Derived data are prepared for downstream analyses, including phylogenetic modeling.

## Dataset description and contents
- File: a single CSV containing the average climate envelope per species for each ECMWF parameter.
- Parameters included:
  - tmin (minimum temperature, K) derived from t_2m
  - tmax (maximum temperature, K) derived from t_2m
  - tmean (mean temperature, K) derived from t_2m
  - trng (temperature range, K) derived from t_2m
  - stl1–stl4 (soil temperature levels 1–4, K)
  - swvl1–swvl4 (volumetric soil water content layers 1–4, m^3 m^-3)
  - ssr (surface net solar radiation, J m^-2)
  - tp (total precipitation, mm)
- Additional metadata:
  - Species identifier (SppID)
  - Taxonomic information (phylum, class, order, family, genus)
  - numrecords (number of GBIF records informing the envelope)
- Notes:
  - All temperature values are in Kelvin; soil moisture in m^3 m^-3; solar radiation in J m^-2; precipitation in mm.
  - Dataset provides per-species envelope values rather than raw occurrence counts.
  - Excludes Antarctica and Arctic islands; includes both native and introduced occurrences for climate tolerance.

## Data quality, biases, and governance considerations
- GBIF data biases are acknowledged (geographic and taxonomic sampling biases).
- Bias corrections include EVI-based weighting and global abundance proxies; still, the data reflect observational biases and may influence envelope estimates.
- Metadata includes authorship and data sources; provenance links to Harris et al. (2022) and the code/repository for reproducibility.
- Data stewardship implications:
  - Ensure ongoing governance of the dataset when reused for comparative analyses or updates (e.g., updating GBIF records, climate inputs, or EVI proxies).
  - Clearly communicate biases and limitations in derived climate envelopes to end users.

## Reuse, provenance, and references
- Primary source: Harris et al. (2022) Strong phylogenetic signals in global plant bioclimatic envelopes, Global Ecology and Biogeography.
- Data preparation and metadata prepared by Claire Harris and Richard Reeve (21/06/2022).
- Code and full methodological details available via the associated Zenodo repository and the cited paper.
- Key references include BGCI (2019), GBIF (2019), MODEIS/EVI methodology (Gibson & Weiss, Huete et al.), and ECMWF data sources (Dee et al., Laloyaux et al.).

## Practical notes for data stewards
- Ensure clear documentation of data sources, processing steps, and bias corrections when integrating into data catalogs.
- Maintain links to the original publication and code for reproducibility.
- Consider updating the envelope dataset as GBIF records, climate reconstructions, or EVI data are refreshed, and communicate any reprocessing that changes envelopes.