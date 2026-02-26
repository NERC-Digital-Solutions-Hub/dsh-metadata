# Supporting documentation for Biota_CR.csv.

## Purpose and calculation
- Concentration ratio (CR) is calculated as the biota stable element concentration divided by the soil stable element concentration.
- The dataset is based on soil and biota stable element data, with Sample_Code serving as a unique sample identifier.
- RAP (from ICRP Reference Animals and Plants) categorizes sample type; Sample_Code, Description, and Collection_Date provide context for each sample.

## Data schema and key fields
- Sample identification and context
  - Sample_Code, Explanation, Sample_Code, Units, Sample_Code, Notes
  - RAP, Explanation, RAP, Units, RAP, Notes
  - Sample_Description, Explanation, Sample_Description, Units, Sample_Description, Notes
  - Collection_Date, Explanation, Collection_Date, Units (dd month yyyy), Collection_Date, Notes
  - Soil_used_for_CR_Calculations, Explanation, Soil_used_for_CR_Calculations, Units, Soil_used_for_CR_Calculations, Notes
- Element-specific CR fields
  - I-127, Explanation (CR on a fresh mass basis; unitless; for animals this is the whole-organism CR); I-127, Units (Unitless); I-127, Notes
  - Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
  - For each element: element-specific CR column with Explanation and Units; typically Unitless; Notes indicate whole-organism ratio for animals when applicable; blank indicates concentration below detection limit (see Detection_Limit_ columns).
- Detection limits
  - Detection_Limit_I-127, Detection_Limit_Li, Detection_Limit_Be, Detection_Limit_B, Detection_Limit_Na, Detection_Limit_Mg, Detection_Limit_Al, Detection_Limit_P, Detection_Limit_S, Detection_Limit_K, Detection_Limit_Ca, Detection_Limit_Ti, Detection_Limit_V, Detection_Limit_Cr, Detection_Limit_Mn, Detection_Limit_Fe, Detection_Limit_Co, Detection_Limit_Ni, Detection_Limit_Cu, Detection_Limit_Zn, Detection_Limit_As, Detection_Limit_Se, Detection_Limit_Rb, Detection_Limit_Sr, Detection_Limit_Mo, Detection_Limit_Ag, Detection_Limit_Cd, Detection_Limit_Cs, Detection_Limit_Ba, Detection_Limit_Tl, Detection_Limit_Pb, Detection_Limit_U
  - Each column is unitless and represents the likely maximum CR value estimated using the biota concentration value for which the detection limit was quoted; where blank, the CR value is taken from the corresponding CR column.
  - Some elements (Cs, Ba, Tl, etc.) have multiple subcolumns (1/2/3) detailing different aspects of the detection-limit representation.
- Notes
  - Notes column provides context on analyses or how samples were used to estimate the whole-organism CR; typically “n/a” when not applicable or provided as required.

## Data interpretation and handling
- Unit and organism scope
  - All CR values are unitless.
  - For animals, CR represents the whole-organism concentration ratio.
- Detection limits and below-detection data
  - Blank in a CR column indicates the concentration ratio was below the detection limit.
  - Corresponding Detection_Limit_… columns provide the estimated maximum CR value when a detection limit was quoted.
- Special cases and formatting
  - Some elements have complex detection-limit columns (e.g., Cs, Ba, Tl) with multiple subfields; interpret these per the provided subcolumns.
  - The Notes column may clarify analyses or how samples were incorporated into whole-organism estimates.

## Practical usage and interpretation
- This documentation supports accurate data QA, transformation, and interpretation when deriving CR values from soil and biota measurements.
- Enables self-serve use by end users through clearly defined column semantics, units (all unitless for CR), and handling of below-detection data.
- Facilitates combining Biota_CR.csv with related datasets (e.g., soil concentrations, RAP classifications) using Sample_Code and Soil_used_for_CR_Calculations to reproduce or extend concentration-ratio calculations.