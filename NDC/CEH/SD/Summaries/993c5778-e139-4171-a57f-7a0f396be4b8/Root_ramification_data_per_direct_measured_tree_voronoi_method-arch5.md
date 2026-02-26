# DATA HEADER INFORMATION for: Root_ramification_data_per_direct_measured_tree_voronoi_method.csv Please also see Manual_2_Belowground_Root_Survey, page 10.

## Overview
- Dataset records the target tree root architecture. For each target tree, every coarse root (up to 1 cm diameter) branching was tagged and measured.
- Measurements follow a direct measurement approach using the Voronoi method to relate ramification to excavation areas.

## Provenance and citation
- DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Programme: ESPA
- Project: P4GES
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo (required for products derived from these data)

## Data structure and key variables
- ZOI (Zone of Interest)
  - Type: Categorical
  - Unit: ZOI2 (Andasibe) / ZOI3 (Anjahamana)
- Site
  - Type: Text
  - Unit: .
- Local name
  - Type: Text
  - Unit: .
- DBH Class (Diameter at Breast Height)
  - Type: Categorical
  - Unit: L (Large) / M (Medium) / S (Small)
- Code_target_tree
  - Type: Text String
  - Unit: .
- Number of ramification
  - Type: Numeric
  - Unit: .
- DiH (Horizontal diameter beginning of ramification)
  - Type: Numeric
  - Unit: Centimeter
- DiV (Vertical diameter beginning of ramification)
  - Type: Numeric
  - Unit: Centimeter
- DfV (Vertical diameter ending)
  - Type: Numeric
  - Unit: Centimeter
- DfH (Horizontal diameter ending)
  - Type: Numeric
  - Unit: Centimeter
- DfM (Mean diameter ending)
  - Type: Numeric
  - Unit: Centimeter
  - Calculation: DfM = (DfH + DfV) / 2
- Total_weight
  - Type: Numeric
  - Unit: grams (g)
- Total_length
  - Type: Numeric
  - Unit: Centimeter
- Orientation
  - Type: Categorical
  - Unit: N (North), S (South), E (East), W (West)
  - Special values: PV (taproot), Vor (ramification from the Voronoi triangle), NA (Not available)
  - Notes: NA indicates ramification direction not visible (root under tree or blocked by stone)

## Data quality and metadata considerations
- Each ramification is attributed to a specific target tree and site, with explicit unit and type definitions to support interoperability.
- DfM is a derived field (mean of DfH and DfV); ensure consistent calculation if reusing data.
- Orientation may be listed as Vor or PV to denote origin context; NA should be treated as missing direction data.
- Data may require “chasing up” to obtain missing observations (as with field collection practices).

## Access, sharing, and governance considerations
- Data creators/sharers should ensure metadata completeness (definitions, units, and coding schemes) for discoverability and reuse.
- Consider potential data availability constraints, embargoes, or proprietary issues as part of sharing decisions.
- Proper citation using the provided DOI and acknowledgement requirements when disseminating derived results.

## Usage notes for stewardship
- Verify consistency of categorical encodings across sites (e.g., DBH Class, Orientation codes).
- Check for completeness at the tree and ramification level; document any gaps or imputation strategies.
- Ensure updates or revisions are reflected in the dataset and accompanying metadata to maintain discoverability and usability.