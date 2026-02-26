# INITIAL WATER HANDLING (WH) Version 1.1 (updated Nov 2001)

- Purpose and scope
  - Protocol for measuring conductivity and pH of precipitation, soil solution, and river water samples.
  - Includes filtration of samples prior to chemical analysis to slow deterioration through filtration, cold storage, and (for Al and Fe) acidification.
  - Acknowledges need for laboratory training, equipment, and health and safety compliance; references background quality control documents.

- Data collection and timing requirements
  - Initial storage: store samples at 1–4°C if more than seven hours before measurement; return to cold storage if filtration is not completed the same day.
  - Conductivity: measure within 36 hours of collection on an unfiltered subsample at 25°C; report to 0.1 µS cm⁻¹.
  - pH: measure within 36 hours on an unfiltered subsample; use separate electrodes; report to 0.01 pH unit.
  - Filtering: perform within 60 hours of collection; record filtering details; filter according to Appendix I; after filtration, analyze for specified ions and DOC (DOC optional for precipitation water).
  - Data capture: unique sample codes must be used; determine priority if sample volume is insufficient for all determinands.

- Sample handling, storage, and analysis timeline
  - Storage: 1–4°C prior to analysis.
  - Analysis window: ideally within 16 days of collection, and definitely within 28 days.
  - If analyses occur remotely, minimize time out of cold storage and use expedited delivery when possible (e.g., next-day delivery).

- Measurement, analysis workflow and determinands
  - After filtration, analyze for: Na⁺, K⁺, Ca²⁺, Mg²⁺, Fe²⁺, Al³⁺, NH₄⁺-N, Cl⁻, NO₃⁻-N, SO₄²⁻, PO₄³⁻, alkalinity, and DOC (DOC optional for some samples).
  - Separate documentation exists for chemical analysis (prioritization of determinands if sample volume is limited).

- Sample labeling, metadata, and data submission
  - Use unique sample identifiers with codes: ECN Site Identification Code, ECN Measurement Code, Location Code, Sampling Date, and sampler code.
  - The final data submitted should include this unique reference to enable database integration (ECN).

- Safety, training, and quality control
  - Some procedures require lab training and chemist guidance, and adherence to health and safety for handling acids and concentrated reagents.
  - Guidance and QA/QC procedures are documented in referenced Protocols and related documents.

- Appendices and equipment
  - Appendix I: Filtering
    - Equipment: filter funnel assembly, membrane filters (0.45 µm), glass fibre filters, vacuum pump (~0.5 bar vacuum).
    - Contamination control: rinse all contact surfaces with deionised/distilled water; use forceps; single-use filters per sample; pre-filtering may be required for soils/rivers.
    - Sample handling: if volume >100 mL, take a 20 mL subsample for Al/Fe and acidify; label all containers with the standardized coding.
  - Appendix II: Bottle and vial washing
    - Cleaning agent free of phosphate and hypochlorite; use appropriate washing equipment or Decon-90 soaking; rinse steps with tap and deionised water; air-dry and re-cap containers for reuse with the same sampler.

- Documentation and supplier references
  - Author references include J.K. Adamson (HMSO, 1978, 1988) for conductivity and pH methodologies.
  - Suppliers listed for filtering components and lab consumables (e.g., BDH, Millipore).

- Data governance implications for Data Stewards
  - Enforce standardized metadata and sample identification to support discoverability and reuse.
  - Ensure complete data pipelines with time-bound measurement windows, storage conditions, and documentation.
  - Maintain provenance through explicit reference to method versions, appendices, and supplier details.
  - Require accompanying documentation (protocols and QA/QC references) with datasets to support reproducibility.
  - Ensure data uploads to ECN database include the unique sample references and all relevant contextual metadata (site, measurement, location, date, sampler).