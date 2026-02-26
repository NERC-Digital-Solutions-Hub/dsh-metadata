# DATA HEADER INFORMATION for Dendrometric_characteristics_of_direct_measured_trees.csv

## Overview
- Presents results of direct field measurements for the pool "above ground biomass," including weights, diameters, heights, coordinates, and distances.
- Associated with the ESPA program and the P4GES project.
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.
- Documented as a data header detailing the structure and meaning of variables in the dataset.

## Data Content and Structure
- Core identifiers: Site_ID (P4GES WP4 site code), ZOI (Zone of Interest), Location (sampling point name).
- Taxonomic information: Species_name (vernacular), Scientific_Name (scientific name).
- Size/classification: Diameter_class (L, M, S), DBH (Diameter at Breast Height).
- Physical measurements: Height_total, H_trunk, Crown_height, Total_length, Length_trunk.
- Spatial measurements: X, X', Y, Y' (distances to crown projections; in meters).
- Diameter measurements at various trunk heights: Basal_diameter (30 cm from ground), Middle_diameter (half trunk), Top_diameter (top of tree).
- Branch/structure metrics: Nb_main_branches (number of main branches).
- Biomass-related measurements: multiple dry and fresh weight fields for various tree components and sampling points.
- Data columns include grouped subfields (e.g., Fresh_weight_of_branches, Fresh_weight_of_DBH_samples, etc.) with enumerated indicators (1, 2, 3, 4) describing component replicates or sample parts.
- Units and field methods are described for each variable (e.g., forester compass used for certain diameter measurements).

## Key Variables and Measurements
- Identifiers and location: Site_ID, ZOI, Location.
- Species: Species_name, Scientific_Name.
- Size and structure: DBH (cm), Height_total (m), H_trunk (m), Crown_height (m), Total_length (m), Length_trunk (m), Nb_main_branches.
- Crown and trunk geometry: X, X', Y, Y' (distance to crown projections), Basal_diameter (cm), Middle_diameter (cm), Top_diameter (cm).
- Biomass components: Dry_weight_of_basal_diameter_samples, Dry_weight_of_branches_samples, Dry_weight_of_DBH_diameter_samples, Dry_weight_of_DBH_samples, Dry_weight_of_leaf_samples, Dry_weight_of_Top_trunk_samples, Fresh_weight_of_basal_diameter_samples, Fresh_weight_of_branches, Fresh_weight_of_leaf, Fresh_weight_of_trunk, and related replicate fields (1–4).
- Sampling detail fields indicate the specific sample position (e.g., basal diameter, DBH, middle trunk, top trunk) and whether measurements are fresh or dry, with units in grams or kilograms as specified.

## Units and Data Collection Details
- Lengths and heights: meters (m).
- Diameters: centimeters (cm).
- Distances: meters (m).
- Weights: grams (g) for many dry/fresh weight measurements; kilograms (kg) for some total weights.
- Data collection referenced to standard forestry measurements (e.g., DBH at 1.3 m, crown height from ground to crown base).

## Provenance, Access, and Usage
- Data provenance: ESPA program; Project P4GES; site-level data with Zone of Interest and sampling locations.
- Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.
- Methodology reference: Manual 1_Classical_Survey (implied for survey procedures).
- Data collaboration notes: Field materials/resources include botanists, local guides, and forester tools; documentation suggests dataset aims to support detailed, scalable biomass analyses.

## Potential Analytical Uses
- Estimate above-ground biomass using direct dendrometric measurements.
- Develop allometric models linking DBH, height, trunk diameters, and biomass components.
- Compare biomass components across species, zones of interest, and sampling points.
- Data can feed into wider datasets by documenting sources, measurement methods, and replicates.

## Considerations and Limitations
- Rich in descriptive fields but may include replicate subfields (1–4) requiring careful alignment during analysis.
- Data scale is local (site and zone-based) and may require upscaling or careful interpretation for broader generalizations.
- Potential data quality issues implied by multiple data fields with typographical variations (e.g., unit naming), necessitating careful metadata checks.
- Access requires proper citation/acknowledgement and adherence to the associated project and institutional requirements.