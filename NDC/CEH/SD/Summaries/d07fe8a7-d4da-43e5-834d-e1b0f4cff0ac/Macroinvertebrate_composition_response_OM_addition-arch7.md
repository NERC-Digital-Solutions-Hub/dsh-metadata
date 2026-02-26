# Macroinvertebrate composition of Welsh upland rivers in response to organic matter addition

- Purpose: Evaluate how macroinvertebrate communities in Welsh upland rivers respond to organic matter (leaf litter) addition using a BACI (before-after-control-impact) design.

- Experimental design and sampling regime:
  - Each stream has an upstream reference (control) zone and a downstream experimental zone, separated by 20–50 m for independence.
  - Time periods:
    - Before (T1): 61–65 days from early Nov 2012 to early Jan 2013; both zones untreated.
    - After (T2): 57–62 days from Jan to Mar 2013; experimental zone received leaf litter addition.
  - Leaf litter manipulation:
    - One-tonne bags containing oak, birch, and alder leaves were proportionally distributed by zone area and placed above the experimental zone.
    - Additional leaf litter (630 kg wet weight) added on 12 Feb and 5 Mar 2013 after storm events.
  - Sampling: Six random macroinvertebrate samples per reach on five occasions (Jan–May 2013).

- Collection methods and instrumentation:
  - Surber net sampler (area 0.1 m2, mesh 330 µm, depth 10 cm).
  - Samples preserved on-site in 70% IMS; lab processing involved rinsing over a 350 µm sieve and preservation in 70% IMS.

- Taxonomy, measurements, and data types:
  - Identification to species level where possible; otherwise genus, family, or coarse levels.
  - Body size measurements (Size1 and Size2) in millimeters; correspondence noted (head width vs. body length).
  - Data captured in flatbed CSV files with 11 columns per Surber sample (site_code, region, month, time, landuse, reach, replicate, taxon_name, Size1, Size2, and a size-related measurement link).
  - Quality control: none documented.

- Data structure and ancillary metadata:
  - Primary data: Surber data in CSV format.
  - Columns include: site_code, region (basin), month, time (Before/After), landuse, reach (Experimental or Control), replicate, taxon_name, Size1, Size2, plus a readme-style comment.
  - Supporting site description CSV: site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment.

- Geospatial and map-ready aspects:
  - Spatial references include British National Grid coordinates and WGS84 latitude/longitude.
  - Distinguishes experimental vs control reaches within streams, enabling spatial analyses of litter manipulation effects on taxa distribution.

- Temporal coverage:
  - Data collected across five months (January–May 2013) with prior baseline (November 2012–January 2013) and after-period manipulation (T2).

- Potential GIS applications:
  - Visualize spatial distribution of macroinvertebrate taxa across streams and habitats.
  - Overlay with land-use and catchment data to assess drivers of community change.
  - Analyze pre- and post-manipulation differences at the reach level (experimental vs control) over time.
  - Integrate size metrics for biovolume or functional trait analyses in GIS-enabled workflows.