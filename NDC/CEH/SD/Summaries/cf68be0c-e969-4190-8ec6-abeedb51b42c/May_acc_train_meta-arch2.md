# Definitions and Training Data for Maximum Likelihood Classifications of Silene dioica and Crataegus monogyna

## Overview
- Documents the definitions, training data, and accuracy assessment data used for maximum likelihood classifications of two plant species (Silene dioica and Crataegus monogyna) in imagery.
- Covers classifications at two spatial resolutions (3 cm and 7 cm) and includes both training and accuracy assessment datasets.

## Pixel Categories
- Edge: Pixels at the edge of floral unit clusters or within small clusters that appear mixed with other features.
- Pure: Whitest/pinkest pixels (species-dependent), located toward the centre of floral unit clusters, less likely to be mixed.
- Other: Regions not part of the focal species (e.g., branches, soil, green vegetation) used as the 'other' category.

## Training Data
- May_train_other: 'Other' category training data used for both 3 cm and 7 cm classifications (provided as shapefiles with polygons for regions of interest).
- May_train_silene_pure: Silene dioica pure pixel training data for both 3 cm and 7 cm classifications (shapefiles with polygons).
- May_train_silene_edge: Silene dioica edge pixel training data for both 3 cm and 7 cm classifications (shapefiles with polygons).
- May_train_cratae_pure: Crataegus monogyna pure pixel training data for both 3 cm and 7 cm classifications (shapefiles with polygons).
- May_train_cratae_edge: Crataegus monogyna edge pixel training data for both 3 cm and 7 cm classifications (shapefiles with polygons).

## Accuracy Assessment Data (3 cm classifications)
- May_acc_silene_3cm: Polygons representing Silene dioica pixels used in accuracy assessment for the 3 cm variant.
- May_acc_cratae_pure_3cm: Polygons representing Crataegus monogyna 'pure' pixels used in accuracy assessment for the 3 cm variant.
- May_acc_cratae_edge_3cm: Polygons representing Crataegus monogyna 'edge' pixels used in accuracy assessment for the 3 cm variant.
- May_acc_other_3cm: Polygons representing 'other' category pixels used in accuracy assessment for the 3 cm variant.

## Accuracy Assessment Data (7 cm classifications)
- May_acc_Silene_7cm: Polygons representing Silene dioica pixels used in accuracy assessment for the 7 cm variant.
- May_acc_Cratae_pure_7cm: Polygons representing Crataegus monogyna 'pure' pixels used in accuracy assessment for the 7 cm variant.
- May_acc_Cratae_edge_7cm: Polygons representing Crataegus monogyna 'edge' pixels used in accuracy assessment for the 7 cm variant.
- May_acc_other_7cm: Polygons representing 'other' category pixels used in accuracy assessment for the 7 cm variant.

## May 7 cm Training Data Variants
- May_7cm_train_other: 7 cm training data for the 'other' category (used to classify May 7 cm imagery).
- May_7cm_train_cratae_pure: 7 cm Crataegus monogyna 'pure' training data.
- May_7cm_train_cratae_edge: 7 cm Crataegus monogyna 'edge' training data.
- May_7cm_train_silene_pure: 7 cm Silene dioica 'pure' training data.
- May_7cm_train_silene_edge: 7 cm Silene dioica 'edge' training data.
- May_7cm_train_acc_other: Accuracy assessment data for the May 7 cm classification trained on the 7 cm dataset, specifically for the 'other' category.

## Data Formats and Usage
- All training and accuracy assessment datasets are provided as shapefiles.
- Each polygon represents a region of interest for the corresponding class or accuracy assessment pixel.
- Data variants were created by removing or merging regions of interest to allow manual threshold value tuning between categories.

## Relevance to Environmental Monitoring
- Provides standardized, QA-driven datasets to support species distribution mapping and vegetation monitoring at multiple spatial scales.
- Enables transparent evaluation of classification performance and model thresholds, supporting policy-relevant monitoring and reporting.
- Designed to be stored, shared, and uploaded to appropriate data portals to facilitate broad accessibility and reuse within environmental monitoring programs.