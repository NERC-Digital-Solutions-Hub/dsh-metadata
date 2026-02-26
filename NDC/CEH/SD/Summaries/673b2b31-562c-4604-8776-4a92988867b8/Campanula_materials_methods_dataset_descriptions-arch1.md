# Campanula rotundifolia cytotype and common garden study

- Study collected and analyzed over 1700 samples (seeds, leaves, or stem cuttings) from geo-referenced locations, mainly in Britain and Ireland, with additional samples globally for context.
- Samples came from volunteers, commercial seeds, and Botanic Gardens; material was processed to enable propagation and a common garden experiment.
- Efforts to sample multiple plants per locality were made when possible (minimum ~5 m apart to reduce sampling the same clone); intensified sampling targeted hexaploids in Wanlockhead (SW Scotland), Teesdale (central England), and Cheddar (south England) due to historical observations.
- Location data were recorded with high resolution when possible but were generalized to preserve site anonymity (0.01° resolution); some material remains in cold storage for future use.

## Cytotype determination and data quality

- Chromosome counts were initially determined cytologically and then verified by flow cytometry; discordant results prompted re-analysis with fresh material.
- Flow cytometry followed the Doležel et al. (2007) protocol using Pisum sativum 'Ctirad' as an internal standard (2C = 9.09 pg) and propidium iodide dye.
- Sample prep involved chopping leaf tissue with standardization to balance peak heights between test and reference materials; nuclei were gated to remove debris/doublets; analyses used both FACSCalibur and Accuri C6 cytometers.
- Desiccation and red/brown coloration affected some British samples and those data were excluded from cytotype analyses.
- Cytotype assignment thresholds (in pg DNA) were determined by visual inspection of genome-size distributions:
  - Diploid: 2.27–2.71 pg
  - Tetraploid: 4.22–4.96 pg
  - Pentaploid: 5.33–5.65 pg
  - Hexaploid: 6.20–7.14 pg
  - Any samples outside these ranges were classified as aneuploids.

## Common garden study design

- Clones derived in a glasshouse from field-collected cuttings or seeds were planted in October 2008 in an external raised bed near CEH Edinburgh (55.86°N, 3.21°W; 190 m a.s.l.).
- Five randomised blocks contained clonal tetraploids, pentaploids, and hexaploids to span the British Isles’ cytotype diversity; within blocks, 55 tetraploid, 1 pentaploid, and 37 hexaploid clones were represented (single replicates per clone per block).
- Layout and clone origins are depicted in Figure 1; spacing was 0.3 x 0.4 m; pollination was not restricted, and occasional weeding was performed to manage competition.

## Phenology and growth measurements

- Phenology (first flowering date, FFD) was recorded in 2009 and 2010 by daily inspections during the flowering period.
- To compare flowering dynamics, on August 3 or 5, 2009 (day 215/217), the total flowering stems per plant and stem-specific metrics (height, seedheads, open flowers, buds) were recorded for stems 1–3 (Dest_harvest_Aug_2009_blocks_1_and_3.csv).
- In September 2009 (day 252), above-ground parts of blocks 2 and 5 were harvested; shoot material was oven-dried and weighed, and the number of flowering stems was recorded (Dest_harvest_Sept_2009_blocks_2_and_5.csv).

## Description of data files

- Campanula_cytotype.csv
  - Country, Location, Sample code, Latitude, Longitude; cytotype assignments linked to the samples.
- campanula_FFD.csv
  - Block number, Clone code, Date of first flowering in 2009, Day-number for 2009, plant condition notes (2009), Date of first flowering in 2010, Day-number for 2010, plant condition notes (2010).
- Dest_harvest_Aug_2009_blocks_1_and_3.csv
  - Block, Clone code, total flowering stems, stem height (cm) for stem 1, seedhead counts on stem 1, open flowers on stem 1, buds on stem 1; repeated for stems 2 and 3; occasional plant-condition notes.
- Dest_harvest_Sept_2009_blocks_2_and_5.csv
  - Block, Clone code, total stem dry weight (g), number of flowering stems.

## References and methodological notes

- Flow cytometry methodology: Doležel, Greilhuber, Suda (2007) Nature Protocols.
- Previous work and context: McAllister (1972); Shepherd (2007); Stevens, Wilson, McAllister (2012) on Campanula rotundifolia in the British Isles.
- The study provides a reproducible data framework for analyzing relationships between cytotype (ploidy), phenology (FFD), growth, and fecundity across clonal lines in a controlled common garden environment.

## Potential uses for analysts

- Analyze correlations between cytotype (diploid, tetraploid, pentaploid, hexaploid) and phenological timing (FFD) across clones.
- Compare growth and fecundity metrics among cytotypes using common garden data to isolate genetic/ploidy effects from environmental variation.
- Model how genome size (in pg DNA) relates to flowering onset, stem production, and seed output.
- Assess geographic patterns of cytotype occurrence and potential range-wide polyploidy dynamics.
- Use dataset as a benchmark for data quality, standardization, and integration of multi-source plant cytotype data (field collections, flow cytometry, and common garden experiments).