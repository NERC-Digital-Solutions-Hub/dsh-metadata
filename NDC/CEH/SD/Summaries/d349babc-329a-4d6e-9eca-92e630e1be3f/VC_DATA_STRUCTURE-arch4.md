# UK Environmental Change Network Vegetation: Coarse Grain (VC)

- Multi-site, multi-year vegetation dataset from the UK Environmental Change Network (ECN) Data Centre, owned by the ECN programme and sponsored by a consortium of UK government departments/agencies.
- Purpose: support understanding of environmental change through plot- and cell-level vegetation data across sites and years; nine-year sampling cadence with woodland subprotocols.
- Access: data available via the ECN Data Centre (data.ecn.ac.uk) or the Environmental Information Platform; usage requires acknowledgement and publication provenance.

## Data Structure and Content

- Data organized into 11 site-specific tables per data type, with core structure:
  - D1VC_xxx: plot-level information per site
  - D2VC_xxx: plot-level observations
  - D3VC_xxx: cell-level observations and features
  - Core metadata fields include SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME, VALUE
- Site-specific metadata capture extensive environmental attributes:
  - Land use, slope, aspect, slope form, and NVCCLASS (NVC class) stored in dedicated tables
- Coding schemes and crosswalks:
  - Land Use (Hodgson codes) and Slope Form (Hodgson codes) with descriptive lists
  - Features in cells coded with simple single-letter codes (e.g., P, W, S)
  - Extensive species/habitat crosswalks map codes to Latin names, common names, and external references
- Taxa and habitat crosswalks support integration with external taxonomic/habitat databases
- Site details:
  - 12 ECN sites (e.g., T01 Drayton, T02 Glensaugh, T03 Hillsborough, …, T12 Cairngorms) with defined coordinate locations and data availability windows (1993–2012 depending on site)

## Data Access, Quality, and Governance

- Access and discovery through the ECN Data Centre and Environmental Information Platform
- Quality and metadata:
  - Accompanying quality information and core metadata documentation are essential for proper interpretation
  - Protocol references and metadata must be cited; data usage acknowledgments and publication provenance are requested
- Metadata governance:
  - Core metadata tables define structure and semantics; detailed metadata documentation governs data standards and field definitions

## Quality Codes and Documentation

- Quality management:
  - ECN site managers assign standard ECN quality codes to indicate data quality factors; codes can be supplemented with text for unusual events (code 999)
- Standard ECN quality codes cover a wide range of conditions (e.g., data loss, sample issues, equipment problems, environmental disturbances, measurement uncertainties, etc.)
- A detailed quality text accompanies unusual events (code 999)

## Key Coding Schemes and Crosswalks

- Land Use (Hodgson codes) and Slope Form (Hodgson codes) with descriptive lists
- Features: single-letter codes representing observed site features
- Species and habitat crosswalks:
  - Large crosswalks map species/habitat codes to Latin names, common names, and external references
  - Enables integration with broader taxonomic and habitat datasets

## Data Leaders Takeaways

- Strategic value:
  - Provides a robust, multi-site, multi-year vegetation evidence base for long-term data strategy, system-wide governance, and ecosystem monitoring
- Governance and stewardship:
  - Treat ECN as a core data asset with consistent metadata standards, discoverability, and update processes
  - Maintain clear data ownership, usage acknowledgments, and publication provenance
- Discovery and usability:
  - Centralize access via the ECN Data Centre; maintain comprehensive metadata to support reuse across teams and partners
  - Use D1/D2/D3 site structures to enable cross-site analytics and trend analyses over time
- Quality and integration:
  - Leverage accompanying quality information to assess data suitability and ensure consistent interpretation across sites and years
  - Use extensive species/habitat crosswalks to enable integration with external taxonomic/habitat databases
- Collaboration and co-ownership:
  - Engage policy colleagues and data users to co-create data products addressing broader needs
  - Consider communities of practice around ECN data standards, metadata, and dissemination to reduce duplication and improve interoperability
- Data productization and dissemination:
  - Develop site-level vegetation indices, year-over-year trends, and habitat composition products aligned with user needs and governance standards
  - Ensure products are discoverable, up-to-date, and accompanied by clear metadata and provenance
- Operational considerations:
  - Plan for long-term stewardship given the nine-year cycle and protocol updates (including woodland subprotocols)
  - Regularly verify data availability, update metadata, and track usage to demonstrate dataset value and impact