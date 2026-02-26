# Campanula rotundifolia cytotype and common garden study

- A large-scale study of Campanula rotundifolia examining cytotype variation and performance across ploidy levels, using both field collections and a controlled common garden.
- Data were collected from nearly 900 geo-referenced locations (primarily Britain and Ireland) with extensive contributions from volunteers; supplementary samples from elsewhere to provide broader context.
- The study produced multiple data files documenting cytotype, phenology, and growth/fecundity measurements, enabling analyses of geographic cytotype patterns and clonal performance in a common environment.

## Plant material and sampling strategy

- Over 1300 samples (seeds, leaves, or stem cuttings) from >800 plants were collected, prioritising geographic spread and habitat diversity.
- Sample types included leaf tissue for cytotyping, seeds for propagation, and cuttings for clonal material.
- To avoid sampling the same clone, efforts aimed for at least 5 m between plants; when feasible, multiple plants per locality were collected.
- Intensive sampling targeted known rare hexaploids in Wanlockhead (SW Scotland), Teesdale (central England), and Cheddar (southern England) to map their extent.
- Samples were stored appropriately during transport and storage; high-precision location data were anonymised to preserve site confidentiality.
- Cytotype results and location details are available in campanula_cytotype.csv; more material remained in cold storage for future use.

## Cytotype determination

- Chromosome counts from root tips were previously obtained and cross-validated by flow cytometry; any conflicts prompted re-analysis.
- Flow cytometry followed the Doležel et al. (2007) protocol using Pisum sativum 'Ctirad' as an internal standard (2C = 9.09 pg) and propidium iodide staining.
- Sample prep involved chopping leaf tissue with internal standard, filtering, RNase treatment, PI staining, and analysis on BD FACSCalibur or Accuri C6 cytometers.
- Data were gated to isolate nuclei, and DNA contents were calculated from the ratio of sample to standard peaks; cytotypes were assigned accordingly.
- Quality control: analyses re-run if full peak coefficients of variation exceeded 5%; stored/dried samples tended to yield higher DNA contents and were excluded from mean DNA content calculations; some group analyses excluded when necessary.
- Flow cytometry data and cytotype assignments are integrated with location data in campanula_cytotype.csv.

## Common garden study design

- Clones for the common garden were generated from cuttings or seeds collected in the preceding two years and planted in October 2008.
- Site: raised bed adjacent to CEH Edinburgh glasshouses ( locality where the naturally occurring cytotype is tetraploid ), at 55.86°N, 3.21°W, 190 m a.s.l.
- Experimental layout: five randomized blocks containing clonal tetraploid, pentaploid, and hexaploid plants; blocks included 55 tetraploid, 1 pentaploid, and 37 hexaploid clones in total.
- Clones were randomly arranged within blocks; pollination was not restricted; occasional weeding occurred to limit competition.

## Phenology and growth assessments

- 3a. Phenology (flowering): daily monitoring in 2009 and 2010; date of first flowering (FFD) recorded as the date when the first flower was sufficiently open for bee visitation. Data stored in campanula_FFD.csv.
- 3b. Growth and fecundity: 
  - August 2009 (days 215/217): counting total flowering stems per plant; measurements on three randomly selected stems per plant (height, seedheads, open flowers, buds, etc.). Data stored in Dest_harvest_Aug_2009_blocks_1_and_3.csv.
  - September 2009 (day 252): harvest of blocks 2 and 5; recording total flowering stems and above-ground biomass (stem dry weight). Data stored in Dest_harvest_Sept_2009_blocks_2_and_5.csv.

## Description of data files

- Campanula_cytotype.csv
  - Columns: Country, Location, Sample code, Latitude, Longitude, Cytotype.
  - Provides cytotype assignments linked to precise locality data (anonymized coordinates where necessary).
- campanula_FFD.csv
  - Columns: Block number, Clone code, Date of first flowering in 2009, Day-number in 2009, Plant condition comments (2009), Date of first flowering in 2010, Day-number in 2010, Plant condition comments (2010).
- Dest_harvest_Aug_2009_blocks_1_and_3.csv
  - Columns: Block number, Clone code, Total flowering stems, Stem height (cm) and counts for various stem features (seedheads, open flowers, buds) for stems 1–3, plus plant condition comments.
- Dest_harvest_Sept_2009_blocks_2_and_5.csv
  - Columns: Block number, Clone code, Total stem dry weight (g), No. of flowering stems.
- Notes: In all files, asterisk (*) indicates dead/missing data; data are organized in columns for easy integration and analysis.

## Data quality, provenance, and limitations

- Multi-source data: field-collected materials and clonal propagation; varying collection intensities across locations.
- Anonymised but precise location data to protect sites; some high-resolution coordinates withheld.
- Cytotype determination included rigorous QC and cross-validation with old chromosome counts; some samples excluded from mean DNA content calculations due to storage/condition effects.
- Some sampling targeted known unusual cytotypes (hexaploids) to map their geographic extent; not all locations could be revisited for additional material.
- The dataset is designed for integration across cytotype, phenology, and growth metrics to analyze how ploidy influences phenology and fecundity in a common environment.

## References

- Doležel J, Greilhuber J, Suda J (2007). Estimation of nuclear DNA content in plants using flow cytometry. Nature Protocols.
- Greilhuber J, Temsch EM, Loureiro JCM (2007). Nuclear DNA content measurement. Flow Cytometry with Plant Cells.
- McAllister HA (1972). The experimental taxonomy of Campanula rotundifolia.
- Stevens CJ, Wilson J, McAllister HA (2012). Biological Flora of the British Isles: Campanula rotundifolia. Journal of Ecology.