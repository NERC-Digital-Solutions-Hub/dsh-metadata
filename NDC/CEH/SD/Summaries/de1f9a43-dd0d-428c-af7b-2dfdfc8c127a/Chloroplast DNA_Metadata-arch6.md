# Chlroplast microsatellite (cpSSR) primer pairs

## Overview
- The document lists chloroplast primer data for cpSSR markers and a chloroplast DNA marker (PCR-RFLP). 
- Several fields are populated (primer names and loci) but many entries are incomplete, with "Primer = .", "locus = .", or "nd = not determined".

## Data elements
- cpSSR primer pairs
  - Primer = ccmp5; locus = locus1
  - Primer = ccmp10; locus = locus2
- Chloroplast DNA marker primer pair (PCR-RFLP)
  - Primer = trnH-psbA; locus = locus3
- Other information lines contain missing values (Primer = ., locus = .) and notes like "nd = not determined".
- Source tags include RBGE = Royal Botanic Garden, Edinburgh.

## Data quality and gaps
- Missing primer sequences and locus values in several entries.
- Inconsistent or incomplete formatting (e.g., typos such as "Chlroplast" vs "Chloroplast").
- Some entries provide only partial information, hindering reuse without further verification.

## Source
- RBGE (Royal Botanic Garden, Edinburgh) appears as the data origin for several lines.

## Implications for data support
- Requires cleaning and structuring into a consistent dataset.
- Need to standardize field names (e.g., marker_type, primer, locus, notes, source).
- Identify and resolve missing data with domain experts or laboratory records.
- Prepare data products to enable easy discovery and self-service analysis.

## Recommendations / Next steps
- Create a curated primer dataset with clear columns: marker_type (cpSSR or chloroplast PCR-RFLP), primer, locus, primer_sequence (if available), notes, source.
- Validate and fill missing values where possible; flag truly undetermined fields.
- Normalize nomenclature and correct obvious typos.
- Deliver generated data products (e.g., CSV/Excel catalog, a searchable index, and a pivot-friendly view) to facilitate reuse and sharing across teams.