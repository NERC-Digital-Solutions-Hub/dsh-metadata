# Benthic organic matter of Welsh upland rivers in response to organic matter addition

## Study design and scope
- Uses a before-after-control-impact (BACI) design with upstream reference and downstream experimental zones within each stream.
- Zones are similar in length and habitat; a 20–50 m separation ensures independence.
- Timeline:
  - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013); no manipulation; both zones treated equally.
  - After period (T2): 57–62 days (early Jan to March 2013); experimental zone receives leaf litter addition throughout.
- Leaf litter manipulation:
  - One-tonne bags containing deciduous leaves (oak, birch, alder) added to the experimental zone at the start of T2.
  - Vegetation net bags maintained to keep a minimum wet weight of 1.7 kg/m2 in the experimental zone.
  - Additional 630 kg (wet weight) of leaf litter added on 12 Feb 2013 and 5 Mar 2013 after storm events.
- Data collected from multiple streams; random placement within the experimental zone using poles.

## Data collection and processing
- BOM sampling: six random samples of benthic organic matter per reach, five sampling occasions (January–May 2013) using a Surber net (0.1 m2 area, 330 µm mesh, 10 cm depth).
- On-site preservation in 70% IMS; laboratory processing involved removing macroinvertebrates, drying to constant weight, and ash-free conversion by combusting a subset at 550°C for 5 hours to correct for inorganic content.
- Measurements: organic matter stocks weighted to 0.01 g; data expressed as grams of organic matter.
- Data management tools used: Surber sampling and a weight-meter in the lab.

## Data structure and metadata
- Primary BOM data format: flatbed CSV with 10 columns:
  - site_code (sampling site)
  - landuse (basin land-use)
  - region (stream basin)
  - time (Before or After manipulation)
  - month (sampling month)
  - reach (Experimental or Control)
  - replicate (replicate code)
  - surber_area (area of the Surber in m2)
  - cpom (coarse particulate organic matter, g)
  - fpom (fine particulate organic matter, g; note: described similarly in text)
- Supporting metadata:
  - Site Description CSV containing 10 columns: site_code, name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment.
  - Location data include grid references and coordinates for geospatial context.

## Quality, provenance, and limitations
- Calibration steps: None documented.
- Quality Control: None documented beyond standard lab processing steps; ash-free correction applied to a subset of samples.
- Potential data considerations:
  - Ensure clarification of cpom vs. fpom units if metadata show inconsistencies (text lists both as coarse, which may indicate a labeling issue).
  - Temporal alignment with sampling months and BACI design (Before/After, Jan–May sampling).
  - Multi-stream BACI design requires careful linking of site_code to zone type (Experimental vs Control) and time.

## Data management and sharing readiness for Data Stewards
- Data format is CSV, which is widely usable for data portals.
- Rich metadata available via site descriptions and core BOM dataset, aiding discoverability and reuse.
- The BACI design provides context for analyses on organic matter response to added leaf litter, supporting data governance around experiment provenance and time-series structure.
- Action items for data stewardship:
  - Verify and standardize cpom/fpom labeling and units across datasets.
  - Validate completeness of metadata (e.g., all streams, zones, replicates properly coded).
  - Ensure linkage between BOM data and Site Description for spatial analyses.
  - Document any QC steps (or lack thereof) to inform data users about reproducibility and limitations.
  
## Timeline and context
- Study period spans late 2012 to spring 2013, focusing on the response of benthic organic matter to deliberate organic matter augmentation in upland Welsh rivers.