# Assigning Relevant Critical Loads/Levels to designated features of protected nature conservation sites

- Purpose and scope
  - Defines a methodology to assign relevant critical loads and critical levels to designated features of protected nature conservation sites.
  - Features include Annex I habitat features, Annex II plant species features (combined as in situ), SPA bird features, Annex II non-plant species features, and England-only SSSI habitat features.
  - Uses empirical evidence and established frameworks (UNECE, EUNIS, NVC) to ensure consistency across Europe and site-specific applicability.
  - Aims to support understanding of how atmospheric deposition (nitrogen, acidity, ammonia, NOx, SO2) affects habitats and dependent species, informing management and policy decisions.

- Phases of assignment
  - Phase 1: Annex I habitat features and Annex II plant species features (in situ; plant species treated as part of habitat).
  - Phase 2: SPA bird features and Annex II non-plant species features (same method as SPA features; indirect linkage via habitat).
  - Phase 3: SSSI habitat features (England only).

- Critical loads for nutrient nitrogen
  - Based on UNECE Long-Range Transboundary Air Pollution framework.
  - Empirical critical loads assigned to habitat classes via EUNIS to ensure consistent habitat terminology.
  - Habitat correspondence tables link EUNIS classes to A/SSSI features and Annex II/SPA features.
  - Sensitivity assessments determine how eutrophication from atmospheric deposition affects features; most habitats are sensitive, with some coastal or highly buffered features less so.
  - Justifications recorded for transparency; uses Noordwijkerhout (2010) values for reliability and impact assessment.

- Critical loads for acidity
  - Based on soil and habitat types across six Broad Habitats (e.g., acid grassland, calcareous grassland, dwarf shrub heath, bogs, montane, unmanaged woodlands).
  - NBN/JNCC habitat correspondence tables map Broad Habitats to Annex I/A/SSSI and Annex II/SPA features.
  - Expert judgement determines sensitivity to acidification; coastal features with high buffering may be not sensitive.
  - Matching of Annex I/IH and Annex II/SPA features to appropriate Broad Habitats; justification and potential impacts documented.

- Exceptions
  - Some Annex I features may not match a suitable EUNIS class; may require additional investigation or site-by-site assessment.
  - Non-matches are indicated; in some cases, no straightforward critical load is assigned and further work is suggested.

- Assigning critical loads for SPA features and Annex II non-plant species
  - Direct nitrogen or acidity deposition effects on bird/species are rare; instead, habitat integrity informs potential impacts on birds or non-plant species.
  - A stepwise, expert-driven approach assesses:
    - Relevant broad habitat for the species (breeding, feeding, roosting).
    - Habitat sensitivity to eutrophication or acidification.
    - Potential impacts on the species’ viability.
    - If negative impacts are likely, assign the most relevant nutrient nitrogen or acidity critical load values based on the habitat.
  - Positive and negative eutrophication effects are acknowledged where evidence exists.
  - If the habitat is deemed insensitive, no critical load is assigned.

- Critical levels
  - Not habitat-specific but applied to broad vegetation types; includes specific receptor considerations (lichens, bryophytes, other vegetation) for NOx, ammonia, and SO2.
  - Time period: annual mean; receptor and corresponding critical level values:
    - NOx: 30 µg/m3
    - SO2: various values (e.g., 20 µg/m3 for forests/natural vegetation; 10 µg/m3 for sensitive lichens)
    - Ammonia: 1 µg/m3 for lichens/bryophytes; 3 µg/m3 for other vegetation (range 2–4 µg/m3)
  - Linkages are made to habitat types using National Vegetation Classification (NVC) and site knowledge to provide site-relevant critical levels for ammonia, NOx, and SO2.

- Linkages and data structure
  - Linkages to APIS (Atmospheric Information System) used to organize data and provide standardized references.
  - Resources: APIS system and Noordwijkerhout framework; fieldwork/lab instrumentation not specified; data structure and metadata documented.
  - Datasets (three CSV files) capturing critical loads/levels for designated features across SAC, SPA, and England-only SSSI:
    - APIS_SAC_sites_feature_critical_load_linkages.csv
    - APIS_SPA_sites_feature_critical_load_linkages.csv
    - APIS_SSSI_sites_feature_critical_load_linkages.csv
  - Key fields include: SITECODE, SITENAME, COUNTRY, DESIGNATION, INTERESTCODE/NAME, INTERESTTYPE, NVC_CODE/BROAD_HABITAT, SENSITIVENDEP, NCLCODE/NCLCLASS, JUSTIFICATIONALLOCATIONNCL, EUNIS, CLMIN_NUTN, CLMAX_NUTN, RECOMMENDED_VALUE, NTEXT, AMMONIA_CL_VALUE/TEXT, NITROGEN_DIOXIDE_CL_VALUE/TEXT, SULPHUR_DIOXIDE_CL_VALUE/TEXT, SPECIES_SENSITIVITY flags and justifications.
  - Additional columns capture justification, sensitivity cues for ammonia, NOx, and SO2, and related notes.

- Data resources and quality
  - Resource locator provided: http://www.apis.ac.uk/srcl
  - Data capture relies on expert judgement and published frameworks; explicit fieldwork instrumentation or calibration details are not specified.
  - Quality control and extensive documentation accompany the data, with transparency on justifications and cross-checks by statutory conservation bodies and CEH where applicable.

- Practical implications for data leaders
  - Establishes a structured, repeatable approach to quantify and map pollutant impacts on protected features, enabling prioritization and targeted conservation actions.
  - Demonstrates integration of multiple data standards (EUNIS, NVC, APIS) to harmonize habitat terminology and facilitate cross-border applicability.
  - Highlights data governance needs: provenance of expert judgments, documentation of justifications, handling of exceptions, and updating mechanisms as scientific understanding evolves.
  - Provides ready-to-use datasets to inform risk assessment, policy development, and site-specific management plans, with clear linkage between features, habitats, and pollutant thresholds.