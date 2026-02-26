# Supporting documentation for Biota_CR.csv.

## Overview
- Concentration ratios (CR) are calculated as the biota stable element concentration divided by the soil stable element concentration.
- Each record uses a unique Sample_Code with metadata describing sample type, collection date, and sample description.
- RAP (Reference Animals and Plants) classification follows ICRP RAPs, indicating sample type context.
- For each element, CR is recorded as a unitless value on a fresh mass basis; if data are below detection limits, corresponding notes and Detection_Limit fields capture the upper-bound indication.
- Notes provide context on analyses or how whole-organism CRs were estimated.

## Data structure and key fields
- Sample_Code
  - Unique sample identifier.
- RAP
  - Sample type based on ICRP Reference Animals and Plants (RAPs).
- Sample_Description
  - Further explanation of the sample where applicable.
- Collection_Date
  - Date of soil sample collection (format: dd month yyyy).
- Soil_used_for_CR_Calculations
  - Identifies the Sample_Code for the soil sample(s) used to estimate the Concentration ratio.
- Elemental CR fields (one per element; all are unitless)
  - I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
  - Each entry represents the concentration ratio on a fresh mass basis (biota/soil).
  - For animals, the CR is the whole-organism concentration ratio.
  - Where blank, the concentration ratio was below the detection limit (see corresponding Detection_Limit_<element> column).
- Detection_Limit_<element> (one per element)
  - The likely maximum CR value estimated using the biota stable element concentration for which the detection limit was quoted.
  - Units are unitless.
  - If present, indicates the detection-limit-derived upper bound; if blank, the preceding CR value stands without a stated detection-limit bound.
- Notes
  - Note on analyses or how samples were used in the estimation of the whole-organism concentration ratio; provided where required.

## Calculation and interpretation details
- CR = biota stable element concentration / soil stable element concentration.
- Soil_used_for_CR_Calculations identifies which soil sample(s) were used in the CR calculation.
- Detection_Limit_<element> fields accompany most element CRs to indicate censorship due to detection limits.
- Some entries specify that certain Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U values are “value estimated using biota stable element concentration for which the detection limit was quoted” or similar phrasing, reflecting data handling near detection limits.
- In practice, a blank CR value indicates the measured concentration ratio was below the detection limit; the corresponding Detection_Limit_<element> provides the upper bound.

## Metadata and data provenance
- Data intended to be trackable and discoverable with metadata; sample and soil codes link CRs to source datasets.
- Notes field captures methodological details or how certain CRs were estimated, especially for whole-organism estimations.

## Data quality, limitations, and considerations for analysts
- Detection-limit censoring: many CRs may be censored at detection limits; interpret censored values with the available Detection_Limit_<element> and Notes.
- Scale and locality: records include diverse samples with RAP classifications; local context may influence CR patterns.
- Data integration: CRs rely on soil concentrations; ensure correct pairing of soil sample codes via Soil_used_for_CR_Calculations.
- Interpretation of “whole-organism” CRs for animals vs potential tissue-specific CRs; notes indicate whether the value represents the entire organism.
- Data completeness: some elements may have missing CR values or limited detection-limit information, affecting cross-element comparisons.

## Practical usage tips for analysts
- Use Sample_Code and Soil_used_for_CR_Calculations to trace source materials and replicate CR calculations.
- Treat Detection_Limit_<element> as the upper-bound when CR is censored; consult Notes for context on estimation methods.
- Leverage RAP classifications to compare CR patterns across reference organisms and plants versus other sample types.
- When aggregating across datasets, account for unitless CRs and uniform treatment of “whole-organism” CRs to avoid misinterpretation.