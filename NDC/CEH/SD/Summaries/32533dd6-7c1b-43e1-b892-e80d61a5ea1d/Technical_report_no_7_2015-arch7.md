# Technical Report No. 7

## Executive-focused overview for GIS specialists
- Documents metadata and core characteristics of three Corine Land Cover (CLC) datasets for the UK, Guernsey, and Jersey, covering CLC 2012 and changes from 2006–2012.
- Datasets are organized as three layers each: CLC-Changes (2006-2012), CLC2006revised, and CLC2012.
- Data intended to support consistent, map-based land cover visualization and change detection across UK regions, with careful attention to projection, datum, and licensing.

## Datasets overview

- Dataset 1: UK (Corine land cover 2006 revised, 2012, and changes 2006-2012)
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Spatial reference: British National Grid
  - Projection: Transverse Mercator
  - Geographic coordinate system: GCS_OSGB_1936
  - Datum: D_OSGB_1936

- Dataset 2: Guernsey (Corine land cover 2006 revised, 2012, and changes 2006-2012)
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Spatial reference: Guernsey Grid
  - Projection: Transverse Mercator
  - Geographic coordinate system: GCS_WGS_1984
  - Datum: D_WGS_1984

- Dataset 3: Jersey (Corine land cover 2006 revised, 2012, and changes 2006-2012)
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Spatial reference: New Jersey Transverse Mercator (New JTM)
  - Projection: Transverse Mercator
  - Geographic coordinate system: GCS_ETRF_1989
  - Datum: D_ETRF_1989

## Copernicus CORINE metadata context (2012)
- Date: 2015-01-09
- Purpose: Metadata for Copernicus Land - CORINE land cover (CLC) 2012 and CLC changes (2006-2012) for the UK, aligned with GMES/Copernicus initial operations.
- Scope: European-wide land cover inventory with 44 classes; aims to support environmental monitoring, policy indicators, and reporting.
- Methodology: Based on photointerpretation of satellite imagery (2011–2013) with supporting aerial imagery (Google Earth); follows EEA technical guidelines and InterChange mapping workflow.
- MMU and classification: MMU 25 ha for status layers; LCC changes MMU 5 ha.
- Integration: National inventories into a seamless Europe-wide layer.

## Technical metadata and access details
- Metadata standard: INSPIRE-compliant (EEA metadata profile) with some extended elements.
- Extent: Global bounding region for UK; geographic bounds listed (West -8.62, East 1.76, South 49.88, North 60.84).
- Spatial resolution: Denominator 100000 (scale ~1:100,000).
- Lineage: Update to reference year 2012; base imagery from 2011–2013; Google Earth imagery used to support interpretation; no up-to-date national map for UK at this update; prior LCM2007 used for comparison.
- Data access: Free, full, and open access with conditions:
  - Acknowledge data source(s) and origin
  - Do not imply EU endorsement of user activities
  - State if data has been adapted or modified
  - EU ownership/right-of-use constraints apply as described
- Metadata language: English (ENG); character set: UTF-8
- Metadata author/date: University of Leicester; 2015-01-09
- Acknowledgments: Funded by Defra and the European Environment Agency under Copernicus/GMES; project partners include Specto Natura.

## Practical implications for GIS work
- Use these datasets to visualize land cover and detect 2006–2012 changes for the UK and Crown dependencies with consistent classification and projection schemes.
- Ensure proper handling of multiple coordinate systems (UK: OSGB 1936, Guernsey WGS84, Jersey ETRF89) and transform where necessary for integrated analysis.
- Leverage the three-layer structure (CLC2012, CLC2006revised, CLC-Changes) to perform change detection, accuracy assessments, and historical comparisons.
- Be mindful of licensing and attribution requirements when distributing or publishing derivatives.