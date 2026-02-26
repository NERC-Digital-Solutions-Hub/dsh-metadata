# DATA HEADER INFORMATION for Forest_inventory.csv

## Overview
- Describes characteristics of trees located on the Zone of Interest, linked to the ESPA programme and P4GES project.
- Includes data provenance, sampling details, and taxonomic information for each recorded tree.
- Acknowledgement of the Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.

## Dataset scope and structure
- Site_ID: P4GES site code; text string.
- trees_subplot: Subplot category by radius (5m? < Small < 10m; 10m < medium < 20m; 20m < Large); categorical (S, M, L).
- trees_area: Surface area of the sampling plot; numeric; unit is square meters (m²).
- trees_local_name: Vernacular/local name of the inventoried species; text.
- trees_scientific_names: Scientific name of the inventoried species; text.
- trees_genera: Genus of the selected tree; text.
- trees_family: Family of the selected tree; text.
- trees_DBH: Breast height diameter of the tree (diameter at 1.3 m); numeric; unit centimeters.
- trees_height: Total height of the tree (from ground to top); numeric; unit meters.
- Field_materials Ressources: Attributions indicating who collected or contributed data (e.g., botanist, forester compass, vertex).

## Provenance and attribution
- Programme: ESPA; Project: P4GES.
- Data collection and labeling involve botanists and foresters; specific field personnel are recorded via Field_materials Ressources.
- Acknowledgement requirement for products derived from the data; implies data use permissions and stewardship considerations.

## Data quality, metadata and governance considerations
- Some metadata elements are unspecified or formatted with placeholders (e.g., Site_ID units shown as "."), indicating incomplete metadata that may need standardization.
- Data may require transformation to be readily usable in dashboards or analyses (e.g., consistent unit handling and field naming).
- Public sharing of underlying datasets is disclosed as a potential barrier in other monitoring contexts; ensure appropriate data governance and sharing practices are in place if outputs are to be disseminated.
- Metadata and provenance should be preserved to support traceability and reuse in monitoring reports and policy evaluations.