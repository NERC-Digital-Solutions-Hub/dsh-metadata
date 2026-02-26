# MODULE 2: SURVEY OF FRESHWATER HABITATS

- Purpose: A field handbook detailing standardized methods to survey freshwater habitats for the Countryside Survey 2000, producing map-based data products and datasets for analysis and policy support.

- GIS relevance:
  - Spatial framework built around 1 x 1 km squares with time-series sampling to monitor changes.
  - Data designed for integration with GIS: explicit site codes, grid references, and map-backed sampling plans.
  - Multiple nested data layers: macroinvertebrate data (RIVPACS), River Habitat Survey (RHS), diatoms, chironomid pupal exuviae, chemical data, and macrophyte transects.
  - Linkages to land use and habitat context via 50 m and 500 m riparian buffers.

- Spatial coverage and sampling framework:
  - Repeated sampling across CS1990 CS2000 time series; CS2000 expanded sample with 568 squares, including 30 new sites and up to 568 total squares; 435 squares to be surveyed in CS2000.
  - Sampling nests include:
    - Repeat 1990 squares (up to 508 previously sampled) and new/additional sites (e.g., MR reserve and MRn recipes for diatom/pupal sampling).
    - Replacement sites for Isle of Man squares; new sites prioritized to improve country-level estimates.
  - Each square mapped with 1:10,000 maps; macroinvertebrate sampling point labeled M; reserve or alternate sites labeled MR/MRn as needed.
  - Field surveys integrate with national grid references (NGR) and land class designations to align with GIS workflows.

- Data collection framework and data model:
  - Four primary field components (plus Ecofact macrophyte transects):
    - Macroinvertebrate sampling (RIVPACS-compatible)
    - River Habitat Survey (RHS) including alder disease and chemical surveys
    - Diatom sampling
    - Chironomid pupal exuviae sampling
  - Additional Ecofact macrophyte transects (up to five 10 m x 2 m transects per square).
  - Each sampling event is tied to a 500 m RHS reach centered on the macroinvertebrate sampling point (M or MRn).
  - Spatial data capture includes:
    - Precise 1:10,000 and 1:50,000 mapping context
    - Upper/lower RHS limits (U/L) on field maps
    - Diatom site (D) and chironomid exuviae site (C)
    - Environmental data fields (width, depth, substratum, velocity, etc.)
  - Data recorded on field forms and later integrated into GIS-ready databases; time-stamped sample dates and precise site identifiers are required.

- Field procedures and data capture workflow:
  - Planning and permissions:
    - Obtain landowner permissions; advance letters and on-site confirmations.
    - Document access issues and coordinate with landowners; carry identification.
  - Survey organization:
    - Two field surveyors per site (A: invertebrate tasks; B: RHS and environmental data).
    - Follow standardized sequencing: macroinvertebrate sampling first, then RHS follow-up, then replicate samples where applicable.
  - Macroinvertebrate sampling (RIVPACS protocol):
    - Standard pond-net (3-minute active sampling plus 1-minute manual search) across habitats proportionally to cover.
    - Collect and label samples with detailed site identifiers; fix in 10% formalin; label bags and pots; transport in secure trays.
    - Take environmental data concurrently (width, depth, substratum, velocity, etc.) across the sampling area (full width and length).
  - River Habitat Survey (RHS):
    - 500 m reach centered on M/MRn; record on RHS form including spot-checks every ~50 m; capture channel features, banktop land-use, vegetation structure, and channel vegetation types.
    - Include alder disease and SERCON components where applicable; follow Environment Agency RHS guidance.
    - Conduct chemical sampling at macroinvertebrate site and preserve in field containers; follow strict chain-of-custody and labeling.
  - Diatoms and chironomid pupal exuviae:
    - Collect diatoms within 25 m of the macroinvertebrate site, prioritizing upstream of sampling disturbance.
    - Collect chironomid pupal exuviae per CPET-guided methods; label and preserve for lab processing.
  - Ecofact macrophyte transects:
    - Record floral composition along transects in the river corridor to complement habitat data.
  - Data integrity and QA:
    - All data entry follows standardized forms; replication and spatio-temporal consistency emphasized.
    - 10% of flowing-water sites include replicates for quality control; inter- and intra-operator variability assessed.
  - Photographs and site records:
    - Take macroinvertebrate and RHS photographs for site re-location and context; include site boards with M and RHS identifiers.

- Permissions, safety, and governance:
  - Permissions required for access and sampling; carry identification; follow landowner requests.
  - Health and safety emphasis: water safety, leptospirosis awareness, life jackets, PPE, lone-worker protocols, and emergency procedures.
  - Field staff training and accreditation required for RHS and RIVPACS-related activities; formal COSHH assessments for fixatives and lab procedures.

- Data management, standards, and GIS readiness:
  - Data model designed for GIS integration:
    - Spatial keys: square codes, M/MRn site codes, and D/C markers for diatoms and pupal exuviae.
    - Geolocated coordinates (NGR) for each sampling point; 1:10,000 and 1:50,000 map references retained for context.
    - Environmental attributes: width, depth, substratum proportions, velocity categories, bedrock/rock features, and channel features (riffles, pools, bars, etc.).
    - RHS, SERCON, and Campture data layers align to a consistent 500 m reach schema with 50 m spot-checks to support multi-layer habitat quality scoring.
  - Data outputs:
    - Field forms and lab forms feed into centralized databases; suitable for GIS analyses, trend detection, and policy support.
    - Time-series data enable assessment of changes across CS1990 and CS2000 cycles.
  - Quality control and auditing:
    - Replication, inter-operator checks, and periodic audits to ensure comparability across surveys and years.
    - Training and accreditation of RHS personnel; standardized field procedures to minimize observer bias.

- Appendices, SERCON, and related guidance:
  - SERCON integration with RHS data to evaluate river conservation value, including naturalness of riparian vegetation and bank vegetation; dedicated SERCON component forms and guidance.
  - Appendix RHS.1–RHS.5 cover health and safety, lone-worker practices, glossary, and field protocols; safety guidance emphasizes leptospirosis risk, first-aid readiness, and safe field practices.
  - Documentation of data standards, field forms, and site reference conventions to support GIS interoperability and reproducibility.

- Endnotes and references:
  - Environment Agency RHS manuals and SERCON framework inform data collection, formatting, and interpretation.
  - Fundamental protocols for macroinvertebrate sampling (RIVPACS), chemical sampling, diatom methods, and CPET-based analyses are documented for consistency and comparability.

- Takeaway for GIS specialists:
  - The module provides a comprehensive, standardised, GIS-friendly data framework for freshwater habitat assessment, enabling robust mapping, time-series analyses, and integration with multiple spatial datasets (land use, hydrology, geography).
  - Central to GIS use are explicit site codes (M, MR, MRn, D, C), precise 1:10,000/1:50,000 mapping context, 1 km square sampling, and a 500 m RHS reach with 50 m spot-checks—designed to yield consistent, multi-layer habitat quality data suitable for policy and conservation analyses.