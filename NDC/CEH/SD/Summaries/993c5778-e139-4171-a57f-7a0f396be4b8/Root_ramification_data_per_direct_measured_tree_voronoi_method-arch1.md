# DATA HEADER INFORMATION for: Root_ramification_data_per_direct_measured_tree_voronoi_method.csv

- The dataset records the target tree root architecture, with each coarse root (diameter up to 1 cm) branching tagged and measured for every target tree.
- The methodology cited includes a Voronoi-based approach for classifying ramification.

## Key fields and definitions

- ZOI (Zone of Interest)
  - Type: Categorical
  - Units: ZOI2: Andasibe / ZOI3: Anjahamana
- Site
  - Type: Text string
  - Unit: .
- Local name
  - Type: Text string
  - Unit: .
- DBH Class (Diameter at Breast Height class)
  - Type: Categorical
  - Units: L (Large) / M (Medium) / S (Small)
- Code_target_tree
  - Type: Text string
  - Unit: .
- Number of ramification
  - Type: Numeric
  - Unit: .
  - Description: Number of ramification branches measured from the north
- DiH (Horizontal diameter beginning of each ramification)
  - Type: Numeric
  - Unit: Centimeters
- DiV (Vertical diameter beginning of each ramification)
  - Type: Numeric
  - Unit: Centimeters
- DfV (Vertical diameter ending of each ramification)
  - Type: Numeric
  - Unit: Centimeters
- DfH (Horizontal diameter ending of each ramification)
  - Type: Numeric
  - Unit: Centimeters
- DfM (Mean diameter ending)
  - Type: Numeric
  - Unit: Centimeters
  - Calculation: DfM = (DfH + DfV) / 2
- Total_weight
  - Type: Numeric
  - Unit: grams
  - Description: Weight of each ramification
- Total_length
  - Type: Numeric
  - Unit: Centimeters
  - Description: Length of each ramification
- Orientation
  - Type: Categorical
  - Units: N (North), S (South), E (East), W (West), Vor (Ramification from the Voronoi triangle), PV (taproot), NA (not available)
  - Description: Indicates where each ramification is directed; Vor indicates the ramification comes from the Voronoi triangle where roots were excavated; PV indicates a vertical taproot; NA if not observed due to obstruction

## Data provenance and references

- DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Programme: ESPA
- Project: P4GES
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data

## Method context

- ZOI, site codes, and local names reflect field collection context.
- The dataset uses direct measurement of ramification characteristics and classifies ramification orientation with explicit references to Voronoi-derived origins or taproot designation.

## Usage considerations for analysts

- Suitable for correlating root-ramification metrics with tree size class (DBH), site/zone, and ramification orientation.
- Enables cross-site comparisons (Andasibe vs. Anjahamana) and analysis of how ramification length, diameter, and weight relate to DBH class.
- Be mindful of potential gaps or NA entries in orientation and other fields; scale and local context may affect generalisability.
- The header points to Manual_2_Belowground_Root_Survey (page 10) for methodological details, which may inform data cleaning, variable definitions, and replication of methods.
- Data may require harmonisation across datasets due to multiple sources and formats; maintain provenance via DOI and project references.