# Technical Report Metadata for Corine Land Cover data 2018. UK.

- The document provides metadata for three UK Corine Land Cover (CLC) datasets: 2018 status map, 2012 revised map, and 2012–2018 change map, covering the UK plus Isle of Man, Channel Islands, Guernsey, Jersey, and Northern Ireland.
- All datasets use UK-specific coordinate systems and share consistent metadata aligned with INSPIRE/EEA standards.

## Datasets

- Dataset 1: Corine land cover 2018 (CLC2018_UK.shp)
  - Description: Final UK status map for 2018.
  - Projection/ CRS: British National Grid; Transverse Mercator; GCS_OSGB_1936; Datum D_OSGB_1936.

- Dataset 2: Corine land cover 2012 (revised) (CLC2012rev_UK.shp)
  - Description: Updated 2012 map for the UK, revised during 2018 change mapping.
  - Projection/ CRS: British National Grid; Transverse Mercator; GCS_OSGB_1936; Datum D_OSGB_1936.

- Dataset 3: Corine land changes (2012–2018) for the UK (CLC_CHA12-18_UK.shp)
  - Description: Changes between 2012 and 2018, mapped directly.
  - Projection/ CRS: British National Grid; Transverse Mercator; GCS_OSGB_1936; Datum D_OSGB_1936.

- Attribute schema (shared across datasets):
  - CLC classification codes at level 3
  - Area (hectares), length, and area of each feature
  - Remarks field and a unique ID

## Copernicus metadata and context

- Datasets are part of Copernicus Land Monitoring (CLC), UK component, with emphasis on land cover and land cover changes.
- Class structure: 44 classes in a hierarchical three-level Corine nomenclature.
- Minimum mapping units (MMU): 25 ha for status layers; 100 m minimum width for linear elements; 5 ha MMU for Land Cover Changes (LCC) in change layers.
- Purpose: support environmental monitoring, indicators, EU policy reporting (e.g., biodiversity, climate change, agriculture, Water Framework Directive).

## Metadata, language, and access

- Metadata language: English
- Metadata standard: INSPIRE-compliant with extended elements
- Online resource: http://cdr.eionet.europa.eu/gb/eea/clc/envvlpnwa/
- File identifier: CLC_metadata_UK
- Character set: UTF-8
- Access and usage: Open access with licensing conditions under EU GMES/Copernicus governance; attribution required; notes on not implying EU endorsement; ownership of results remains with EU bodies

## Spatial context and data extent

- Geographic bounding box: West -8.62, East 1.76, South 49.88, North 60.84
- Spatial resolution indicator (denominator): 100000 (1:100,000 scale guidance)

## Lineage and data production

- The UK Corine Land Cover updates for 2018 used Sentinel-2 and Landsat-8 imagery from 2017; supported by Google Earth imagery for interpretation.
- Production followed EEA technical guidelines with InterChange tooling for mapping CLC changes; revision of the 2012 map completed alongside 2018 updates.

## Quality control

- Internal quality control (University of Leicester): each Working Unit (WU) quality-checked by two interpreters; use of InterCheck software; findings fed back to interpreters and corrected before finalizing WUs.
- External quality control (European Technical Team, CTT): two remote verifications in Feb and June 2018 to ensure harmonized European CLC2018 standards; error logging and feedback provided to interpreters.

## Provenance and acknowledgement

- Project conducted by University of Leicester (Centre for Landscape and Climate Research) in collaboration with Specto Natura, funded by the European Environment Agency under Copernicus grant EEA/IDM/R0/16/009/UK.

## Metadata authors and contacts

- Originator: University of Leicester
- Custodian: Defra
- Point of contact: European Environment Agency
- Owner: European Commission - DG Enterprise and Industry (DG-ENTR)
- Topic: Environment, imagery/earth cover

## Additional notes

- The metadata package includes details about the record-keeping, governance, and licensing framework that governs distribution and use of Copernicus-derived UK CLC data.