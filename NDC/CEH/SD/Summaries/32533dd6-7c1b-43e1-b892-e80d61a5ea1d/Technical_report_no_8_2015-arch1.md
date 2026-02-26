# Technical Report No. 8

- Overview
  - This report documents internal and external quality assessment of three datasets: CLC2012_UK.mdb (UK including Northern Ireland and Isle of Man), CLC2012_UK_GG.mdb (Channel Islands: Guernsey), and CLC2012_UK_JE (Jersey).
  - Focus is on quality control processes, their findings, and implications for the final land cover database.

- Internal quality control (IQC)
  - All work units (WUs) underwent IQC.
  - An independent photo-interpreter (Geoff Smith) reviewed each WU using InterCheck, with the same imagery and ancillary data as the initial interpreter.
  - Feedback was returned as shapefiles; interpreters updated the WUs accordingly.
  - Each WU was interpreted twice by two different people.

- External quality control (EQC)
  - Two remote verifications by the European Technical Team (CTT) in July 2013 and September 2014.
  - Purpose: ensure UK production met standards for harmonised European CLC2012.
  - Sample: 7 WUs in total (3 + 4), representing 19% of UK coverage; checked across interpreters.
  - Method: identical to IQC, using InterCheck; errors logged as points with descriptive attributes and fed back with a verification report.
  - Verification outcomes were categorized as Accepted (A), Conditionally Accepted (CA), or Rejected (R) for each WU/layer.

- Results and typical issues
  - External verification highlighted recurring issues in the CLC2006 layer and the CLC changes 2006-2012 layer.
  - Typical problems identified:
    - Omissions of small built-up areas and infrastructure (e.g., industries, airports, wind turbines).
    - Inaccuracies between continuous urban fabric (111) and Industry (121).
    - Inaccuracies in mineral extraction (131) and dumpsites (132); green urban areas (141) and sport/recreation (142).
    - Confusion between arable (211) and pasture (231); between pasture (231) and natural grasslands (321).
    - Incomplete forest patches, imprecise forest boundaries, and misclassification of mixed forests.
    - Unclear boundaries for moors/heathland (322) vs natural grassland (321) and peatlands (412).
    - Bare rocks (332) often misclassified as sparse vegetation (333); intertidal flats (423) and estuaries (522) required revisiting.
  - Change layer considerations:
    - Care needed to use the latest IMAGE2012 imagery to map changes correctly.
    - Ensure changes >5 ha are separated from complex changes.
  - Some WUs were rejected or required re-interpretation due to the above issues or imagery limitations.

- Post-verification actions and recommendations
  - All identified errors were addressed and corrected.
  - The two WUs that were rejected were re-interpreted by a different interpreter using additional IMAGE2012 imagery.
  - General remarks and guidance were applied to all subsequent WUs to maintain high final data quality.

- Endorsement and acknowledgments
  - Acknowledged contributions from the University of Leicester (Centre for Landscape and Climate Research) and Specto Natura.
  - Supported by Defra and the European Environment Agency under the EU Copernicus Programme (grant and funding details provided).

- Implications for data quality and usability
  - Demonstrates a rigorous, multi-stage QC framework (internal and external) to ensure harmonised cross-European land cover data.
  - Highlights the critical role of up-to-date imagery, standardized classifications, and thorough revision of legacy layers.
  - Provides a documented trail for data provenance, quality flags (A/CA/R), and corrective actions to support reproducibility and usability by researchers and policymakers.