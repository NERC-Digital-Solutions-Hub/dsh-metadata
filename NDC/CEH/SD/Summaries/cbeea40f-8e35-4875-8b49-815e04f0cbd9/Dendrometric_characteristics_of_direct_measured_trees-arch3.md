# DATA HEADER INFORMATION for Dendrometric_characteristics_of_direct_measured_trees.csv

## Overview
- Presents direct field measurements for the pool "above ground biomass" including weights, diameters, heights, coordinates, and related metrics.
- Associated with the ESPA programme and the P4GES project; DOI provided for the dataset.
- Acknowledges Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Data scope and provenance
- Contains results from field measurements used to assess above-ground biomass in trees.
- Sites referenced: Zone of Interest (ZOI) includes Lakato, Andasibe, Anjahamana, and Didy.
- Data includes both vernacular and scientific names for species; multiple field roles and equipment indicated (botanist, forester compass, decameter).
- Data publication and sharing are governed by metadata quality and data provenance requirements; public sharing of underlying data is noted as a potential barrier in practice.

## Key variables and data structure
- Identification and location
  - Site_ID (text), ZOI (categorical), Location (text)
- Taxonomy
  - Species_name (vernacular), Scientific_Name (scientific)
- Size and form indicators
  - Diameter_class (categorical: Large, Medium, Small), DBH (numeric, cm), Height_total (numeric, m), H_trunk (numeric, m)
- Spatial positioning
  - X, X', Y, Y' (numeric, meters) representing projections relative to trunk and crown
- Dendrometric diameters
  - Basal_diameter, Middle_diameter, Top_diameter (numeric, cm)
- Trunk and crown measures
  - Length_trunk (m), Crown_height (m), Total_length (m), Nb_main_branches (numeric)
- Biomass samples (weights)
  - Dry_weight_of_basal_diameter_samples, Dry_weight_of_branches_samples, Dry_weight_of_DBH_diameter_samples, Dry_weight_of_DBH_samples, Dry_weight_of_leaf_samples, Dry_weight_of_Top_trunk_samples, Fresh_weight_of_basal_diameter_samples, Fresh_weight_of_branches, Fresh_weight_of_DBH_samples, Fresh_weight_of_leaf, Fresh_weight_of_Middle_trunk_samples, Fresh_weight_of_Top_trunk_samples, Fresh_weight_of_trunk
  - Units include grams (g), kilograms (kg); many fields indicate multiple subsamples (e.g., 1, 2) or parts of measurements
- Data labeling and collection context
  - Field materials/resources include botanist, forester compass, decameter
  - Information layout emphasizes measurement context (above-ground biomass core)

## Data quality, metadata, and governance
- Data should undergo quality assurance, cleaning, transformation, and clear presentation (reports, charts, dashboards).
- Metadata completeness is a recurring challenge; some fields provide explicit unit and method details, while others may require verification from originators.
- Data governance considerations include sharing underlying data appropriately and meeting standard data storage and update practices.
- The header text itself serves as an essential metadata scaffold, describing variable types, units, and provenance.

## Access, use, and acknowledgements
- DOI provided for dataset access and citation.
- Programme and project links: ESPA and P4GES websites.
- Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Relevance for monitoring and evaluation
- Illustrates a comprehensive set of dendrometric and biomass-related measurements suitable for monitoring above-ground biomass and forest structure.
- Demonstrates integration of field measurements with metadata standards (site, zone, species, units) to support policy scrutiny, evaluation, and future decision-making.
- Highlights practical barriers and governance needs common to monitoring initiatives (data gaps, access, metadata quality, data sharing, and data stewardship).