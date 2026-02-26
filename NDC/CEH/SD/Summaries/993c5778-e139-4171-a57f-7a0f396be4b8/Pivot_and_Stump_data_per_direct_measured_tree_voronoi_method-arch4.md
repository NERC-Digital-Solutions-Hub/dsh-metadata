# DATA HEADER INFORMATION for Pivot_and_Stump_data_per_direct_measured_tree_voronoi_method.csv

## Overview
- Documents measurements of stump, pivot (taproot), and surface roots for trees felled and analyzed using a direct measured approach with a Voronoi method.
- Describes terminology (pivot/taproot, stump) and the procedure (stump cut and taproot excavated and weighed).
- References related materials (Manual_2_Belowground_Root_Survey, page 9).

## Data elements, structure, and types
- ZOI (Zone of Interest): Categorical; Unit = /; examples include Andasibe, Anjahamana.
- Location: Text; Name of sampling point location.
- Site_Id: Text; Code for the site where the target tree was collected.
- Local_name: Text; Vernacular/local tree name.
- Code_target_tree: Text; Code linking to the site, species name, and diameter class.
- Weight_Freshtotal_Pivot: Numeric; Fresh total weight of Pivot (taproot) in grams.
- Weight_Freshsample_Pivot: Numeric; Fresh weight of Pivot sample in grams.
- Weight_Drysample_Pivot: Numeric; Dry weight of Pivot sample in grams.
- Weight_Freshtotal_Stump: Numeric; Fresh total weight of Stump in grams.
- Weight_Freshsample_Stump: Numeric; Fresh weight of Stump sample in grams.
- Weight_Drysample_Stump: Numeric; Dry weight of Stump sample in grams.
- Weight_Freshtotal_CR0: Numeric; Fresh total weight of coarse roots found above soil (CR0) in grams.
- Weight_Freshsample_CR0: Numeric; Fresh weight of CR0 sample in grams.
- Weight_Drysample_CR0: Numeric; Dry weight of CR0 sample in grams.

## Data provenance and references
- DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Programme: ESPA
- Project: P4GES
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo
- Related documentation: Manual_2_Belowground_Root_Survey (page 9)

## Location and metadata context
- Zone of Interest (ZOI) and location fields support geographic and site-level context for each measurement.
- Code_target_tree links each measurement to species and diameter class information via the associated site code.

## Data quality and governance considerations
- Consistent units: all weight measurements are in grams (g).
- Clear distinction between total weights and component weights (sampled vs. total) to support compositional analysis.
- Metadata completeness (location, site, local name, and target tree code) facilitates discoverability and reuse.

## Practical implications for data strategy
- Ensures traceability from site to specific trees and their below-ground components.
- Supports cross-site and cross-project data integration by standardizing metadata and measurement units.
- Enables verification and replication through explicit documentation of measurement methods and data sources.