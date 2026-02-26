# Collection/Generation

## Overview
- The CEH digital 1:50,000 river network of Great Britain was the first of its kind in the UK.
- Produced by the Institute of Hydrology (now CEH) from the mid-1970s to the late 1990s; led by Roger Moore and Dave Morris with later minor modifications.
- Digitised the Ordnance Survey 1:50,000 2nd series (Landranger) blue line layer, including single blue lines and centre-lines from double rivers, lakes, and estuaries.
- Gaps in source material were closed using local knowledge to create a continuous river network from source to mouth.

## Nature and Units of Recorded Values
- Attributes include:
  - ID: unique integer identifying the line segment
  - LENGTH: length of the line segment in metres
  - TYPE: feature type, one of River, Canal, Pipe, Misc (miscellaneous channels including estuary, lake centre-lines, and some underground channels)

## Purpose
- Intended for higher-resolution mapping of rivers and streams.
- Web Map Service (WMS) available for viewing; vector data downloadable under licence with specified restrictions.
- Combined rivers and channels provide continuous river lines suitable for network analysis, though bespoke tools may be required.
- CEH's Integrated Hydrological Digital Terrain Model (IHDTM) defines flow paths based on these lines and is used to support the Flood Estimation Handbook (FEH), accessible via the FEH CD-ROM.

## Quality/known Limitations
- Widely used within CEH science and integral to FEH analyses.
- Not suitable for general use due to caveats:
  - Not available in a GIS geometric network format, limiting common GIS analyses (e.g., tracing network paths, identifying contributing sources).
  - No river names included; possible inconsistent classification between river and miscellaneous channels.
  - Canals and pipes datasets are known to be of lower quality.
- Data have undergone quality controls, but limitations remain.

## Updates and Maintenance
- Substantial work completed to produce a single, consistent networked dataset with attribute enhancements (e.g., river names) within CEH's Intelligent River Network.
- Online tools developed to link sites and identify locations on the rivers.
- For additional information or updates, contact CEH (enquiries@ceh.ac.uk).