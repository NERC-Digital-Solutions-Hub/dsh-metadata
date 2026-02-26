# Introduction to the DATABASE Catalogue

- Purpose within the Pontbren Database: Provide borehole logs, equipment details, and site-specific metadata to support discoverability, provenance, and reuse of groundwater-related datasets.
- Target for data stewards: Emphasizes robust data organization, documentation, and traceability of data collection methods and instrumentation to enable trustworthy reuse.

## Scope of the provided data in this document chunk

- Equipment and methods used for borehole drilling and probing
  - Drill/boring tools: hand auger with AQ drill rod/guide tube, pneumatic hammer, Atlas Copco RAB hand held air flush rotary drill, Atlas Copco Leopard rotary/percussive drill.
  - Tubing and completion: 16 gauge, 44.5 mm aluminium access tubing; completeness details (typical depths and sample intervals such as NP20–NP23).
- N-probe installations and sites
  - NP20, NP21, NP22, NP23 boreholes associated with multiple sites:
    - Site S3 (Easternmost, Central, Westernmost) within the PEN-TAL-Y-CEIN LLANFAIR CAEREINION area and COED CWM-Y-LLWYNOG LLANFAIR CAEREINION.
  - Grid references, datums, and site descriptors included (e.g., SJ grid references).
- Borehole log content
  - Depths (depth mBGL), diameters, and completion details; soil descriptions (color, texture, mottling), thickness intervals, and depth to various layers.
  - Specific soil/rock descriptions (e.g., silty clay, clayey gravel, mottling, sandstone/mudstone fragments) and structural notes (e.g., boulders, gravel content).
  - Date of borings and logging events (e.g., 14/05/06) and the organization responsible (Centre for Ecology and Hydrology; Groundwater Monitoring and Drilling Ltd).
- Data records and structure
  - Sheet-based borehole logs with repeated entries per site and per borehole; explicit references to “BOREHOLE LOG” entries, datum levels, and descriptive sections (thickness, depth, reduced level).
- Associated documentation and provenance
  - Explicit attribution to Groundwater Monitoring and Drilling Ltd and CEH; documentation context provided (Appendices and field notes) for provenance and context.
- Appendix D: Streamflow gauging data
  - Flow metered spot measurements with start/finish times and flow estimates for multiple sites; demonstrates cross-domain governance and data integration with streamflow observations.

## Data quality, provenance, and metadata considerations for data stewards

- Provenance and attribution
  - Borehole logs and drilling events attributed to specific contractors and CEH; include date stamps and site descriptors for traceability.
- Metadata completeness
  - Rich descriptive text for lithology, layer boundaries, and sampling intervals; ensure consistency of units, coordinate references, and datum across records.
- Data structure and discoverability
  - Logs organized by borehole with clear identifiers (NP numbers) and site names; coordinate references provided as grid references; support cross-linking with other datasets (e.g., streamflowAppendix D).
- Data quality and assurance
  - Text-heavy, descriptive QA relies on site interpretation; occasional entries indicate dry boreholes (e.g., “Water Not struck”), which should be captured as non-recovered data points.
- Interoperability challenges
  - Heterogeneous formats and long-form descriptive logs; potential for variations in depth notation, term usage, and site naming across logs and appendices.
- Documentation alignment
  - Matches with Appendix B (Groundwater borehole logs) and Appendix D (Streamflow gauging) to support end-to-end data lineage.

## Implications for data governance and reuse

- Documentation discipline
  - Maintain comprehensive borehole logs with consistent field descriptions, standardized units, and explicit metadata fields to enable robust reuse.
- Metadata standards
  - Enforce harmonized metadata definitions for depth (mBGL), datum level, thickness, and soil descriptions; include site location references and sampling intervals.
- Versioning and updates
  - Track any reprocessing or updates to borehole logs and associated equipment details; ensure updates propagate to catalogues and cross-dataset links.
- Usability and discoverability
  - Preserve provenance notes (contractor, date, site) and ensure cross-references to related data (e.g., streamflow measurements) are preserved to enable multi-dataset analyses.

## Key challenges and considerations highlighted

- Complex, site-specific log narratives in free text require careful curation for reuse.
- Variability in equipment configurations and drilling methods across boreholes.
- Mixed data types (descriptive logs, geometric/site data, and time-stamped measurements) demand coherent integration in the data catalogue.
- Ensuring consistent linkage between borehole logs (NP numbers) and site-level datasets for cross-domain analyses.

## Takeaways for data stewards

- Preserve rich provenance and equipment metadata to support reproducibility and traceability.
- Standardize core metadata fields (location, depth, datum, sample intervals, lithology) while retaining descriptive content for context.
- Maintain clear cross-dataset connections (e.g., borehole logs with corresponding streamflow and other hydrological measurements) to support governance and reuse across the dataset’s multi-site, multi-instrument scope.