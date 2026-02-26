# WH Protocol

## Overview
- Purpose: To measure the conductivity and pH of samples of precipitation, soil solution, and river water, and to filter these samples prior to chemical analysis.
- Rationale: Samples deteriorate after collection; to slow deterioration, use filtration, cold storage (1–4°C), and, for Al and Fe determinations, acidification. Safety and training requirements apply for certain steps and chemical handling.
- Scope: Covers initial handling, measurement, filtering, storage prior to analysis, and related documentation.

## Data governance considerations for Data Stewards
- Standardization: Clear procedures and criteria to ensure comparable data across sites (units, measurement methods, timing).
- Metadata and provenance: Require unique sample identifiers and codes, including ECN Site Identification Code, ECN Measurement Code, Location Code, Sampling Date, and sampler code; capture sequencing of steps and any deviations.
- Data quality and traceability: Document filtering details, sample volumes, and determinand priorities when volumes are insufficient; record laboratory and equipment used.
- Timeliness and updates: Adhere to defined time windows to minimize degradation; minimize cold storage interruptions during transit; document next-step destinations if samples are sent elsewhere.
- Safety and training: Acknowledge that some activities require laboratory training and compliance with health and safety requirements; guidance from chemists may be necessary.

## Procedures, time windows, and data elements
- Initial storage and handling
  - Store samples cold (1°C–4°C) if >7 hours elapse before conductivity/pH measurement.
  - If filtering is not completed the same day as measurements, return samples to cold storage; in-transit samples must be kept in a cool box with pre-frozen blocks.
- Conductivity measurement
  - Measure within 36 hours of collection on an unfiltered subsample at 25°C; express results to 0.1 µS cm⁻¹.
  - Conductivity must be measured before pH on the same subsample; do not return the subsample to the main sample after measurement.
- pH measurement
  - Measure within 36 hours of collection on an unfiltered subsample; use a separate glass and reference electrode as specified.
  - Express results to two decimal places (0.01 pH unit).
- Filtering
  - Complete filtering within 60 hours of collection following Appendix I procedures.
  - Record filtering details using unique sample codes; after filtration, analyze for a suite of determinands in a prioritized order if sample volume is limited.
  - Post-filtration storage: store filtered samples at 1°C–4°C; analysis should occur within 16 days, and definitely within 28 days of collection.
  - Al and Fe determinations may require acidification; if volume permits, transfer a 20 mL subsample from each sample and acidify with 20 µL HCl.
- Chemical analysis prerequisites
  - Analyses target: dissolved Na⁺, K⁺, Ca²⁺, Mg²⁺, Fe²⁺, Al³⁺, NH₄⁺–N, Cl⁻, NO₃⁻–N, SO₄²⁻, PO₄³⁻, alkalinity, and dissolved organic carbon (DOC; optional for some waters).
  - A priority order is defined for determinands when sample volume is insufficient to measure all.
- Documentation and data submission
  - Ensure unique reference codes accompany data submitted to ECN database.
  - Document work performed on each dataset as part of dataset provenance.

## Sample labeling and metadata
- Labeling requirements
  - Contain ECN Site Identification Code (e.g., T06), ECN Measurement Code (e.g., PC), Location Code (e.g., 01), Sampling Date, plus any sampler/instrument codes to uniquely identify the sample.
- Data capture considerations
  - Record all steps, timings, and any deviations to maintain a complete data lineage from collection to analysis.

## Storage, transport, and safety
- Storage
  - Maintain 1°C–4°C storage conditions; ensure analyses occur within 16–28 days.
- Transport
  - Minimize out-of-cold-storage time during transit; aim for next-day delivery and avoid Friday dispatch if possible to reduce weekend storage.
- Safety and equipment
  - Some steps require trained personnel and specialized equipment; follow health and safety guidelines; consult chemists for chemical analyses and handling of acids.

## Appendix highlights (data-relevant practices)
- Appendix I: Filtering
  - Required equipment: filter funnel assembly, membrane filters (0.45 µm), glass fibre filters, vacuum pump.
  - Handling: avoid touching filters and contact surfaces with hands; use forceps; dedicate a filter per sample.
  - Pre-filtering: soil solution and river water may require pre-filtering through glass fibre filters, washed with 250 mL distilled water before use.
  - Subsampling for metals: for volumes >100 mL, transfer a 20 mL subsample for Al and Fe determinations; acidify with 20 µL HCl.
  - Sample labeling: use the following fields—ECN Site Identification Code, ECN Measurement Code, Location Code, Sampling Date, and additional sampler codes; apply to final data submission.
  - Suppliers and components: specific catalogs for filters, membranes, and labware; detailed rinsing and handling routines to ensure sample integrity.

- Appendix II: Bottle and vial washing
  - Cleaning protocol: first use and then approximately every six months or after heavy soiling; use cleaning agents free of phosphate and hypochlorite.
  - Decontamination options: Decon products or Decon-90 for manual cleaning; run rinses with tap water and then deionized/distilled water; air-dry containers in a clean environment and cap promptly.
  - Documentation: maintain records of cleaning intervals and methods; ensure containers are ready for reuse with the same sampler.

## Compliance and quality assurance
- Emphasizes training, proper equipment, and adherence to documented procedures to ensure reliable data across sites.
- Requires traceable documentation, standardized metadata, and a clear data lineage from collection through analysis to reporting.