# Material and methods and metadata

- Study context
  - CEH monitoring studies conducted in 2012 and 2013 in the English Lake District.
  - Lakes: Windermere, Bassenthwaite Lake, Derwent Water.
  - Species collected: Roach, Perch, Ruffe, Brown Trout, Pike, Vendace.

- Sampling and sample preparation
  - Fish samples frozen at -20°C soon after collection.
  - Defrosted, weighed, gutted; whole-fish samples ashed at 500°C.
  - Ashes digested with aqua regia (3:1 HNO3:HCl) at 175°C for 12 minutes using a microwave.

- Analytical methods
  - Elements measured by ICPMS or ICPOES.
  - ICPMS operation: quantitative or semi-quantitative modes.
    - Quantitative: external calibration with internal standards (Ga, In, Re) to correct drift/matrix effects.
    - Semi-quantitative: kinetic energy discrimination (KED) with helium; uses concentration–intensity curves over a wide mass range.
  - LOD determination: from reagent blanks; where not possible, instrument LODs estimated (default 0.001 µg/L, tied to a mean method LOD of 0.001 mg/kg).
  - Results reporting: concentrations given as mg/kg fresh weight (converted from ash weight using fresh-to-ash mass ratio).

- Data products and intended use
  - Data intended for model validation in radioecological wildlife transfer contexts.
  - Example citation: 2015 Journal of Environmental Radioactivity study on extrapolation approaches for wildlife transfer models.

- Data structure and metadata
  - Key identifiers and fields include: Laboratory_id, Sample_id, Lake, Fish_species_common_name, Fish_species_latin_name, Site_name_or_number, Date_fish_sampled.
  - Sample measurements: Gutted_ashed_fish_mass_in_grams, Gutted_fresh_fish_mass_in_grams, Ratio_of_wet_fish_mass_to_ashed_fish_mass.
  - Element concentration columns (example formats): Li_mg_kg_quantitative, Be_mg_kg_quantitative, Na_ICPOES_mg_kg_quantitative, Mg_ICPOES_mg_kg_quantitative, Al_mg_kg_quantitative, Fe_ICPOES_mg_kg_quantitative, Cd_mg_kg_quantitative, Pb_mg_kg_quantitative, U_mg_kg_quantitative, and many others.
  - Detection qualifiers: some columns include “<” to indicate concentrations below the limit of detection (LOD).
  - Units and semantics: most elemental concentrations provided in mg/kg (fresh weight) with some columns indicating units as appropriate for the instrument (ICPOES or ICPMS) and specific measurement mode (quantitative or semi-quantitative).
  - Data dictionary notes: each field has an explanatory description and unit specification; includes lab/sample identifiers, lake/site context, sampling date (dd/mm/yyyy), and mass ratios.

- GIS mapping considerations
  - Spatial linking keys: Lake name and Site_name_or_number enable association with geospatial layers of lakes/sites.
  - Temporal aspect: Date_fish_sampled allows time-series visualization or trend analysis.
  - Attribute enrichment: elemental concentration fields can be mapped as spatial surfaces (e.g., contaminant distribution by lake/site) or joined to GIS attributes for policy or public-facing maps.
  - Data integration: mass measurements and species information support species-, lake-, and site-specific spatial analyses when combined with GIS layers.

- Data quality and limitations
  - Data quality relies on rigorous lab calibration, internal standards, and LOD reporting; some elements have detections below LOD indicated by “<”.
  - LODs for certain semi-quantitative measurements may be estimated when blanks do not permit standard LOD calculation.

- Reference to broader use
  - Data described here are intended for validation in environmental radioactivity and wildlife transfer modeling literature (e.g., Beresford et al., 2015).