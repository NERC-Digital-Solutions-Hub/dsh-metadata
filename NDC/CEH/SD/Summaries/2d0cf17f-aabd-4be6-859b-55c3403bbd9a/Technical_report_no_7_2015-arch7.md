# Centre for Landscape and Climate Research Department of Geography Technical Report No. 7

## Overview
- Metadata report for Copernicus Land - CORINE Land Cover (CLC) 2012 datasets covering the UK (including Northern Ireland and the Isle of Man) and the Channel Islands (Guernsey and Jersey).
- Documents three MDB datasets with three layers each: CLC-Changes (2006-2012), CLC2006revised, and CLC2012.
- Purpose: support map-based GIS visualisations and analysis of land cover and land cover change.

## Datasets and technical details

- Dataset 1: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for the UK
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Projection/CRS: British National Grid; Transverse Mercator; GCS_OSGB_1936; Datum D_OSGB_1936

- Dataset 2: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for Guernsey
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Projection/CRS: Guernsey Grid; Transverse Mercator; GCS_WGS_1984; Datum D_WGS_1984

- Dataset 3: Corine land cover 2006 (revised), 2012 and changes (2006-2012) for Jersey
  - Filename: CLC2012_UK.mdb
  - Layers: CLC-Changes (2006-2012), CLC2006revised, CLC2012
  - Projection/CRS: New JTM (Transverse Mercator); GCS_ETRF_1989; Datum D_ETRF_1989

## Metadata framework and standards

- Metadata language: English
- Metadata basis: INSPIRE-compliant (EEA metadata profile with some extended elements)
- Online resource and links provided for metadata and contact points

## Geographic extent and resolution

- Extent: West -8.62, East 1.76, South 49.88, North 60.84
- Spatial resolution: 1:100,000

## Dataset description and lineage

- Abstract: CLC 2012 and CLC changes (2006-2012) as part of Copernicus Land; time series from 1990 with updates through 2012; 44-class Corine nomenclature; MMU 25 ha for status layers; MMU 5 ha for changes
- Purpose: monitoring land cover, environmental change indicators, and support for EU policies (biodiversity, climate, agriculture, Water Framework Directive)
- Methodology: products based on photointerpretation of satellite imagery (2011-2013); Google Earth imagery used to support interpretation; reliance on InterChange for mapping CLC changes

## Access, licensing, and usage constraints

- Data access governed by EU Regulation 1159/13 (granting conditions for GMES/Copernicus data)
- Open access with attribution; users must acknowledge source; modifications must be stated; EU ownership considerations apply

## Contact, acknowledgments, and provenance

- Point of contact: University of Leicester (Originator), Defra (Custodian), European Environment Agency (Owner)
- Acknowledgments: University of Leicester, The Centre for Landscape and Climate Research, Specto Natura; supported by Defra and EEA under EU Copernicus funding

## Implications for GIS practice

- Enables map-based visualization of land cover and changes at 1:100,000 scale across the UK and Channel Islands
- Provides three-layer structure per jurisdiction for change analysis, historical revision, and current status
- Requires handling of multiple coordinate systems; ensure proper on-the-fly or re-projection in GIS workflows
- Metadata adheres to INSPIRE/EEA standards, facilitating data integration and interoperability within GIS projects and policy analyses