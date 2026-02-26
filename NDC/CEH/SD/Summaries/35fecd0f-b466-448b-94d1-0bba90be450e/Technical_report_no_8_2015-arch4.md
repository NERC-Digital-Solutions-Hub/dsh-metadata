# Technical Report No. 8

## Overview
- Documents internal and external quality assessment processes for the datasets: CLC2012_UK.mdb (UK including Northern Ireland and Isle of Man), CLC2012_UK_GG.mdb (Channel Isles and Guernsey), and CLC2012_UK_JE (Jersey).
- Aims to ensure harmonised, high-quality land cover maps (CLC2012) across the UK and Crown dependencies.

## Internal quality control
- Work Units (WUs) interpreted twice by two different people.
- Finished units reviewed by an independent photo-interpreter (Geoff Smith) using InterCheck software with identical imagery/ancillary data.
- Feedback from the reviewer exported as shapefiles and acted upon by interpreters before finalisation.
- Emphasis on thorough revision to maintain high-quality database.

## External quality control results
- Two remote verifications by the European Technical Team (CTT) in July 2013 and September 2014.
- External checks covered 7 WUs, representing 19% of UK coverage; included visual checks of CLC2006 revision and CLC-Changes2006-2012 layers.
- Errors recorded as points with descriptive attributes and reported for each WU; reviewed against verification reports.
- Verification outcomes categorized as Accepted (A), Conditionally accepted (CA), or Rejected (R); some WUs were reinterpreted after feedback.

## Findings and common errors
- Typical issues in CLC2006 layer:
  - Omissions of small/discontinuous built-up areas and infrastructure (industries, airports, wind turbines).
  - Confusion between continuous urban fabric (111) and Industry (121).
  - Inaccuracies in mineral extraction (131) and dumpsites (132); green urban areas (141) and sport/recreation (142).
  - Misclassification between arable (211) and pasture (231); pasture (231) vs natural grasslands (321).
  - Forest patches missing or boundaries imprecise; mixed forests issues.
  - Boundaries of moors/heathland (322) vs natural grassland (321) and peatland (412); bare rocks (332) often misclassified as sparse vegetation (333).
  - Issues with intertidal flats (423) and estuaries (522).
- Mapping of changes was generally correct, but some changes were missed or not mappable due to imagery limitations (IMAGE availability).
- Specific notes: need for imagery from IMAGE2012 to ensure change accuracy; separate >5 ha changes from complex polygons.
- Remarks and guidance applied to subsequent units to ensure high-quality final database.

## Data management and workflow implications (for Data Leaders)
- Importance of robust, two-tier QA: internal double interpretation plus independent external verification to support harmonisation across regions.
- Documentation of errors and corrective actions is essential for traceability and future improvements.
- Use of standardized validation tools (InterCheck) and consistent imagery (latest IMAGE2012) to improve reliability.
- Need to manage metadata, lineage, and updates across datasets to maintain discoverability and credibility.
- Re-interpretation of rejected units demonstrates adaptability and commitment to data quality.

## Data products and collaboration
- Datasets produced with attention to cross-border consistency to support European CLC harmonisation.
- Collaboration among the University of Leicester, Centre for Landscape and Climate Research, Specto Natura, Defra, and the European Environment Agency under an EU Copernicus programme grant.
- Acknowledges the importance of governance, transparency, and shared standards across participating organisations.

## End notes
- Main problems identified in the 2006 layer prompted further revision to improve accuracy and harmonisation.
- Full details are documented in the verification reports (Büttner, 2013; 2014).