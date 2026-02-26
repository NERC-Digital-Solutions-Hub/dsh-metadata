# Glastir Monitoring & Evaluation Programme FIELD HANDBOOK Freshwater , Version 2013.02

- Purpose: Guide for field-based freshwater surveys under the Glastir Monitoring & Evaluation Programme (GMEP), detailing survey design, data collection, laboratory analyses, data storage, and quality assurance to produce standardized data on ponds, macrophytes, invertebrates, and water chemistry.

## Overview of sampling framework and objectives
- Stratified sampling design: 1 km squares across Wales with proportional sampling within strata; half of squares focus on Glastir priority areas.
- Pond-focused fieldwork within each square, with random selection of a “survey pond” for condition assessment.
- Definitions: pond is a standing water body 25 m2 to 2 ha, usually holding water for at least four months; boundary and outer area considerations (maximum winter water level) are used for mapping and area calculations.
- Aims include documenting pond condition, biological quality, and habitat features through standardized survey methods and data capture.

## Data collection workflow and sequence of tasks
- Pre-survey: field habitat mappers identify ponds and record basic attributes; random selection of a survey pond within each square.
- On-site roles: two freshwater surveyors per pond (Surveyor A and Surveyor B) with distinct tasks (e.g., water sampling, pond attribute recording, plant and macroinvertebrate surveys).
- Data capture on tablets: forms used include Pond Checklist (water chemistry and macroinvertebrate data), Pond Attributes (pond characteristics and environment), Pond Plants (macrophyte surveys), and Macrophyte Survey data.
- Health and safety: risk assessment for sampling; high-risk conditions halt sampling; safety gear recommended for wading and testing.
- Data submission cadence: samples, data, and plant/macroinvertebrate specimens dispatched monthly to Freshwater Habitats Trust (formerly Pond Conservation).

## Data capture: forms, parameters, and procedures
- Pond Checklist: records water chemistry (pH, conductivity, turbidity in the field; alkalinity, SRP, TON from filtered samples), pond attributes, and macroinvertebrate data; requires pond square and pond identifiers, date, and complete field notes.
- Pond Attributes: collects pond location, boundary, perimeter features, inflows/outflows, sketch of pond, photographs, and boundary delineation; ensures correct attribution to site.
- Macrophyte (Pond Plants) survey: identifies all wetland plants within the pond boundary; counts abundance using DAFOR-like categories; records submerged, floating, and emergent species; notes shade and overhang.
- Macrophyte data entry: two sheets for plant data; taxonomic nomenclature aligned to standard flora references; rare species require confirmation and potential specimen submission; sampling methods include walking/wading and grapnel sampling for submerged plants.
- Macroinvertebrate survey: 3-minute net sampling across multiple habitats (divided equally among habitats, with optional sub-sampling for large sites) plus an additional 1-minute targeted search (surface, under logs) to supplement species lists; samples preserved in formalin and labeled with square, pond, date; 25 cm2 net with 900 µm mesh; avoidance of silt-rich or overly large plant accumulations.
- Chemistry sampling: field measurements (pH, conductivity, turbidity) and laboratory analyses (PO4-P, TDN/TN, alkalinity) using filtered samples; use of 50 ml filtered aliquots for specific determinands; samples labeled with project, square, pond, date details; transfer and packaging guidelines for laboratory analysis.

## Data structure, storage, and electronic recording
- Electronic data capture: data entered directly into tablet PCs; plant and invertebrate data organized into dedicated CSV tables.
- Data tables (examples):
  - GMEP_POND_INVERTS_2013_16.csv: pond macroinvertebrate species lists and counts by square; includes YEAR, TAXA_NAME, COUNT, coordinates, and Land Classification (LC).
  - GMEP_POND_MACROPHYTES_2013_16.csv: pond macrophyte records by species, category (emergent, submerged, floating), abundance, coordinates.
  - GMEP_POND_MACROPHYTES_SUMMARY_2013_16.csv: summary metrics such as percent cover by vegetation category, pond overhang, shade, and Biotic Integrity Index (IBI), PSYM scores, and PSYM category.
  - GMEP_POND_ENV_SURVEY_2013_16.csv: environmental attributes by variable (e.g., field descriptions, values) for each pond.
  - GMEP_POND_CHEMISTRY_2013_16.csv: chemistry measurements (conductivity, pH, PO4-P, TDN/TN, alkalinity) with sampling metadata.
- Data fields and units: standardized fields include SQ_ID, pond number, year, easting/northing (10 km resolution), LC (ITE land classification), and multiple measurement units (µS for conductivity, mg/l CaCO3 for alkalinity, etc.).
- Abundance and cover scales: abundance for invertebrates and plants use standardized categories (Dominant, Abundant, Frequent, Occasional, Rare) and plant cover scales (D, A, F, O, R).
- PSYM and IBI: biological quality assessed via PSYM (Predictive System for Multimetrics) with a final PSYM category (good/moderate/poor/very poor); IBI score used within PSYM framework to gauge aquatic community health.

## Laboratory analyses and quality assurance
- Chemistry analyses performed at UK Centre for Ecology and Hydrology (UKCEH), Lancaster using accredited methods (e.g., Seal Analytical AQ2 for PO4-P; Skalar Formacs CA16 for TDN/TN; alkalinity via titration).
- QA and governance: adherence to DEFRA Joint Codes of Practice (JCoPR) for quality and reproducibility; PSYM methodology used for integrated quality assessment; data handling and reporting follow field and lab protocols to ensure traceability.

## Data provenance, governance, and sharing
- Data flow: field data and samples collected in the field, entered via tablet PCs, laboratory analyses performed at UKCEH, and results forwarded to project teams (Freshwater Habitats Trust) for archival and analysis.
- Documentation and references: extensive methodological references (Glasitir field handbook, PSYM manual, environmental classification schemes) to support data interpretation and comparability across surveys.
- Data accessibility and structure: dataset schemas are explicit (CSV table structures, field names, and descriptions) to facilitate data integration, querying, and reproducible analysis.

## Key challenges and considerations for data support
- Understanding the “ask”: translating survey design and field methods into usable data products and ensuring alignment with end-user needs.
- Handling patchy/wide-form data: integrating data from multiple forms, habitats, and timepoints into coherent datasets.
- Data quality and consistency: standardized data capture, calibration of field instruments, and consistent taxonomic identification across survey teams.
- Data interoperability: aligning field data with laboratory results, GIS coordinates, and the PSYM/IBI quality metrics for robust ecological interpretation.
- Data dissemination: ensuring outputs are shareable, reusable, and capable of informing policy and management decisions.

## Summary for data-focused readers
- The document provides a comprehensive, standardized workflow for collecting pond, macrophyte, invertebrate, and chemistry data in Wales, with explicit forms, sampling protocols, and data structures to support robust ecological assessment and reporting.
- It emphasizes careful data capture, clear metadata, rigorous QA, and the use of established ecological indices (PSYM, IBI) to translate field observations into meaningful quality assessments.
- For data support roles, the key opportunities lie in integrating these diverse data streams into cohesive data products, ensuring metadata completeness, and facilitating end-user access to self-serve analyses and interpretable summaries.