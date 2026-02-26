# CEH digital 1:50,000 river network of Great Britain

## Collection/Generation
- The first comprehensive UK digital river network for its scale, produced by the Institute of Hydrology (now CEH) between the mid-1970s and the late 1990s.
- Digitised the "blue line" layer from the Ordnance Survey 1:50,000 2nd series (Landranger) maps, plus centre-lines for double‑sided rivers, lakes, and estuaries.
- All gaps in the source material were closed, using local knowledge where needed, to create a continuous river network from source to mouth.
- The dataset was created using manual digitising or laser scanners.

## Nature and Units of Recorded Values
- Attributes:
  - ID: unique integer identifying the line segment
  - LENGTH: length of the line segment in metres
  - TYPE: feature type, one of:
    - River
    - Canal
    - Pipe (man-made channels for transporting water such as aqueducts and leats)
    - Misc (miscellaneous channels including estuary and lake centre-lines and some underground channels)

## Purpose
- Intended for higher resolution mapping of rivers and streams.
- A Web Map Service (WMS) is available for viewing; vector data can be downloaded under licence with use restrictions.
- The combined rivers and channels network provides continuous river lines suitable for network analysis, though bespoke tools may be required.
- Used to define rivers within CEH’s Integrated Hydrological Digital Terrain Model (IHDTM) and is aligned with the FEH (Flood Estimation Handbook) workflows.

## Quality / Known Limitations
- Not provided in a format suitable as a geometric network for standard GIS analysis (limits network tracing, upstream source attribution, etc.).
- Lacks river names as attributes.
- Line classification (river vs. miscellaneous channel) may be inconsistent across the country, though subject to high-level quality control.
- Canals and pipes datasets are known to be of lower quality than rivers.

## Access, Licensing & Maintenance
- The vector dataset is downloadable under licence; licensing conditions describe use restrictions.
- A WMS is available for viewing the dataset.
- CEH has undertaken significant work to create a single, consistent network at this scale, including attribute data such as river names (e.g., within the Intelligent River Network) and online tools to link sites and identify locations.
- For further information or updates, contact CEH (enquiries@ceh.ac.uk).