# Technical Report No. 8

## Overview
- Reports on internal and external quality assessment of CLC2012 UK datasets: CLC2012_UK.mdb (UK including Northern Ireland and Isle of Man), CLC2012_UK_GG.mdb (Channel Islands, Guernsey), and CLC2012_UK_JE (Jersey).
- Emphasizes a rigorous QA workflow to ensure a harmonised European CLC2012 baseline.

## Internal Quality Control
- All work units (WUs) underwent internal QC.
- Finished units were reviewed by an independent photo-interpreter (Geoff Smith) using the same imagery and ancillary data as the initial interpreter.
- InterCheck software used; feedback delivered as exported shapefiles and addressed by interpreters.
- Each WU was interpreted twice by two different people, ensuring double-checks.

## External Quality Control
- Two remote verifications by the European Technical Team (CTT) in July 2013 and September 2014.
- Seven WUs reviewed (19% of UK coverage), representing early project work and later contributions.
- Process mirrored internal QC: visual checks of CLC2006 revision and CLC-Changes2006-2012 layers with InterCheck; errors recorded as points with descriptive attributes; verification reports provided.

## External Verification Results and Typical Issues
- Documented results per WU include revision layer status, change layer status, verification dates, interpreters, and comments (A = Accepted, CA = Conditionally Accepted, R = Rejected).
- Typical problems identified in the CLC2006 layer:
  - Omissions of small or discontinuous built-up areas and infrastructure (e.g., industries, airports, wind turbines).
  - Misclassification between close classes (e.g., urban fabric vs. Industry; arable vs. pasture; pasture vs. natural grasslands).
  - Boundary precision issues for forest patches, moors/heathlands, and peatlands; confusion in sparse vs. dense vegetation.
  - Issues with intertidal flats and estuaries; general need for clearer delineation of certain land-cover types.
- Change mapping generally correct but some missed changes due to limited summer 2013 imagery.
- Important methodological notes:
  - Use the latest IMAGE2012 imagery to ensure correct change mapping.
  - Separate changes greater than 5 ha from complex change polygons.
- All identified errors were addressed; two WUs initially rejected were re-interpreted by a different interpreter using additional IMAGE2012 images.

## Implications for Data Leaders
- Demonstrates a robust, multi-tier QA workflow essential for reliable data products.
- Highlights the value of independent verification to achieve data harmonisation across a larger European dataset.
- Underlines the need for up-to-date imagery and clear change delineation practices to maintain data quality and usability.
- Shows the importance of documenting errors and corrections (via shapefiles and detailed verification reports) to support traceability, metadata quality, and future data governance.
- Indicates ongoing collaboration and feedback loops between production teams and external reviewers to improve data standards and consistency.

## Datasets and Scope Details
- Data products are delivered as structured geospatial databases (MDB format) and accompanying verification artifacts.
- The project involved collaboration among the University of Leicester (Centre for Landscape and Climate Research), Specto Natura, with support from Defra and the European Environment Agency under a EU grant.

## Acknowledgement
- Acknowledges contributions from University of Leicester, Centre for Landscape and Climate Research, Specto Natura; funded by Defra and EEA under the EU's Copernicus/European Union programme.