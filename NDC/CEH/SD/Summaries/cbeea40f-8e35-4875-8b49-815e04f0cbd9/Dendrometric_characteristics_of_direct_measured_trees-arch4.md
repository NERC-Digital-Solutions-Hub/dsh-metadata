# DATA HEADER INFORMATION for Dendrometric_characteristics_of_direct_measured_trees.csv

## Overview
- Provides results of direct field measurements for the pool "above ground biomass," focusing on weights, diameters, heights, coordinates, distances, and related dendrometric data.
- Associated with the ESPA Programme and the P4GES project; includes a DOI for data citation.
- Acknowledgement required for outputs derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Data structure and key variables
- Core identifiers and context:
  - Site_ID, Zone of Interest (ZOI), Location (sampling point name)
  - Species_name (vernacular), Scientific_Name
- Morphometrics and structure:
  - Diameter_class (Large >20 cm; Medium 10–20 cm; Small <10 cm)
  - DBH (Diameter at Breast Height), Height_total, H_trunk
  - X, X', Y, Y' (crown projection coordinates on ground)
  - Basal_diameter, Middle_diameter, Top_diameter
  - Length_trunk, Crown_height, Total_length
  - Nb_main_branches
- Biometric weights (all related to various parts/samples):
  - Dry_weight_of_basal_diameter_samples, Dry_weight_of_branches_samples, Dry_weight_of_DBH_diameter_samples, Dry_weight_of_DBH_samples, Dry_weight_of_leaf_samples, Dry_weight_of_Top_trunk_samples, and similar Fresh_weight counterparts
  - Each weight measure has subfields describing sample type, numeric value, unit (e.g., grams, kilograms)
- Data collection context:
  - Field materials/resources include forester compass, botanist, local guides
  - Units specified for each variable (meters, centimeters, grams, kilograms, etc.), though some entries show inconsistencies (e.g., “gramm,” “Kilogramm,” and some Unit fields marked as ".").

## Provenance, access, and usage rights
- Data originate from field measurements conducted under the ESPA and P4GES programs.
- DOI provided for data traceability and citation.
- Acknowledgement is required for outputs derived from these data, reflecting collaboration with local institutions.

## Metadata quality and notes
- Rich metadata describing each variable, including:
  - Variable type (Categorical/Numeric) and Units
  - Field materials/resources per variable (e.g., botanist, forester compass)
- Observed inconsistencies and potential quality issues:
  - Some Unit values are "." or inconsistent (e.g., gramm vs. gram, Kilogramm vs. Kilogram)
  - Some field descriptions include typographical variations or ambiguous naming
- These factors may require harmonization when integrating with other datasets or producing standardized analytics.

## Governance, collaboration, and stewardship
- Dataset involves multiple contributors across roles (botanists, foresters, local guides), reflecting cross-field collaboration.
- Structure supports data discoverability and reuse through detailed definitions and the associated DOI.
- Clear citation guidance and acknowledgment requirements help sustain proper data stewardship and credit.

## Implications and guidance for Data Leaders
- Align with data strategy by cataloging this dataset as a dendrometric asset with detailed, model-ready measurements for above-ground biomass.
- Use the metadata to assess data quality, identify gaps (e.g., inconsistent units, incomplete fields), and plan standardization across datasets.
- Promote co-ownership and feedback loops with end users (policy colleagues, researchers) to ensure data products meet needs.
- Ensure data products emphasize provenance, metadata completeness, and updates to support reliable dissemination.
- Leverage the dataset to inform data governance around measurement standards (DBH, crown measurements, diameter profiles) and improve interoperability with other forestry/dendrometric data.

## Related resources
- Reference to Manual 1_Classical_Survey for methodological context.