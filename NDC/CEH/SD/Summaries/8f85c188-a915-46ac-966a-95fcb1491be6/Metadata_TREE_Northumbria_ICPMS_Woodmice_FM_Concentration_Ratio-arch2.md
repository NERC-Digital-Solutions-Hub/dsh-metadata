# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

- Purpose and scope
  - Describes a dataset capturing concentration ratios of multiple elements in woodmice tissue relative to nearby dry soil.
  - Units not specified; ratios are defined as Fresh Mass Woodmice (wholebody) divided by Dry Mass Soil.
  - Data are intended to support environmental monitoring by comparing vertebrate exposure to environmental metal contamination over time and across sites.

- Key data fields (categories)
  - Biological/taxonomic identifiers
    - Latin_Species_Name
    - Common_Species_Name
  - Spatial and temporal context
    - Site
    - Date_Sample_Collected
  - Sampling description and notes
    - CEH_Sample_Description
    - Notes
  - Soil link for ratio calculation
    - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
  - Concentration ratio measurements (element-by-element)
    - For each element (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U)
      - [Element]_Concentration_Ratio_1
      - [Element]_Concentration_Ratio_2
        - Note: 1 = not applicable; 2 = actual concentration ratio (Fresh Woodmice / Dry Soil)
        - Some elements use a less-than marker (e.g., <I, <Be, <Ni, <Ag, <U) to indicate a value reported as a threshold
      - This structure indicates two-part ratio data per element, with the second part containing the usable ratio in most cases
  - Special markers
    - <I, <Be, <Ni, <Ag, <U markers indicate concentration ratios reported as “less than” values

- Data quality, processing, and presentation
  - The dataset assumes verification, quality assurance, and transformation as part of standard monitoring practice.
  - Outputs are intended to be presented in clear formats (e.g., tables of ratios) and stored/uploaded to appropriate data portals.

- Uses and implications for environmental monitoring
  - Enables assessment of how small mammal tissue metal burdens relate to soil contamination across sites and time.
  - Supports cross-site comparisons, trend analysis, and policy-relevant health assessments by standardizing ratio calculations and metadata.

- Challenges and opportunities
  - Increasing the value of these datasets by integrating with other relevant environmental data (e.g., additional species, landscape factors) rather than treating them as standalone measurements.
  - Enhancing accessibility to the underlying data used to derive the concentration ratios to enable broader analysis and reuse.