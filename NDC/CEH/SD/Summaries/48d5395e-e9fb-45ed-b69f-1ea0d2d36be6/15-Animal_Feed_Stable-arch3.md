# Supporting documentation for 15-Animal_Feed_Stable.csv

## Purpose and scope
- Provides a data dictionary for a dataset on stable concentrations of elements in the total diet of animals.
- Key contextual fields: Animal, Location, Feeding.
- Chemical/measured variables cover Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th (in mg per kg dry mass) along with uncertainty (Unc_*) and detection limits (Detection_Limit_*).

## Key variables and definitions
- Animal: General type of animal (text).
- Location: Location name where the sample was collected (text).
- Feeding: Description of feeding regimes (text).
- Cs_mg/kg_dm: Concentration of stable Cs in the total diet (mg/kg dry mass). Blank = below detection limit.
- Unc_Cs_mg/kg_dm: Uncertainty (quadratic propagation) of Cs concentration (mg/kg dry mass). Blank = below detection limit.
- Detection_Limit_Cs_mg/kg_dm: Detection limit for Cs in the total diet (mg/kg dry mass). Blank = concentration above detection limit.
- Sr_mg/kg_dm, Unc_Sr_mg/kg_dm, Detection_Limit_Sr_mg/kg_dm: Analogous definitions for stable Sr.
- K_mg/kg_dm, Unc_K_mg/kg_dm, Detection_Limit_K_mg/kg_dm: Analogous definitions for stable K.
- Na_mg/kg_dm, Unc_Na_mg/kg_dm, Detection_Limit_Na_mg/kg_dm: Analogous definitions for stable Na. Note: Na-related fields show irregular naming (1, 2, 3 suffixes) in the metadata.
- Ca_mg/kg_dm, Unc_Ca_mg/kg_dm, Detection_Limit_Ca_mg/kg_dm: Analogous definitions for stable Ca.
- Mg_mg/kg_dm, Unc_Mg_mg/kg_dm, Detection_Limit_Mg_mg/kg_dm: Analogous definitions for stable Mg. Formatting inconsistencies observed (e.g., Mg_mg/ kg_dm).
- P_mg/kg_dm, Unc_P_mg/kg_dm, Detection_Limit_P_mg/kg_dm: Analogous definitions for stable P.
- Pb_mg/kg_dm, Unc_Pb_mg/kg_dm, Detection_Limit_Pb_mg/kg_dm: Analogous definitions for stable Pb. Some fields show incomplete notes (e.g., Unc_Pb_mg/kg_dm, detection limit phrasing).
- U_mg/kg_dm, Unc_U_mg/kg_dm, Detection_Limit_U_mg/kg_dm: Analogous definitions for stable U.
- Th_mg/kg_dm, Unc_Th_mg/kg_dm, Detection_Limit_Th_mg/kg_dm: Analogous definitions for stable Th.

## Data quality, interpretation, and handling
- All concentration values are on a dry mass basis (mg/kg_dm).
- Blank entries in concentration fields indicate concentrations below the detection limit (censored data).
- Uncertainty fields provide quadratic propagation uncertainty for the corresponding concentrations.
- Detection limit fields indicate the minimum detectable concentration; blanks imply the concentration is above the detection limit.
- Data governance implications: explicit metadata for each variable supports transparency, traceability, and reproducibility in environmental health monitoring.

## Relevance for monitoring frameworks
- Standardizes essential data elements (sample context, analyte concentrations, uncertainties, detection limits) to enable aggregation, comparison, and longitudinal monitoring.
- Facilitates data sharing and governance by making underlying measurements and their limits explicit.
- Supports gap identification and data improvement by highlighting where data are missing, uncertain, or censored.
- Encourages consistency across datasets by clearly defining units (mg/kg dry mass) and the interpretation of non-detects.

## Notable considerations and potential issues
- Inconsistent naming/formatting in certain fields (e.g., Na and Mg-related entries; Na_Unc_Na_mg/kg_dm with 1/2/3 suffixes) that may require cleaning for robust ingestion.
- Some notes appear truncated or variable in phrasing (e.g., Pb_Unc_mg/kg_dm notes, detection-limit wording), requiring careful data validation during implementation.