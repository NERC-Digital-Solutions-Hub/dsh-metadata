# Global plant climate envelopes

## Aim
- Produce a bioclimatic envelope for every species recorded in GBIF over the past century using occurrence records and historical climate.
- Adjust envelopes for collection effort using the Enhanced Vegetation Index (EVI) from MODIS.

## Data Sources
- GBIF occurrence records (1901–2018).
- ECMWF climate reconstructions (CERA-20C and ERA-Interim) for 1901–2018 (monthly means of daily means for most variables; precipitation and solar radiation from monthly means of daily forecast accumulations).
- Excluded Antarctica and Arctic islands (Greenland) due to data quality.

## Methodology
- Data scope:
  - Started with ~212 million GBIF records.
  - Filtered to species with accepted names in The Plant List (to remove marine/fossil data), yielding ~215,000 species and ~100 million records.
  - Removed 3,441 botanic garden locations via a 0.02-degree buffer; also tested top recording institutions with similar results; retained original data after checks.
  - GBIF records include native and alien occurrences; inclusion of introductions helps define tolerable climates.
- Climate extraction:
  - For each GBIF record (or parent for annuals), extract climate variables for the recording month and the preceding 11 months (12-month profile).
  - Average the 12 months per climate variable; for temperature, also compute min and max.
  - For each species, bin records into 1,000 bins per climate variable to create envelope profiles.
- Bias correction:
  - Correct for spatial/taxonomic biases in GBIF data using weighting by the global distribution of plant collections relative to a proxy of abundance (EVI from MODIS) to reduce observation bias.
  - Weight climate-bin profiles by the number of records and average to obtain a single value per species per climate variable.
- Outputs:
  - Generates species-level envelopes tailored to 11 climate variables plus derived temperature metrics.

## Dataset Description
- File: a single CSV containing the average climate envelope per species for each ECMWF parameter:
  - tmin, tmax, tmean, trng (temperature metrics)
  - stl1–stl4 (soil temperature levels 1–4)
  - swvl1–swvl4 (volumetric soil water layers 1–4)
  - ssr (surface net solar radiation)
  - tp (total precipitation)
- Metadata:
  - SppID (unique species identifier)
  - Taxonomic information (phylum, class, order, family, genus)
  - numrecords (number of GBIF records informing the envelope)
  - All derived from t_2m (Temperature at 2m)
- Exclusions:
  - Antarctica and Arctic islands due to data quality concerns.
- Documentation and code:
  - Full methods and code available via associated paper and a Zenodo repository (DOI: 10.5281/zenodo/6452065).

## Data Quality, Access, and Reuse
- Strengths:
  - Large, global scale dataset combining historical climate with broad species occurrences.
  - Bias correction using EVI to improve representativeness across climate space.
  - Clear per-species envelopes with explicit metadata and taxonomic context.
- Considerations for Data Leaders:
  - GBIF biases persist, especially in under-sampled regions; envelopes account for this but users should recognize residual biases.
  - Data is historical (1901–2018); assess fit when applying to current or future risk analyses.
  - Data lineage is documented (GBIF, ECMWF reanalyses, EVI proxy); code and methods are publicly available to support reproducibility.
  - Dataset is a single CSV with per-species summaries, enabling integration into broader data products and systems requiring discoverable, well-documented data assets.