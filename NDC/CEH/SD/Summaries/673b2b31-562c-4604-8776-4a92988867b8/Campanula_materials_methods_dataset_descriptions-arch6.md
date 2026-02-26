# Campanula rotundifolia cytotype determination and common garden study

## Overview
- Large, multi-year dataset focusing on cytotype variation (diploid, tetraploid, pentaploid, hexaploid) and how ploidy relates to flowering phenology and growth.
- >1700 samples collected from Britain and Ireland (geo-referenced), including volunteer contributions; samples stored and later propagated for a common garden.
- Sampling aimed to minimize clonal repeats; intensified sampling in known hexaploid hotspots to determine their extent.
- Data describe both field-collected material and a controlled common-garden experiment planted in 2008 near CEH Edinburgh.

## 1. Plant material
- Seed, leaf, and stem-cutting materials collected from many sites; most locations geo-referenced; anonymity preserved by presenting coordinates at 0.01° resolution.
- Storage and propagation: seeds germinated; cuttings rooted in a cool glasshouse; some leaf material stored at -20°C.
- Sampling strategy: multiple plants per locality when possible (minimum 5 m apart); in some areas only a single plant available.
- Notable emphasis on hexaploids; targeted intensive sampling in Wanlockhead (SW Scotland), Teesdale (central England), and Cheddar (southern England).
- Residual material retained in CEH Edinburgh with sample codes linked to campanula_cytotype.csv.

## 2. Cytotype determination

### 2a. Preparation and analysis of Campanula rotundifolia samples by flow cytometry
- Method: one-step flow cytometry protocol (Doležel et al. 2007) with Pisum sativum 'Ctirad' as internal standard and propidium iodide dye.
- Procedure: chop test sample + standard in buffer, filter, treat with RNase, stain with PI, and adjust mixing to equalize peak heights.
- Instruments: Becton Dickinson FACSCalibur or Accuri C6 flow cytometers; daily calibration; gating on FSC/SSC and then fluorescence plots to isolate nuclei.
- Quality control: reanalysis if CV of peaks >5%.
- Data handling: DNA content ratios used to assign cytotypes; some British samples affected by collection-to-processing delays or sample condition (desiccation or color change) and were excluded from Cx analyses.

### 2b. Assignment of cytotype
- Genome size (pg DNA) ranges used for assignment:
  - 2.27–2.71 pg: diploid
  - 4.22–4.96 pg: tetraploid
  - 5.33–5.65 pg: pentaploid
  - 6.2–7.14 pg: hexaploid
- Samples outside these ranges classified as aneuploids.
- Chromosome-counted references used to calibrate flow cytometry results.

## 3. Common garden study

### 3a. Common garden assessments - Phenology
- Clones generated from field material; planted Oct 2008 in an external raised bed at CEH Edinburgh (55.86°N, 3.21°W; 190 m a.s.l.).
- Five randomised blocks containing clones of tetraploid, pentaploid, and hexaploid cytotypes.
- Each block included 55 tetraploids, 1 pentaploid, and 37 hexaploids (layout shown in Figure 1).
- Phenology measured in 2009–2010 by daily inspection; first flowering date (FFD) recorded when flowers opened enough for nectar for bees.
- Data stored in campanula_FFD.csv.

### 3b. Growth and fecundity
- August 2009 (days 215/217): counted total flowering stems per plant; measured up to three stems per plant (height, seedheads, open flowers, buds) across blocks 1 and 3; additional notes on plant condition.
- September 2009 (day 252): harvesting of above-ground parts in blocks 2 and 5; stem dry weight and number of flowering stems recorded.
- Data stored in two files: Dest_harvest_Aug_2009_blocks_1_and_3.csv and Dest_harvest_Sept_2009_blocks_2_and_5.csv.

## 4. Description of data files

- Campanula_cytotype.csv
  - Columns: Country (A), Location (B), Sample code (C), Latitude (D), Longitude (E), Cytotype (F)
- campanula_FFD.csv
  - Columns: Block number (A), Clone code (B), Date of first flowering in 2009 (C), Date converted to day number in 2009 (D), Plant condition 2009 (E), Date of first flowering in 2010 (F), Date converted to day number in 2010 (G), Plant condition 2010 (H)
- Dest_harvest_Aug_2009_blocks_1_and_3.csv
  - Columns: Block number (A), Clone code (B), Total number of flowering stems on the plant (C), Height of stem no. 1 (D), No. of swollen seedheads on stem no. 1 (E), No. of other seedheads on stem no. 1 (F), No. of open flowers on stem no. 1 (G), No. of flower buds on stem no. 1 (H), and similarly for stem no. 2 (I–M), stem no. 3 (N–R), plus plant condition notes (S)
- Dest_harvest_Sept_2009_blocks_2_and_5.csv
  - Columns: Block number (A), Clone code (B), Total stem dry weight (C), No. of flowering stems (D)

Notes
- In all files, asterisk (*) indicates dead or missing data.
- Data arranged in columns with codes linking to clones and cytotypes as described.

## 5. References
- Doležel J, Greilhuber J, Suda J (2007). Estimation of nuclear DNA content in plants using flow cytometry. Nature Protocols 2(9): 2233-2244.
- McAllister HA (1972). The experimental taxonomy of Campanula rotundifolia L. Ph.D. thesis, University of Glasgow.
- Shepherd JR (2007). Polyploidy and the phylogeography of Campanula rotundifolia L. in the British Isles and Ireland. MSc thesis, University of Edinburgh.
- Stevens CJ, Wilson J, McAllister HA (2012). Biological Flora of the British Isles: Campanula rotundifolia. J Ecol 100(3): 821-839.