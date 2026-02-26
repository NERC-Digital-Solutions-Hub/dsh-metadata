# Procedure for enumeration, isolation, preservation and identification of E. coli isolates NERC project NE/N019555/1

## Purpose
- Describes the method for enumerating, isolating, preserving, and identifying E. coli isolates that are resistant to third-generation cephalosporins or carbapenems from various sample types collected for the study.

## Data generated
- Counts of E. coli colonies on selective media (ESBL, KPC, TBX, MacConkey with antibiotics) from different matrices (fecal, soil, solid waste, water, wastewater).
- Isolate metadata (sample ID, source type, date, plate ID, media type, antibiotic supplement used, dilution factors, incubation conditions).
- Subcultures of presumptive E. coli onto MacConkey with antibiotics for confirmation.
- Preservation data: culture sweeps stored in TSB with 30% glycerol at -80°C.
- Confirmation and identification results: API 20E results, oxidase test results, and final organism identification steps.
- Backup isolates if initial API 20E confirmation is negative.

## Workflow and data flow
- Prepare buffers and media:
  - 10× PBS and 1× PBS solutions.
  - CHROMagar ESBL and CHROMagar KPC media with appropriate supplements.
  - TBX and MacConkey media with cefotaxime or meropenem as required.
- Sample processing by type:
  - For fecal/soil/solid waste:
    - Suspend 1–5 g in PBS, vortex, settle, and plate dilutions on ESBL, KPC, and TBX plates.
    - Incubate at 37°C for 18–24 h; identify typical E. coli colonies.
    - Subculture at least 3 colonies from ESBL to MacConkey + cefotaxime and from KPC to MacConkey + meropenem.
    - Store a culture sweep in TSB with 30% glycerol at -80°C.
  - For supply water:
    - Filter through 0.22 μm membranes onto mTEC plates (one with cefotaxime, one with meropenem).
    - Incubate with a two-stage protocol (2 h at 37°C, then 18 h at 44°C); count presumptive E. coli colonies.
    - Subculture at least three colonies onto MacConkey + the same antibiotic.
    - Store a culture sweep at -80°C in glycerol.
  - For wastewater:
    - Use 9-fold dilution, filter, and process as for water samples on mTEC plates with antibiotics; follow same incubation and subculture steps; preserve isolates.
- Confirmation and identification:
  - Confirm E. coli with API 20E on one isolate per sample; if the initial result is negative, test a second isolate from the same sample.
  - Perform API 20E procedure (oxidase test, inoculation, reagent handling, incubation at 36 ± 2°C for 18–24 h) and interpret using the standard reading table.
  - If API 20E results are unidentifiable, perform additional tests (nitrate reduction with NIT reagents, growth on MacConkey, etc.) as described in the procedure.
  - Use API-20E online or equivalent identification tools to finalize organism identification.
- Documentation and traceability:
  - Record all steps, results, and interpretations; maintain lot numbers for media and reagents; note any deviations or repeat tests.

## Metadata, documentation and labeling
- Labeling requirements:
  - Plates labeled with agar type, date, and sample ID.
- Essential metadata to capture:
  - Sample type (fecal, soil, waste, water), source, collection date, sample ID, plate IDs, media type, antibiotic concentrations, dilution factors, incubation conditions, colony counts, selected isolates, API 20E results, oxidase results, final identification, and storage details (isolate ID, storage medium, glycerol concentration, storage location).

## Preservation, storage and data retention
- Preservation method:
  - Culture sweeps suspended in tryptic soy broth with 30% glycerol and stored at -80°C in cryovials.
- Storage formats and organization:
  - Maintain cryovials with unique identifiers; track storage location and lot details; preserve working and backup isolates as appropriate.
- Data retention:
  - Maintain records linking sample IDs, isolate IDs, plate IDs, and API results to enable traceability and future genetic analyses.

## Data quality and validation
- Confirmation strategy:
  - One E. coli isolate per sample is tested with API 20E; if negative, a second isolate is tested to confirm presence.
- QA considerations:
  - Adhere to specified incubation times and temperatures; prepare supplements fresh and use the same day; follow labeling and storage directions to avoid mix-ups.
- Handling anomalous results:
  - If identification is unclear, perform additional tests (nitrate reduction, MacConkey growth patterns) and re-assess with API tools.

## Data governance, access and sharing considerations
- Provenance and lineage:
  - Maintain complete provenance from sample collection through processing, isolation, confirmation, and storage; document media lots, reagent preparations, and any deviations.
- Data management:
  - Ensure standardized data entry templates for all metadata fields; implement versioning for API results and identification outcomes.
- Access and retention:
  - Apply appropriate access controls for stored isolates and associated data; ensure long-term storage plans are in place for glycerol stocks and sequencing/dimensional data if generated.

## Challenges and considerations for data stewards
- Heterogeneous sample types and complex workflows may create variable data richness; ensure consistent metadata capture across matrices.
- Inter-lab and multi-site formatting differences; establish standard naming conventions and data schemas.
- Large volumes of culture and storage data require robust inventory management and tracking systems.
- Potential for incomplete or negative API confirmation; ensure processes accommodate secondary testing and clear documentation of decision points.

## Key data elements to capture for governance
- Sample metadata: sample ID, source type, collection date, weight/volume, matrix.
- Processing metadata: buffer volumes, dilutions, media types and lots, supplement preparations, incubation conditions.
- Plate and culture data: plate IDs, media used, antibiotic supplements, colony counts, colony morphology notes.
- Isolate metadata: isolate ID, source plate, subculture results, storage details (location, glycerol percentage, date).
- Confirmation data: API 20E results, oxidase test results, supplementary test results, final organism identification.
- Provenance links: links between sample, plate, isolate, and storage records.