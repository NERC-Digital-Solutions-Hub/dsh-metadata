# Stable isotope values for 108 water samples collected in the Gandak River Basin, in Bihar, India

## Overview
- Study presents stable isotope values (d18O and dD) for 108 water samples collected between February 2017 and February 2019 in the Gandak River Basin, Bihar, India.
- Sample types include surface water, groundwater, and rainfall; specific electrical conductivity (SEC) was measured at the source for most samples.
- Sample handling: unfiltered water bottled at source in Nalgene bottles, air excluded; SEC measured in the field; stable isotopes analyzed at British Geological Survey laboratories (UK).
- Part of the CHANSE (Coupled Human And Natural Systems Environment) project.

## Data scope and collection
- Temporal span: February 2017 to February 2019.
- Water categories: surface water (rivers/canals), groundwater (tube wells, hand pumps), and rainfall (rainwater/rain collectors).
- Data collected to support understanding of water sources, hydrological processes, and isotopic signatures across diverse sources within the Gandak Basin.
- Data structure combines:
  - General information about sample collection
  - Variable descriptions (data dictionary)
  - Site locations with detailed metadata per sample

## Variables and data dictionary
- key fields:
  - sample_date: date when the sample was taken
  - d18O_VSMOW2 (‰): oxygen-18 concentration relative to VSMOW
  - dD_VSMOW2 (‰): deuterium concentration relative to VSMOW
  - SEC_uS/cm: specific electrical conductivity in microSiemens per centimeter
- metadata handling:
  - All fields use blank to indicate missing values
  - Detailed per-sample metadata exists, including source type, water type, geographic coordinates, depth, and sampling notes

## Dataset structure and key fields
- Sample identifiers and sources (examples): numerous entries such as 13965-0001, 13965-0002, up through 13966-0019, 14466-0010, and many others, plus several labeled groups (e.g., CHPat, NIGL, S1–S13, etc.).
- Site location details per sample include:
  - lat (latitude) and long (longitude)
  - surface_elevation_mOD (meters above mean datum)
  - Source_use (domestic, irrigation, temple, nursery, hotel, etc.)
  - source_depth_m (depth of source well or bore)
  - Notes (sampling conditions, pump status, water source nuances, temperature or bubbles, proximity to canals or wetlands, etc.)
- Source types cover rivers (e.g., Gandak), canals (main/subsidiary), groundwater sources (tube wells, hand pumps, wells), and rainfall events.

## Site locations and sampling notes
- The dataset provides extensive site-level metadata for many samples, including:
  - Geographic coordinates (lat/long) and local context (river Gandak, canal networks, groundwater wells, domestic and agricultural uses)
  - Depths from shallow to deeper boreholes (ranging from 0 to over 150 meters in some entries)
  - Sampling notes detailing pumping times before sampling, equipment used, and local conditions (e.g., water tasting notes, presence of bubbles, canal water usage, or proximity to wetlands and canals)
  - Some entries indicate mixed or uncertain sources (e.g., “Probably hand pump,” “Likely rainfall,” “SubsidiaryCanal”)

## Data quality, metadata and challenges
- Metadata richness varies by entry; some fields are blank or partially filled.
- Notes reveal potential variability sources:
  - Pumping duration and prior use affecting isotopic and conductivity readings
  - Mixed water sources in some locations (groundwater and canal water influence)
  - Occasional references to air bubbles or sampling artifacts (e.g., bubbles in CFC & SF6 flow)
- The dataset’s sheer size and diversity (multiple sample IDs, source types, and sites) pose challenges for standardization and discoverability without a robust data dictionary and consistent units/coordinate references.

## Implications for data governance and reuse (Data Leaders perspective)
- Strengths:
  - Rich, provenance-traced isotopic and conductivity data across a broad hydrogeographic setting
  - Detailed site-level metadata enabling source attribution and hydrological interpretation
  - Clear indication of measurement provenance (field collection, laboratory analysis at BGS)
- Gaps and improvements to support data strategy:
  - Standardize sample identifiers and source_type/source_water_type taxonomies
  - Ensure complete metadata for all fields (e.g., fill missing lat/long, elevation, depth, and notes)
  - Publish a formal data dictionary and data quality flags to support automated validation
  - Use a consistent coordinate reference system and unit conventions (e.g., WGS84, standard SI units)
  - Improve discoverability and interoperability by providing machine-readable formats (CSV/JSON) with metadata in a accompanying schema or README
  - Track data lineage and processing steps (from field collection to isotope analysis) for reproducibility
- Potential uses:
  - Isotope-based tracing of groundwater and surface water interactions
  - Assessment of groundwater recharge and source contributions in the Gandak Basin
  - Integration with broader CHANSE datasets to analyze human-natural system interactions in the region

## Takeaways for action
- Implement a standardized data model for isotopic and hydrochemical datasets to enhance FAIR principles (Findable, Accessible, Interoperable, Reusable).
- Ensure comprehensive metadata coverage for all samples, including complete coordinates, depths, source types, and sampling conditions.
- Create clear data stewardship guidelines and a data dictionary to improve future reuse by data leaders, policy colleagues, and external partners.