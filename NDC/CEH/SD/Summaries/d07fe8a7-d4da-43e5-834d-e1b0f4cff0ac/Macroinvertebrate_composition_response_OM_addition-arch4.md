# Macroinvertebrate composition of Welsh upland rivers in response to organic matter addition

## Experimental design and sampling regime
- Study uses a before-after-control-impact (BACI) design with upstream reference (control) and downstream experimental zones within each stream.
- Zones are similar in length and habitat; a 20–50 m gap ensures independence between zones.
- Time periods:
  - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013); no manipulation; both zones treated equally.
  - After period (T2): 57–62 days (Jan to Mar 2013); experimental zone receives leaf litter addition; reference zone remains unmanipulated.
- Leaf litter manipulation:
  - One-tonne bags containing deciduous leaves (oak, birch, alder) added proportionally to experimental zone at start of T2 to simulate natural senescence.
  - Vegetable net bags maintained to ensure minimum wet weight of 1.7 kg m⁻² in experimental zone.
  - Additional 630 kg (wet weight) of leaf litter added on 12 Feb and 5 Mar 2013 following two large storm events.
- Sampling framework:
  - Six random macroinvertebrate samples per reach on five occasions (Jan, Feb, Mar, Apr, May 2013).
  - Samples preserved on-site in 70% industrial methylated spirit (IMS); later processed in the lab. 

## Collection methods and laboratory procedures
- Field method: Surber net sampler (area 0.1 m², mesh 330 µm, depth 10 cm).
- Laboratory processing: samples rinsed, macroinvertebrates separated from debris, preserved in 70% IMS.
- Taxonomic work: identification to species level where possible; otherwise genus, family, or coarse levels.
- Body measurements: Size1 and Size2 in millimetres recorded for each individual; notes indicate whether measurement is head width or body length.
- Instrumentation: microscope used for identification.

## Data structure and recorded variables
- Data files: flatbed CSV format.
- Surber data (11 columns):
  - site_code, region, month, time (Before/After), landuse, reach (Experimental/Control), replicate, taxon_name, Size1, Size2, Comment.
- Variable specifics:
  - Taxon_name: lowest possible taxonomic resolution.
  - Size1/Size2: body measurements in mm; comments indicate correspondence (e.g., head width, body length).
- Metadata and supporting records:
  - Miscellaneous supporting documents include site_description.csv with 10 columns (site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment) and related site descriptions.

## Data quality, provenance, and notes for reuse
- Calibration steps and quality control: Not documented.
- Data provenance: field collection details, sampling schedule, and leaf litter manipulation described; specimen processing and taxonomic identification methods outlined.
- Data accessibility considerations for data leaders:
  - Clear BACI design and explicit upstream/downstream roles aid integration with data systems and governance frameworks.
  - Metadata includes geographic coordinates, elevations, catchments, and survey campaigns to support discoverability and cross-dataset linkage.
  - Data granularity includes temporal (monthly sampling), spatial (multiple sites/zones), and biological (taxon-level with size metrics) dimensions.
- Potential improvements for future reuse:
  - Include calibration/quality control procedures and data validation steps.
  - Provide data processing workflows and versioning to enhance reproducibility.