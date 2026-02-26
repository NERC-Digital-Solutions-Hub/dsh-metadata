# Stable isotope values for 108 water samples collected in the Gandak River Basin, in Bihar, India are presented, with accompanying values for SEC (specific electrical conductivity) for most of these samples.

## Overview
- Dataset comprises 108 water samples collected between February 2017 and February 2019.
- Sample types include surface water, groundwater, and rainfall.
- Measurements include stable isotope values (d18O and dD) and specific electrical conductivity (SEC).
- Isotope analyses conducted at British Geological Survey laboratories (UK); SEC measured at the sampling site.
- Data collected as part of the CHANSE (Coupled Human And Natural Systems Environment) project.

## Data contents and variable descriptions
- Sample identifiers: BGS LIMS or Lab Code; sample_id for each record (e.g., 13965-0001, 14466-0001, NIGL_001, CHPat01, etc.).
- sample_date: date when the sample was taken.
- d18O VSMOW2 (‰): Oxygen-18 concentration relative to VSMOW.
- dD VSMOW2 (‰): Deuterium concentration relative to VSMOW.
- SEC uS/cm: Specific electrical conductivity at the time of sampling.
- All fields use blank to denote missing values.
- Metadata notes may accompany records (sampling conditions, equipment, time of pump operation, etc.).

## Site locations and sampling context
- Records include detailed location metadata (latitude, longitude, surface_elevation_mOD) and sampling context (source_type, source_water_type, source_depth_m, Source_use).
- Source types cover a range of water sources: River Gandak, canals, tributaries, groundwater from tube wells or hand pumps, rainfall/rainwater, domestic or irrigation uses.
- Water types include Groundwater, River Gandak, Canal, Rainwater, and Rainfall.
- Depths vary widely (from 0 to over 150 meters in some groundwater wells).
- Notes provide contextual sampling information (e.g., proximity to canals, pumping times before sampling, issues like air bubbles or sediment, or domestic/irrigation usage).

## Data provenance and collection methods
- Field collection: samples unfiltered and bottled at the source in Nalgene bottles, filled to brim to minimize air.
- SEC measured at the source with a field SEC meter.
- Isotope analyses performed at British Geological Survey laboratories in the UK.
- Data tied to CHANSE project activities; sample IDs and associated metadata reflect laboratory and field workflows (BGS LIMS/Lab Code, sample_date, etc.).

## Data quality, completeness, and governance considerations
- Missing values are allowed and represented as blanks.
- Some records contain uncertain or qualitative notes (e.g., “Probably hand pump,” “Difficult to read,” or timing notes about pumping duration), indicating variable metadata completeness.
- High level of spatially diverse sources (river, groundwater wells, canals, rainfall) requires careful harmonization for cross-source comparisons.
- Data are spread across multiple subdatasets or identifiers (e.g., 13965-xxxx, 13966-xxxx, 14466-xxxx, NIGL_xxx, CHPatxx, Sx, etc.), necessitating consistent data governance to ensure unified discovery, interoperability, and versioning.
- Standard units and references are specified (d18O and dD in per mil relative to VSMOW; SEC in µS/cm), but cross-dataset harmonization is recommended for ongoing use.

## Practical implications for Data Stewards
- Ensure a formal data dictionary and data dictionary for all fields (sample_id, sample_date, isotopes, SEC, source_type, source_water_type, depth, notes).
- Maintain provenance trails linking field collection, field measurements, and laboratory analyses.
- Implement data quality checks to flag implausible isotope values, inconsistent dates, or anomalous SEC readings.
- Normalize source_type and source_water_type categories across all subdatasets to enable cross-dataset querying and analyses.
- Provide guidance on handling missing data and how to treat records with uncertain metadata (e.g., “Probably hand pump”).
- Document all data processing steps (e.g., calibration, data entry, unit conversions) and release notes for updates or corrections.
- Plan for updates and version control to accommodate new samples or reanalysis results from ongoing CHANSE-related work.
- Ensure dataset is catalogued in appropriate data portals with clear access rights, licensing, and metadata for discoverability.

## Recommendations for users and future work
- Create a consolidated, harmonized master dataset by aligning identifiers, units, and categorical fields across all source datasets.
- Develop a metadata-rich data portal entry including sampling context, measurement methods, QA/QC procedures, and data lineage.
- Where possible, fill gaps in metadata (e.g., exact source_depth_m for all records, measurement dates for all samples) to enhance reusability.
- Consider publishing derived analyses (e.g., regional groundwater–surface water isotope relationships) alongside the raw data, with clear citation and provenance.