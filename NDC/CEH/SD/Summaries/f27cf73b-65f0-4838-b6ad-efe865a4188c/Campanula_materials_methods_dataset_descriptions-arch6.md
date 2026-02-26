# Campanula rotundifolia cytotype and common garden study data

- Overview
  - A large-scale collection and analysis of Campanula rotundifolia across Britain, Ireland, and contextually elsewhere, focusing on cytotype variation and how it relates to growth, phenology, and fecundity.
  - Data governance includes sample provenance, cytotype verification, and a common garden experiment to compare tetraploid, pentaploid, and hexaploid clones.

- Plant material: sampling and provenance
  - >1300 samples (seeds, leaves, or stem cuttings) from nearly 900 geo-referenced locations across diverse habitats.
  - Emphasis on Britain and Ireland; some samples from elsewhere for broader context.
  - Many samples collected by volunteers; samples from multiple plants per locality when possible to avoid clonal redundancy.
  - Sample handling and storage practices:
    - Leaves and cuttings stored cool for transport; seeds air-dried and seeds stored at 4°C; dried leaf material stored at -20°C.
    - Propagation material kept as clonal material for the common garden study.
  - Location data and anonymity:
    - Cytotype and location details stored in campanula_cytotype.csv with 0.01° resolution.
    - GPS or Ordnance Survey sources used; higher-resolution data preserved in original records but generalized to protect site privacy.
  - Special sampling efforts:
    - Targeted intensive sampling in Wanlockhead (SW Scotland), Teesdale (central England), and Cheddar (southern England) due to reports of hexaploids outside typical range.
  - Material retention:
    - Excess samples retained in cold storage at CEH Edinburgh for potential future use.

- Cytotype determination: methods and verification
  - Historical cytotype counts via root-tip cytology; later verification by flow cytometry for calibration.
  - Flow cytometry protocol (aligned with standard Doležel et al. 2007):
    - Internal standard: Pisum sativum L. 'Ctirad' (2C = 9.09 pg).
    - Sample prep: leaf tissue chopped with standard buffer, stained with propidium iodide, RNase treatment to avoid RNA staining.
    - Analysis: flow cytometers (BD FACSCalibur or BD Accuri C6) with standard gating to isolate nuclei; peak height comparisons against internal standard for DNA content.
    - Quality checks: replicate analyses if peak CV > 5%.
  - Data handling:
    - Cytotype assignments stored in campanula_cytotype.csv; discrepancies resolved by reanalysis with fresh samples.
    - Stored materials may yield slightly higher DNA content estimates; such samples excluded from mean DNA content calculations when appropriate.
  - Data integrity notes:
    - Some samples analyzed in groups or from stored/dried material excluded from mean cytotype calculations to maintain accuracy.

- Common garden study: design and execution
  - Setup:
    - Clonal material produced from field-collected seeds/cuttings in a glasshouse; planted October 2008 in a raised bed next to CEH Edinburgh glasshouses.
    - Site characteristics: natural tetraploid region nearby; 55.86°N, 3.21°W; 190 m elevation.
    - Experimental design: five randomized blocks; includes tetraploid, pentaploid, and hexaploid clones; 55 tetraploid, 1 pentaploid, and 37 hexaploid clones distributed across blocks.
    - Management: no pollination restrictions; occasional weeding.
  - Phenology (flowering timing):
    - First flowering date (FFD) recorded daily in 2009 and 2010; FFD defined as the date the first flower is sufficiently open for bee visitation.
    - Data stored in campanula_FFD.csv.
  - Growth and fecundity assessments:
    - August 2009: counting total flowering stems per plant; measuring three random flowering stems per plant in blocks 1 and 3; data stored in Dest_harvest_Aug_2009_blocks_1_and_3.csv.
    - September 2009: harvesting above-ground parts in blocks 2 and 5; measuring total flowering stems and drying stems for biomass data; data stored in Dest_harvest_Sept_2009_blocks_2_and_5.csv.
  - Data collection notes:
    - Block structure and clone codes documented to link phenology and growth data with cytotype status.
    - Data entries flagged for dead plants or missing data with an asterisk.

- Description of data files and data structure
  - Campanula_cytotype.csv
    - Columns: Country, Location, Sample code, Latitude, Longitude, Cytotype
  - campanula_FFD.csv
    - Columns: Block number, Clone code, Date of first flowering in 2009, Day number in 2009, Plant condition notes 2009, Date of first flowering in 2010, Day number in 2010, Plant condition notes 2010
  - Dest_harvest_Aug_2009_blocks_1_and_3.csv
    - Columns: Block number, Clone code, Total number of flowering stems, Height of stem 1, Number of swollen seedheads on stem 1, Number of other seedheads on stem 1, Number of open flowers on stem 1, Number of buds on stem 1, (repeat for stems 2 and 3), Plant condition notes
  - Dest_harvest_Sept_2009_blocks_2_and_5.csv
    - Columns: Block number, Clone code, Total stem dry weight, Number of flowering stems
  - Notes:
    - Asterisks indicate dead plants or missing data.
    - Data are arranged in columns within each file; sample codes link across files to the same clone and cytotype.

- Data quality, limitations, and provenance
  - High-level QA: double-checking cytotype assignments via flow cytometry; reanalysis for discordant results; exclusion of certain samples from mean DNA content calculations due to storage/drying effects.
  - Anonymization: precise locality data generalized to 0.01° grid to protect site privacy; original precise coordinates retained in internal records.
  - Sampling gaps and challenges:
    - Non-uniform sampling across locales; some localities yield single plants, limiting clonal diversity representation per site.
    - Patchy sampling in hexaploids outside typical ranges necessitated targeted follow-ups.
  - Data integration: cross-referencing across multiple data files via clone codes and sample codes to enable multi-dimensional analyses (cytotype, phenology, growth, and fecundity).

- Potential data products and reuse
  - Public or restricted-access datasets enabling:
    - Cytotype distribution analysis across geographic gradients.
    - Relationships between ploidy level and flowering phenology, growth rates, and seed production.
    - Comparative analyses of growth and phenology across ploidy groups in a controlled common garden environment.
  - Data products could include dashboards or pivot views linking cytotype with FFD, stem counts, biomass, and seed production for end-user exploration.

- References (methodological context)
  - Flow cytometry protocols and nuclear DNA content estimation (Doležel et al. 2007; Greilhuber et al. 2007).
  - Foundational taxonomy and prior cytotype observations (McAllister 1972; Stevens, Wilson, McAllister 2012).
  - Figure 1 details layout of clones within the common garden study for replication and interpretation.