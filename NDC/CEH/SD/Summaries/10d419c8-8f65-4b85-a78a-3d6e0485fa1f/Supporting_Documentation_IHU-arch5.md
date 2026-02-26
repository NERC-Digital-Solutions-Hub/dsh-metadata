# Integrated Hydrological Units of the United Kingdom

- Purpose and scope
  - Provides polygon layers representing hydrological units at multiple spatial resolutions: Hydrometric Areas with Coastline, Hydrometric Areas without Coastline, Groups, Sections, and Catchments.
  - Distinction between coastline and IHDTM-based boundaries; IHU introduced in 2015 to extend hydrological unit detail.
  - Used for organizing UK river flow measurement and hydrometric data management; supports cross-scale analysis and data integration.

- Layer descriptions and relationships
  - Hydrometric Areas with Coastline: administrative groupings of river catchments used for management; includes numbering systems for the UK and Ireland; NRFA gauging numbers follow the same scheme.
  - Hydrometric Areas without Coastline: same entities as with coastline but boundaries follow IHDTM; better for aligning with IHDTM grid, not ideal for cartography.
  - Groups: medium-resolution units (~400 km² typical); comprise one or more Sections; can be combined to form Hydrometric Areas without Coastline.
  - Sections: drainage areas between confluences with named rivers; linked to a single Group and to one Catchment; may use UNKNOWN in unsettled names; S_ID identifies the section, S_NAME provides public name.
  - Catchments: finest detail; upstream area from each Section outlet; may overlap multiple Sections/Groups; only layer where polygon overlaps occur.

- Data quality, coverage, and limitations
  - Quality constrained by the underlying IHDTM (50 m grid resolution).
  - Coverage: Hydrometric Areas with Coastline covers GB and NI; other layers currently GB-only due to lack of suitable NI river geometries; minor rivers may be missing even in GB.
  - Not all hydrometric areas are hydrologically complete for NI (clipped to national boundary).
  - No routine updates; updates occur only if errors are found or if underlying rivers/drainage data improve.
  - Islands reassigned in 2014 to existing nearby areas to achieve full UK surface coverage.

- Data creation and geometry
  - Boundaries derived from CEH IHDTM; GB coastline aligned to Meridian2; NI boundary/coastline from OS GB Panorama.
  - Each Hydrometric Area is a single feature; islands merged based on proximity and numbering conventions.
  - Topology: datasets processed to be gap- and overlap-free; every country point belongs to exactly one Hydrometric Area.

- Format, access, and metadata
  - Primary format: Geodatabase (preserves NULL values); Esri Shapefile converts NULLs to zeros or empty strings—note when downloading.
  - Attributes structured per layer (e.g., HA_NUM, HA_NAME, HA_ID for areas; G_ID, G_NAME for groups; S_ID, S_NAME for sections; S_AREA_KM2, KMSQ for catchments).
  - Table schemas provide descriptive fields and cross-references across layers (e.g., G_ID ties sections to groups; HA_ID links sections to hydrometric areas).
  - Large dataset scale (hundreds of thousands of features in Sections and Catchments).

- History and governance context
  - Hydrometric Areas originated in the 1930s to standardize hydro-meteorological data collection; numbering and naming conventions evolved over time.
  - The current IHU framework consolidates previous datasets and aligns with CEH and NRFA data; cross-border considerations for NI are noted.

- Practical implications for Data Stewards
  - Maintain comprehensive metadata and document the IHDTM-based methodology and island-merge decisions.
  - Ensure interoperability with IHDTM grids when integrating with other datasets; manage versioning and updates when underlying terrain or drainage data improve.
  - Address NI data gaps, clipping, and potential hydrological incompleteness; clearly communicate coverage limits to data users.
  - Be mindful of NULL handling in Shapefiles versus Geodatabases; communicate data format caveats to stakeholders.
  - Consider governance implications of long-term maintenance given no routine updates unless errors or improvements are found.