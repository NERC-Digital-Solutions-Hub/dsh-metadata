# Supporting documentation for 17-Transfer_Parameter_Vegetal_Stable.csv

## Purpose and scope
- Metadata and field definitions for the 17-Transfer_Parameter_Vegetal_Stable.csv dataset.
- Records transfer factor values (Fv) for stable elements in vegetal samples (olive oil and wine context), including associated uncertainties, detection limits, and sample metadata.
- Data supports analysis of how elements transfer from plant material into consumables, with end-user tools likely to involve dashboards and self-serve analyses.

## Data structure and key fields
- Core identifiers:
  - Sample_Code: unique sample identifier
  - Sample_Type: general description of the sample
  - Location: collection site name
  - Sample_Description: portion of plant analysed (e.g., part of the plant)
  - Collection_Date: date of sample collection (formatted as dd-mm-yyyy)
- Transfer factor fields (Fv) and related metadata for each element:
  - Cs_Fv; Unc_Cs_Fv; Detection_Limit_Cs_Fv
  - Sr_Fv; Unc_Sr_Fv; Detection_Limit_Sr_Fv
  - K_Fv; Unc_K_Fv; Detection_Limit_K_Fv
  - Na_Fv; Unc_Na_Fv; Detection_Limit_Na_Fv
  - Ca_Fv; Unc_Ca_Fv; Detection_Limit_Ca_Fv
  - Mg_Fv; Unc_Mg_Fv; Detection_Limit_Mg_Fv
  - P_Fv; Unc_P_Fv; Detection_Limit_P_Fv (note: multiple subfields indicated as 1, 2, 3 in the documentation)
  - Pb_Fv; Unc_Pb_Fv; Detection_Limit_Pb_Fv
  - U_Fv; Unc_U_Fv; Detection_Limit_U_Fv
  - Th_Fv; Unc_Th_Fv; Detection_Limit_Th_Fv
- Units:
  - Fv fields are described as Unitless or kg dry matter per L for olive oil and wine; some entries explicitly reference wine variants.
- Data completeness and limits:
  - “Where blank, then below detection limit” guidance for many fields.
  - Some entries include notes about detection limits and measurement uncertainty.

## Data quality and consistency considerations
- Documentation quality:
  - Field explanations contain inconsistencies/typos (e.g., fragmented phrases, mixed unit notes) that affect clarity.
  - Some fields mix contextual qualifiers (e.g., “wine” vs general unit descriptions) which may require harmonization.
- Unit and formatting consistency:
  - Inconsistent unit labeling across fields; need normalization to a single standard.
- Handling multi-part fields:
  - P_Fv, and similarly named fields, show multiple subfields (1, 2, 3) that should be clearly mapped to specific contexts.
- Data cleaning recommendations:
  - Normalize all Fv-related values to a single unit scheme.
  - Standardize date format to ISO (YYYY-MM-DD) for ingestion and downstream processing.
  - Resolve and expand multi-part fields to explicit, consistently named columns.
  - Treat blank values as below detection limit, and consider a separate indicator flag for below-detection entries if needed.
  - Validate detected values against detection limits and flag anomalies.

## End-user guidance and potential data products
- How to use:
  - Filter by Sample_Type and Location to compare transfer factors across contexts (e.g., plant parts, olive oil vs wine).
  - Compare Fv values across elements, considering Unc_Fv to assess uncertainty.
  - Use Detection_Limit fields to distinguish true non-detections from low-level detections in analyses.
- Potential data products:
  - Dashboards displaying Fv by element, sample type, and location with error bars for uncertainties.
  - Pivot tables summarizing mean/median Fv by element and sample type.
  - Reports highlighting samples with Fv near or below detection limits, and those with high uncertainty.

## Practical notes for data management
- Provenance and governance:
  - Dataset documents transfer factors for stable elements in vegetal samples (olive oil and wine context).
- Data integration:
  - When merging with other datasets, ensure consistent column order and naming; align unit conventions before join.
- Publication considerations:
  - Clearly document how below-detection-limit values were treated in any results or visualizations.