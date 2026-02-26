# Technical Report No. 8

## Overview of datasets
-, Datasets covered: CLC2012_UK.mdb (UK including Northern Ireland and Isle of Man), CLC2012_UK_GG.mdb (Channel Islands, Guernsey), and CLC2012_UK_JE (Jersey).
- Purpose: internal and external quality assessment of land cover maps generated for these regions.

## Internal quality control
- All work units (WUs) underwent internal QC.
- Finished WUs were sent to an independent photo-interpreter ( Geoff Smith ) for evaluation using the same imagery and ancillary data.
- InterCheck software used for verification; feedback returned as exported shapefiles and implemented by interpreters.
- Each WU was interpreted twice by two different people to ensure consistency.

## External quality control
- Two remote verifications by the European Technical Team (CTT) occurred in July 2013 and September 2014.
- Purpose: ensure UK-produced data aligns with harmonised European CLC2012 standards.
- Verification covered 7 WUs (about 19% of UK coverage), representing work from multiple interpreters over time.
- Process mirrored internal QC, using InterCheck; errors recorded as points with descriptive attributes and accompanied by verification reports detailing error types.

## Findings from external verification
- Verification results highlighted the ongoing importance of revising the CLC2006 layer due to prior inaccuracies.
- Typical error types identified:
  - Omissions of discontinuous built-up areas (112) and infrastructure (industries, airports, wind turbines).
  - Misclassifications between continuous urban fabric (111) and Industry (121).
  - Inaccuracies in mineral extraction (131) and dumpsites (132); green urban areas (141) and sport/recreation (142).
  - Misclassifications between arable (211) and pasture (231); confusion between pasture (231) and natural grasslands (321).
  - Incomplete forest patches; boundaries of forests and mixed forest issues.
  - Unclear boundaries for moors/heathland (322) vs. natural grassland (321) and peatland (412).
  - Bare rocks (332) often misclassified as sparse vegetation (333).
  - Intertidal flats (423) and estuaries (522) require revisiting.
- Mapping of changes generally correct, but some changes missed due to imagery limitations; important considerations included using IMAGE2012 imagery and separating >5 ha of change from complex changes.
- Two WUs were rejected and re-interpreted by a different interpreter after feedback and with updated imagery; other remarks were applied to subsequent WUs.

## Common issues and recommended actions
- Emphasis on revising the inherited issues from CLC2006 and applying updates based on latest imagery.
- Ensure use of IMAGE 2012 for accurate change mapping.
- Properly separate large changes (>5 ha) within complex change polygons.
- Ongoing feedback integration to improve subsequent WU interpretations.

## Outcomes and corrective actions
- All identified errors were addressed and corrected.
- The two early WUs that were rejected were re-interpreted by different interpreters; feedback informed subsequent processing to improve data quality.

## Acknowledgement
- Project conducted by the University of Leicester, Centre for Landscape and Climate Research, and Specto Natura.
- Supported by Defra and the European Environment Agency under Grant Agreement 3541/B2012/R0-GIO/EEA.55055 in the European Unionernicus Programme, with funding by the European Union.