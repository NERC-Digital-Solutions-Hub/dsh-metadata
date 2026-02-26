# Glastir Monitoring & Evaluation Programme FIELD HANDBOOK Freshwater, Version 2013.02

- Purpose and scope
  - Standardised field methods for surveying ponds within the Glastir Monitoring & Evaluation Programme (GMEP) to assess ecological quality.
  - Data collected across 1km survey squares in Wales, with random and targeted sampling, excluding urban/seaward-dominated squares.
  - Field data fed into a central database and used to compute a pond Biological Quality assessment (PSYM).

- Sampling design and survey framework
  - Stratified sampling: random 1km squares within strata, with additional sampling targeted at Glastir priority areas.
  - Exclusion criteria: squares with >75% urban land or >90% sea excluded.
  - Pond-focused approach: identification of ponds in each square, random selection of a pond for the in-situ condition survey, and creation of a permanent record.

- Field data collection workflow and data capture
  - Primary field roles: habitat mappers identify ponds; pond surveyors perform condition assessments.
  - Core data capture forms recorded on PC tablets:
    - Pond Checklist: water chemistry, macroinvertebrate data.
    - Pond Attributes: pond characteristics and environmental information.
    - Pond Plants: macrophyte survey data.
  - Mandatory data elements: square number, pond reference, survey date; location details; photography with marker board indicating pond, square, date.
  - Boundary and mapping procedures: define outer pond boundary, walk perimeter, sketch outline, estimate area, and record inflows/outflows.
  - Pond age and permanence: record estimated age (new ponds up to ~10 years) and permanence (never, rarely, sometimes, annually).

- Water chemistry component
  - Field measurements: conductivity, pH, turbidity (visual turbidity categories).
  - Laboratory analyses (50 ml filtered samples): phosphate (PO4-P), total dissolved nitrogen (TDN), alkalinity.
  - Sampling protocol: single representative sample from typical pond area; avoid inflows; label and store samples for lab analysis.

- Macrophyte (macrophyte) survey
  - Objective: record all wetland plant species within the pond boundary and estimate abundance.
  - Abundance scale: D, A, F, O, R; total cover by submerged, floating-leaved, and emergent species; shade estimations (pond overhang and margin shading).
  - Identification: field identifications to species where possible; collect samples for uncertain taxa; rare species require confirmation with care to minimise impact.
  - Specimen handling: pressed, pickled, and/or photographed specimens; targeted species may be sent to Freshwater Habitats Trust for verification.
  - Data entry: two-part macrophyte form; two sheets allow recording of species and coverage; total cover calculations for plant groups and shade metrics.

- Macroinvertebrate survey
  - Objective: compile a comprehensive pond macroinvertebrate list within a 3-minute net sampling window plus 1 minute of visual search.
  - Habitat-based sampling: identify main pond habitats (e.g., soft sediment, submerged vegetation, inflow areas) and sample proportionally across habitats.
  - Netting protocol: 25 cm2 net, 900 µm mesh; vigorous, time-divided sampling; minimize disturbance to non-target organisms.
  - Additional search: 1 minute of surface/under objects sampling to capture missed taxa.
  - Preservation and storage: samples placed in formalin-filled bags, labeled, and stored in storage pots; prevent cross-contamination between sites.
  - Transit: clearly labeled containers and Transport Emergency (TREM) cards for hazardous materials; ensure samples are ready for laboratory analysis.

- Data handling, laboratory protocols, and analytics
  - Data entry: all survey data entered electronically into tablet-based systems; abundance estimates use a defined scale.
  - Laboratory analyses (UK CEH): PO4-P, alkalinity, TDN/TN, conducted using accredited methods and standard instruments.
  - PSYM (Predictive System for Multimetrics): a standardized ecological quality assessment combining plant and invertebrate metrics; environmental data feed PSYM predictions to benchmark current conditions against an undegraded state.
  - Quality assurance: adherence to DEFRA Joint Codes of Practice (JCoPR) to ensure scientific quality, repeatability, and auditability.

- Data structure and outputs
  - Key datasets (example tables and descriptions):
    - GMEP_POND_INVERTS_2013_16.csv: pond macroinvertebrate species list per pond, with counts; fields include square ID, year, taxa name, count, and 10km coordinates.
    - GMEP_POND_MACROPHYTES_2013_16.csv: aquatic macrophyte records within pond boundaries; includes square ID, species, category (emergent, submerged, floating, etc.), abundance, and coordinates.
    - GMEP_POND_MACROPHYTES_SUMMARY_2013_16.csv: summary metrics for macrophytes (percent cover by total vegetation, submerged, floating-leaved, emergent; percentage pond overhung; shade; PSYM and IBI-like indices).
    - GMEP_POND_ENV_SURVEY_2013_16.csv: pond environmental attributes (variable name, description, and value) linked to square, year, and coordinates.
    - GMEP_POND_CHEMISTRY_2013_16.csv: chemistry data for headwater ponds (SAMPLE_DATE, determinand, value, units, and coordinates).
  - Data standards and identifiers: use of square numbers, pond numbers, and standardized LC (Land Classification) codes; data tables include -9999 for missing data; coordinates in OSGB 1936 framework.

- Analysis and interpretation
  - PSYM-based quality categorisation (Good, Moderate, Poor, Very Poor) derived from plant and invertebrate metrics versus environmental predictions.
  - Biological quality guidance used to diagnose degradation drivers (e.g., eutrophication, metal contamination) and support management decisions.
  - The dataset supports regional comparison across years (2013–2016) and can inform pond conservation and policy planning.

- Governance, reporting, and collaborators
  - Compliance with JCoPR for methodological and data integrity; FE/CEH collaboration across GMEP staff, Freshwater Habitats Trust, and Welsh Government stakeholders.
  - Documentation and references provided for field methods, taxonomy, and analytical procedures.
  - Field teams and key personnel listed for program governance and operational continuity.

- Relevance for Data Leaders
  - Demonstrates end-to-end data pipeline: field collection, tablet-based data capture, laboratory analyses, standardized metrics (PSYM), and integrated datasets.
  - Emphasises data discoverability and interoperability through explicit data structures, metadata, and consistent identifiers (square/pond IDs, LC codes).
  - Highlights data quality assurance practices (JCoPR, standardized protocols, specimen handling, and cross-checks between field and lab data).
  - Provides a blueprint for managing complex, multi-component ecological datasets across years and regions, with explicit attention to data standards, provenance, and traceability.