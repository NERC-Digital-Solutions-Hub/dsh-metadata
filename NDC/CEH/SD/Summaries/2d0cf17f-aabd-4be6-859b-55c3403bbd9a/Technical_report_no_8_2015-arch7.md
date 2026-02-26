# Technical Report No. 8

## Executive Summary

- Focuses on internal and external quality assessment of three datasets: CLC2012_UK.mdb (UK, including Northern Ireland and Isle of Man), CLC2012_UK_GG.mdb (Channel Islands: Guernsey), and CLC2012_UK_JE (Jersey).
- Internal quality control: workflow-wide checks where each Work Unit (WU) was interpreted twice by two different people, with an independent photo-interpreter (Geoff Smith) using InterCheck software; feedback loop implemented before finalising each WU.
- External quality control: two remote verifications by the European Technical Team (CTT) in July 2013 and September 2014 to ensure harmonised European CLC2012; 7 WUs checked externally, representing 19% of UK coverage.
- External verification method: detailed visual checks of CLC2006 revision and CLC-Changes2006-2012 using InterCheck; errors fed back as shapefile points with attributes and verification reports.
- External verification results indicate various error types and levels, informing targeted revisions.

## Datasets Covered

- CLC2012_UK.mdb: UK including Northern Ireland and the Isle of Man.
- CLC2012_UK_GG.mdb: Channel Isles, Guernsey.
- CLC2012_UK_JE: Jersey.

## Internal Quality Control

- All Work Units (WUs) underwent internal QC.
- Finished units sent to independent photo-interpreter for double-checking.
- InterCheck software used with the same imagery/ancillary data as initial interpretation.
- Feedback provided as exported shapefiles; interpreters revised accordingly.
- Every WU interpreted twice by two different interpreters.

## External Quality Control

- Two remote verifications by the European Technical Team (CTT): July 2013 and September 2014.
- Purpose: verify UK production quality to guarantee harmonised European CLC2012.
- Verification process: same InterCheck-based checks; errors documented as points with descriptive attributes; verification reports detailing error types.
- External verification covered a subset of WUs (7 WUs, 19% of UK coverage).

## External Verification Results and Typical Errors

- Verification outcomes categorized as Accept (A), Conditioned Accept (CA), or Rejected (R) per interpreter.
- Cases of note:
  - NT: Rejected due to missed forest clear-cuts; timing related to imagery availability (summer 2013 vs. later).
  - TA: Rejected due to multiple class mistakes and omissions; reinterpreted by another interpreter after feedback.
  - SN: Accepted; no major mistakes.
  - Other interpreters showed a mix of CA and R outcomes with notes on specific corrections required.
- Overall emphasis on revising the CLC2006 layer due to earlier verification findings.

## Main Problems Identified and Recommendations

- Omissions of small built-up areas (e.g., 112) and infrastructure (industries, airports, wind turbines).
- Inaccuracies separating adjacent classes (e.g., continuous urban fabric 111 vs Industry 121).
- Misclassifications in mineral extraction (131) and dumpsites (132).
- Inaccuracies separating green urban areas (141) and sport/recreation (142).
- Boundary issues between arable (211) and pasture (231), and between pasture (231) and natural grasslands (321).
- Forest patch completeness and boundary precision; some mixed forests misclassified.
- Boundary ambiguity between moors/heathland (322) and natural grassland (321) or peatland (412).
- Bare rocks (332) often misclassified as sparse vegetation (333).
- Intertidal flats (423) and estuaries (522) require revisiting.
- Change-mapping: ensure use of latest IMAGE2012 imagery; separate >5 ha of complex change; ensure accurate mapping of changes across time.
- Recommendation to perform thorough revision of inherited CLC2006 issues and address errors identified in external verifications.

## Change Mapping and Imagery Considerations

- Importance of using the latest IMAGE2012 imagery to map changes correctly.
- Need to separate more than 5 hectares of change within complex polygons.
- Some changes could not be mapped due to imagery availability; adjustments made in subsequent WUs.

## Outcome and Actions Taken

- All identified errors were addressed and corrected.
- Two WUs that were rejected during external verification were re-interpreted by different interpreters using additional IMAGE2012 data.
- Remarks and general advice from verification applied to subsequent WUs to improve final database quality.

## Acknowledgment

- Project conducted by University of Leicester, Centre for Landscape and Climate Research, and Specto Natura.
- Supported by Defra and the European Environment Agency under Grant Agreement 3541/B2012/R0-GIO/EEA.55055 in the European Union's Copernicus Programme, with EU funding.