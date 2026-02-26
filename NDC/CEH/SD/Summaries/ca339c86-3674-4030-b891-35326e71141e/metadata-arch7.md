# Global plant climate envelopes

## Overview
- A data product delivering bioclimatic envelopes for each species recorded in GBIF (1901–2018), derived from occurrence data and historical ECMWF climate reconstructions.
- Envelopes are adjusted for sampling bias using the Enhanced Vegetation Index (EVI) to improve representativeness for GIS mapping and analysis.
- Output is a single CSV with per-species average climate envelope values ready for map-based visualization and spatial analyses.

## Data sources
- GBIF occurrence records (1901–2018) for plant species (filtered to accepted names; excludes marine/fossil records).
- Climate reconstructions: ECMWF CERA-20C and ERA-Interim, providing monthly means for 11 climate variables; final 39 years (1979–2018) replaced with ERA-Interim data for greater spatial resolution to complete 1901–2018 timeline.
- Enhanced Vegetation Index (EVI) for 2001–2015 as a proxy for plant density and to correct observation bias.
- Exclusions: Antarctica and Arctic islands (including Greenland) due to data quality; botanic garden locations and country centroids were treated to reduce misgeoreferenced records.

## Aim
- Produce a bioclimatic envelope for every GBIF-recorded species over the past century, reflecting climates the species could tolerate based on occurrence timing and location, corrected for sampling effort.

## Methodology
- Data curation:
  - Start with ~212 million GBIF records; filtered to ~215,000 species and just over 100 million records after removing non-target records and garden-related biases.
  - Botanic gardens and country centroids excluded via 0.02° buffer checks; tested additional filters (top 100 institutions) with similar results.
  - GBIF data treated as informative about climate tolerance (native vs. introduced status not distinguished).
- Climate extraction:
  - For each GBIF record (or parent for annuals), extract climate variables for the record’s month and the preceding 11 months (12-month window) to form a climate profile.
  - Average the 12 months per climate variable; for temperature, also compute minimum and maximum values.
- Enveloping and bias correction:
  - Bin records per species into 1,000 bins for each climate variable.
  - Correct for biases in collection effort by weighting bins by the ratio of global species distribution to a proxy of abundance (EVI).
  - Final per-species envelope value per climate variable is the global-weighted average across records, weighted by the number of records.
- Output variables:
  - 14 ECMWF parameters: tmin, tmax, tmean, trng, stl1–stl4, swvl1–swvl4, ssr, tp.
  - Included metadata: SppID, taxonomic information (phylum, class, order, family, genus), and numrecords (records informing the envelope).
  - Note: All derived from t_2m (temperature at 2m) for temperature-related variables.
- Exclusions and caveats:
  - Antarctica and Arctic islands excluded due to data quality.
  - GBIF biases addressed via EVI-based weighting; results rely on the representativeness of available records and climate reconstructions.

## Data format and access
- Dataset: a single CSV file containing the average climate envelope values per species for each ECMWF parameter, along with species identifiers and taxonomy.
- Documentation and code:
  - Full methodological details and code available via the associated Zenodo link.
  - References include GBIF, BGCI, The Plant List, ERA-Interim, CERA-20C, and EVI methodology sources.

## Practical GIS implications
- Enables map-based visualization of species’ climate tolerances across regions and time periods.
- Can be joined to species distribution maps or biodiversity layers using SppID or taxonomic fields.
- Useful for policy, conservation planning, and public-facing climate-vulnerability analyses by illustrating species’ potential responses to climate variability.