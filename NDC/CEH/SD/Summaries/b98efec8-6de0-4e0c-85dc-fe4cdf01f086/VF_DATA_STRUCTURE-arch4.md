# Dataset Originator

- The ECN Data Centre (Centre for Ecology and Hydrology) manages environmental change datasets used to understand causes and consequences of environmental change; site-specific data come from a consortium of UK government departments and agencies funding monitoring or network coordination.
- Sponsoring organisations include DEFRA, Natural England, NERC, SEPA, and others; users must acknowledge data use and provide a reprint of any publications citing ECN data; contact is the ECN Data Centre.

## Data Structure, Download Format, and Documentation

- Primary data fields in downloads:
  - SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME (VEG_SPEC or Q1/Q2/Q3), VALUE (species or quality code).
- Supporting documentation:
  - ECN_VF2.csv (plot-level information), ECN_VF3.csv (cell-level information), ECN_VF_qtext.csv (quality narrative text for codes).
- Codes:
  - Species codes follow VESPAN with cross-references to BRC codes.
  - Quality codes Q1–Q3 indicate data quality; 999 denotes unusual events with accompanying text.
- Site metadata and explanatory information:
  - Site codes T01–T12 with coordinates; land use (Hodgson codes), slope form, features, etc.; mappings between Latin names and external taxonomic concepts.

## Data Model and Metadata Details

- Site codes and coordinates underpin spatial context; subentries exist for some sites (e.g., T12 Cairngorms 1/2).
- Land Use (Hodgson) codes map to descriptions (e.g., grasslands, cereals, woodland, heath).
- Slope Form: Convex, Straight, Concave.
- Features: Path, Wall, Stream, Hedge, Ditch, Fence, Bank, Boundaries, None.
- Species: Extensive cross-references between ECN codes (VESPAN/BRC) for plant taxa; numerous taxa included.
- Explanatory codes cover habitat, vegetation structure, and taxon-specific annotations.

## Data Scope and Sampling Protocol

- Spatial scope: Multiple ECN sites across the UK with defined coordinates and metadata.
- Sampling protocol:
  - At least two 10m x 10m plots per NVC type per site.
  - Species presence recorded in 40cm x 40cm cells within plots.
  - Longitudinal design: surveys every three years; some sites conduct annually for higher temporal resolution.
  - Emphasis on accompanying quality information to interpret data validity.

## Usage, Quality, and Reproducibility

- Data quality is anchored to embedded quality codes and accompanying narratives; protocols ensure comparability across sites for cross-site and temporal analyses.
- Reproducibility is supported by standardized procedures and rich metadata to interpret context.
- Data citation: acknowledge ECN data usage and share a reprint of publications citing ECN data.
- Discoverability: ECN_VF2.csv and ECN_VF3.csv metadata enhance understanding of site, plot, and cell-level context.

## Practical Takeaways for Data Leaders

- Governance and strategy:
  - Use standardized protocols and rich metadata to ensure data quality, comparability, and reuse across networks.
  - Maintain clear ownership and publication/citation requirements to quantify value and impact.
- Data discovery and accessibility:
  - Ensure metadata (site, plot, cell, land use, slope, features) is discoverable and well-documented to reduce gaps.
  - Use cross-referenced species coding (VESPAN/BRC) for interoperability with external taxonomic resources.
- Data quality management:
  - Leverage embedded quality codes and quality narratives to assess data reliability and contextual issues.
- Collaboration and systems thinking:
  - Value aggregation across sites and partners to understand broader environmental change signals.
  - Maintain open channels for data contribution and feedback to improve products and user satisfaction.

## Key Challenges and Considerations

- Understanding user needs and ensuring data products meet them through documentation and quality notes.
- Achieving a comprehensive overview of available data due to dispersed site-level data.
- Data gaps and granularity: ensuring adequate coverage and granularity for targeted analyses.
- Access barriers and data protection considerations (potential paywalls or restrictions in broader contexts).
- Efficiently verifying data content and format across a large, heterogeneous dataset.
- Data standards and metadata clarity: reliance on multiple code systems (Hodgson, VESPAN, BRC) requires robust mapping and documentation.
- Sector coordination and communities of practice: leveraging networks to avoid duplication and improve data practices.

## Explanatory Information: Species Codes (Examples)

- Provides mappings between species codes and Latin names or equivalent external references (e.g., Rumex obtusifolius with multiple cross-references to other names and groups).
- Includes numerous entries showing alternative taxon concepts, synonyms, and cross-references to other taxonomic databases.

## Explanatory Information: Quality Codes (Examples)

- Defines a range of quality indicators and notes for data integrity, including:
  - 100–199: general data issues (e.g., no information, sample lost, partial loss, equipment-related problems).
  - 200–299: sampling/recording conditions (e.g., adverse weather, insects affecting sampling, non-standard dates/times).
  - 500–509: laboratory-related notes (e.g., no sample, contaminated samples, measurement issues).
  - 999: Unusual event – see accompanying quality text.