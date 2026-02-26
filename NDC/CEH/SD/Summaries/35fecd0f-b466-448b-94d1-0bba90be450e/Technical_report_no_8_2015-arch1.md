# Technical Report No. 8

## Overview
- Assesses internal and external quality control measures for three datasets: CLC2012_UK.mdb (UK including Northern Ireland and Isle of Man), CLC2012_UK_GG.mdb (Channel Isles, Guernsey), and CLC2012_UK_JE (Jersey).
- Aim is to support a harmonised European CLC2012 through thorough verification and correction processes.

## Quality Control Processes

- Internal quality control
  - Working Units (WUs) interpreted by two different people.
  - Independent photo-interpreter (Geoff Smith) reviewed using InterCheck with the same imagery/ancillary data.
  - Feedback provided as shapefiles; interpreters revised accordingly until completion.

- External quality control
  - Two remote verifications by the European Technical Team (CTT) in July 2013 and Sept 2014.
  - Seven WUs checked in total (about 19% of UK coverage); diverse interpreters represented.
  - Verification used InterCheck; errors documented as points with attributes and returned with verification reports.

## External Verification Findings

- Typical errors identified (in CLC2006 layer) included:
  - Omissions of small/discontinuous built-up areas and infrastructure (industries, airports, wind turbines).
  - Confusion between continuous urban fabric (111) and Industry (121).
  - Inaccuracies in mineral extraction (131) and dumpsites (132).
  - Inaccuracies in green urban areas (141) and sport/recreation (142).
  - Difficulties distinguishing arable (211) vs. pasture (231), and pasture (231) vs. natural grasslands (321).
  - Forest patches, boundaries, and mixed forests; moors/heathland vs. natural grassland/peatland boundaries; bare rocks vs. sparse vegetation; intertidal flats (423) and estuaries (522).
- Emphasis on revising the inherited CLC2006 layer to improve accuracy.

## Change Mapping and Imagery

- Changes were generally mapped correctly but some missed changes occurred due to limited satellite imagery at the time.
- Important guidance:
  - Use the latest IMAGE2012 imagery for change mapping.
  - Separate greater than 5 ha of change from complex polygons.

## Revisions and Improvements

- All identified errors were addressed.
- Two WUs that were initially rejected were re-interpreted by different interpreters using additional IMAGE2012 imagery.
- Feedback had broader implications, with remarks applied to subsequent WUs to improve overall quality.

## Data Source and Collaboration

- Acknowledges collaboration between:
  - University of Leicester, Centre for Landscape and Climate Research
  - Specto Natura (consultancy)
  - Defra and the European Environment Agency
- Funded under the European Union’s GNSS/EEA framework (European Union funding for the Copernicus/EGI program).

## Implications for Use

- Highlights the importance of thorough, repeated quality checks for harmonisation across Europe.
- Demonstrates the need for up-to-date imagery and careful handling of change detection to ensure consistent mapping across datasets.
- Provides a documented process for QA which supports reliability for analysts relying on data-driven insights and cross-border comparisons.