# The CEH digital 1:50,000 river network of Great Britain

## Overview
- First extensive digital river network for Great Britain, produced by the Institute of Hydrology (now CEH) between the mid-1970s and late 1990s.
- Digitised from the Ordnance Survey 1:50,000 Landranger “blue line” maps, including single blue lines and centre-lines for rivers, lakes, and estuaries.
- Gaps closed using local knowledge to create a continuous river network from source to mouth.

## Data content and structure
- Attributes:
  - ID: unique integer for each line segment
  - LENGTH: length in metres
  - TYPE: River, Canal, Pipe, or Misc (miscellaneous channels including estuary/lake centre-lines and some underground channels)
- Purpose: high-resolution mapping of rivers and streams; suitable for network analysis with a continuous river network at this scale.
- Related models: CEH’s IHDTM (Integrated Hydrological Digital Terrain Model) uses flow paths based on these lines and informs the Flood Estimation Handbook (FEH).

## Access and licensing
- Web Map Service (WMS) available for viewing.
- Vector dataset downloadable under licence with specific usage restrictions.
- CEH provides online tools for linking sites and identifying locations on rivers; information available via CEH.

## Quality, limitations and caveats
- Not provided as a GIS geometric network, limiting standard network analyses (e.g., tracing network paths) without bespoke tooling.
- Lacks river names; occasional inconsistent classification between River and Misc across the country.
- Canals and pipes datasets are known to be of lower quality despite overall quality control for rivers and miscellaneous channels.

## Maintenance and related work
- Significant effort to produce a single, consistent network with attribute information (e.g., river names) and to enable online tools for site linkage and location identification.
- Ongoing work and related resources available through CEH (enquiries@ceh.ac.uk).

## Practical notes for GIS specialists
- Valuable for high-resolution hydrological and network analyses when combined with IHDTM/FEH data.
- May require data cleaning, augmentation (e.g., adding river names), and possibly bespoke tooling to perform full network tracing or network-based queries.
- Be mindful of licensing restrictions and data quality caveats when using for public-facing outputs or analyses requiring precise network topology.