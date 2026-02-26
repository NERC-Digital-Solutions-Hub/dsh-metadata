# Material and methods and metadata

- Scope and samples
  - Fish were collected in 2012 and 2013 as part of CEH monitoring studies from Windermere, Bassenthwaite Lake, and Derwent Water in the English Lake District.
  - Species included: Roach, Perch, Ruffe, Brown trout, Pike, and Vendace.
  - Samples were frozen at -20°C as soon as possible after collection, then defrosted, weighed, gutted, and ashed at 500°C. The ash was weighed for subsequent analysis.

- Laboratory analysis and measurements
  - Ash digests were prepared using aqua regia (3:1 HNO3:HCl) at 175°C for 12 minutes in a microwave (CEM MarsXpress).
  - Elemental analysis was performed by ICPMS or ICPOES (Perkin Elmer).
  - ICPMS measurements used:
    - Quantitative mode: external calibration with internal standards (Ga, In, Re) to correct drift and matrix effects.
    - Semi-quantitative mode: kinetic energy discrimination (KED) with helium.
  - LODs (limits of detection) were calculated from the digestion reagent blank, accounting for dilution. For some semi-quantitative elements where blanks could not determine instrument LODs, LODs were estimated at 0.001 µg L⁻¹ (equivalent to a mean method LOD of 0.001 mg kg⁻¹).
  - Results are reported as mg kg⁻¹ fresh weight, converted from ash weight using the fresh-to-ash mass ratio for each sample.

- Data use and validation
  - Results are intended for model validation, e.g., in the context of extrapolation approaches in radioecological wildlife transfer models (reference to Beresford et al., 2015 in the Journal of Environmental Radioactivity).

- Data schema and metadata
  - The dataset includes laboratory and sample identifiers:
    - Laboratory_id: CEH centralised chemistry laboratory unique sample identifier.
    - Sample_id: CEH Radiochemistry laboratory unique sample identifier.
  - Location and sample details:
    - Lake: name of the lake in the English Lake District.
    - Fish_species_common_name and Fish_species_latin_name.
    - Site_name_or_number: CEH Lake ecosystems group site number or name.
    - Date_fish_sampled: date of sampling (dd/mm/yyyy).
  - Mass measurements:
    - Gutted_ashed_fish_mass_in_grams.
    - Gutted_fresh_fish_mass_in_grams.
    - Ratio_of_wet_fish_mass_to_ashed_fish_mass.
  - Element concentration data:
    - A comprehensive set of element concentration fields, e.g. Li_mg_kg_quantitative, Be_<, Be_mg_kg_quantitative, Na_ICPOES_mg_kg_quantitative, Mg_ICPOES_mg_kg_quantitative, Al_<, Al_mg_kg_quantitative, P_ICPOES_mg_kg_quantitative, S_mg_kg_semi_quantitative, K_ICPOES_mg_kg_quantitative, Fe_ICPOES_mg_kg_quantitative, Co_<, Co_mg_kg_quantitative, Ni_<, Ni_mg_kg_quantitative, Cu_mg_kg_quantitative, Zn_mg_kg_quantitative, Se_mg_kg_quantitative, Br_<, Br_mg_kg_semi_quantitative, Rb_mg_kg_quantitative, Sr_mg_kg_quantitative, Y_mg_kg_semi_quantitative, Zr_<, Zr_mg_kg_semi_quantitative, Nb_<, Nb_mg_kg_semi_quantitative, Mo_<, Mo_mg_kg_quantitative, Rh_<, Rh_mg_kg_semi_quantitative, Pd_<, Pd_mg_kg_semi_quantitative, Cd_mg_kg_quantitative, Sn_<, Sn_mg_kg_semi_quantitative, Sb_<, Sb_mg_kg_quantitative, Cs_mg_kg_quantitative, Ba_mg_kg_quantitative, La_<, La_mg_kg_quantitative, Ce_<, Ce_mg_kg_quantitative, Pr_<, Pr_mg_kg_quantitative, Nd_<, Nd_mg_kg_semi_quantitative, Sm_<, Sm_mg_kg_semi_quantitative, Eu_<, Eu_mg_kg_semi_quantitative, Gd_<, Gd_mg_kg_semi_quantitative, Tb_<, Tb_mg_kg_semi_quantitative, Dy_<, Dy_mg_kg_semi_quantitative, Ho_<, Ho_mg_kg_semi_quantitative, Er_<, Er_mg_kg_semi_quantitative, W_<, W_mg_kg_quantitative, Tl_<, Tl_mg_kg_semi_quantitative, Pb_mg_kg_quantitative, U_<, U_mg_kg_quantitative, etc.
  - Detection-limit notation:
    - A "<" (or "<" in the column name) indicates the element concentration was below the limit of detection (LOD), with the LOD value shown as the concentration in fresh weight where applicable.
  - Units:
    - Most concentration values are in mg kg⁻¹ (fresh weight).
  - Notes:
    - Some elements reported with semi-quantitative or qualitative designations (e.g., certain ICPMS/ICPOES modes) and corresponding data formats.

- Data quality, limitations, and provenance
  - Data produced by CEH centralised chemistry laboratory under CEH monitoring studies.
  - LOD handling follows blanks-based calculations, with some instrument LODs assumed when blanks were not applicable.
  - The dataset is prepared for cross-study model validation and future data sharing, with explicit identifiers and metadata to support traceability.