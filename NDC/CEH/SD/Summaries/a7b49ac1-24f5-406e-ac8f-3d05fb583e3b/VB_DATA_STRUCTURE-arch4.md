# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Baseline (VB) Dataset

- Overview
  - Focus: Vegetation Baseline (VB) data from the ECN to study environmental change impacts on vegetation.
  - Originator: ECN Data Centre (Centre for Ecology and Hydrology); contact ecn@ceh.ac.uk.
  - Owners: ECN programme funded by UK government departments and agencies; data usage should be acknowledged with a reprint of any publication citing the dataset.

- Data structure and access
  - Storage: Core data in an Oracle database with site-specific tables.
    - D1VB_xxx: Core vegetation data by site.
    - D2VB_xxx: Plot-related data by site.
  - Key fields: SITECODE, SYEAR, PLOTPID, PLOTTYPE, FIELDNAME, VALUE, plus metadata (units, type, required, reference).
  - Metadata and reference: M_DESC (site metadata), M_REFFIELD (field names/species codes).
  - Protocol reference: http://www.ecn.ac.uk/measurements/terrestrial/v
  - Access and usage: Data available via the ECN Data Centre and Environmental Information Platform; acknowledgement required for data use and a reprint of publications citing the data.

- Sampling protocol and data collection
  - Grid sampling: ~400 sample grid positions aligned with the National Grid; up to 100 randomly located infill points for under-represented vegetation types.
  - Plot layout: 2m x 2m plots centered on grid/infll points; plots oriented N, E, S, W; permanently marked for continuous monitoring.
  - Survey scope: One-off vegetation survey to generate maps and select plots for ongoing monitoring; long-term monitoring results available via ECN channels.

- Site coverage and data scope
  - 12 sites (codes/names: T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House – Upper Teesdale, T05 North Wyke, T06 Rothamsted, T07 Sourhope, T08 Wytham, T09 Alice Holt, T10 Porton Down, T11 Y Wyddfa – Snowdon, T12 Cairngorms).
  - Time frame: Primarily 1993–2000 (with some sites earlier or later); site coordinates and date ranges documented.
  - Data organization: Site-specific vegetation data stored in D1VB_xxx and D2VB_xxx with core metadata in accompanying docs.

- Data content and coding
  - Features (presence/absence codes): P (Path), W (Wall), S (Stream), H (Hedge), D (Ditch), F (Fence), B (Bank), N (Natural boundary), X (No feature).
  - Species codes: Extensive taxon-to-code mapping covering Latin names, synonyms, and common names; includes mappings to related taxon concepts (e.g., Salix spp., Sambucus nigra, Solanum dulcamara, etc.). The dataset contains numerous alias relationships (e.g., Salix aurita = Salix caprea) and cross-references to multiple taxonomic entries.
  - Quality information: A quality component accompanies the data; users should consult the quality metadata for proper interpretation.

- Quality codes and metadata
  - Standard ECN quality codes: A comprehensive list (e.g., 100 No information available; 101 No sample/reading taken; 102 Sample lost; 103 Partial loss; 104 Sample frozen; 120 Liming vicinity; 135 Disturbance; 200 Adverse weather; 239 Taxon identified with high/medium/low confidence; etc.).
  - 999: Unusual event (with accompanying quality text to view details in the quality metadata).
  - Purpose: Allows site managers to flag data issues affecting data quality, sampling conditions, laboratory processing, and environmental factors.

- Governance, usage, and dependencies
  - Publication and citation: Acknowledgement of data use is requested; provide a reprint of any publication citing the data to ECN.
  - Interoperability: Dataset designed with a structured schema to support cross-site comparisons and integration with ECN data and platforms.
  - Documentation: Metadata documentation and references accompany the dataset to guide interpretation and integration.

- Practical takeaways for data leaders
  - The VB dataset offers a structured, multi-site vegetation baseline captured via a controlled grid and plot-based sampling, suitable for cross-site analytics and trend assessment.
  - Oracle-based schema (D1VB_xxx and D2VB_xxx) enables systematic querying by site, year, plot, and species/quality codes, supporting governance and stewardship across networks.
  - Prioritize consulting the quality information and metadata to ensure correct interpretation and integration into broader data systems.
  - Maintain proper data-citation practices (acknowledgement and reprint submissions) to support data value demonstration and ongoing stewardship.
  - Access is centralized through ECN channels, with data products and outputs available via the ECN Data Centre and Environmental Information Platform.

- Notable consideration for data integration
  - The extensive and evolving species code mappings, including numerous synonyms and cross-references, require careful reconciliation when integrating with other taxonomic vocabularies or external data sources.
  - The comprehensive quality code set is essential for assessing data reliability, especially when performing cross-site or long-term analyses.