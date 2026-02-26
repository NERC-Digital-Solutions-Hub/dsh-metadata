# Macroinvertebrates of two abstracted streams - taxon data.csv

## Overview
- Dataset containing species-level descriptions of macroinvertebrate communities from two Lowther catchment streams in the UK, upstream and downstream of abstraction points.
- Includes supporting habitat and geographical data to contextualise biological observations.

## Data provenance and contributors
- Sample collection: François Edwards, Peter Scarlett, Gearóid Webb
- Laboratory analysis: Gearóid Webb, François Edwards, Helen Vincent
- Supporting information: Peter Scarlett, Gearóid Webb, François Edwards
- Sampling dates: 23–24 September 2010
- Data versioning: Version control shows a 1.0 creation (21/06/2016) and a 2.0 update to support further information (22/06/2016)

## Data content and structure
- Taxon dataset (taxon data.csv)
  - Columns (A–E):
    - A: Sample identifier (based on waterbody and position relative to abstraction: upstream US or downstream DS, plus replicate 1–5)
    - B: Taxon name (as per Davies and Edwards 2011)
    - C: Taxon code (as per Davies and Edwards 2011)
    - D: Life stage (L = larva/nymph, P = pupa, A = adult, U = not relevant)
    - E: Abundance in sample (per 0.0625 m²)
- Supporting information (Table 1)
  - Columns include environmental and site attributes such as:
    - Stream name, position relative to abstraction, grid references, northings/eastings, altitude, slope, distance from source
    - Altitude at source, geology codes (solid and drift), NC C solid/drift classifications
    - Wetted width, water depth
    - Habitat Quality Assessment (HQA) and Habitat Modification Score (HMS) and their class
- Taxon naming and coding
  - Valid taxonomic names and unique taxon identification codes aligned with Davies and Edwards (2011)
  - Cross-referenced codes facilitate interoperability with external taxon lists

## Methods and quality assurance
- Study context: Two streams (Howes Beck and Heltondale Beck) are tributaries of the Lowther, within the Eden catchment (Cumbria)
- Sampling design: Five riffles sampled per 100 m reach around abstraction points; sampling reaches ~100 m in length
- Field methods:
  - Reach measurement: water depth and wetted width recorded as triplets and averaged
  - Habitat assessment: River Habitat Survey (RHS) methodology
  - Biological sampling: Surber sampler (mesh 250 µm, area 0.0625 m²); depth ~5 cm; five riffles per reach
  - Sample handling: field preservation with 4% formaldehyde
- Laboratory processing:
  - Samples washed through 250 µm sieve; macroinvertebrates identified to lowest possible taxonomic level
  - Taxa validity and codes drawn from Davies & Edwards (2011)
  - Data entry validated by cross-checking printouts with laboratory sheets

## Metadata, standards, and identifiers
- Data standards:
  - Taxon names and codes reference Davies and Edwards (2011)
  - Geographic information includes OS grid references, northings, and eastings
  - Habitat and environmental measures follow RHS and Intelligent River Network (Version 17) frameworks
- Documentation and supporting materials:
  - Supporting environmental information is organized in a structured table with consistent column definitions
  - Method references for environmental variables and habitat assessments are explicitly cited

## Access, sharing, and governance considerations
- Data governance:
  - Clear provenance, authorial attribution, and versioning evident (1.0 and 2.0 notes)
  - Metadata-rich dataset enabling discoverability and reuse by dataset curators, researchers, and data users
- Potential access considerations:
  - Original data collected in 2010; users should consider context and temporal relevance
  - Data are described with detailed methodological metadata to support interoperability, replication, and integration with other datasets

## Versioning and updates
- Version 1.0 created on 21/06/2016
- Version 2.0 updated on 22/06/2016 to support additional information
- Documentation indicates ongoing attention to descriptive metadata and data usability

## Practical implications for Data Stewards
- Ensure continued accessibility of both taxon data and supporting environmental information, preserving links between sample codes and site attributes
- Maintain alignment with Davies & Edwards (2011) taxon coding to support interoperability with other datasets
- Preserve spatial context via OS grid references and coordinate data; consider updating with modern GIS-compatible formats if needed
- Retain validation records (cross-check against lab sheets) to support data quality audits
- Document any data usage restrictions or licensing terms alongside the metadata to clarify sharing permissions
- Consider archiving incentives for re-use, such as providing a data dictionary, sample code mapping, and clear reproduction workflows of the field and lab methods