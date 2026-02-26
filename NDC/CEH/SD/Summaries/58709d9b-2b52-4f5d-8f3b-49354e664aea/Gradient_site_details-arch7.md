# ecosystem function and stocks data

- A large, messy point-based dataset describing ecosystem function and species richness observations across sites in Wiltshire, particularly Salisbury Plain, collected around June 2014.
- Contains multiple references to Schedule 3 Species Rich and Schedule 1 Land, with sample metadata (SiteCode, LandUse, Date sampled, Number of replicates) and geographic coordinates.
- Data appears to be a raw extract with inconsistent field alignment, duplicated fragments, and corrupted text in many records.

## What the data describes

- Observations of ecosystem function and species richness at numerous sites (e.g., STOKEHILL, ENFORD, CORNBURY FARM, IMBER, MANOR FARM, UPAVON) on Salisbury Plain.
- Two principal thematic strands:
  - Schedule 3 Species Rich data points (points tagged with Schedule 3, SiteCode, LandUse, Date sampled, Number of replicates, and coordinates).
  - Schedule 1 Land observations (land use descriptions and site metadata).
- Repeated references to grazing land and various land-use descriptions, often accompanied by approximate coordinates (Longitude/Latitude, GRIDREF, postcodes).

## Spatial coverage

- Region: Salisbury Plain, Wiltshire, UK.
- Numerous sites with latitude/longitude and grid references (e.g., around 51.x degrees N, -2.x degrees W).
- Coordinates accompany SiteCode and LandUse descriptors, suggesting a dense spatial dataset suitable for point-based GIS mapping.

## Temporal coverage

- Sampling dates clustered in June 2014 (e.g., 21/06/2014, 23/06/2014, 24/06/2014, 25/06/2014, 27/06/2014).
- Some dates appear within the metadata of Schedule 3 Species Rich observations; a few entries show placeholder or misparsed values for dates.

## Data structure and quality

- Fields repeatedly seen: SiteCode, LandUse, Date sampled, Number of replicates taken, Longitude, Latitude, GRIDREF, in, Post code, Schedule 1, Schedule 3, Species Rich, Location Description.
- Numerous data quality issues:
  - Misaligned or corrupted values (text interspersed with numbers, inconsistent field ordering).
  - Duplicates and truncated fragments (repeated phrases like “Date sampled =” or “Number of replicates taken =” with incomplete values).
  - Some fields appear to contain concatenated or misparsed text rather than clean attribute values.
- Overall, the dataset requires substantial cleaning and validation before GIS use.

## Implications for GIS use

- Potential to create map-based visuals of species richness and grazing land across Salisbury Plain.
- Requires data cleaning to extract clean, consistent fields suitable for GIS:
  - Key attributes: SiteCode, LandUse, Date sampled, Number of replicates, Longitude, Latitude (or GRIDREF converted to coordinates), Schedule type (1 or 3), and species richness values.
  - Separate layers for Schedule 3 Species Rich points and Schedule 1 land-use observations.
- Coordinate system and projection need verification (likely WGS84 lat/long or UTM; conversion may be needed).
- Join or reconcile partial fields where SiteCode links to multiple observations or where date/replicate data are incomplete.

## Recommended data preparation steps

- Clean and standardize schema:
  - Extract and normalize core fields: SiteCode, LandUse, Date sampled, Number of replicates taken, Longitude, Latitude, Grid Reference, Schedule (1 vs 3), and species richness value where present.
  - Remove clearly corrupted rows or attempt to split misparsed fields into valid components.
- Validate coordinates:
  - Ensure all records have valid latitude/longitude; convert GRIDREFs if needed.
  Ensure dates follow a consistent format.
- Create GIS-ready layers:
  - Point layer for Schedule 3 Species Rich observations (with richness value, replicates, and site attributes).
  - Layer for Schedule 1 Land-use observations (site-level attributes, dates, and location).
- Metadata and provenance:
  - Document data sources, cleaning steps, and any assumptions about field mappings.
  - Note any records that were omitted or heavily edited due to quality concerns.

## Caveats and considerations

- Data quality issues may limit the reliability of some observations; treat some entries as provisional until cleaned.
- Some fields contain overlapping or ambiguous information (e.g., in-field descriptors vs coordinates); careful parsing is required.
- Data appears to originate from multiple schedules and possibly multiple datasets; ensure correct linkage between Schedule 3 Species Rich entries and corresponding site metadata.

## Intended GIS outputs and next steps

- Spatial distribution maps of species richness (Schedule 3) across Salisbury Plain with site-level metadata (SiteCode, LandUse, Date sampled, replicates).
- Thematic maps of grazing land and land-use types (Schedule 1) across the same region.
- Dashboards or overlays showing sampling intensity (replicates) alongside richness values.
- Seek a cleaned data extract from the data custodian to confirm field definitions and to validate values before formal GIS publication.