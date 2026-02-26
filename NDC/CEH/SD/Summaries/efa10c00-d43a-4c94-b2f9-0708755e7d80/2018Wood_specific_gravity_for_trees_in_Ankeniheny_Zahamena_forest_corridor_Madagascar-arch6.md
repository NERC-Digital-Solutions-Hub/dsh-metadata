# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

- Overview
  - Dataset documenting wood specific gravity (WSG) and density at 12% moisture content (D12) for wood cores from trees sampled in the Ankeniheny-Zahamena forest corridor, Madagascar.
  - Analyses conducted by the UFR Sciences du bois of the Forestry and Environment Department, ESSA-forêts, Université d’Antananarivo.
  - Related materials: Manual 4_Wood_Specific_Gravity; DOI: https://doi.org/10.5285/efa10c00-d43a-4c94-b2f9-0708755e7d80; ESPA Programme and Project P4GES referenced.
  - Acknowledgement required for products derived from these data (UFR Sciences du bois de l’ESSA-forêts, Université d’Antananarivo; Laboratory des Radio Isotopes, Université d’Antananarivo).

- Data content and structure
  - Variables describe per-sample measurements and contextual information.
  - Key fields include:
    - Day_of_collection (text): day when wood cores were collected.
    - Zone (text): P4GES zone code.
    - Identification (text): wood cores identification.
    - Trees_Local_name (text): vernacular/local tree name.
    - Trees_scientific_name (text): scientific name of sampled trees.
    - Trees_total_height (numeric, meters): visually estimated total tree height.
    - Ttrees_DBH (numeric, centimeters): diameter at breast height (1.3 m).
    - Trees_PHF_index (numeric): quality indicators of tree form (P: crown position, H: crown form, F: stem form).
    - Remarks (text): additional notes.
    - Vsat (numeric, cubic centimeters): saturated volume of the wood core (archimedean method).
    - M12 (numeric, grams): weight at 12% moisture content.
    - V12 (numeric, cubic centimeters): volume at 12% moisture content.
    - Manhy (numeric, grams): anhydrous weight of the sample.
    - D12 (numeric, g/cm3): density at 12% moisture content (D12 = M12 / V12).
    - WSG (numeric, g/cm3): wood specific gravity (WSG = Manhy / Vsat).
  - Note: "x" denotes missing data.

- Measurement methods and units
  - Vsat: saturated volume measured by balance using water displacement (Archimedes principle).
  - M12: weight of the sample at 12% moisture content (balance).
  - V12: volume at 12% moisture content (water displacement method).
  - Manhy: anhydrous weight (balance).
  - D12: density at 12% moisture content (D12 = M12 / V12).
  - WSG: wood specific gravity (WSG = Manhy / Vsat).
  - Units: Vsat and V12 in cubic centimeters; M12 and Manhy in grams; D12 and WSG in grams per cubic centimeter; height in meters; DBH in centimeters.
  - Data notes indicate potential formatting inconsistencies and missing values.

- Data provenance and access
  - Collected and analyzed by the UFR Sciences du bois, ESSA-forêts, Université d’Antananarivo.
  - Associated with ESPA Programme and the P4GES project.
  - DOI provided for data provenance and citation: https://doi.org/10.5285/efa10c00-d43a-4c94-b2f9-0708755e7d80.
  - Documentation includes a manual (Manual 4_Wood_Specific_Gravity) and explicit acknowledgement requirements for derived products.

- Data quality, limitations, and considerations
  - Notes indicate potential missing data (x = missing data).
  - Data spans multiple related measurements with inherent propagation of uncertainty from field collection and measurement methods.
  - The dataset is described in header metadata; users may need to verify data formats and consistency when integrating with other datasets or systems.
  - Data may come from field conditions with variability in measures like total height and DBH estimations.

- Potential uses and data products
  - Create self-serve tools (dashboards, pivot tables) to explore WSG and D12 by species, zone, or tree form quality.
  - Cross-link WSG/D12 with species names to support forestry inventories, carbon modeling, or ecological studies.
  - Map or tabulate WSG by zone, local name, or scientific name to inform policy, conservation planning, or wood density analyses.
  - Combine with additional datasets (e.g., species distributions, climate data) to enhance insights into wood properties across the forest corridor.

- Practical considerations for data support
  - Ensure clear definition and unit consistency when combining with other datasets.
  - Promote outputs and collect feedback to improve data products; maintain acknowledgment requirements in disseminated work.
  - Plan for handling missing data and documenting any data cleaning or transformations applied.