# Macroinvertebrates of the Thames catchment

## Overview
- Dataset describing species-level macroinvertebrate communities from wadeable rivers in the Thames catchment, UK.
- Collected across three seasons: Autumn 2009, Spring 2010, Autumn 2010.
- Includes supporting habitat data and site-level context.

## Data content and structure
- Files:
  - Macroinvertebrates of the Thames catchment - taxon data.csv (species-level abundances)
  - Macroinvertebrates of the Thames catchment - environmental variables.csv (site ecological variables)
  - Macroinvertebrates of the Thames catchment - supporting information.csv (site metadata)
- Taxon data (columns):
  - Site code, Sample date, Season (A = autumn, S = spring), Taxon code, Taxon name, Life stage (L = larva/nymph, P = pupa, A = adult, U = not relevant), Abundance
- Environmental variables (columns):
  - Site code, Sample date, Wetted width (m), Water depth (cm), % cover of rock pavement, % cover of boulders/cobbles, % cover of pebble/gravel, % cover of sand/clay, % cover by macrophytes
- Supporting information (columns):
  - Site code, Site name, Waterbody name, Easting, Northing, OS grid reference
- Sample identifiers are defined by a unique combination of site code and sample date; a site code key is provided in the supporting information.

## Geographic and GIS-related aspects
- 18 sampling sites in the Thames catchment with point locations described by Easting/Northing and OS grid references.
- Map variables were derived for the sites using the Intelligent River Network (IRN, Version 17) to extract environmental variables for classification of rivers in Britain (Dawson et al. 2002).

## Methodology and data processing
- Field sampling:
  - Rivers sampled using a 1 mm mesh kick net following the RIvPACS protocol.
  - Recorded site variables: depth, width, substrate cover, macrophyte cover.
  - Samples preserved in 4% formaldehyde in the field; later processed in the lab.
- Laboratory processing:
  - Samples washed through a 500 μm sieve; macroinvertebrates identified to the lowest taxonomic level available (usually species).
  - Taxonomic names and unique taxon codes provided per Davies, C. and Edwards, F.K. (2011) code list.
  - Data validated by crosschecking printouts with laboratory sheets.
- Data integration:
  - Taxon and site data linked via site codes and sample dates; taxon codes align with Davies & Edwards (2011).
  - Map variables derived using IRN methodology (Dawson et al. 2002) for spatial analysis.

## Data quality, provenance, and versioning
- Version history:
  - Version 1.0 (28/06/16): created by F. Edwards.
  - Version 1.1 (07/07/2016): minor revisions by F. Edwards.
- Contributors:
  - Sample collection: Gearóid Webb, Peter Scarlett, Roger Baker, François Edwards.
  - Laboratory analysis: Gearóid Webb, François Edwards, Helen Vincent.
  - Supporting information: Peter Scarlett, Gearóid Webb, François Edwards.
  - Planning and management: François Edwards, Michael Bowes.

## How to use in GIS and spatial analyses
- Combine site coordinates with environmental variables to map spatial patterns in macroinvertebrate communities and habitat characteristics.
- Use taxon abundances to create species distribution or richness maps across the Thames catchment and across seasons.
- Link to supporting information for enhanced site context (waterbody names, precise grid references) and to interpret environmental gradients via IRN-derived variables.

## Considerations and limitations
- Not all sites were sampled in every season; temporal coverage is uneven.
- Taxonomic resolution depends on field and lab processing; life stage data and codes are standardized per Davies & Edwards (2011).
- Data reflect the Thames catchment; applicability to other regions requires caution.