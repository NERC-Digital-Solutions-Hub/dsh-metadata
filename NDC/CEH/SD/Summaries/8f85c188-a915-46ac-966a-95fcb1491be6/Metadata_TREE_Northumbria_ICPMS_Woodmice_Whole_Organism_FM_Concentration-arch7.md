# TREE_Northumbria_ICPMS_Woodmice_Whole_Organism_FM_Concentration

- Overview
  - A tabular data schema for concentrations of multiple elements in wood mouse whole-organism tissue, measured as fresh mass (FM) and expressed in mg/kg.
  - Includes both biological metadata and a broad suite of elemental concentrations.
  - Structured to support spatial (Site) and temporal (Date_Sample_Collected) analyses, suitable for GIS-based mapping and exploration.

- Key metadata fields
  - Latin_Species_Name, Common_Species_Name: scientific and common names of the species.
  - Site: sampling location (spatial identifier for GIS linkage).
  - Date_Sample_Collected: sampling date (temporal dimension).
  - CEH_Sample_Description: description of the UKCEH sample.
  - Notes: notes related to tissues used to calculate the whole-organism concentration.
  - Units and explanations for metadata fields are provided (Units = n/a for textual fields; Explanations describe each field).

- Concentration fields (elements and units)
  - Concentrations are provided for a wide range of elements, including I, Li, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U.
  - All concentration values are in mg/kg (fresh mass).
  - Some fields include markers indicating censored data (less-than values), e.g., <I, <Ni, <Ag, <U, where the corresponding concentration is below detection or reporting threshold.
  - Column naming conventions include both the element symbol and the measurement type (e.g., I_mg_kg_whole_organism_FM).

- Data structure and interpretation
  - The dataset is organized as rows representing samples, with a consistent set of descriptive fields followed by multiple concentration measurements.
  - Textual fields (species, site, date, notes) provide anthropogenic and biological context for GIS joins and filtering.
  - Concentration fields enable spatial analyses of metal/metalloid burdens across sampling sites and over time.
  - The accompanying explanations clarify the meaning of each field and the handling of special values (e.g., less-than markers).

- GIS-related applications
  - Map elemental concentrations by site to identify spatial patterns of exposure or accumulation.
  - Combine with site shapefiles for choropleth or symbol-based visualization of multi-element data.
  - Link temporal data (Date_Sample_Collected) to observe trends or seasonal variation.
  - Use species metadata to compare concentrations across related taxa or to filter analyses by species name.

- Data quality and considerations
  - Data may include measurements below detection limits (indicated by less-than markers).
  - Some fields use Units = n/a (text descriptors) rather than numeric measurements.
  - Consistency across data sources, data standards, and resolution can affect integration; notes describe tissue preparations and calculation methods for whole-organism concentrations.
  - With data held across various fields and potential missing values, careful validation and metadata interpretation are recommended before GIS integration.