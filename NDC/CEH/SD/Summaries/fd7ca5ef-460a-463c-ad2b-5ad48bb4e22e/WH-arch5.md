# INITIAL WATER HANDLING (WH) Version 1.1 (updated Nov 2001)

## Overview
- A protocol to measure conductivity and pH of precipitation, soil solution, and river water, and to filter samples before chemical analysis.
- Deterioration of samples is mitigated by filtration, cold storage, and, for Al and Fe, acidification.
- Requires laboratory training, appropriate equipment, and health and safety compliance.

## Data collection lifecycle and timing
- Initial storage:
  - Store in cold conditions (1–4°C) if more than 7 hours pass before measurement.
  - If not analyzed same day, return to cold storage; send samples promptly if sent to another site.
- Conductivity measurement:
  - Within 36 hours of collection on an unfiltered subsample at 25°C; results to 0.1 µS cm-1.
- pH measurement:
  - Within 36 hours on an unfiltered subsample; separate glass and reference electrodes; results to 0.01 pH unit.
- Filtering:
  - Performed within 60 hours of collection; document filtering details; use unique sample codes.
  - After filtration, analyze for specified ions and dissolved organic carbon (DOC); DOC optional for precipitation water.
- Storage prior to chemical analysis:
  - Maintain 1–4°C; aim to analyze within 16 days, but no later than 28 days.
  - If samples are sent to another location, minimize storage time and arrange next-day delivery.

## Metadata, identifiers, and traceability
- Unique sample codes must be recorded and associated with all data.
- Containers must be labeled with:
  - ECN Site Identification Code (e.g., T06)
  - ECN Measurement Code (e.g., PC)
  - Location Code (e.g., 01)
  - Sampling Date
  - Additional sampler or instrument codes as needed to uniquely identify the sample (appears with final ECN database submission).
- For volumes >100 ml, transfer a 20 ml subsample for Al and Fe determinations and acidify with 20 µl HCl.

## Data handling, quality, and documentation
- Handling and processing practices:
  - Use dedicated filter funnels, membranes, and laboratory techniques; avoid contact with filter surfaces.
  - Pre-filter soil solution (SS) and river water (WQ) if required; pre-wash filters with 250 ml distilled water.
  - Filter equipment and sample containers must be thoroughly rinsed; use forceps; one filter per sample.
- Documentation and records:
  - Record all filtering details and sample codes; maintain records for final data submission to ECN database.
  - Document bottle and vial washing procedures; ensure containers are cleaned with phosphate- and hypochlorite-free agents; use appropriate Decon products.
- Standard labeling and consistency:
  - Ensure consistent labeling and coding across all samples and datasets to support discoverability and interoperability within the ECN database.

## Safety, training, and references
- Acknowledge need for laboratory training and safety when handling acids and other reagents.
- Methods and QC procedures are supported by referenced HMSO documents and internal appendices.

## Appendices (summary)
- Appendix I. Filtering
  - Equipment: filter funnel assembly, membrane filters, glass fibre filters, vacuum pump.
  - Procedures: rinse parts, handle filters with forceps, single-use filters, possible pre-filtering for SS and WQ, aliquot 20 ml for Al/Fe when volume >100 ml, acidify as required.
  - Labeling and data capture: unique sample codes for data submission.
  - Supplier information.
- Appendix II. Bottle and vial washing
  - Cleaning agents (phosphate- and hypochlorite-free), Decon products, rinsing steps, drying and recapping protocols.
  - Maintenance schedule and supplier guidance.

## Practical implications for Data Stewards
- Ensure schema alignment with ECN database fields: site ID, measurement code, location, date, and sampler/instrument details.
- Enforce data provenance: track storage conditions, timing windows, and filtration steps to support data quality assessments.
- Support metadata completeness: capture all labeling conventions, sample IDs, and method details (Appendix I–II) in data records.
- Promote timely data availability: enforce the 36-hour measurement windows and 60-hour filtration window, with clear storage deadlines for analysis.
- Facilitate interoperability across systems: standardize units, codes, and determinands listed for analysis to enable cross-site data sharing and reuse.