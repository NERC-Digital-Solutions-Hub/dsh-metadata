# Site code and site name mappings for Thames and tributaries monitoring

## Overview
- The document lists mappings between site codes and their corresponding site names and locations.
- Sites are spread across rivers and tributaries in the Thames catchment area (notably Thame, Thames, Cherwell, Evenlode, Windrush, Ock, Pang, Wye, Kennet, Coln, Leach/Embourn, Jubilee River, The Cut, Lodden) with specific location references (e.g., Wheatley, Islip, Hampton Poyle, Cassington Mill, Swinford, Newbridge, etc.).
- There are 22 site entries represented by two- to three-letter codes.
- The format consistently pairs a code with a “Site name = [Location]” description, suitable for use as a unique identifier in GIS workflows.

## Included sites (code — site name at location)
- Tm — Thame at Wheatley
- Ra — Ray at Islip
- Ch — Cherwell at Hampton Poyle
- Ev — Evenlode at Cassington Mill
- TS — Thames at Swinford
- TN — Thames at Newbridge
- Wi — Windrush at Newbridge
- Le — Leach at Lechlade (Mill Lane)
- Cl — Cole at Lynt Bridge
- Cn — Coln at Whelford
- Oc — Ock at Abingdon
- Pa — Pang at Tidmarsh
- Tso — Thames at Sonning
- Lo — Lodden at Charvil
- Cu — The Cut at Paley Street
- TR — Thames at Runnymede
- Wy — Wye at Bourne End
- TW — Thames at Wallingford
- TH — Thames at Hannington Wick
- Ke — Kennet at Woolhampton
- En — Emborne at Brimpton
- Ju — Jubilee River at Pocock's Bridge

## GIS and data-usage notes
- Use the codes as stable unique identifiers to join with other data layers (e.g., coordinates, attributes, time-series measurements).
- The site names provide human-readable context for map labels and legend entries.
- Grouping by river or sub-basin (e.g., Thames and its tributaries) can aid in thematic mapping and analysis.

## Data quality considerations
- The text provides names and locations but does not include geographic coordinates; geocoding or linking to a gazetteer is required to create precise point features.
- Some site names may have variations or historical spellings (e.g., "Emborne" vs. "Emborne"); verify with authoritative datasets.
- Ensure consistent interpretation of locations (e.g., “Mill Lane” at Lechlade) when integrating with other data sources.

## Suggested GIS workflow
- Extract the code-to-site-name mappings into a structured attribute table (Code, Site_Name, Location).
- Obtain or assign coordinates for each site (from gazetteers, hydrological datasets, or official site datasets) and create a point layer.
- Create a relational link between the code and any time-series or measurement data stored elsewhere.
- Visualize by grouping or symbolizing by river, proximity to towns, or data availability.
- Validate mappings with end users and iterate based on feedback.