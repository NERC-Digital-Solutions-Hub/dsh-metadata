# CEH digital 1:50,000 river network of Great Britain

## Overview and provenance
- First of its kind in the UK, produced by the Institute of Hydrology (now CEH) from the mid-1970s to the late 1990s.
- Digitised the blue line layer from Ordnance Survey 1:50,000 (Landranger) maps, creating a continuous river network from source to mouth.

## Data structure and attributes
- Three attributes per line segment:
  - ID: unique integer
  - LENGTH: length in metres
  - TYPE: River, Canal, Pipe (man-made channels), or Misc (including estuary and lake centre-lines)
- Web access: a Web Map Service (WMS) is available; the vector dataset can be downloaded under licence with usage restrictions.

## Purpose and use
- Intended for high-resolution mapping of rivers and streams.
- Supports network analysis (though may require bespoke tools).
- Aligns with CEH's IHDTM (Integrated Hydrological Digital Terrain Model) flow paths and FEH (Flood Estimation Handbook) definitions.

## Interoperability and usage within policy frameworks
- FEH integration via IHDTM-consistent rivers; used to inform flood modelling and related environmental health monitoring.
- Provides the data backbone for location linking and site identification in hydrological assessments.

## Limitations, quality, and governance
- Not a GIS-ready geometric network; standard GIS network analyses (e.g., tracing sources to outlets) are limited without additional processing.
- May lack river names; possible inconsistencies in classifying lines as River vs Misc across the country.
- Canal and Pipe datasets are known to be of lower quality.
- Licensing restricts usage; publicly sharing underlying datasets can pose barriers to reuse.
- Metadata gaps may impede quick verification of suitability for particular monitoring needs.
- Requires data transformation to enhance usability for some analyses.

## Updates, maintenance, and access
- Ongoing efforts to produce a consistent, networked dataset with richer attributes (e.g., river names) within CEH’s Intelligent River Network.
- Online tools exist for linking sites and identifying locations on rivers.
- For information or access, contact CEH (enquiries@ceh.ac.uk).