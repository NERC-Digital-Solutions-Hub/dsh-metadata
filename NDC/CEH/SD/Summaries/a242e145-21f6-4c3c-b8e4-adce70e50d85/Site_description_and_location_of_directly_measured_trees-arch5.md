# DATA HEADER INFORMATION for Site_description_and_location_of_direct_measured_trees.csv

## Purpose and scope
- Records information on the characteristics of the target tree environment.
- Associated with ESPA Programme and P4GES Project; DOI provided.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).
- Cross-reference to Manual_2_Below_Ground_Root_Survey for related data.

## Data structure and key fields
- Zone of Interest (ZOI): Categorical field with four values (Lakato, Andasibe, Anjahamana, Didy).
- Location: Village name where the target tree was collected (text string).
- Code_Site: Site code where the target tree was collected (text string).
- Species: Local name of the species (text string).
- Code_target_tree: Code for each target tree, linked to site, species, and diameter class (text string).
- Diameter class: Categorical with three classes (L: Large >20 cm DBH; M: Medium 10–20 cm DBH; S: Small 5–10 cm DBH).
- Longitude: GPS longitude in decimal degrees (numeric, WGS84).
- Latitude: GPS latitude in decimal degrees (numeric, WGS84).
- Altitude: Ellipsoidal height of the tree in meters (numeric); measured with GPS devices (eTrex 30 Garmin noted).
- Slope: Slope for each target tree (numeric, degrees).

## Metadata and identifiers
- DOI: https://doi.org/10.5285/a242e145-21f6-4c3c-b8e4-adce70e50d85
- Programme: ESPA
- Project: P4GES
- Data linkage: Code_target_tree ties together Code_Site, species, and diameter class.

## Data governance, quality, and sharing
- Data governance focus: standardization of accuracy, consistency, metadata, and format; preparation before sharing.
- Data availability and limitations: assess disclosure risks, proprietary issues, and embargoes; document updates and ensure mechanisms for refreshing data.
- Quality assurance: apply QA, cleaning, and transformation steps prior to sharing; maintain documentation of work performed on datasets.
- Sharing and recognition: ensure sharing limitations are respected; proper acknowledgement required; provide portal catalogue and accessible metadata.

## Practical implications for Data Stewards
- Ensure timely intake from multiple sites and compatibility across systems and formats.
- Maintain consistent metadata and alignment with user needs to support discovery and reuse.
- Track and update site, tree, and environmental measurements; enforce data provenance and citation requirements.