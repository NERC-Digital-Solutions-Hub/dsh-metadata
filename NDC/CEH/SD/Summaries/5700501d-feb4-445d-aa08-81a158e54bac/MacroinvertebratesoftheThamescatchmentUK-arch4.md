# Macroinvertebrates of the Thames catchment

## Overview
- Species-level descriptions of macroinvertebrate communities from 18 wadeable rivers in the Thames catchment, UK.
- Data collected over three seasons: Autumn 2009, Spring 2010, and Autumn 2010; not all sites sampled each time.
- Includes supporting habitat data and site-level identifiers.

## Data files and content
- Macroinvertebrates of the Thames catchment - taxon data.csv
- Macroinvertebrates of the Thames catchment - environmental variables.csv
- Supporting information.csv
- Key mappings: site codes, taxon codes/names, and sample identifiers are defined across the files.

## Collection, processing, and methods
- Sampling framework: 18 sites; RIvPACS field protocol; 1 mm mesh kick net.
- Field measurements: site depth, width, substrate cover, and macrophyte cover recorded.
- Sample handling: samples preserved in 4% formaldehyde; lab processing involved washing and identifying macroinvertebrates to the lowest taxonomic level possible (usually species).
- Taxonomic standard: valid taxonomic names and unique taxon codes per Davies & Edwards (2011).
- Data validation: entries cross-checked against laboratory sheets.
- Geospatial and environmental context: map variables derived for site locations using Intelligent River Network (IRN, v17); key references provided.

## Data structure and variables
- Sample identifiers: unique combination of site code and sample date (season indicated as Autumn or Spring).
- Taxon data columns: site code, sample date/season, taxon code, taxon name, life stage (L, P, A, U), abundance.
- Supporting information columns: site code, site name, waterbody name, Easting, Northing, OS grid reference.
- Environmental variables columns: site code, sample date, wetted width (m), water depth (cm), % cover of rock pavement, % cover of boulders/cobbles/pebble/gravel/sand/clay (sum to 100%), % cover by macrophytes.

## Provenance, standards, and quality
- Version history: 1.0 created 28/06/2016; 1.1 minor revisions dated 07/07/2016 (both by F. Edwards).
- Taxon naming and coding aligned with Davies & Edwards (2011) code list; map variables derived per Dawson et al. (2002).
- Quality controls include data entry validation through crosschecks with laboratory records.

## User-oriented considerations for data leaders
- Comprehensive documentation supports data discoverability and reuse (taxon codes, site mappings, and sampling context).
- Standardized taxonomic references and metadata enable integration with broader freshwater biodiversity datasets.
- Clear responsibilities and contributor roles (sampling, laboratory analysis, supporting information, planning/management) facilitate governance and collaboration.
- Dataset design supports evaluating data coverage, granularity, and potential gaps for informing data strategy and cross-network data coordination.