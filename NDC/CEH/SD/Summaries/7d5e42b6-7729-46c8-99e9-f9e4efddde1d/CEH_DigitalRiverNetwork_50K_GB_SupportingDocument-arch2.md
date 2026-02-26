# The CEH digital 1:50,000 river network of Great Britain

## Overview
- First of its kind in the UK, developed by the Institute of Hydrology (now CEH) from the mid-1970s to the late 1990s.
- Digitised the Ordnance Survey 1:50,000 (Landranger) blue line layer to create a continuous river network from source to mouth.
- Includes single blue-line rivers, plus centre-lines for double-sided rivers, lakes, and estuaries; gaps closed with local knowledge.

## Data collection/generation
- Methods: manual digitising and laser scanning.
- Attributes per line segment: 
  - ID: unique integer
  - LENGTH: metres
  - TYPE: River, Canal, Pipe, or Misc (miscellaneous channels including estuary and lake centre-lines)
- Purpose: high-resolution mapping; suitable for network analyses; WMS available for viewing; vector data downloadable under licence.
- Relationship to other datasets: forms the basis for CEH’s IHDTM flow paths, aligned with FEH definitions.

## Data characteristics and related datasets
- IHDTM flow paths are defined on the same lines and are consistent with IHDTM grids.
- FEH (Flood Estimation Handbook) uses these definitions; FEH software and data accessible via the FEH CD-ROM.

## Quality and limitations
- Not provided as a GIS-ready geometric network, limiting certain standard GIS analyses (e.g., tracing along a defined network, source-contributions to outlets).
- May lack river names; classification between River and Misc can be inconsistent across the country.
- Canals and pipes datasets are known to be of lower quality.
- Data have undergone quality control, but caveats remain for general use.

## Applications and integration
- Widely used within CEH science and central to Flood Estimation Handbook analyses.
- CEH’s Intelligent River Network adds river names and enhanced attributes; efforts to link sites and identify locations via online tools.

## Access, licensing, and data management
- Availability:
  - Web Map Service (WMS) for viewing
  - Vector data for download under licence (usage restrictions apply)
- Data management: ongoing work to provide a single consistent network with enriched attributes and online tools; data and updates are managed by CEH.
- Contact for information: enquiries@ceh.ac.uk

## Maintenance and future developments
- Significant work already completed to create a consistent, name-enriched network (Intelligent River Network).
- Continued development of online tools for site linking and location identification; aims to improve broader data accessibility and reuse.