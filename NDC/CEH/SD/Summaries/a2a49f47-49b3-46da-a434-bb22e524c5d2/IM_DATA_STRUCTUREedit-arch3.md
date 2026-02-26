# ECN Data Centre Moth Dataset Description

- Purpose: Provides environmental health monitoring data via standardized light-trap surveys of Macrolepidoptera, intended to scrutinise policy impacts, inform future decisions, and support reporting on environmental change and biodiversity at multiple UK sites.
- Context: Managed and owned by the UK Environmental Change Network (ECN) with a consortium of government departments and agencies; data are intended for public use with appropriate acknowledgements and publication receipts.

## Data provenance and governance

- Originator: ECN Data Centre (Centre for Ecology and Hydrology).
- Owners: ECN programme funded by a consortium of UK government departments/agencies (multi-organisation sponsorship list provided).
- Usage expectations: Acknowledge data usage; provide one reprint of any publication citing the data; transparency around data provenance and attribution is encouraged to demonstrate data value.
- Protocols and comparability: ECN uses standard operating procedures to ensure comparability across sites; an accompanying document (im.pdf) explains data collection procedures.
- Access considerations: Data sharing and metadata completeness can be barriers; data governance and open-data practices are emphasized, with Site Managers responsible for quality codes and textual quality notes (see ECN_IM_qtext.csv).

## Data structure and content

- Dataset origin and description:
  - Site-level moth trap data collected nightly using a standard light trap methodology (Rothamsted Insect Survey approach).
  - Data downloads include a per-site unique code (SITECODE), location code (LCODE), sampling date (SDATE), year, week, and measured variable values (VALUE).
  - Supporting documentation:
    - ECN_IM2.csv: Details the trap period (how many days traps were open; typically PERIOD = 1, but variable where not).
    - ECN_IM_qtext.csv: Site manager-provided quality text to accompany quality codes, with 999 indicating an unusual event requiring manual review.
- Sites and location metadata:
  - Site codes: T01 (Drayton) through T12 (Cairngorms) with precise coordinates for each site.
  - Explanatory information: A mapping of site codes to site names and lat/long coordinates is provided.
- Variables and measurements:
  - FIELDNAME: Repeated fields such as Q1, Q2, Q3, etc., representing quality-coded measurements; COMMON NAME fields provide taxonomic/generic identifications for macrolepidoptera.
  - A comprehensive mapping exists between numeric codes and species names (e.g., 100 = Alder Kitten, 101 = Poplar Kitten, etc.), with many thousands of entries covering macrolepidoptera species and macros/macros unidentified categories.
- Quality and metadata:
  - ECN_IM_qtext.csv stores quality-related text; multiple quality codes can apply per field, including circumstances that may affect data quality (e.g., weather, sampling conditions, debris).
  - Quality codes (ECN quality code taxonomy) are included (ECN_IM_qtext.csv and the separate Quality codes list), including codes 100–999 with descriptive notes.
- Notable data notes:
  - Some entries refer to species pairs (e.g., 3392 Mesapamea secalis/didyma) where separation requires dissection; females may be inseparable without dissection.
  - Species 3394 (Amphipyra berbera berbera) may also appear as 2507 in past records; currently treated as the same subspecies.
  - The dataset includes both identified macro species and “Unidentifiable” macro/micro categories to reflect varying identification confidence.

## Protocol and methodology

- Standard method: Macrolepidoptera identified using a standard light trap; methodology aligns with Rothamsted Insect Survey practices.
- Frequency and timing: Data recorded nightly; supplementary quality information should accompany the data when used.
- Data comparability: Protocols are designed to ensure data comparability across different ECN sites; accompanying documentation (im.pdf) explains data collection procedures in detail.

## Data quality and metadata considerations

- Metadata completeness: Site-level metadata, sampling dates, trap periods, and quality notes are provided; however, metadata gaps or inconsistencies can be barriers to rapid use.
- Data quality controls: Quality codes and accompanying textual notes enable assessment of data quality issues for each observation.
- Transformation and use: The dataset may require transformation or cleaning prior to integration into dashboards or reports, given the variety of fields (Q1–Q8) and the large species code mapping.
- Data governance: Public sharing of underlying data is encouraged but requires appropriate data management and governance practices at the point of data use and publication.

## Access, usage, and governance guidance

- Data download structure:
  - Each ECN site has a unique SITECODE; LCODE identifies site location; SDATE is the sampling date; VALUE is the measured value for the given FIELDNAME.
  - The ECN_IM2.csv file provides spatial-temporal context (periods traps were open).
- Acknowledgement and citations:
  - Users should acknowledge ECN data usage and provide a reprint if their work cites ECN data.
  - Site managers may contribute quality codes (ECN_IM_qtext.csv) describing data quality issues to accompany the standard dataset.
- Documentation and support:
  - An accompanying protocol document (im.pdf) and the ECN_IM2.csv/ECN_IM_qtext.csv files provide essential metadata and quality context to implement monitoring frameworks.

## Implications for monitoring frameworks

- Strengths for policy monitoring:
  - Multi-site, standardized, nightly moth-trap data supports trend analysis in biodiversity and environmental change across the UK.
  - Rich species-level coding enables fine-grained indicators of community composition and phenology.
- Key challenges to address:
  - Data gaps due to equipment or sampling conditions, and the need for robust metadata and quality assurance processes.
  - Handling the large, complex species-code mapping and ensuring consistent species identifications across sites.
  - Dealing with unidentified or macro/micro categories and the implications for indicator development.
  - Data governance considerations around publicly sharing underlying data and ensuring proper attribution.
- Practical actions for authors of monitoring frameworks:
  - Establish clear metadata requirements (site codes, coordinates, sampling dates, trap periods, data quality notes).
  - Define data cleaning, transformation, and aggregation steps to produce reliable biodiversity indicators.
  - Incorporate quality flags (and the associated textual notes) to filter or adjust analyses for data reliability.
  - Plan for long-term data stewardship, including updates to site codes, species mappings, and quality protocols.

## Summary of end-to-end considerations

- The ECN dataset provides a robust, multi-site, nightly macrolepidoptera monitoring framework with detailed site metadata, standardized collection protocols, and extensive species coding.
- Its value for environmental health monitoring lies in its capacity to track biodiversity changes, phenology shifts, and responses to policy or environmental drivers across time and space.
- To maximize usefulness for monitoring frameworks, ensure rigorous metadata capture, transparent handling of data quality issues, and clear governance around data sharing and attribution.