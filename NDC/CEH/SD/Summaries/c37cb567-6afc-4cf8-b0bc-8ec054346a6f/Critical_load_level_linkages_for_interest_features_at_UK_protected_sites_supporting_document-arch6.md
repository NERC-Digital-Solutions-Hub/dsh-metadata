# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

- Objective: Attribute appropriate critical loads and critical levels to designated features of SACs, SPAs, and A/SSSIs, using a structured, transparent methodology that links habitat or species features to nitrogen and acidity stress indicators.

- Phases of assignment:
  - Phase 1: Annex I habitat features and Annex II plant species features (Avec plant species treated as in situ components of habitat).
  - Phase 2: SPA bird features and Annex II non-plant species features (assessed similarly to SPA features; indirect linkage via habitat).
  - Phase 3: A/SSSI habitat features only.

- Critical loads for nutrient nitrogen:
  - Based on UNECE Long-Range Transboundary Air Pollution guidance; empirical, from experiments and gradient studies.
  - Assigned to habitat classes in EUNIS to ensure consistency across Europe.
  - Habitat correspondence tables determine links between EUNIS classes and Annex I/A/SSSI/SPA interest features.
  - Sensitivity and impact judgments focus on eutrophication effects; most habitats are assessed, with some coastal or highly buffered features deemed not sensitive.
  - Exceptions: non-matches between Annex I features and suitable EUNIS classes may require further literature review or site-level assessment.

- Critical loads for acidity:
  - Based on soil/habitat types across six Broad Habitats (e.g., acid grassland, calcareous grassland, etc.), using NBN/JNCC mappings to assign Broad Habitats to features.
  - Designated features assessed for acidity sensitivity; coastal features with high buffering may be not sensitive.
  - Justifications documented for transparency; applicability to Annex I, Annex II/SPA, and A/SSSI features.
  - Habitat-to-load linkages established for transparency; where applicable, features are matched to corresponding Broad Habitats.

- Exceptions and direct-bird/non-plant considerations:
  - Direct nitrogen or acidity loads to bird features are generally unsuitable; linkages rely on habitat condition affecting bird viability (breeding, feeding, roosting).
  - Where habitats are deemed insensitive to acidity or eutrophication, no critical load is assigned.

- Critical levels (not habitat-specific):
  - Set to cover broad vegetation types (e.g., forests, arable, semi-natural) with some receptor-specific notes (e.g., ammonia for lichens and bryophytes).
  - Example values and references:
    - NOx: annual mean, receptors include all; 30 µg/m3 (WHO, CLRTAP, AQ Directive)
    - SO2: annual mean, receptors include forests and natural vegetation; 20 µg/m3; and sensitive lichens; 10 µg/m3
    - Ammonia: annual mean, receptors include lichens/bryophytes and other vegetation; 1 µg/m3 (lichens/bryophytes), 3 µg/m3 (other vegetation; 2–4 µg/m3 uncertainty)
  - Linkages created between habitats and species where possible to provide site-relevant critical levels for ammonia, NO2, and SO2, supported by National Vegetation Classifications (NVC) and site knowledge.

- Data sources and provenance:
  - Primary sources and frameworks include APIS, EUNIS classifications, Noordwijkerhout Expert Workshop (UNECE 2010), NBN/JNCC habitat mappings, National Vegetation Classifications (NVC), and WHO/CLRTAP references.
  - Data are organized to maintain transparency on justifications, reliability, and potential exceedance impacts.

- Data outputs and structure:
  - Three primary datasets (CSV) for linkage between features and critical loads/levels:
    - APIS_SAC_feature_critical_load_level_linkages.csv
    - APIS_SPA_feature_critical_load_level_linkages.csv
    - APIS_SSSI_feature_critical_load_level_linkages.csv
  - Core fields (representative examples across datasets):
    - INTERESTCODE, INTERESTNAME, INTERESTLAYNAME, INTERESTTYPECODE, INTERESTTYPE
    - NVC_CODE, APIS_NAME, BROAD_HABITATCODE, BROADHABITAT
    - DEPTYPE (deposition type: F, M, G)
    - SENSITIVENDEP (is feature sensitive to nutrient nitrogen)
    - NCLCODE, NCLCLASS (critical load classification)
    - JUSTIFICATIONALLOCATIONNCL (justification for N-load linkage)
    - EUNIS (EUNIS classification used for critical loads)
    - CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE (empirical nutrient nitrogen CRLs)
    - NTEXT (additional information)
    - SENSITIVEACIDITY (is feature sensitive to acidity)
    - ACCODE, ACIDITYCLASS (acidity CRL linkage)
    - JUSTIFICATIONA (justification for acidity linkage)
    - ATEXT (additional information)
    - BRYOPHYTES, LICHENS (species interest indicators)
    - AMMONIA_CL_VALUE, AMMONIA_CL_TEXT (ammonia critical level and notes)
    - NITROGEN_DIOXIDE_CL_VALUE, NITROGEN_DIOXIDE_CL_TEXT
    - SULPHUR_DIOXIDE_CL_VALUE, SULPHUR_DIOXIDE_CL_TEXT
    - SPECIESSENSITIVEN, SPECIESSENSITIVITYN, JUSTIFYSPECIESSENSITIVITYN
    - SPECIESSENSITIVEA, SPECIESSENSITIVITYA, JUSTIFYSPECIESSENSITIVITYA
    - SPECIES_SENSITIVE_NH3, JUSTIF_SPECIES_SENSITIVE_NH3, SPECIES_SENSITIVE_NH3_TEXT
    - SPECIES_SENSITIVE_NOX, JUSTIF_SPECIES_SENSITIVE_NOX, SPECIES_SENSITIVE_NOX_TEXT
    - SPECIES_SENSITIVE_SO2, JUSTIF_SPECIES_SENSITIVE_SO2, SPECIES_SENSITIVE_SO2_TEXT
    - Additional notes on species sensitivity fields (NH3, NOX, NOX, SO2)
  - Structure is designed to support site-specific application and casework (case-by-case justification, reconciliation with NVC and APIS naming).

- Data access and references:
  - Resource locator for data usage: http://www.apis.ac.uk/srcl
  - Fieldwork, calibration, data units, and QA notes are largely not applicable (NA) for this dataset.
  - Documentation includes detailed field definitions and the rationale behind linkage decisions and sensitivity judgments.

- Practical use for data support:
  - Enables self-serve exploration of how designated features relate to nitrogen and acidity stress via structured, linked datasets.
  - Provides transparent, auditable justifications for each critical load/level assignment, supporting policy work, conservation planning, and reporting.
  - Supports potential site-by-site assessments and updates as new science or classifications become available.