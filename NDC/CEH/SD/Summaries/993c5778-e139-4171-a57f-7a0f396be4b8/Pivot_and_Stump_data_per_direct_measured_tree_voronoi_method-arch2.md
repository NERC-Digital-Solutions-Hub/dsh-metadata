# DATA HEADER INFORMATION for Pivot_and_Stump_data_per_direct_measured_tree_voronoi_method.csv

## Overview
- Metadata and structure for a dataset documenting stump, pivot (taproot), and surface-root measurements on felled trees.
- Pivot refers to the vertical taproot; stump is the remaining above-ground portion above the root system between cut point and individualized roots.
- After felling, the stump is cut and the taproot excavated and weighed.
- Part of ESPA Programme and P4GES project; DOI provided; acknowledgement required for derived products.

## Data scope and purpose
- Purpose: record direct measurements of below-ground and above-ground tree components to support environmental monitoring and biomass/carbon assessments.
- Focus: weight data (fresh and dry) for pivot, stump, and coarse roots above soil (CR0) per tree.
- Spatial context: data labeled by Zone of Interest (ZOI) and location details to enable regional analyses.

## Variables and data schema
- Zone of Interest (ZOI)
  - ZOI, Information = Zone of Interest
  - ZOI, Variable Type = Categorical
  - ZOI, Unit = /
  - Examples: ZOI2: Andasibe, ZOI3: Anjahamana
- Location
  - Location, Information = Name of sampling point location
  - Location, Variable Type = Text String
  - Location, Unit = .
- Site identity
  - Site_Id, Information = Code given to the site where the target tree was collected
  - Site_Id, Variable Type = Text String
  - Site_Id, Unit = .
- Target tree identifiers
  - Local_name, Information = Vernacular/local name of the target tree
  - Local_name, Variable Type = Text String
  - Local_name, Unit = .
  - Code_target_tree, Information = Code given to each target tree: Code_site associated with species name and the diameter class
  - Code_target_tree, Variable Type = Text String
  - Code_target_tree, Unit = .
- Measurements (weights in grams)
  - Weight_Freshtotal_Pivot, Weight_Freshtotal_Pivot, Variable Type = Numeric
  - Weight_Freshtotal_Pivot, Unit = grammes (g)
  - Weight_Freshsample_Pivot, Weight_Freshsample_Pivot, Variable Type = Numeric
  - Weight_Freshsample_Pivot, Unit = g
  - Weight_Drysample_Pivot, Weight_Drysample_Pivot, Variable Type = Numeric
  - Weight_Drysample_Pivot, Unit = g
  - Weight_Freshtotal_Stump, Weight_Freshtotal_Stump, Variable Type = Numeric
  - Weight_Freshtotal_Stump, Unit = g
  - Weight_Freshsample_Stump, Weight_Freshsample_Stump, Variable Type = Numeric
  - Weight_Freshsample_Stump, Unit = g
  - Weight_Drysample_Stump, Weight_Drysample_Stump, Variable Type = Numeric
  - Weight_Drysample_Stump, Unit = g
  - Weight_Freshtotal_CR0, Weight_Freshtotal_CR0, Variable Type = Numeric
  - Weight_Freshtotal_CR0, Unit = g
  - Weight_Freshsample_CR0, Weight_Freshsample_CR0, Variable Type = Numeric
  - Weight_Freshsample_CR0, Unit = g
  - Weight_Drysample_CR0, Weight_Drysample_CR0, Variable Type = Numeric
  - Weight_Drysample_CR0, Unit = g

## Measurements and units
- Fresh total and sample weights for Pivot, Stump, and CR0 (coarse roots above soil)
- Corresponding dry weights for Pivot, Stump, and CR0
- All weights recorded in grams (g)

## Provenance, project context, and acknowledgments
- Records originate from direct measurements of stump, pivot, and surface roots after felling.
- Related materials: Manual_2_Belowground_Root_Survey (referenced, page 9).
- Projects: ESPA Programme; Project P4GES; DOI provided for dataset reference.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## How this supports environmental monitoring and data reuse
- Provides standardized biomass-related measurements essential for assessing below-ground carbon stocks and root architecture.
- Data are prepared in a structured, catalogue-able format suitable for integration with other environmental datasets.
- Encourages data sharing and reuse by clearly defining fields (locations, identifiers, and weights) and by pointing to data portals and DOIs.
- Fits the Analysts Monitoring the Environment aim: verify data quality, apply standard methods, and present outputs (e.g., in reports or maps) to support long-term environmental health assessments and policy performance evaluation.