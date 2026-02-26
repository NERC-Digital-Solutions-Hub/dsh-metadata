# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

## Purpose and scope
- Presents metadata and data structure for two CSV datasets derived from a reference site in the Chernobyl Exclusion Zone.
- Focuses on radionuclide and stable element concentrations in biota and soil, plus estimated dose rates.
- Supports standardised environmental health assessment and policy monitoring through consistent, reusable data formats.

## Data structure and key fields

- Concentration_ratios.csv
  - Core fields: Sampling_date (dd/mm/yyyy), ICRP_RAP (RAP reference), Latin_Name, Common_Name, Code, GP_Point, Sex, Fresh_sample_mass_kg, Tissue, sample.
  - Derived metrics: Concentration ratio (CR) fields for multiple elements (e.g., Li_CR, Be_CR, Na_CR, Mg_CR, Al_CR, P_CR, K_CR, Ca_CR, V_CR, Cr_CR, Mn_CR, Fe_CR, Co_CR, Ni_CR, Cu_CR, Zn_CR, As_CR, Se_CR, Rb_CR, Sr_CR, Mo_CR, Cd_CR, Cs_CR, Ba_CR, Tl_CR, Pb_CR, U_CR), each representing the ratio of fresh biota activity concentration to dry soil activity concentration.
  - Data quality notes: entries include <Element and related notes to indicate cases where tissue concentrations were below the detection limit (LOD) and how total body content is estimated or censored (e.g., reporting as “<10..” when appropriate).

- Stable_element_concentrations.csv
  - Core fields: Sampling_date, ICRP_RAP, Latin_Name, Common_Name, Code, Latitude, Longitude, GP_point, Sex, Sample_or_tissue_type, wholebody_mass_kg, sample.
  - Per-element measurements: Element_mg_kg_FM (in biota per mg fresh mass) and Element_mg_kg_DM (in soil per mg dry mass), repeated for each stable element.
  - Data quality notes: similar LOD considerations as in the radionuclide dataset, with <Element entries indicating censored measurements.

- Across both datasets, ICRP Reference Animals and Plants (RAP) are used to standardise comparisons, and the Code/GP_Point fields map samples to specific collection sites.

## Data quality, processing, and interpretation

- Data are intended to be verified, quality assured, cleaned, and transformed from established sources.
- Concentration ratios (CR) provide a standardized measure of bioaccumulation by comparing biota concentrations to soil concentrations.
- LOD handling rules:
  - If tissue concentrations are below LOD, an estimated total body content is reported with appropriate qualifiers.
  - If tissue contributions below LOD account for more than 10% of body burden, whole-body estimates are reported as censored (< value); if less than 10%, approximations are used and flagged.
  - Many elements include explicit notes (e.g., <Li, <Na, etc.) to indicate censoring decisions.
- Data are designed to enable cross-study comparisons and transparent dose-rate estimation via standardised reference values.

## Outputs, interpretation, and applications

- Enables categorisation and assessment of environmental radionuclide and stable-element burdens in the Chernobyl Reference Site.
- Supports estimation of dose rates to biota using standard RAP references and concentration metrics.
- Outputs can be visualised in reports, maps, and charts to monitor environmental health and policy performance over time.

## Data storage, access, and sharing

- Metadata describes dataset structure, column headings, units, and data provenance to facilitate storage and portal uploads.
- The standardized formatting supports data reuse, integration with other datasets, and public or stakeholder access to underlying data.

## Relevance to Analysts Monitoring the Environment

- Aligns with the archetype’s goal of using data to demonstrate environmental health in a consistent format for scrutiny over time.
- Employs established references (ICRP RAP) and standardised data products to support monitoring responsibilities and policy evaluation.
- Highlights ongoing challenges and opportunities:
  - Increasing dataset value through linkage with additional environmental data (e.g., other sites, temporal trends).
  - Ensuring broad access to underlying data to enable secondary analyses and wider reuse.