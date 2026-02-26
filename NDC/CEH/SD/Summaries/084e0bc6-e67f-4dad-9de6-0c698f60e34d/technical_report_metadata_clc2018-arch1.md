# Technical Report Metadata for Corine Land Cover data 2018. UK.

## Overview
- UK component of Copernicus CORINE Land Cover (CLC) data for 2018, including three datasets: CLC2018_UK.shp, CLC2012rev_UK.shp, and CLC_CHA12-18_UK.shp.
- UK coverage includes Isle of Man, Channel Islands (Guernsey, Jersey), and Northern Ireland.
- Attribute tables include CLC level-3 classification codes, area (ha), length, area of features, remarks, and a unique ID.

## Datasets

- Dataset 1: Corine land cover 2018 (CLC2018_UK.shp)
  - Status map for the UK for 2018.
  - Projection: British National Grid; Projection: Transverse Mercator; Geographic: GCS_OSGB_1936; Datum: D_OSGB_1936.

- Dataset 2: Corine land cover 2012 (revised) for the UK (CLC2012rev_UK.shp)
  - Updated 2012 map produced during 2018 change-mapping process.
  - Same spatial properties as dataset 1.

- Dataset 3: Corine land changes (2012-2018) for the UK (CLC_CHA12-18_UK.shp)
  - Changes between 2012 and 2018 mapped directly.
  - Same projection and datum as above.

## Metadata and standards

- Copernicus land monitoring metadata; English language; INSPIRE-compliant metadata with extended elements.
- Base parameters: 44 Corine classes; minimum mapping unit (MMU) for status maps is 25 hectares; minimum width of linear elements is 100 metres; MMU for land cover changes (LCC) is 5 hectares.
- Data lineage: 2017 Sentinel-2 and Landsat-8 imagery; support imagery from Google Earth; produced using InterChange with EEA guidelines to revise the 2012 map.
- Purpose: provide consistent land cover and land cover change information for Europe and support environmental indicators and EU policy monitoring.

## Spatial and licensing details

- Geographic extent: West -8.62, East 1.76; South 49.88, North 60.84.
- Spatial resolution: 1:100,000 denominator.
- Metadata file: CLC_metadata_UK; language: English; encoding: UTF-8.
- Access limitations: governed by Commission delegated regulation EU No 1159/13 (regarding GMES data) and related provisions; open access with conditions:
  - Acknowledge data source when distributing or publishing.
  - Do not imply official EU endorsement of user activities.
  - Indicate if data have been adapted or modified.
  - EU ownership of information and data produced under Copernicus funding.

## Provenance and lineage

- Lineage: Corine Land Cover UK updated for 2018; main objective to detect and map land cover changes above 5 ha; imagery basis: 2017 Sentinel-2 and Landsat-8; supported by Google Earth imagery.
- Produced to align with European technical guidelines for CLC and to harmonize UK outputs with European CLC 2018.

## Quality control and verification

- Internal quality control by University of Leicester; each mapping unit (WU) independently checked by two interpreters; InterCheck software used; feedback returned and corrections applied.
- External quality control by European Technical Team (CTT) in Feb and June 2018; remote verifications covered multiple WUs; errors logged as shapefile points with descriptive attributes and corrective reports provided to interpreters.

## Access, hosting, and contacts

- Originator: University of Leicester (Centre for Landscape and Climate Research).
- Custodian: Defra.
- Point of contact: European Environment Agency.
- Owner: European Commission - DG Enterprise and Industry (DG-ENTR).
- Topic: Environment; Imagery base maps / earth cover.
- File identifier: CLC_metadata_UK.

## Acknowledgments

- Project conducted by University of Leicester, Centre for Landscape and Climate Research, and Specto Natura.
- Funded by the European Environment Agency under Grant Agreement EEA/IDM/R0/16/009/UK via the EU Copernicus Programme.