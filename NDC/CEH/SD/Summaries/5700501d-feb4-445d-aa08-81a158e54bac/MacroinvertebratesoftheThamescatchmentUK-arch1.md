# Macroinvertebrates of the Thames catchment

- This dataset provides species-level descriptions of macroinvertebrate communities from wadeable rivers in the Thames catchment, UK, collected across three seasons (Autumn 2009, Spring 2010, Autumn 2010) with accompanying habitat data.

## Study design and data collected

- 18 sampling sites across the Thames catchment.
- Sampling occurred in Autumn 2009, Spring 2010, and Autumn 2010; not all sites were sampled in every occasion.
- Samples defined by a unique combination of site code and sample date; a site-code key is provided in the supporting information.

## Methods

- Field sampling: 1 mm mesh kick net following the RIvPACS protocol; site variables recorded include depth, wetted width, substrate cover, and macrophyte cover.
- Sample handling: samples washed into plastic bags, preserved in 4% formaldehyde in the field.
- Laboratory processing: in the lab, samples were washed through a 500 μm sieve; macroinvertebrates identified to the lowest taxonomic level possible (usually species).
- Taxonomic reference: valid taxon names and unique taxon identification codes align with Davies, C. and Edwards, F.K. (2011) Code list for recording the macroinvertebrates in freshwater in the British Isles.
- Data validation: data entry validated by crosschecking with laboratory sheets.
- Spatial variables: map variables derived for sampling points using Intelligent River Network (Version 17); methodology described by Dawson et al. (2002).

## Data files and structure

- Taxon data: includes Site code, Sample date, Season (Autumn or Spring), Taxon code, Taxon name, Life stage (L, N/A; e.g., larva/nymph, pupa, adult; or not relevant), and Abundance in sample.
- Environmental variables: Site code, Sample date, Wetted width (m), Water depth (cm), % cover of rock pavement, % cover of boulders/cobbles, % cover of pebble/gravel, % cover of sand/clay, and % cover by macrophytes.
- Supporting information: Site code, Site name, Waterbody name, Easting, Northing, OS grid reference; includes a key to site codes.
- Data files are complemented by a separate supporting information file detailing site-level context and sampling details.

## Data quality, provenance, and governance

- Version history: Version 1.0 (28/06/16) created by F. Edwards; Version 1.1 (07/07/2016) with minor revisions by F. Edwards.
- Contributors: 
  - Sample collection: Gearóid Webb, Peter Scarlett, Roger Baker, François Edwards
  - Laboratory analysis: Gearóid Webb, François Edwards, Helen Vincent
  - Supporting information: Peter Scarlett, Gearóid Webb, François Edwards
  - Planning and management: François Edwards, Michael Bowes
- Data quality practices include taxonomic validation against a standard code list, cross-checks between laboratory sheets and data entries, and standardized habitat measurements.

## Use cases and considerations for analysts

- Enables analysis of macroinvertebrate community composition and its relationships with habitat variables (width, depth, substrate, macrophyte cover).
- Suitable for correlations, diversity and ecosystem assessments, or models similar to those used in RIVPACS-type workflows.
- Consider the temporal and spatial limitations: 18 sites, three sampling periods with incomplete site coverage across seasons; careful handling of site- and time-level missingness.
- Well-documented metadata and defined taxon coding facilitate data merging with external datasets and replication of analyses.