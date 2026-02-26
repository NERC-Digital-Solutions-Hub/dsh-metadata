A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

## Overview
- Metadata-rich dataset reporting radionuclide and stable element measurements from a reference site in the Chernobyl Exclusion Zone.
- Includes concentration ratios (biota to soil) and estimated dose rates.
- Curated and hosted by the NERC Environmental Information Data Centre (EIDC). DOI provided.

## Data files and schema
- Concentration_ratios.csv
  - Contains sampling and biota/soil concentration ratio data across elements.
  - Key columns include Sampling_date, ICRP_RAP, Latin_Name, Common_Name, Code, GP_Point, Sex, Fresh_sample_mass_kg, Tissue, sample, and per-element CR fields (e.g., Li_CR, Be_CR, Na_CR, Mg_CR, …, U_CR).
  - Each element-specific CR column is accompanied by explanatory notes on how values are calculated and how non-detects are handled.
- Stable_element_concentrations.csv
  - Contains stable element concentrations in biota (fresh mass) and soil (dry mass) with geographic and sample metadata.
  - Key columns include Sampling_date, ICRP_RAP, Latin_Name, Common_Name, Code, Latitude, Longitude, GP_point, Sex, Sample_or_tissue_type, wholebody_mass_kg, sample, and per-element measurements:
    - (Element)_mg_kg_FM (biota, fresh mass)
    - (Element)_mg_kg_DM (soil, dry mass)
  - Repeats the same non-detect handling notes as in the concentration ratios file for each element.
- Elements covered (examples): Li, Be, Na, Mg, Al, P, K, Ca, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Cd, Cs, Ba, Tl, U, plus applicable stable elements.

## Key columns and meanings (patterns)
- Temporal and identification data: Sampling_date; Code; Latin_Name; Common_Name; GP_Point/GP_point.
- Biological/physical context: Tissue or Sample_or_tissue_type; Fresh_sample_mass_kg; wholebody_mass_kg; Sex; Latitude/Longitude for stable elements.
- Measurements and units: 
  - Concentration ratios (CR) for biota vs. soil (e.g., Li_CR, Na_CR, …) with CR defined as fresh biota activity concentration divided by dry soil activity concentration.
  - Stable element concentrations: Element_mg_kg_FM (biota, mg/kg fresh mass) and Element_mg_kg_DM (soil, mg/kg dry mass).
- Data quality notes: Extensive guidance on handling non-detects (LOD), tissue-level contributions, and when to report as “less than” values (<10..), including how whole-body estimates are derived.

## Data handling and quality notes
- Non-detects and estimation:
  - If an element is not detectable in all tissues for an animal, LOD values are used to estimate tissue content.
  - If estimated tissue contribution to total body content >10% from below-LOD tissues, whole-body value is reported as a “less than” value.
  - If below-LOD tissues contribute <10% of the body burden, the estimated whole-body concentration is treated as a reasonable approximation; such values are indicated by <10..
- Concentration ratios (CR) interpretation:
  - CR is the ratio of fresh biota concentration to dry soil concentration; used to compare uptake relative to soil.
- Units and bases:
  - Fresh mass (FM) vs. dry mass (DM) baselines are used for different measurements; explicit per-element columns exist for both contexts in stable element data.
- Documentation style:
  - Each element has paired CR or concentration columns with consistent explanatory notes, ensuring traceability of methodology across elements.

## Metadata, provenance, and accessibility
- Data are documented with explicit explanations for each column, units, and the meaning of fields (ICRP_RAP references, Latin/Common names, sample identifiers, geography).
- Source and hosting: NERC Environmental Information Data Centre; DOI provided for dataset reference.
- Structured to support discoverability, reuse, and cross-linking with related data products (e.g., dose-rate estimation).

## Implications for Data Leaders
- The dataset exemplifies a richly annotated data asset with strong emphasis on metadata, data provenance, and transparent handling of non-detects, enabling robust data governance and reuse.
- Strengths:
  - Clear data dictionary for both radionuclide and stable element measurements.
  - Comprehensive treatment of detection limits and body-burden estimation rules.
  - Geospatial and organism metadata support integration with broader data ecosystems.
- Considerations for optimization:
  - Harmonize unit conventions and ensure consistent interpretation across teams adopting the data.
  - Maintain and update metadata to reflect methodological changes or new reference standards (ICRP RAP references).
  - Align data product outputs with user needs (policy colleagues, researchers) through co-ownership and clear data products that demonstrate derivable metrics (e.g., dose-rate estimates).
  - Address data gaps and access barriers by documenting data availability constraints and potential pathways for data acquisition or supplementation.