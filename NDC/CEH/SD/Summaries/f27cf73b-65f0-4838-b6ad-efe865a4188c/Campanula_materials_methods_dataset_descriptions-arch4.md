# Campanula rotundifolia cytotype and common garden study

- Scope and aim
  - Large-scale collection of Campanula rotundifolia material to determine cytotypes and examine how ploidy influences growth, phenology, and fecundity in a common garden setting.
  - Emphasis onBritain and Ireland with broader context from elsewhere; many samples collected by volunteers.
  - Data designed for integration with wider ecological and cytogenetic research, with careful metadata to support reuse.

- Plant material and sampling
  - Over 1300 samples (seeds, leaves, or stem cuttings) from about 900 geo-referenced locations across diverse habitats.
  - Both field-collected material and material from commercial suppliers or Botanic Gardens; some samples from volunteers.
  - Storage and propagation: leaf material dried or stored at -20°C, seeds air-dried and kept at 4°C; cuttings rooted in a cool glasshouse for clonal propagation.
  - Sampling design
    - Preference for more than one plant per locality with at least 5 m between plants to reduce clonal sampling, though in many cases only a single plant per locality was found.
    - Targeted intensive sampling in known hexaploid-outlier areas (Wanlockhead, Teesdale, Cheddar) to map their extent.
  - Geographic data and privacy
    - Location details provided at 0.01° resolution in campanula_cytotype.csv; coordinates derived from GPS or Ordnance Survey maps to protect site anonymity.

- Cytotype determination and flow cytometry
  - Baseline cytotype data partially validated by prior root-tip cytology; flow cytometry used to calibrate and confirm cytotypes.
  - Protocol
    - One-step flow cytometry per Doležel et al. (2007) with internal standard Pisum sativum L. 'Ctirad' 2C = 9.09 pg and propidium iodide.
    - Sample prep involves chopping leaf tissue with standard, filtration, RNase treatment, and PI staining; analysis performed on BD FACSCalibur or Accuri C6 cytometers.
    - Data analysis includes gating to remove debris/doublets, and calculating DNA content from test vs. standard peak means.
    - Reanalysis performed if multiple peaks indicated mixed cytotypes; inconsistent results resolved by repeating with fresh material.
  - Data management and quality control
    - Stored/dried samples tended to yield higher DNA content estimates and were excluded from mean cytotype DNA-content calculations.
    - Samples analyzed in groups excluded from mean calculations; full CV check (CV ≤ 5%) required for accepting peak data.
  - Output
    - campanula_cytotype.csv contains sample metadata, coordinates, and assigned cytotype; links to detailed sample information.

- Common garden study design
  - Propagation and planting
    - Clonal material produced in a glasshouse from cuttings or seed-derived plants from field locations within two preceding years.
    - Planting in October 2008 in a raised bed near CEH Edinburgh, with local topsoil and 20% grit, in 0.3 x 0.4 m spacing.
  - Ploidy treatments and layout
    - Five randomized blocks including tetraploid, pentaploid, and hexaploid clones.
    - Blocks contain 55 tetraploid, 1 pentaploid, and 37 hexaploid clones across layout in Figure 1.
  - Management
    - Randomized blocks; pollination not restricted; occasional weeding to reduce competition.

- Phenology and growth assessments
  - Phenology (FFD)
    - Daily monitoring in 2009 and 2010 to record the first flowering date (FFD) when a flower was sufficiently open for bees.
    - Data stored in campanula_FFD.csv.
  - Growth and fecundity
    - August 2009: counted total flowering stems per plant; measured height and seedhead metrics on stems (three stems per plant sampled in some blocks).
    - September 2009: destructive harvest of blocks 2 and 5; measured total stem dry weight and number of flowering stems.
    - Data stored in Dest_harvest_Aug_2009_blocks_1_and_3.csv and Dest_harvest_Sept_2009_blocks_2_and_5.csv.

- Data files and structure
  - Campanula_cytotype.csv
    - Columns include: Country, Location, Sample code, Latitude, Longitude, Cytotype.
  - campanula_FFD.csv
    - Columns: Block number, Clone code, Date of first flowering in 2009 and 2010 (and day-number conversions), plant condition notes.
  - Dest_harvest_Aug_2009_blocks_1_and_3.csv
    - Columns: Block number, Clone code, total flowering stems, stem height, seedhead counts, open flowers, buds per stem (3 stems per plant across blocks 1 and 3), plant condition notes.
  - Dest_harvest_Sept_2009_blocks_2_and_5.csv
    - Columns: Block number, Clone code, total stem dry weight, number of flowering stems.
  - Data notes
    - An asterisk (*) marks dead plants or missing data; datasets organized by columns with clone codes linking observations across files.

- Key considerations, caveats, and data quality
  - Geographic data anonymization reduces precision to protect sites.
  - Stored vs fresh material affects DNA-content estimates; filtered accordingly for cytotype analyses.
  - Some samples were excluded from mean DNA content calculations due to storage effects or group analysis.
  - Availability of multi-year phenology data provides insight into flowering dynamics across ploidy levels.

- References
  - Flow cytometry and nuclear DNA content methodologies (Doležel et al. 2007; Greilhuber et al. 2007).
  - Foundational cytogenetic and ecological literature on Campanula rotundifolia (McAllister 1972; Stevens et al. 2012).