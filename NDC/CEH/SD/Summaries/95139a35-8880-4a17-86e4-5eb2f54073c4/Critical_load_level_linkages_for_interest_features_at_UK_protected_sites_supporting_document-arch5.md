# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

## Purpose and scope
- Splits the assignment of critical loads/levels to designated features into three phases:
  - Phase 1: Annex I habitat features and Annex II plant species features (combined as plants are in situ within habitats).
  - Phase 2: Special Protection Area (SPA) bird features and Annex II non-plant species features (using the same method as SPA features).
  - Phase 3: A/SSSI habitat features only.
- Focuses on establishing relevant critical loads for nutrient nitrogen and acidity, linked to designated features, to assess potential impacts of atmospheric deposition.

## Methodology and standards

- Critical loads for nutrient nitrogen
  - Based on UNECE Long-Range Transboundary Air Pollution framework.
  - Empirical loads assigned to habitat classes in the European Nature Information System (EUNIS) to ensure harmonised habitat terminology.
  - Habitat correspondence tables map EUNIS classes to Annex I features, A/SSSI, or Annex II/SPA features.
  - Sensitivity judgements determine which features are affected by eutrophication; most features are assessed, with transparency for those deemed not sensitive.
  - Noordwijkerhout Expert Workshop (2010) values used; justifications for matches are recorded.

- Critical loads for acidity
  - Based on six Broad Habitats (e.g., acid grassland, calcareous grassland, etc.).
  - JNCC/NBN correspondences link Broad Habitats to Annex I/A/SSSI or Annex II/SPA features.
  - Designated features are assessed for sensitivity to acidification; coastal features often buffered and less sensitive.
  - Matches between Annex I/II features and Broad Habitats are documented with justifications and described impacts of exceedance.

- Exceptions and indirect assessments
  - When Annex I features do not map to a suitable EUNIS class, further science reviews may be required.
  - For SPA and Annex II non-plant species, direct nitrogen or acidity loads are not always applicable; instead, habitat impacts on breeding/feeding/roosting are considered.
  - Where habitats are insensitive to acidity or eutrophication, no critical loads are assigned.

- Critical levels
  - Not habitat-specific; set for broad vegetation types with separate considerations for ammonia (e.g., lichens and bryophytes).
  - Examples include:
    - NOx: 30 µg/m3 (annual mean)
    - SO2: 20 µg/m3 (annual mean) for forests/natural vegetation; 10 µg/m3 for sensitive lichens
    - Ammonia: 1 µg/m3 (lichens/bryophytes); 3 µg/m3 (other vegetation; 2–4 µg/m3 uncertainty)
  - Linkages made to habitats and species where possible using National Vegetation Classifications (NVC) and site knowledge.
  - Receptors include NOx, SO2, and ammonia with guidance to use habitat-species associations to determine site-relevant levels.

## Data model and structure

- Data products
  - Three CSV datasets:
    - APIS_SAC_feature_critical_load_level_linkages.csv
    - APIS_SPA_feature_critical_load_level_linkages.csv
    - APIS_SSI_feature_critical_load_level_linkages.csv
- Core fields and purpose
  - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME: codes and names for features
  - INTERESTTYPECODE, INTERESTTYPE: feature type (e.g., habitat, bird)
  - NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADB HABITAT
  - DEPTYPE: deposition type (F M G)
  - SENSITIVENDEP: sensitivity to nutrient nitrogen
  - NCLCODE, NCLCLASS: empirical critical load classes and descriptions
  - JUSTIFICATIONALLOCATIONNCL: justification for nitrogen load linkage
  - EUNIS: EUNIS classification used for critical loads
  - CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE: empirical critical loads for nutrient nitrogen
  - NTEXT: additional information
  - SENSITIVEACIDITY, ACCODE, ACIDITYCLASS, JUSTIFYSPECIESSENSITIVITYA: acidity-related linkage fields
  - AMMONIA_CL_VALUE, AMMONIA_CL_TEXT: ammonia-related critical levels
  - NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT: NO2-related thresholds
  - SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT: SO2-related thresholds
  - SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN: species sensitivity to nitrogen
  - SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIFYSPECIESSENSITIVITYA: species sensitivity to acidity
  - SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NH3_TEXT: ammonia sensitivity
  - SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_NOX_TEXT: NOx sensitivity
  - SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, SPECIES_SENSITIVE_SO2_TEXT: SO2 sensitivity
- Data provenance and transparency
  - Emphasises transparent justification of allocations and the use of standard references (EUNIS, NVC, APIS, CLRTAP, WHO).
  - Documentation of linkages and rationale to support reproducibility and auditability.

## Governance, quality, and update considerations

- Transparency and traceability
  - Justifications for each linkage are recorded to support transparency and auditability.
  - Documentation ties to established classifications (EUNIS, NVC) and recognized expert knowledge.
- Data freshness and maintenance
  - The methodology anticipates updates and ongoing alignment with current science; however, explicit update procedures are not detailed in the excerpt.
- Quality control notes
  - Quality control fields are largely NA in this dataset, indicating reliance on expert judgement and standard classifications, with room for future QC steps.

## Practical implications for Data Stewards

- Ensuring standards compliance
  - Dataset uses established European standards (EUNIS, APIS, NBN/JNCC, Noordwijkerhout 2010) for consistency and interoperability.
- Metadata and discoverability
  - Rich metadata fields and structured linkage tables facilitate discovery and reuse by researchers and decision-makers evaluating deposition impacts on designated features.
- Interoperability and interoperability challenges
  - Complex multi-layer associations (habitats, species, broad habitats, nitrogen vs. acidity) require careful governance of metadata, versioning, and documentation.
- Resource and access considerations
  - Data references include an APIS resource locator for extended context and methods.

## Key references and resources

- Noordwijkerhout Expert Workshop (UNECE 2010) for critical load values
- European Nature Information System (EUNIS) for habitat terminology
- APIS (Automated Processing of Information on Site) for feature linkages
- NBN/JNCC correspondences for Broad Habitats
- WHO, CLRTAP, and AQ Directive as sources for critical level values
- National Vegetation Classifications (NVC) and site knowledge for linkages