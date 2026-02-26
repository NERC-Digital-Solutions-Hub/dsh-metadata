# TREE_Northumbria_ICPMS_Woodmice_mg_per_tissue_FM_Concentration

- Overview
  - A dataset documenting concentrations of multiple trace elements in total wood mouse tissue (milligrams per tissue fresh mass) from Northumbria.
  - Intended to support environmental health monitoring to scrutinise policy, inform decisions, and guide future actions.

- Data structure and content
  - Biological identifiers: Latin_Species_Name, Common_Species_Name.
  - Sampling context: Site, Date_Sample_Collected, CEH_Sample_Codes, CEH_Sample_Description, Tissue sampled.
  - Concentration measurements: a wide range of elements (I, Li, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Tl, Pb, U) with units mg_per_tissue_FM.
  - Data format notes: some measurements use a “less than” marker (<) to indicate detection limits; several tissues show "No data collected" or specific missing data.
  - Specific data gaps noted: No data for Hind Leg Bone and woodmice 8 liver; no data collected for woodmice thyroid for multiple elements; some tissues lack data for certain metals.

- Notable data gaps and limitations
  - Incomplete tissue coverage for thyroid and certain bones/livers.
  - Missing data for some animals (e.g., woodmice 8 liver) and some tissue types.
  - Occurrence of less-than values requiring appropriate handling in analyses.

- Data quality and governance considerations
  - Rich metadata (species, site, date, sample codes, tissue) supports traceability and provenance.
  - Presence of detection-limit indicators (<) requires careful statistical treatment.
  - Gaps in data highlight the need for consistent sampling, complete metadata, and transparent reporting to support cross-site comparisons and policy evaluation.
  - Sharing underlying data and metadata is implied as best practice but may encounter barriers if datasets are incomplete or sensitive.

- Relevance to monitoring framework aims
  - Enables assessment of wildlife exposure to a broad suite of metals, informing environmental health risk assessments and policy decisions.
  - Supports decision-making with structured data on biological concentration by tissue and site, enabling trend analysis and gap identification.
  - Highlights the importance of data governance (quality assurance, data cleaning, transformation, and clear presentation) to effectively communicate complex findings.