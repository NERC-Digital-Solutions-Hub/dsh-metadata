# Macroinvertebrate leaf decomposers of Welsh upland rivers in response to organic matter addition

- A BACI (before-after-control-impact) field experiment across 8 Welsh upland streams to test how added leaf litter affects macroinvertebrate leaf decomposers.
- Each stream has an upstream reference zone and a downstream experimental zone, separated by 20–50 meters to maintain independence.

## Spatial design and geography

- Study units: 8 streams, each with paired reference (upstream) and experimental (downstream) zones.
- Within-stream arrangement ensures similar habitat structure and hydrology between zones.
- Geo-referenced data available via site description file, including:
  - Site_code, Eastings, Northings, Latitude, Longitude, Elevation (metres).
  - Region (stream basin), Catchment, Land use, and grid references.
  - Reach designation indicating Experimental or Control site.
- Data suitable for GIS mapping of stream location, zone type, and sampling points; allows integration with other spatial layers (land use, catchment, hydrology).

## Temporal design

- Timeline: before period (T1) Nov 2012–Jan 2013; after period with leaf litter manipulation (T2) Jan–Mar 2013.
- Leaf litter manipulation:
  - 1 tonne bags of oak, birch, alder leaves deployed above experimental zone at start of T2; additional leaf litter (630 kg wet weight) added on 12 Feb and 5 Mar after storm events.
- Sampling schedule includes:
  - T1 (before) and T2 (after) litter bag collections, with subset replacements to measure decomposition during the manipulation period.
  - Some samples left in situ for ~18 weeks (T18) and others collected at end of T2.

## Data collection and processing

- Litter bags:
  - Nylon mesh bags (two mesh sizes): fine (500 µm) and coarse (5 mm) to regulate invertebrate colonisation.
  - Each bag filled with five grams of air-dried leaves; 48 replicate bags per stream (24 reference, 24 experimental) for each mesh type.
  - Bags deployed in pairs on metal poles and covered with cobbles to facilitate colonisation.
- Collection and lab processing:
  - Bags collected at T1 and T2; additional bags deployed during T2.
  - On return to lab: contents rinsed through 250 µm sieve; leaf material air-dried; macroinvertebrates identified to species where possible; some taxa identified to genus/family if species-level was not possible.
  - Identifications conducted visually; microscopy used for lab work.
- Data and metadata:
  - Field records and lab results stored in two main data structures: bag data and site description data.
  - Supporting site description file includes coordinates and catchment context.

## Data structure and variables

- Bag data (10 columns):
  - site_code, region, date, time (Before/After manipulation), landuse, reach (Experimental or Control), Replicate, BagMesh (leaf bag type), taxon_name, abundance.
- Site description (10 columns in site description file):
  - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey Campaign, Catchment.
- Data are provided as flat CSV; taxa identified to species when possible, otherwise genus/family or coarse levels.

## Taxonomy and units

- Units: invertebrate abundance per bag.
- Taxonomic resolution:
  - Species-level identification where possible; some taxa identified at genus, family, or coarser levels (e.g., Chironomidae, Oligochaeta).

## Quality control and limitations

- No formal quality control steps documented.
- Taxonomic resolution varies by specimen; potential inconsistencies in identification depth.
- Temporal and spatial sampling constraints (8 streams; discrete time points) limit extrapolation beyond study conditions.
- The dataset is designed for spatial analyses across streams and temporal comparisons before vs after leaf litter addition.

## How to use for GIS and data products

- Join bag data to site description data on site_code to create spatial layers of sampling locations, zones (reference vs experimental), and temporal stages (T1, T2, T18).
- Create maps of:
  - Experimental vs control reach design within each stream.
  - Leaf litter manipulation zones overlaid with land use and catchment context.
  - Abundance of key taxa across mesh types and time periods.
- Build time-series or BACI-style analyses by linking date, reach type, and abundance per taxon.
- Explore data quality and standardization by examining taxonomic resolution and consistency across streams and sampling periods.