# Cellulolytic decomposition of Welsh upland rivers in response to organic matter addition

## Overview
- Study of cellulolytic decomposition response to organic matter addition in Welsh upland rivers using a before-after-control-impact (BACI) design.
- Each stream has an upstream reference zone and a downstream experimental zone with a 20–50 m separation to ensure independence.
- The experiment comprises a before period (T1: early Nov 2012–early Jan 2013) with no manipulation, and an after period (T2: Jan–Mar 2013) during which the experimental zone received leaf litter additions.
- Leaf litter was delivered via 1-tonne bags containing oak, birch, and alder leaves, with additional leaf material added on two dates after storm events.
- Data capture focuses on tensile strength of calico cotton strips as a proxy for cellulolytic decomposition, with calculations of percent loss relative to controls.

## Experimental design and sampling regime
- BACI design with:
  - Upstream reference (control) zone and downstream experimental (manipulated) zone per stream.
  - Similar zone length, habitat structure, slope, flow, land use; 20–50 m between zones.
- Before period (T1): 61–65 days (early Nov 2012–early Jan 2013); no manipulation; both zones treated equally.
- After period (T2): 57–62 days (early Jan–Mar 2013); experimental zone receives leaf litter throughout T2.
- Leaf litter additions:
  - Initial delivery of leaf litter from 1-tonne bags (oak, birch, alder) proportional to experimental zone area.
  - Vegetation nets used to maintain a minimum wet weight (1.7 kg m^-2) in the experimental zone.
  - Additional 630 kg (wet weight) of leaf litter added on 12 Feb 2013 and 5 Mar 2013 after two large storm events.

## Data collection and processing methods
- Experimental units: Six cotton strips placed randomly in each reach (experimental sites) before and after manipulation.
- Sample handling:
  - Strips recovered at end of T1 and T2, frozen at -20°C.
  - In laboratory: rinsed in tap water, oven-dried to constant mass at 65°C.
  - Tensile strength measured with a Hounsfield machine (25 kN load cell, 40 mm test gap); one breaking_strain estimate per strip.
  - Three untreated control strips included to account for transit and washing losses.
- Related literature cited for methodology (e.g., Jenkins et al. 2013; Hladyz et al. 2011; Layer et al. 2010; Jenkins et al. 2013).

## Data structure and recorded values
- Data are stored as flatbed CSV files.
- Core dataset (cellulolytic decomposition):
  - Columns: site_code, region, date, time, landuse, reach, replicate, exposure, breaking_strain, %_loss.
  - breaking_strain: measured in Newtons.
  - %_loss: percent loss of tensile strength relative to the control batch.
  - exposure: number of days exposed.
- Supporting metadata:
  - DURESS_CU_site_description.csv with 10 columns: site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment.
  - Site metadata includes geographic coordinates, elevation, survey campaign, and river catchment.

## Data quality, calibration, and control
- Calibration steps: none specified.
- Quality control: none explicitly stated for the main dataset; use of replicate strips (A–F) and control strips to assess non-manipulation-related losses.
- Data integrity notes:
  - Samples preserved and processed consistently (frozen, dried, and tested with standardized equipment).
  - References linked to external literature; caution advised regarding long-term link persistence (external URLs may not be permanent).

## Metadata and provenance considerations for Data Stewards
- Datasets include explicit experimental design details (BACI structure, zones, timing, leaf litter treatments) essential for reproducibility and secondary analysis.
- Key variables and units are clearly defined (breaking_strain in Newtons; %_loss as a computed metric).
- Site-level context provided via site_description dataset to support geospatial analyses and cross-referencing with catchment data.
- Potential reuse aspects:
  - Enables meta-analyses of litter-induced cellulolytic activity across streams.
  - Supports metadata-driven discovery (site_code, region, coordinates, landuse, survey campaigns).
- Data sharing and governance considerations:
  - Ensure alignment with CEH Data Catalogue records or equivalent repositories.
  - Maintain provenance by linking main data with site descriptions and referenced literature.
  - Consider data licensing, citation requirements, and future link maintenance to external literature.

## Access, reuse, and cataloging considerations for Data Stewards
- Ensure the data are discoverable via the CEH Data Catalogue or equivalent metadata records.
- Provide clear data dictionaries and unit specifications in metadata to aid interoperability.
- Link the main dataset to the site_description file and to relevant literature references to support context and re-use.
- Anticipate potential interoperability challenges across systems and formats when integrating with other datasets (e.g., differing sample types, lab equipment, or measurement protocols).