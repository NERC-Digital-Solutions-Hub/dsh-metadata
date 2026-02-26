# Campanula rotundifolia: Cytotype determination and a common garden study

- Overview
  - Collected and analyzed >1700 samples (seeds, leaves, stem cuttings) from geo-referenced locations, mainly Britain and Ireland; some samples from elsewhere for context.
  - Samples stored and transported under cold conditions; seeds germinated, cuttings rooted in glasshouse; leaf material stored at -20°C.
  - Wherever possible, multiple samples per locality were taken with at least 5 m between plants to avoid clonal redundancy; intensified sampling in areas with known hexaploids outside the western range.
  - Location data are provided at 0.01° resolution to preserve site anonymity; excess material stored at CEH Edinburgh identified by sample codes.

- Cytotype determination
  - Some chromosome counts were previously established; flow cytometry used to calibrate and verify, with repeats if conflicts occurred.
  - Flow cytometry method and controls
    - One-step protocol (Doležel et al. 2007) using internal standard Pisum sativum L. 'Ctirad' (2C = 9.09 pg) and propidium iodide (PI).
    - Sample prep: leaf tissue chopped with standard, filtered, RNase treatment, PI staining; adjust test:standard ratios to equalize peak heights.
    - Instruments: FACSCalibur or Accuri C6; daily calibration; gating to exclude debris/doublets; data analyzed with Cyflogic (FACSCalibur) or standard Accuri software.
    - Quality control: repeat analyses if peak coefficients of variation >5%.
  - Data handling and cytotype assignment
    - Genome size (pg DNA) plotted alongside known chromosome-counted samples.
    - Cytotypes assigned by broad ranges: diploid 2.27–2.71 pg, tetraploid 4.22–4.96 pg, pentaploid 5.33–5.65 pg, hexaploid 6.2–7.14 pg.
    - Samples outside these ranges flagged as aneuploids.

- Common garden study
  - Clonal material generated in a glasshouse from field-collected seeds and cuttings; planted in October 2008 in a raised bed near CEH Edinburgh (55.86°N, 3.21°W; 190 m a.s.l.).
  - Experimental design
    - Five randomised blocks incorporating tetraploid, pentaploid, and hexaploid clones; total 55 tetraploid, 1 pentaploid, 37 hexaploid clones.
    - Layout shown in Figure 1; no pollination restrictions; weeding conducted to reduce competition.
  - Phenology and growth data collection
    - Phenology: First flowering date (FFD) recorded daily in 2009 and 2010 (FFD determined when the first flower was open to bees).
    - Growth and fecundity: 
      - August 2009: counts of flowering stems per plant, stem height, swollen seedheads, open flowers, flower buds for up to three stems per plant (Blocks 1 and 3).
      - September 2009: harvest of above-ground parts (Blocks 2 and 5); total stem dry weight and number of flowering stems.
  - Data files associated with common garden data
    - campanula_FFD.csv: Block, Clone code, 2009 and 2010 FFD dates (and day-number conversions), plant condition comments.
    - Dest_harvest_Aug_2009_blocks_1_and_3.csv: Block, Clone, total flowering stems, stem height (stem 1), seedhead counts, flower counts, and condition notes for stems 1–3.
    - Dest_harvest_Sept_2009_blocks_2_and_5.csv: Block, Clone, total stem dry weight, number of flowering stems.
  - Data interpretation notes
    - Asterisks indicate dead plants or missing data.
    - Clone codes link back to cytotype information in campanula_cytotype.csv.

- Data files and metadata (structure)
  - Campanula_cytotype.csv: Country, Location, Sample code, Latitude, Longitude, Cytotype.
  - campanula_FFD.csv: Block, Clone code, Date of first flowering (2009), Day number (2009), plant condition comments (2009), Date of first flowering (2010), Day number (2010), plant condition comments (2010).
  - Dest_harvest_Aug_2009_blocks_1_and_3.csv: Block, Clone code, metrics on flowering stems, stem 1 height, seedhead counts, flower counts, and condition notes for stems 1–3.
  - Dest_harvest_Sept_2009_blocks_2_and_5.csv: Block, Clone code, total stem dry weight, number of flowering stems.
  - Column annotations indicate dead/missing data with “*” and cross-linking between files via clone and sample codes.

- References and methodology context
  - Flow cytometry methodology and genome size estimation (Doležel et al. 2007) used for cytotype assignments.
  - Prior chromosome counts and phylogeographic context referenced for interpretation (e.g., Shepherd 2007; McAllister 1972; Stevens et al. 2012).

- Practical implications for data governance (Data Stewards perspective)
  - Provenance and traceability: clear linkage from field samples to cytotype assignments to controlled, replicated common garden data.
  - Metadata completeness: well-documented file structures, column definitions, and sample codes to enable reuse and cross-study integration.
  - Anonymization of location data: geographic precision reduced to 0.01° to protect site privacy while preserving analysis capability.
  - Data quality controls: explicit QC criteria (e.g., CV threshold, repeat analyses) and handling of problematic samples (desiccated/coloured leaves excluded from DNA content analyses).
  - Storage and stewardship: samples stored at CEH Edinburgh; multiple data formats prepared for robust sharing and long-term preservation.
  - Interoperability considerations: multiple data files with interlinked identifiers; potential challenges in aligning across formats and ploidy categories; careful documentation essential for reuse.

- References
  - Doležel J, Greilhuber J, Suda J (2007). Estimation of nuclear DNA content in plants using flow cytometry. Nature Protocols.
  - McAllister HA (1972); Shepherd JR (2007); Stevens CJ et al. (2012) for context on Campanula rotundifolia.

- Note on study layout
  - Figure 1 depicts the clonal arrangement across five blocks in the common garden study, illustrating the sampling and replication structure used for phenology and growth measurements.