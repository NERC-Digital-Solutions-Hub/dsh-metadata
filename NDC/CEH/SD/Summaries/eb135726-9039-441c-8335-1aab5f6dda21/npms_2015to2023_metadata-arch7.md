# National Plant Monitoring Scheme survey data (2015-2023)

## Overview
- Plot-level plant occurrence data for 2015–2023 across the UK, Channel Islands, and Isle of Man.
- Observations include plant species occurrences, Domin frequency-abundance (cover) estimates, habitat attributes, plot type, sampling date, and precise spatial location.
- Enables reconstruction of sampling history, including gaps, for any NPMS plot sampled between 2015–2023.
- Data are intended to support monitoring of habitat quality and plant diversity changes, with potential integration into GIS-based analyses and visualisations.

## Data Files and Schema
- locations_2015to2023.csv
  - Unique location_id, location_type (plot type, e.g., square/linear), samplecount (number of samples at location).
- sampleInfoWithLatLong_2015to2023.csv
  - Sample-level records: id, survey_id (NPMS code: 87 Wildflower; 154 Inventory; 155 Indicator), date_start, location_id, entered_sref and entered_sref_system (spatial reference used), LATITUDE, LONGITUDE, monad and monadCRS (spatial unit/CRS), country, created_on, created_by_id.
- sampleAttributes_2015to2023.csv
  - Attribute values linked to samples via sample_id; includes caption and text_value (e.g., NPMS Habitat).
- occurrences_2015to2023.csv
  - Species observations linked to samples via sample_id; taxonconversionkey and preferred_taxon; domin (Domin score per observation), record_status (verification), sensitivity_precision (blur/privacy indicator).
- npmsHabitatLookup.csv
  - Mapping between NPMS broad habitat and fine-scale habitat categories.
- dominScores.csv
  - Lookup harmonising Domin values across survey types; includes midPoint for cover-category interpretation.

## Spatial and Temporal Details
- Temporal coverage: 2015–2023.
- Spatial details:
  - Location coordinates (LATITUDE/LONGITUDE) and monad (1 km square) identifiers with corresponding monadCRS (OSGB/British National Grid, OSIE/Irish Grid, or UTM30).
  - Entered spatial references may use OSGB, OSIE, or WGS84 (EPSG:27700, 29902, or 4326).
  - Data can be linked across tables via location_id and sample_id.
- Data provenance:
  - Collected online by volunteers through the NPMS website/app into a PostgreSQL/PostGIS Indicia database; extracted for distribution.
- Data structure supports GIS joins to map plot locations, habitats, and species occurrences across time.

## Data Provenance and Quality Assurance
- NPMS is designed to monitor habitat quality and plant diversity; data are vetted through:
  - Online data capture with structured fields, a species dictionary, and controlled vocabulary for habitats.
  - Automated geographic range checks; iRecord-based expert verification for certain records.
  - A project Steering Group oversees quality assurance; external peer review used where risk warrants.
  Public data publishing to enable independent review; uncertainty and limitations addressed in outputs.

## Accessing and Using the Data (GIS-oriented)
- Files are CSV-based and link via sample_id and location_id; join examples:
  - To obtain habitat info for each sample, join sampleInfoWithLatLong_2015to2023.csv with sampleAttributes_2015to2023.csv on sample_id and filter caption = 'NPMS Habitat'.
- Example workflows (conceptual):
  - Use SQL or a GIS/database tool to LEFT JOIN sampleInfoWithLatLong_2015to2023 with sampleAttributes_2015to2023 on id/sample_id to attach habitat attributes to samples.
  - Merge with locations_2015to2023.csv to attach plot type and sampling counts.
  - Join occurrences_2015to2023.csv to add species-level distributions per sample.
- Data access is primarily via the NPMS data resources and the Indicia/PostgreSQL/PostGIS backend; data dictionary and guidance are available with the dataset.

## Applications for GIS
- Map plot locations and sampling history across years to visualize survey coverage and gaps.
- Visualise habitat distributions and changes over time using NPMS habitat lookups.
- Map species occurrences by location, with Domin cover values to explore abundance patterns.
- Integrate with other spatial layers (land cover, protected areas, drivers) for habitat-change analyses and UK biodiversity indicators.

## Limitations and Considerations
- Field recording quality varies; formal QA of field recording is planned for future phases.
- Some records may be sensitive; sensitivity_precision flags records that are spatially blurred to 10 km.
- Data are provided as snapshots (2015–2023) from a volunteer-based scheme; uncertainty is addressed through model-based analyses and documented QA.
- Documentation and guidance (survey guidelines, habitat definitions, and indicators) are maintained on the NPMS site for up-to-date context.

## References and Resources
- NPMS project overview, guidance, and related publications (design, QA, and analyses) linked through NPMS and CEH/BSBI/JNCC collaboration pages.
- Example sources include design papers, ecological monitoring guidance, and technical reviews related to NPMS data products.

Note: For detailed file-level definitions, refer to the file descriptions above and the NPMS guidance and resources referenced in the dataset documentation.