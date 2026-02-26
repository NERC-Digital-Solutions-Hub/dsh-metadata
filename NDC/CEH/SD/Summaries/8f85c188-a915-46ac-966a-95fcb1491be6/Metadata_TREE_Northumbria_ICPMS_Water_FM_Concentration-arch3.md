# TREE_Northumbria_ICPMS_Water_FM_Concentration

## Purpose and scope
- Defines a dataset structure for Northumbria ICP-MS water concentration measurements.
- Captures both sample metadata and a comprehensive set of inorganic element concentrations in water.
- Intended to support environmental health monitoring, policy scrutiny, and informing future decision-making.

## Dataset structure and key fields
- Core sample metadata
  - CEH_Sample_Identifier: UKCEH sample code
  - CEH_Sample_Description: UKCEH sample description
  - Site: Sampling site
  - Sampling_Date: Date the sample was collected
  - Notes: Notes on preparation
- Analyte concentrations (all in mg/L)
  - Al_mg_l, As_mg_l, B_mg_l, Ba_mg_l, Be_mg_l, Ca_mg_l, Cd_mg_l, Ce_mg_l, Co_mg_l, Cr_mg_l, Cs_mg_l, Cu_mg_l, Fe_mg_l, K_mg_l, La_mg_l, Li_mg_l, Mg_mg_l, Mn_mg_l, Mo_mg_l, Na_mg_l, Ni_mg_l, Pb_mg_l, Pr_mg_l, Rb_mg_l, Sb_mg_l, Se_mg_l, Si_mg_l, Sn_mg_l, Sr_mg_l, Ti_mg_l, U_mg_l, V_mg_l, W_mg_l, Zn_mg_l
  - Notes on value representations: some concentrations use a "less than" (<) marker to indicate values below detection or reporting thresholds; some entries include explanatory notes (e.g., "n/a" for not applicable).
  - Several fields include column-specific explanations (e.g., <Cs, <Sn) to denote sub-threshold values or special markers.
- Data conventions
  - Column names follow the pattern Element_mg_l with accompanying Explanation fields in the source.
  - Some typographical inconsistencies exist in the source (e.g., Mo_l vs Mo_mg_l) but the intended unit is mg/L for all listed concentrations.
  - Acknowledges that underlying data may require transformation and careful interpretation of less-than values.

## Metadata, quality assurance, and presentation
- Each field is accompanied by an Explanation to clarify meaning (e.g., sample identifiers, preparation notes, and concentration interpretations).
- Emphasizes the need for quality assurance, data cleaning, transformation, and clear presentation in reports, charts, or dashboards.
- Highlights the importance of sharing underlying data appropriately and establishing data governance to ensure datasets meet standards and remain up to date.

## Data governance and accessibility considerations
- Public sharing of datasets can be a barrier to data usage.
- Metadata gaps or inadequate metadata can hinder verification of suitability.
- Data management challenges include ensuring up-to-date metadata, standardization, and storage/sharing practices.

## Relevance to monitoring framework aims
- Demonstrates a concrete example of measuring environmental health indicators (metal concentrations in water) to inform policy evaluation.
- Illustrates how to structure, document, and share monitoring data to enable scrutiny and future decision-making.
- Underlines the importance of metadata clarity, data quality, and governance to maximize usefulness for monitoring frameworks.

## Key challenges illustrated (as relevant to authors of monitoring frameworks)
- Lack of data or data at a usable standard.
- Limited access to data or delays in obtaining it.
- Siloed information within and between organizations.
- Barriers to using data that require public sharing of datasets.
- Keeping data up to date and maintaining metadata quality.
- Inadequate metadata hindering verification of data suitability.
- Data formats requiring effortful transformation for usability.
- Challenges in communicating complex findings clearly.
- Establishing and maintaining data governance processes for storage, sharing, and upkeep.