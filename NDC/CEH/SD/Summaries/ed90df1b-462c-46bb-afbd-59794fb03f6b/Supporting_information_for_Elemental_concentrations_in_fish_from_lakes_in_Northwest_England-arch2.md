# Material and methods and metadata

- Study scope and context
  - Fish were collected during CEH monitoring studies in 2012 and 2013 from Windermere, Bassenthwaite Lake, and Derwent Water in the English Lake District.
  - Target species: Roach (Rutilus rutilus), Perch (Perca fluviatilis), Ruffe (Gymnocephalus cernuus), Brown trout (Salmo trutta), Pike (Esox lucius), and Vendace (Coregonus albula).
  - Samples were frozen at -20°C promptly after collection and later processed for chemical analysis.

- Sampling and handling
  - Each fish was weighed, gutted, and the whole-fish samples were ashed at 500°C.
  - Ash was digested with aqua regia (3:1 HNO3:HCl) at 175°C for 12 minutes in a microwave system.

- Analytical methods
  - Elemental analysis was performed by ICPMS (Perkin Elmer NeXION 300D) or ICPOES (Perkin Elmer 7300 DV).
  - ICPMS operation modes:
    - Quantitative mode with external calibration and internal standards (Ga, In, Re) to correct drift and matrix effects.
    - Semi-quantitative mode using kinetic energy discrimination (KED) with helium, deriving concentrations from an intensity vs. mass response curve.
  - ICPOES was used for certain elements; both methods provided concentration data in mg kg^-1 fresh weight (fw), after converting from ash weight using a fresh-to-ash mass ratio.

- Quality assurance and detection limits
  - Limits of detection (LOD) were calculated from digestion reagent blanks (mean + 3×SD), incorporating dilution from digestion.
  - For some semi-quantitative ICPMS elements where blanks did not yield a usable LOD, instrument LODs were estimated from sensitivity and set to 0.001 µg L^-1 (equivalent to a 0.001 mg kg^-1 mean LOD).
  - Where measurements were below LOD, the value is reported with a less-than sign (e.g., Be_<) to indicate non-detects.

- Data products and reporting
  - Results are reported as mg kg^-1 fresh weight (fw).
  - Masses are reported for both gutted ashed mass and gutted fresh mass, with ratios provided (wet mass to ashed mass).
  - Data are structured with explicit metadata fields and a clear data dictionary to enable reproducibility and future use.

- Data structure and metadata (sample and measurement identifiers)
  - Key identifiers and fields include: Laboratory_id (CEH centralised chemistry lab), Sample_id (CEH Radiochemistry lab), Lake, Fish_species_common_name, Fish_species_latin_name, Site_name_or_number, Date_fish_sampled (dd/mm/yyyy).
  - Measurements include Gutted_ashed_fish_mass_in_grams, Gutted_fresh_fish_mass_in_grams, Ratio_of_wet_fish_mass_to_ashed_fish_mass.
  - Element concentration fields cover various elements with prefixes indicating measurement type and unit, e.g., Li_mg_kg_quantitative, Al_mg_kg_quantitative, Na_ICPOES_mg_kg_quantitative, Se_mg_kg_quantitative, etc.
  - For elements with detectability issues, both "<LOD" indicators and corresponding numerical values are provided; semi-quantitative and quantitative measurement modes are distinguished (e.g., Br_mg_kg_semi_quantitative vs Br_mg_kg_quantitative).

- Data usage and applications
  - The dataset is intended for model validation and methodological development in environmental radioecology and wildlife transfer models (reference to the 2015 Journal of Environmental Radioactivity paper on extrapolation approaches).
  - Outputs support standardised monitoring and enable cross-data comparisons over time and across sites.
  - Emphasizes the importance of storing datasets in centralized repositories and ensuring accessibility of the underlying data to stakeholders.

- Relevance to monitoring and transparency
  - The documentation demonstrates a standardised, QA-driven workflow from collection to analysis to metadata curation.
  - Data schemas and explicit metadata enhance interoperability, reuse in policy evaluation, and combination with other environmental datasets.
  - Aligns with analysts’ monitoring aims: transparent data handling, standardized outputs (maps, reports, charts), and preparation of datasets for portals and broader scrutiny.