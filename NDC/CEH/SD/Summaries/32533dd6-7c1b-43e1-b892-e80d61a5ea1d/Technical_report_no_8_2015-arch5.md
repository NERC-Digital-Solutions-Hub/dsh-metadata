# Technical Report No. 8

## Overview
- quality assessment of three CLC2012 UK datasets: CLC2012_UK.mdb (UK including Northern Ireland and Isle of Man), CLC2012_UK_GG.mdb (Channel Islands and Guernsey), and CLC2012_UK_JE (Jersey).
- focus on internal and external quality control to support harmonised European CLC2012 data.

## Datasets Covered
- CLC2012_UK.mdb: United Kingdom including Northern Ireland and Isle of Man.
- CLC2012_UK_GG.mdb: Channel Islands, Guernsey.
- CLC2012_UK_JE: Jersey.

## Internal Quality Control
- all work units (WUs) underwent internal QC.
- finished units sent to independent photo-interpreter (Geoff Smith) for validation.
- InterCheck software used with the same imagery/ancillary data as initial interpreter.
- feedback exported as shapefiles and acted upon by interpreters.
- each WU interpreted twice by two different people to ensure consistency.

## External Quality Control
- two remote verifications by the European Technical Team (CTT): July 2013 and Sept 2014.
- 7 WUs checked in total (3 in 2013, 4 in 2014), representing about 19% of UK coverage.
- methodology mirrored internal QC: visual checks of CLC2006 revision and CLC-Changes2006-2012 layers using InterCheck; errors logged as shapefile points with attributes; verification reports provided.
- results summarized in table 2.3; classifications labeled as Accepted (A), Conditionally Accepted (CA), or Rejected (R) with explanations.

## Findings and Common Issues
- Recurrent issues in CLC2006 layer revisions:
  - Omissions of small built-up areas and infrastructure (e.g., industries, airports, wind turbines).
  - Confusions between similar classes (e.g., 111 Urban Fabric vs 121 Industry; 131/132; 141/142).
  - Inaccuracies in separating land cover classes (arable 211 vs pasture 231; 231 vs natural grasslands 321).
  - Forest patches and boundaries often incomplete or imprecise; difficulty with mixed forests; moors/heathland boundaries.
  - Bare rocks (332) often misclassified as sparse vegetation (333); intertidal flats (423) and estuaries (522) require revisiting.
- Change mapping caveats:
  - reliance on IMAGE2012 imagery; some changes not mappable due to imagery availability.
  - ensure >5 ha of change is separated from complex change polygons.

## Remediation and Quality Assurance Actions
- all identified errors addressed and corrected.
- two WUs rejected during external QC were re-interpreted by a different interpreter using additional IMAGE2012 imagery.
- guidance and best-practice remarks were applied to all subsequent WUs to ensure high-quality final datasets.

## Acknowledgment
- project conducted by University of Leicester, Centre for Landscape and Climate Research, and Specto Natura.
- supported by Defra and the European Environment Agency under Grant Agreement 3541/B2012/R0-GIO/EEA.55055 (EU Copernicus Programme).

## Implications for Data Stewards
- demonstrates a robust, multi-layered quality governance framework combining internal and external QC to ensure dataset reliability and European harmonisation.
- emphasizes the importance of:
  - standardized verification tools (InterCheck) and consistent imagery/ancillary data.
  - double interpretation and independent validation to reduce biases and errors.
  - documented error reporting and remediation workflow for auditability.
  - timely updates and re-interpretation when issues are identified, including use of latest imagery.
  - clear metadata and provenance trails to enable discoverability and reuse across organisations.