# CEH digital 1:50,000 river network of Great Britain

## Overview
- First of its kind in the UK; produced by the Institute of Hydrology (now CEH) from the mid-1970s to the late 1990s.
- Digitised the Ordnance Survey 1:50,000 (Landranger) blue line layer, including single and centre-lines for rivers, lakes, and estuaries.
- Gaps closed using local knowledge to create a continuous river network from source to mouth.

## Data structure and content
- Attributes:
  - ID: unique integer identifying each line segment
  - LENGTH: length in metres
  - TYPE: feature type (River, Canal, Pipe, Misc)

## Purpose and usage
- Intended for higher-resolution mapping of rivers and streams.
- Web Map Service (WMS) available for viewing; vector data downloadable under licence.
- The dataset supports network analysis (may require bespoke tools).
- CEH's Integrated Hydrological Digital Terrain Model (IHDTM) uses the same lines for flow paths; linked to FEH (Flood Estimation Handbook) via FEH software.

## Quality and limitations
- Widely used within CEH; significant caveats for general use.
- Not provided as a GIS-ready geometric network; limits standard network tracing (e.g., identifying all sources to an outlet).
- Lacks river names; potential inconsistencies between river and miscellaneous classifications.
- Canals and pipes datasets are known to be of lower quality.

## Updates and maintenance
- Efforts underway to produce a consistent, named network (e.g., within CEH's Intelligent River Network).
- Online tools exist for linking sites and identifying locations on rivers.
- For updates, contact CEH (enquiries@ceh.ac.uk).

## Access and licensing
- Viewing: WMS available.
- Download: vector dataset available under licence with usage restrictions.

## Related datasets and tools
- CEH IHDTM (Integrated Hydrological Digital Terrain Model)
- FEH (Flood Estimation Handbook) software and data (via FEH CD-ROM) for river-based flood analyses
- CEH initiatives to improve linkage between sites and river locations through online tools.