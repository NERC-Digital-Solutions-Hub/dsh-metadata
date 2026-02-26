# DATA HEADER INFORMATION for Pivot_and_Stump_data_per_direct_measured_tree_voronoi_method.csv

## Overview
- Records measurements of stump, pivot (taproot), and surface roots for individual trees.
- Pivot = vertical taproot at the base of the target tree; Stump = above-ground cut portion with identifiable below-ground roots.
- After tree felling, stump is cut and taproot excavated and weighed.
- Data supports environmental monitoring efforts by providing biomass-related measurements at the tree level.

## Dataset scope and purpose
- Directly measured, tree-level data collected using a Voronoi-method approach (as implied by the file name).
- Aims to capture fresh and dry weights for different root components to inform biomass, carbon, or root health assessments within monitoring frameworks.
- Data intended for reuse with clear provenance and attribution requirements.

## Key data fields and definitions
- ZOI (Zone of Interest): Categorical field with values such as Andasibe (ZOI2) and Anjahamana (ZOI3).
- Location: Text string describing the sampling point location.
- Site_Id: Text string code for the site where the target tree was collected.
- Local_name: Vernacular/local name of the target tree.
- Code_target_tree: Text code linking site, species, and diameter class for each target tree.
- Weight_Freshtotal_Pivot: Fresh total weight of the pivot (taproot) in grams.
- Weight_Freshsample_Pivot: Fresh weight of the pivot sample in grams.
- Weight_Drysample_Pivot: Dry weight of the pivot sample in grams.
- Weight_Freshtotal_Stump: Fresh total weight of the stump in grams.
- Weight_Freshsample_Stump: Fresh weight of the stump sample in grams.
- Weight_Drysample_Stump: Dry weight of the stump sample in grams.
- Weight_Freshtotal_CR0: Fresh total weight of coarse roots found above soil (CR0) in grams.
- Weight_Freshsample_CR0: Fresh weight of the CR0 sample in grams.
- Weight_Drysample_CR0: Dry weight of the CR0 sample in grams.

## Measurements and units
- All weight measurements are numeric and recorded in grams (g).
- Distinct components measured: pivot (taproot), stump, and coarse roots (CR0), with both total and sample weights (fresh and dry where applicable).

## Location and sampling metadata
- Zone of Interest (ZOI) indicates location category or site group.
- Location, Site_Id, Local_name provide descriptive and coded identifiers for traceability.
- Code_target_tree links the measurement to a specific tree, integrating site, species, and diameter context.

## Provenance and credits
- DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Programme: ESPA
- Project: P4GES
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo (required for products derived from these data)

## Data governance and accessibility considerations
- Metadata and dataset structure support standardization across monitoring outputs.
- Public sharing of underlying data is a consideration; proper attribution and provenance are emphasized.
- Data management at the source is important to ensure metadata completeness, quality, and future usability.

## Relevance for monitoring frameworks
- Provides tangible, measureable root biomass components that can inform environmental health indicators and policy scrutiny.
- Demonstrates careful specimen-level data collection, traceability, and clear definition of variables to reduce misinterpretation.
- Highlights practical data governance challenges (metadata completeness, data sharing barriers, and standardization across organisations) relevant to designing robust monitoring frameworks.