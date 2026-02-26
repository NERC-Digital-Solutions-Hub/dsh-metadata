# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Coarse Grain (VC) Dataset

## Overview and purpose
- Standardized vegetation presence data collected across multiple UK sites to enable cross-site and temporal comparisons.
- Aims to support consistent reporting of environmental health and policy performance over time.
- Dataset managed by ECN Data Centre (Centre for Ecology and Hydrology); dataset owners include a consortium of UK government departments/agencies.
- Data usage is encouraged with acknowledgment of ECN data and submission of reprints for publications citing the data.

## Sampling protocol and design
- Plot-level sampling:
  - Fifty 2 m x 2 m plots per site selected randomly.
  - Within each plot, species presence recorded in twenty-five 40 cm x 40 cm cells.
- Sampling cadence:
  - Vegetation surveys repeated every nine years.
- Woodland protocol:
  - If plots fall within woodland, the woodland protocol is applied; data available via ECN Data Centre or Environmental Information Platform.
- Quality information:
  - Users should consult accompanying quality information when using the data.

## Data collection and quality management
- Data lifecycle:
  - ECN verifies required data, quality assures, cleans, and transforms data for analysis.
  - Outputs include categorical assessments of environmental health against standards, presented as reports, maps, and charts.
- Data stewardship:
  - Datasets stored and uploaded to appropriate portals to ensure ongoing accessibility and reuse.

## Data structure and storage
- Core data organization:
  - Data stored in site-specific tables within an Oracle database.
  - Three data levels per site:
    - D1VC_xxx: site-level data (e.g., SITECODE, SYEAR, etc.)
    - D2VC_xxx: plot-level data (e.g., PEDATE, LANDUSE, SLOPE, ASPECT, SLOPEFORM, NVCCLASS)
    - D3VC_xxx: cell-level data (e.g., FIELDNAME, VALUE, with cell-specific details)
- Example fields:
  - SITECODE, Description; SITECODE, Units; SITECODE, Type; SITECODE, Required?; SITECODE, Reference table
  - SYEAR, Description; SYEAR, Units; SYEAR, Type; SYEAR, Required?
  - PLOTPID, Description; PLOTPID, Units; PLOTPID, Type; PLOTPID, Required?
  - CELLID, Description; CELLID, Units; CELLID, Type; CELLID, Required?
  - FIELDNAME, Description; FIELDNAME, Units; FIELDNAME, Type; FIELDNAME, Required?
  - VALUE, Description; VALUE, Units; VALUE, Type; VALUE, Required?
- Site-level metadata (D1VC) and plot-level/cell-level (D2VC, D3VC) fields described; core metadata structure detailed in ECN documentation.

## Sites and dataset scope
- 11 ECN vegetation sites (site codes and names):
  - T01 – Drayton (1993–2011)
  - T02 – Glensaugh (1994–2011)
  - T03 – Hillsborough (2003)
  - T04 – Moor House - Upper Teesdale (1993–2011)
  - T05 – North Wyke (1993–2011)
  - T07 – Sourhope (1993–2011)
  - T08 – Wytham (1993–2011)
  - T09 – Alice Holt (1994–2011)
  - T10 – Porton Down (1994–2012)
  - T11 – Y Wyddfa - Snowdon (1999–2010)
  - T12 – Cairngorms (1998–2011)
- Site coordinates and ranges provided for each site.

## Land Use and slope form
- Land Use (Hodgson codes): Standardized code set (1–22) describing land use at sampling (e.g., Ley grassland, permanent grassland, cereals, woodland types, heath, moor, parks, golf courses, etc.).
- Slope Form (Hodgson codes):
  - 1 = Convex
  - 2 = Straight (rectilinear)
  - 3 = Concave

## Features in cells
- Cell-level feature codes describe observed features (e.g., Path, Wall, Stream, Hedge, Ditch, Fence, Bank, Natural boundary, No feature, etc.).

## Species and taxonomic codes
- Extensive species coding: numeric codes linked to Latin names, BRC concepts, and names in the BRC database.
- Enables robust species- and taxon-level analyses with mappings across Latin names, common names, and database identifiers.
- Example mappings show many-to-one relationships between names and codes.

## Protocol references and acknowledgments
- Protocol Reference: http://www.ecn.ac.uk/measurements/terrestrial/v
- Data usage acknowledgment:
  - Please acknowledge ECN data use.
  - Consider sending one reprint of any publication citing ECN data.

## Quality Codes
- ECN site managers assign standard quality codes to indicate factors affecting data quality; codes are drawn from a standard list with 999 for unusual events (with accompanying text).
- Standard ECN quality codes include:
  - 100 through 151, 501–513, 999, among others, covering issues such as information availability, sample handling, partial loss, equipment problems, debris, environmental disturbances, data edits, laboratory conditions, etc.
- If an unusual event occurs not covered by standard codes, a quality text is attached (quality code 999).

## Practical implications for analysts
- Enables standardized, repeatable analyses across sites and time, supporting temporal and spatial trend analyses of vegetation and environmental health.
- Data are highly structured and require referencing site-level (D1VC), plot-level (D2VC), and cell-level (D3VC) tables, with detailed field definitions and codes for land use, slope form, features, and species.
- Quality information is essential when leveraging the data for policy performance assessments or environmental change studies.
- Data access and reuse are supported through the ECN Data Centre and related platforms, with formal acknowledgment and publication-reprint sharing encouraged.