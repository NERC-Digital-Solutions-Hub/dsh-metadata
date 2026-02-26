# Global plant climate envelopes

## Aim
- Produce a bioclimatic envelope for each GBIF-recorded plant species for the past century (1901–2018) using occurrence records and historical climate, adjusted for collection effort with Enhanced Vegetation Index (EVI).

## Data sources
- Occurrence records: Global Biodiversity Information Facility (GBIF) from 1901–2018.
- Climate reconstructions: ECMWF reanalysis datasets CERA-20C and ERA-Interim; monthly means of daily values for 11 variables; ERA-Interim used to complete 1979–2018 with higher spatial resolution.
- Vegetation proxy: Global mean Enhanced Vegetation Index (EVI) from MODIS (2001–2015) to correct sampling bias.
- Exclusions: Antarctica and Arctic islands (e.g., Greenland) due to data quality; no native/alien distinction in GBIF data, but survival in new climates is valued.

## Methodology and processing
- Data volume and filtering:
  - GBIF history filtered from ~212 million to ~215,000 species and just over 100 million records after removing marine species, fossils, and georeferencing errors linked to botanic gardens and country centroids.
  - Included records from top institutions with similar results; retained original data after checks.
  - All records treated as potential year-round presence for at least one year prior to collection.
- Climate profiling:
  - For each GBIF record, extracted climate for the recording location for the month of collection and the preceding 11 months (12-month profile).
  - Variables averaged across 12 months; for temperature, also computed min and max.
  - Each species’ records binned into 1,000 bins per climate variable to form envelopes.
- Bias correction and weighting:
  - Corrected for spatial/taxonomic recording biases by weighting species profiles by the ratio of global collection distribution to a proxy of plant abundance (EVI), reducing observation bias.
  - Weighted averaging by the number of records to produce final per-species climate values.
- Data integrity:
  - Metadata and code are available (Zenodo DOI linking to full methods and code).

## Dataset content and structure
- Output: a single CSV per species containing average envelope values for each ECMWF parameter.
- Included fields:
  - Temperature variables: tmin (K), tmax (K), tmean (K), trng (K).
  - Soil temperature: stl1–stl4 (K).
  - Soil moisture: swvl1–swvl4 (m^3 m^-3).
  - Surface radiation and precipitation: ssr (J m^-2) and tp (mm).
  - Species identifiers: SppID.
  - Taxonomy: phylum, class, order, family, genus.
  - Data provenance: numrecords (number of GBIF records informing the envelope).
- Derived from 12-month climate profiles anchored to each record’s location and date.

## Data quality, limitations, and caveats
- Limitations:
  - GBIF data exhibit strong spatial and taxonomic biases (under-sampling in tropics; over-sampling in Western Europe, Eastern USA, Australia).
  - Data rely on proxies for plant abundance (EVI) and do not distinguish native vs. introduced status.
  - Exclusion of Antarctica and Arctic islands may omit relevant data for some taxa.
- Mitigations:
  - Bias correction through EVI weighting and record-count weighting.
  - Comprehensive metadata and code availability to enable replication and assessment.
- Implications for use:
  - Suitable for monitoring plant climatic tolerances and informing policy decisions on vulnerability under climate change, with transparent, reproducible methods.

## Data governance and accessibility
- Methods and code linked via associated paper and Zenodo (code DOI provided).
- Data are shared with provenance notes (SppID, taxonomy, numrecords) to support transparency and reuse in monitoring frameworks.

## Relevance for monitoring frameworks and policy decisions
- Provides a standardized, bias-adjusted foundation for assessing plant species’ climate envelopes over time.
- Enables comparability across species and regions, supporting risk assessments, conservation planning, and scenario analyses within environmental health monitoring frameworks.
- Emphasizes data provenance, methodological transparency, and governance-ready outputs (open data and code).