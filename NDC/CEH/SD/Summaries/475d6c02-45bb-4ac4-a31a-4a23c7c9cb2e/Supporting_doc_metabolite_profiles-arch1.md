# Supporting Documentation for Untargeted metabolomic profiles of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

- Aim and scope
  - Untargeted metabolomic profiling of paired cultures of four Streptomyces strains isolated from a Minnesota nature reserve.
  - Investigates how metabolism changes in adjacent interacting bacterial cultures; samples taken daily from day 2 to day 6.

- Data format and accessibility
  - Raw LC-MS data provided as open-source mzML files (mass-to-charge, elution time, ion counts, metadata).
  - Data collected in both positive and negative ionisation modes.
  - mzML format is readable by common metabolomics software (e.g., UmetaFlow).

- Experimental design and sampling
  - Bacteria grown as adjacent pairs on solid ISP2 medium; daily sampling for days 2–6.
  - Each pairing prepared in quadruplicate (n=20 total per pairing) to allow metabolite and RNA sampling in triplicate daily (with one spare).
  - Four strains tested in pairwise interactions; includes background controls labeled as “agar” (no microbes present).

- File naming and metadata
  - Naming convention: [n/p] - [2/3/4/5/6] - [A/B/C/D/agar] - [1/2/3]
    - n/p: negative or positive ionisation mode.
    - 2–6: day post inoculation.
    - First letter: bacterial strain; second letter: neighbouring cultured strain (agar indicates a background control).
    - If no second letter, neighbour equals the first strain.
    - Last digit: replicate number.

- Culturing and media
  - Spores standardized to 1 × 10^9 CFU/mL in 20% glycerol; diluted 10-fold to 1 × 10^8 CFU/mL in ISP2 broth.
  - Inoculation: 4 μL onto ISP2 agar, placed 1 cm apart in pairs.
  - ISP2 recipe provided (yeast extract, malt extract, glucose, agar optional, pH 7.2).

- Metabolite extraction
  - Metabolites extracted from rectangular agar plugs (including mycelia and surrounding agar).
  - Extraction: 1 mL of precooled 100% methanol (-48 °C) with three freeze–thaw cycles; centrifugation and collection of supernatant.
  - Drying, reconstitution in 200 μL 20% methanol, sonication, filtration prior to injection.

- LC-MS data acquisition
  - Instrumentation: Q Exactive Plus mass spectrometer with Ultimate 3000 UHPLC; Hypersil GOLD C18 column.
  - Mobile phases: A = water + 0.1% formic acid; B = methanol + 0.1% formic acid.
  - Gradient and run conditions: 95% A for 2 min, linear gradient to 95% B over 8 min, 2 min hold, return to 95% A, re‑equilibrate; 40 °C column; 0.4 mL/min; 5 μL injection.
  - Quality controls: blank injections at batch start/end; pooled QC every 6th injection; randomized sample sequence.
  - Data acquisition: full MS scans in both positive and negative modes; m/z 90–1350, resolution 70,000; AGC target 3e6; max IT 200 ms.

- Data processing and related datasets
  - Raw data converted to mzML format; this deposit contains mzML files.
  - Analyzed peak datasets are available in a separate related deposit.
  - Metadata and instrument settings embedded in mzML; open-source compatibility emphasized.

- Experimental replication and quality control
  - Biological triplicates for sampling and analysis; multiple timepoints with destructive sampling.
  - Randomized sequence to mitigate systematic bias; blank and QC injections to monitor carryover and drift.

- Funding and provenance
  - Funded by Natural Environment Research Council (NERC) NE/T010959/1 and National Science Foundation (USA) 1935458.