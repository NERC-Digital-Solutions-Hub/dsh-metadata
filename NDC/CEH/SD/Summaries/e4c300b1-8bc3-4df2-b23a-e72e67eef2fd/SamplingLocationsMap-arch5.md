# Site name mappings for river monitoring network

- Overview
  - A mapping of short site codes to full site names and locations for a network of river monitoring sites.
  - Examples include:
    - Tm -> Thame at Wheatley
    - Ra -> Ray at Islip
    - Ch -> Cherwell at Hampton Poyle
    - Ev -> Evenlode at Cassington Mill
    - TS -> Thames at Swinford
    - TN -> Thames at Newbridge
    - Wi -> Windrush at Newbridge
    - Le -> Leach at Lechlade (Mill Lane)
    - Cl -> Cole at Lynt Bridge
    - Cn -> Coln at Whelford
    - Oc -> Ock at Abingdon
    - Pa -> Pang at Tidmarsh
    - Tso -> Thames at Sonning
    - Lo -> Lodden at Charvil
    - Cu -> The Cut at Paley Street
    - TR -> Thames at Runnymede
    - Wy -> Wye at Bourne End
    - TW -> Thames at Wallingford
    - TH -> Thames at Hannington Wick
    - Ke -> Kennet at Woolhampton
    - En -> Emborne at Brimpton
    - Ju -> Jubilee River at Pocock's Bridge

- Implications for Data Stewards
  - Provides a standardized set of site codes and descriptive names to enable consistent linking of data across datasets and portals.
  - Facilitates discoverability and cross-referencing of time-series data (flow, level, water quality, etc.) by site.

- Metadata and governance considerations
  - Each entry should be accompanied by metadata: exact coordinates, river system, operator, measurement types, units, and data cadence.
  - Maintain a versioned governance record to track changes in site naming, relocations, or closures.
  - Align with controlled vocabularies and metadata schemas to support interoperability.

- Data quality and interoperability
  - Validate accuracy of codes and site names against authoritative sources.
  - Ensure consistent formatting and avoid duplicate or conflicting entries across systems.
  - Prepare for updates when sites are renamed, decommissioned, or new sites are added (e.g., new crossings or tributaries).

- Data availability and sharing considerations
  - Use the mapping to populate and index data catalogs, portals, and discovery tools.
  - Document data provenance and lineage for each site to support reuse and trust.

- Potential challenges to address
  - Incomplete understanding of user needs for site coverage and prioritization.
  - Timely incorporation of changes from field operators or site managers.
  - Handling diverse data systems and formats across the site network.

- Suggested next steps for implementation
  - Create or update a metadata record for each site with standardized fields (code, name, coordinates, river, location description, operator, data types, update frequency).
  - Establish a governance workflow for adding, updating, or retiring sites.
  - Integrate the site mapping with overarching data catalogs and user-facing portals to ensure discoverability and consistent linking to datasets.