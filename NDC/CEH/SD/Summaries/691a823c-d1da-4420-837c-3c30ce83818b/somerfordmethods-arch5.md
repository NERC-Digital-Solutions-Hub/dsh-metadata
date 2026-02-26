# Somerfordmethods.docx

## Overview
- Documents the results of a grazing experiment in Somerford Mead floodplain meadow alongside the River Thames upstream of Oxford.
- Datasets cover 1987–2013 (with a final 2014 survey) across 9 plots under three grazing treatments (Cattle, Sheep, No grazing) with replication.
- Data focus on plant species abundance within 1 m x 1 m quadrats; abundance recorded per species per quadrat, with a final per-quadrat species count.

## Collection methods and sampling design
- Each plot contains 10 quadrats, totaling 90 quadrats across the 9 plots.
- Plots are permanently marked with metal pegs; recording locations fixed over time.
- In 1991–2013, quadrat abundance is estimated by counting the number of 0.25 m x 0.25 m cells (out of 16) in which a species occurs (cells-based presence–absence). In 2014, abundance is expressed as percentage ground area covered.
- The spatial layout includes a 10 m x 10 m stand per plot with fixed NGR coordinates for each plot.
- Documentation mentions Figure 1 for quadrat positions and Figure 2 for the 16-cell subdivision schema.

## Data formats, units, and structure
- Three file formats/variants:
  - 1987–1989 (baseline): abundance scale 1–16 based on occurrences across 16 cells.
  - 1991–2013 (response data): abundance scale 1–16 as above.
  - 2014: final survey with abundance scale 1–100 representing percent cover.
- Data tables: rows = quadrats, columns = species names, cell values = abundance, blanks = species not recorded in that quadrat, final column = total number of species in the quadrat.

## Taxonomy, quality control, and data cleaning
- Taxonomic names updated in 2022 to align with Stace's New Flora of the British Isles (2019 edition) to resolve synonyms.
- Species counts within quadrats checked by Dr M.J. Stone; arithmetic corrections applied as needed.
- Raw data collected by multiple recorders; annual QA carried out by Dr A. McDonald (1987–2013) and J.O. Mountford (2014).
- Original field sheets: paper proformas held by Floodplain Meadows Partnership (floodplain-meadows-project@open.ac.uk).

## Provenance, documentation, and references
- Field data collection and digitisation details documented; remaining field sheets and data provenance described.
- Detailed methodology and context published: McDonald, 2001 (Succession during the re-creation of a flood-meadow 1985–1999; Applied Vegetation Science).
- Taxonomic framework reference: Stace, 2019 (New flora of the British Isles, 4th ed.).

## Data structure specifics and notes on data handling
- Data files are table-based: quadrats as rows, species as columns; non-recorded species left blank; final column shows per-quadrat species richness.
- 1991–2013 data used a 16-cell subdivision within each 1 m × 1 m quadrat; 2014 data uses % cover instead of cell counts.
- Plot layout and quadrat positions are fixed; recording procedures specify the recorder starting position and reference (e.g., recorder begins at number 1; facing the River Thames).
- Data input corrections and anomalies discussed in detail (e.g., miscopied values, pseudospecies, genus-level identifications, Dutch pseudospecies terms, inconsistent tallies, and habitat-related misidentifications).

## Corrections, assumptions, and data quality notes
- 1987–1989 field data sheets are not available; data for this period drawn from a separate document/table (“Somerford Mead frequency data”).
- 1994 data contain discrepancies between printed and handwritten species lists; field data input reviewed and corrected; some species listed as guesses or miscoded.
- 1999–2000 notes document multiple issues including miscopies (e.g., Taraxacum agg. vs. Rumex crispus), pseudospecies, genus-only identifications, and multiple entries for the same taxon.
- 2000–201- era notes describe numerous pseudospecies in Dutch terminology, uncertain identifications, and adjustments to reflect field sheets and keys.
- Specific corrections include combining tallies for some plots, addressing duplicate entries, and reassigning identifications where field sheets disagreed with summaries.
- Some entries are non-numeric (e.g., plus signs, ticks) and have been converted to a notation for presence/very small cover in the database.
- Overall, the dataset includes extensive post-collection cleaning to align field data with updated taxonomy and to resolve inconsistencies across years.

## Availability and governance for Data Stewardship
- Raw field sheets and documentation are retained by the Floodplain Meadows Partnership.
- The dataset has undergone formal quality assurance and taxonomic harmonisation; provenance and correction history are documented within the metadata.
- The data collection and processing approach, including the paper proformas and digitisation steps, are described to support reproducibility and future updates.

## References
- McDonald, Alison. (2001). Succession during the re-creation of a flood-meadow 1985-1999. Applied Vegetation Science. 4. 10.1111/j.1654-109X.2001.tb00485.x.
- Stace, C. (2019). New flora of the British Isles (4th edition). C&M Floristics, Ipswich.