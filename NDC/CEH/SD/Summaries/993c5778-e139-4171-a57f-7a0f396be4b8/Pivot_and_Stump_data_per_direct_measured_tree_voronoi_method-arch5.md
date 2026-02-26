# DATA HEADER INFORMATION for Pivot_and_Stump_data_per_direct_measured_tree_voronoi_method.csv

## Overview
- Records information on stump, pivot (taproot), and surface roots for directly measured trees using a Voronoi method.
- Clarifies definitions: Pivot is the vertical taproot; Stump is the above-ground portion between the cut point and where roots are identifiable; after felling, the stump is cut and the taproot excavated and weighed.
- Includes DOI, project details, and acknowledgment requirements for derived products.

## Dataset Schema and Key Fields
- ZOI, Information = Zone of Interest; Variable Type = Categorical; Unit = /
  - Examples: ZOI2: Andasibe, ZOI3: Anjahamana.
- Location, Information = Name of the sampling point location; Variable Type = Text String; Unit = .
- Site_Id, Information = Code given to the site where the target tree was collected; Variable Type = Text String; Unit = .
- Local_name, Information = Vernacular/local name of the target tree; Variable Type = Text String; Unit = .
- Code_target_tree, Information = Code linking to each target tree, associated with site, species name, and diameter class; Variable Type = Text String; Unit = .
- Weight_Freshtotal_Pivot, Information = Fresh total weight of Pivot (taproot); Variable Type = Numeric; Unit = g.
- Weight_Freshsample_Pivot, Information = Pivot (taproot) sample fresh weight; Variable Type = Numeric; Unit = g.
- Weight_Drysample_Pivot, Information = Pivot (taproot) sample dry weight; Variable Type = Numeric; Unit = g.
- Weight_Freshtotal_Stump, Information = Fresh total weight of Stump; Variable Type = Numeric; Unit = g.
- Weight_Freshsample_Stump, Information = Stump sample fresh weight; Variable Type = Numeric; Unit = g.
- Weight_Drysample_Stump, Information = Stump sample dry weight; Variable Type = Numeric; Unit = g.
- Weight_Freshtotal_CR0, Information = Fresh total weight of the coarse roots found above soil (CR0); Variable Type = Numeric; Unit = g.
- Weight_Freshsample_CR0, Information = CR0 sample fresh weight; Variable Type = Numeric; Unit = g.
- Weight_Drysample_CR0, Information = CR0 sample dry weight; Variable Type = Numeric; Unit = g.
- Note: Weights are provided for both fresh and dry forms across Pivot, Stump, and CR0 components.

## Provenance, Access, and Acknowledgments
- DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Programme: ESPA; Project: P4GES
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo
- Reference to related materials: Manual_2_Belowground_Root_Survey (page 9)

## Data Quality and Governance Considerations
- Ensure consistent use of units (grams) across all weight-related fields.
- Maintain clear interpretation of ZOI values and precise site/local identifiers to enable cross-dataset linking.
- Validate that Code_target_tree correctly maps to site, species name, and diameter class.
- Monitor for timely data submission from data creators to avoid incomplete records, especially for weight measurements post-excavation.
- Manage data sharing and updates in line with any embargoes or restrictions, and track provenance for derived products.

## Usage Notes for Data Stewards
- Use metadata to support discoverability: clearly tag fields by type (categorical vs numeric) and unit.
- Document any data transformations (cleaning, unit harmonization, or aggregation) performed before sharing.
- Ensure proper attribution by requiring acknowledgment as specified, particularly for products derived from this dataset.