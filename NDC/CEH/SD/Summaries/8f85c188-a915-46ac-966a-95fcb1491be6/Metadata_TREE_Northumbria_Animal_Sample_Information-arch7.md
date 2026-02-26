# TREE_Northumbria_Animal_Sample_information

- Overview
  - A metadata-style dataset describing animal samples from Northumbria, intended for map-based GIS analysis. Captures taxonomic information, sampling details, spatial references, and specimen measurements to support spatial visualization and exploration.

- Key fields and what they capture
  - Taxonomic names
    - Latin_Species_Name: Scientific name of species
    - Common_Species_Name: Common name of species
  - Sampling and location
    - Site: Sampling site identifier
    - Date_Sample_Collected: Collection date
    - Sampling_Location_Or_National_Grid_Reference: Spatial reference (grid reference or location)
  - Identification codes and descriptions
    - CEH_Sample_Codes_Associated_with_Animal_Or_Sample: CEH-derived codes linked to the sample
    - CEH_Sample_Description: Description of the CEH sample
  - Measurements and physical attributes
    - Length_mm: Body length in millimetres
    - Width_mm: Body width in millimetres
    - Depth_mm: Body depth in millimetres
    - Wholebody_Fresh_Mass_kg: Fresh mass in kilograms
    - Wholebody_Freeze_Dried_Mass_kg: Freeze-dried mass in kilograms
    - Wholebody_Ash_Mass_kg: Ash mass in kilograms
  - Counts, sex, and notes
    - n: Number of animals or samples
    - Sex: Sex of the animal (where determined)
    - General_Notes: Additional notes about the sample
  - Processing and analysis
    - Sample_Preparation_And_Analysis_Performed: Information on preparation and analyses conducted
  - Special cases
    - Frogspawn: Noted as bulk samples of multiple eggs; measurements may be inapplicable

- Data quality and standardization considerations
  - Missing data
    - Not Recorded appears for several measurement fields; requires handling during data cleaning
  - Units
    - Measurements use millimetres (mm) and kilograms (kg); ensure consistency across records
  - Data fragmentation
    - Data may be held in multiple sources; plan for integration and provenance tracking
  - Taxonomic naming
    - Presence of both Latin and Common names; consider standardizing to a preferred nomenclature for GIS joins
  - Special cases
    - Frogspawn bulk samples require careful interpretation for per-sample statistics

- GIS relevance and recommended workflows
  - Spatial mapping
    - Use Sampling_Location_Or_National_Grid_Reference to plot sampling points; convert to a consistent CRS (e.g., British National Grid or WGS84) as needed
  - Classification and visualization
    - Symbolize by species (Latin/Common name), date, or sex
    - Create attribute-driven visualizations for lengths, masses, and counts
  - Data integration
    - Join with external spatial layers (sites, habitats, protected areas) to enrich context
  - Data preparation
    - Clean and normalize: resolve Not Recorded values, standardize units, harmonize species names, and document data provenance
  - Temporal analysis
    - If Date_Sample_Collected is complete, enable temporal mapping of sampling events

- End-user considerations
  - This dataset is designed to support end-user exploration of spatial patterns in species distribution, sample characteristics, and sampling effort across Northumbria.