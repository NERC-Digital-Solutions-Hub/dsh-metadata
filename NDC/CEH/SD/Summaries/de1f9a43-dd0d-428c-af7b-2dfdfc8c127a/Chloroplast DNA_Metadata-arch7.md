# Chlroplast microsatellite (cpSSR) primer pairs and chloroplast DNA marker primer pair (PCR-RFLP)

## Overview
- The document lists chloroplast DNA primer information, including cpSSR primer pairs and a chloroplast DNA marker primer pair for PCR-RFLP.
- cpSSR primer pairs:
  - Primer = ccmp5, locus = locus1
  - Primer = ccmp10, locus = locus2
- Chloroplast DNA marker primer pair (PCR-RFLP):
  - Primer = trnH-psbA, locus = locus3
- Some fields contain placeholders or are not determined:
  - Primer = ., locus = .
  - Other information, Primer = ., Other information, locus = .
- RBGE (Royal Botanic Garden, Edinburgh) is referenced in the data context.
- nd = not determined appears for certain primer/locus fields.

## Data fields and structure
- Key fields present:
  - Primer
  - locus
- Grouping indicates marker type:
  - cpSSR primer pairs (ccmp5, ccmp10) with corresponding loci (locus1, locus2)
  - Chloroplast DNA marker primer pair (trnH-psbA) with locus3
- Additional placeholders:
  - "Other information" fields with missing values
  - Instances of nd = not determined

## Provenance
- Mentions RBGE = Royal Botanic Garden, Edinburgh, suggesting source or reference context for the primer data.

## Data quality and gaps
- Significant missing values (both primers and loci are "." in several fields).
- Inconsistent or incomplete metadata (e.g., "Other information" fields with no content).
- No primer sequences or detailed assay information provided.
- Ambiguity in data lineage beyond the RBGE reference.

## Potential GIS usage
- As an attribute dataset linked to plant sampling locations, the primer/locus data could support:
  - Visualization of sampling sites by cpSSR or PCR-RFLP markers
  - Spatial patterns of chloroplast marker distribution across populations
  - Integration with other geospatial data (sampling coordinates, species, collection date)

## Recommendations for GIS-ready data
- Fill in missing values for primers and loci; remove or clearly flag incomplete records.
- Standardize field names (e.g., primer_id, locus_id, marker_type, assay_type, source).
- Add primer sequences and assay details if available.
- Document data provenance and lineage with a formal metadata record (source RBGE, collection year, method).
- Establish consistent data standards for loci naming (e.g., locus1, locus2, locus3) and ensure unique identifiers across records.
- Incorporate spatial metadata (sampling coordinates, associated dataset IDs) to enable map-based analyses.