# Material and methods and metadata

- Study and samples
  - CEH monitoring studies conducted in 2012 and 2013.
  - Lakes: Windermere, Bassenthwaite Lake, and Derwent Water in the English Lake District, UK.
  - Species collected: Roach (Rutilus rutilus), Perch (Perca fluviatilis), Ruffe (Gymnocephalus cernuus), Brown trout (Salmo trutta), Pike (Esox lucius), Vendace (Coregonus albula).
  - Sample handling: fish frozen at -20°C soon after collection; defrosted, weighed, gutted; whole-fish ash prepared at 500°C.
  - Ash digests: digested with aqua regia (3:1 HNO3:HCl) at 175°C for 12 minutes in a microwave (CEM MarsXpress).
  
- Analytical methods
  - Instrumentation: ICPMS (Perkin Elmer NexION 300D) and ICPOES (Perkin Elmer 7300 DV).
  - Modes:
    - Quantitative ICPMS with external calibration; internal standards (Ga, In, Re at 10 µg L⁻¹) to correct drift and matrix effects.
    - Semi-quantitative ICPMS using kinetic energy discrimination (helium) to extrapolate concentrations from a response curve over a wide mass range.
  - Limits of detection (LOD):
    - Calculated from method blanks (reagent blanks) as y_b plus 3s_b, accounting for sample digestion dilution.
    - For some semi-quantitative measurements where blanks could not define LODs, an instrument LOD of 0.001 µg L⁻¹ (equivalent to 0.001 mg kg⁻¹) was assigned.
  - Reporting: element concentrations reported as mg kg⁻¹ on a fresh weight basis (converted from ash weight via the fresh-to-ash mass ratio).
  - Data use: results intended for model validation (e.g., applications in wildlife transfer models); referenced in Beresford et al. 2015 (Journal of Environmental Radioactivity).

- Data structure and metadata
  - Laboratory identifiers: Laboratory_id (CEH centralised chemistry lab), Sample_id (Radiochemistry lab).
  - Sample and site information: Lake, Fish_species_common_name, Fish_species_latin_name, Site_name_or_number, Date_fish_sampled.
  - Sample mass data: Gutted_ashed_fish_mass_in_grams, Gutted_fresh_fish_mass_in_grams, Ratio_of_wet_fish_mass_to_ashed_fish_mass.
  - Measurements: concentrations for numerous elements (e.g., Li, Be, Na, Mg, Al, P, S, K, Ca, Ti, Mn, Fe, Co, Ni, Cu, Zn, Se, Br, Rb, Sr, Y, Zr, Nb, Mo, Rh, Pd, Cd, Sn, Sb, Cs, Ba, La, Ce, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, W, Tl, Pb, U) with qualifiers:
    - Quantitative (mg kg⁻¹) or semi-quantitative (mg kg⁻¹) measurements.
    - Some elements marked with "<" indicating below the limit of detection (LOD).
  - Data quality and provenance: explicit metadata descriptions for every field; emphasis on data source tracing, variable naming (e.g., Li_mg_kg_quantitative, Al_<), and units; intention to make datasets discoverable with metadata.