# Somerfordmethods.docx

- The data document the results of a grazing experiment in Somerford Mead, a restored floodplain meadow on the River Thames upstream of Oxford, collected 1987–2014.
- Experimental setup: 9 plots (3 treatments: Cattle grazing, Sheep grazing, No grazing; each with 3 replicates) within a 10 m x 10 m stand. Each plot contains 10 permanently located 1 m x 1 m quadrats (total of 90 quadrats). Plots are time-series with fixed recording locations.
- Fieldwork timing: Data collected in June of each year; plots were hay-cut in July; grazing treatments applied from August 1991 onward.

- Data coverage by year/format:
  - 1987–1989 (baseline, pre-treatments): abundance per species in each quadrat based on presence across 16 cells within the quadrat (scale 1–16).
  - 1991–2013 (treatment response): abundance based on presence in 16 cells per quadrat (scale 1–16).
  - 2014 (final survey): abundance as percentage ground area covered by each species in the quadrat (scale 1–100); final column indicates total species per quadrat.

- Units and interpretation:
  - 1997–2013: abundance scale 1–16 (number of cells in which the species occurred).
  - 2014: abundance scale 1–100 (percent ground cover).

- Quality control and taxonomic housekeeping:
  - Taxonomic updates to align with Stace's New Flora of the British Isles (4th ed., 2019) in 2022.
  - Annual quality assurance by Dr A. McDonald (1987–2013) and J.O. Mountford (2014).
  - Corrections for arithmetic and species counts; field sheets reconciled with database entries where needed.

- Data structure and content:
  - Each data file is a table: columns = species names; rows = quadrats (identified in the first column); cell values = abundance in that quadrat; blanks = species not recorded.
  - The final column in each row provides the total number of species per quadrat.
  - Plot coordinates (NGR) are provided for all plots; there is a schematic layout (Figure 1) and quadrat subdivision scheme (Figure 2).

- Corrections, assumptions, and notes (from Dr M.J. Stone, 2022 digitisation):
  - 1987–1989: No field data sheets; data reconstructed from the “Somerford Mead frequency data” document.
  - 1994: Two summaries with mismatching species lists; field data input reconciled with the summaries; some species renamed or treated as pseudospecies; discrepancies resolved through field-data checks.
  - 1994–2014: Numerous pseudospecies entries, genus-level identifications, and coding (e.g., + or tick marks) standardized (replaced with "p" for presence or coded equivalents).
  - Specific issues include multiple entries for certain species, miscopied data between field sheets and summaries, and updates to reflect current taxonomy (e.g., Lotus uliginosus now L. pedunculatus; Tragopogon forms; Deschampsia cespitosa).
  - Some quadrats had incomplete or ambiguous identifications; such entries were handled using the most appropriate pseudospecies labels or genus identifications as documented.
  - Non-numeric entries in 2014 were standardized to numeric codes (e.g., "p").
  - Notable data refinements include flattening duplicates, consolidating bare ground totals, and aligning tallies with field sheets where possible.

- Access, provenance, and references:
  - Raw paper proformas originally used for field data are held by the Floodplain Meadows Partnership.
  - Key publications:
    - McDonald, Alison (2001). Succession during the re-creation of a flood-meadow 1985–1999. Applied Vegetation Science.
    - Stace, C. (2019). New flora of the British Isles (4th edition).
  - This dataset provides a long-term time series of species composition under different grazing regimes, suitable for analyses of succession, grazing effects, and habitat management on floodplain meadows.