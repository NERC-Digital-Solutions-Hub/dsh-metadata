# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Baseline (VB)

- Purpose and governance
  - Baseline vegetation dataset for environmental change research; designed to be discoverable and usable by researchers.
  - Data managed by the ECN Data Centre/Centre for Ecology and Hydrology; governed by formal metadata and protocol documentation.
  - User obligations include acknowledging data use and sending a reprint of any citing publication.

- Dataset scope and content
  - Spans roughly 1991–2000 across 12 sites (T01–T12), with site-specific date ranges.
  - Method: approximately 400 grid positions plus up to 100 infill points; 2m x 2m plots, oriented to N/E/S/W; species lists recorded per plot.
  - Data structure: core data stored in an Oracle-based schema with 12 site-specific tables (D1VB_xxx) and related plot metadata; fields include SITECODE, SYEAR, PLOTPID, PLOTTYPE, FIELDNAME, VALUE, etc.
  - Content details: plots include plot-type classifications (e.g., standard, woodland); extensive species and feature coding with mappings to Latin/common names; documentation and metadata describe coding schemes and provenance.

- Metadata, quality, and access
  - Dataset governed by metadata and protocol documentation; core metadata tables exist and are described in accompanying materials.
  - Access via ECN Data Centre and Environmental Information Platform; users must acknowledge data use and provide copies of publications.
  - Quality information is essential: consult accompanying quality metadata to understand provenance, plot measurements, and coding schemes.
  - Updates and sharing: structures are in place for data availability and potential updates; sharing may be subject to restrictions or embargoes.

- Ingest, curation, and provenance
  - Ingest from multiple sites (12) into a standardized Oracle schema; map site-specific fields to standardized descriptors; maintain metadata completeness for site codes, years, plot IDs, types, fields, and values.
  - Track provenance: document data originators (ECN Data Centre) and any data transformations or cleaning steps.
  - Documentation alignment: ensure metadata and protocol references remain in sync with the 12-site data tables.

- Interoperability and coding schemes
  - Contains extensive species and feature coding with numerous synonyms and cross-references (as illustrated by the long mapping of species codes to various names).
  - Interoperability challenges due to legacy formats and site-specific conventions; require careful metadata mappings to enable cross-site discovery and reuse.

- Quality codes and practical considerations for data stewards
  - Uses a standardized ECN quality code list (e.g., 100–237) with 999 for unusual events; codes indicate issues such as data loss, sampling anomalies, or contaminants.
  - Practically, stewards must capture and convey quality codes alongside data; a quality text field provides context for non-standard events.

- Key challenges (as relevant to this dataset)
  - Incomplete understanding of user needs across 12 sites with differing histories.
  - Timely data acquisition from multiple site coordinators.
  - Achieving metadata and plot-level coding consistency across long time spans.
  - Interoperability across multiple systems/formats and legacy conventions.
  - Managing large, age-diverse vegetation datasets with long-term monitoring.
  - Handling older databases and bespoke solutions while maintaining metadata alignment and discoverability.

- Implications for data stewardship
  - Ensure robust ingestion pipelines and cross-site metadata mappings to enable discoverability.
  - Preserve and document provenance, including data originators and transformations.
  - Maintain comprehensive metadata and quality metadata to support data quality assessment.
  - Communicate data availability, restrictions, and embargoes clearly to data users.
  - Manage extensive species/feature coding with careful standardization to support interoperability and reuse.