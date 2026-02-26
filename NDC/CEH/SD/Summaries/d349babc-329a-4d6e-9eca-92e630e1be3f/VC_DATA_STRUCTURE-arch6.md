# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Coarse Grain (VC)

- Purpose and scope: A long-running vegetation dataset for environmental change monitoring, with data usage acknowledged to ECN and citation requirements for publications.
- Data platform: Stored and managed by the ECN Data Centre; accessible via ECN data platforms.

## Data structure and core fields

- Data model:
  - D1VC_xxx: site-specific plot data
  - D2VC_xxx: environmental metadata and site-level measurements
  - D3VC_xxx: cell-level data (features per cell)
- Core fields common across tables: SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME, VALUE
- Outputs and formats: Designed to support analysis through self-serve formats (dashboards, pivot-like views) and accompanying quality metadata.

## Sampling design and site information

- Sampling design:
  - 50 random 2m x 2m plots per site
  - Species presence recorded in 25 cells (40 cm x 40 cm) within each plot
  - Re-surveyed at nine-year intervals
- Environmental context:
  - D2VC_xxx includes PEDATE, LANDUSE (Hodgson codes), SLOPE, ASPECT, SLOPEFORM, NVCCLASS (NVC class)
  - D3VC_xxx contains coded cell-level features (e.g., paths, walls, streams, hedges)

## Taxonomy and codes

- Taxon and species codes:
  - Extensive numeric-to-name mappings linking species codes (FIELDNAME) to Latin names, common names, and taxonomic concepts
  - Example pattern: multiple entries showing the same numeric code associated with different taxon names or synonyms (e.g., Salix aurita related to Salix caprea, Salix cinerea, Salix herbacea, etc.)
  - Crosswalks cover a broad range of vascular plants, bryophytes, and lichens
- Feature and land-use codes:
  - Land Use: Hodgson codes 1–22 (e.g., Ley grassland, Cereals, Deciduous/Coniferous woodland)
  - Slope Form: convex (1), straight (2), concave (3)
  - Cell features: P = Path, W = Wall, S = Stream, H = Hedge, D = Ditch, F = Fence, B = Bank, N = Natural boundary, X = No feature

## Protocols, quality, and metadata

- Quality metadata:
  - ECN standard quality codes (100–513) plus 999 for unusual events (with accompanying quality text)
  - Codes capture data collection issues (e.g., no information, sample loss, partial loss, equipment problems, environmental disturbances, etc.)
- Data quality guidance:
  - Quality codes are supplied by site managers and should be reviewed alongside the data to assess reliability and context
  - Unusual events (code 999) require reading the accompanying quality text for full context
- Metadata and documentation:
  - Core metadata, site-specific descriptions, and protocol details are documented in ECN metadata resources and the Measurements Protocol for terrestrial vegetation

## Temporal and site coverage

- Sites: 11 site codes (e.g., T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House - Upper Teesdale, T05 North Wyke, T07 Sourhope, T08 Wytham, T09 Alice Holt, T10 Porton Down, T11 Y Wyddfa – Snowdon, T12 Cairngorms)
- Temporal range: Date ranges vary by site (examples include 1993–2011, up to 2012 for some sites)

## Data access, usage, and support

- Access: Data hosted and curated by the ECN Data Centre; available via ECN data platforms
- Acknowledgement: Users should acknowledge ECN and provide one reprint of any publication citing the data
- Data harmonization considerations:
  - Patchy data across sites and formats may require harmonization when combining datasets
  - Understanding the data model is essential: 11 site tables for plots, environmental metadata, and cell-level observations
  - Field names reference standardized taxonomic and quality codes; users may need to consult the taxon crosswalks and quality code definitions

## Practical implications for data support

- Key tasks for data support:
  - Navigate and interpret extensive taxon code mappings to correctly identify species
  - Integrate data across D1, D2, and D3 tables while respecting site-specific variations
  - Apply quality codes and read accompanying quality texts to assess data reliability
  - Harmonize across patchy data and multiple code systems (land use, slope form, features, taxa) for robust analyses
- Contact and references:
  - ECN Data Centre (ecn@ceh.ac.uk)
  - Protocol reference: http://www.ecn.ac.uk/measurements/terrestrial/v