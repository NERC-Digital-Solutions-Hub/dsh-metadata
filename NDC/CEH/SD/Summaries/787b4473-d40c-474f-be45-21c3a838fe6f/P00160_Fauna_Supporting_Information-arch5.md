# Soil fauna data from Sourhope field experiment site, Scotland, 2002-2003 [NERC Soil Biodiversity Programme] - Supporting Information

- Overview
  - Data from the NERC Soil Biodiversity Programme (1999–present) focusing on soil biota diversity and ecological processes at the Sourhope field site in the Scottish Borders (grid NT8545019630).
  - This dataset pertains to project 160: Diversity and functional role of predatory beetles and their prey in the Sourhope ecosystem.
  - Timeframe: field data collected during 2002–2003; includes sampling across multiple methods and dates.
  - Primary purpose: support understanding of soil biota diversity, functional roles, and responses to treatments.

- Experimental design and site context
  - Site design: randomized complete block with 5 blocks, 6 treatments per block (30 plots total).
  - Treatments used in this faunal study: control, nutrient enhancement (N + L: nitrogen and lime), chlorpyrifos insecticide, and combinations as applicable.
  - Plot dimensions: 20 m x 12 m with buffer zones between plots.
  - Management: monthly mowing May–Sept with cut material removed.
  - Location details: Sourhope field site, Macaulay/SF (now James Hutton) Institute.

- Data collection and sampling methods
  - Invertebrate sampling periods: July and October 2002; April, June, and October 2003.
  - Sampling methods by organism group:
    - Collembola and spiders: pitfall traps (1 week deployment; ethylene glycol as preservative).
    - Soil invertebrates: soil cores (2 cores per sub-plot) analyzed via Tullgren funnel extraction over two weeks.
    - Slugs: defined area traps (DAT) with abaited collar and periodic checks.
  - Taxonomic scope and identifications:
    - Collembola identified to species for July 2002; spiders identified to species across sampling periods.
    - Beetles, slugs, and spiders identified using standard taxonomic references (listed in the dataset documentation).
  - Data documentation: detailed metadata and a data dictionary accompany the dataset.

- Data structure and content
  - Data file: P00160_ALL_FAUNA.csv (CSV format).
  - Key fields (examples):
    - TYPE: Sampling type (SOIL INVERTEBRATES - TULLGREN; COLLEMBOLA - PITFALL; PITFALL; SPIDER - PITFALL; SLUGS).
    - DESCRIPTION: Narrative of sampling method.
    - DATE / SAMPLING_DATE: Sampling occasion (month/year) and actual date.
    - BLOCK, MAIN_PLOT, SUB_PLOT: Block and plot identifiers (1–5; A–F; sub-plots).
    - CELL_X, CELL_Y: Grid cell coordinates.
    - TREATMENT: Treatment code (Control, Biocide, Nitrogen & Lime, etc.).
    - SPECIES: Species name (where identified).
    - SP_COUNT_TRAP, SP_COUNT_m2: Counts per trap and per square meter.
    - BIOMASS: Biomass metric (where applicable).
  - Data interpretation notes:
    - Data are organized by sampling type and plot, with counts and biomass where relevant.
    - Species-level identifications are tied to specific sampling occasions; some taxa only identified in certain periods.

- Taxonomic references and supporting materials
  - Identification keys and references used for taxa (Collembola, spiders, beetles, slugs) are documented alongside the dataset.
  - Related resources: SOURHOPE FIELD DATA HANDBOOK 2003 and related papers (Scott et al., 2003) provide broader data handbook context and methodology.

- Data quality control and limitations
  - Quality control: numeric range checks, formatting conformity, and logical integrity checks implemented.
  - caveats and disclaimers:
    - Data are subject to quality assurance but not guaranteed for accuracy or fitness for a particular use.
    - NERC disclaims liability for any loss or damage arising from use of the data.
  - Limitations to consider for stewardship and reuse:
    - Some identifications (e.g., Collembola to species) are limited to specific sampling events.
    - Data are tied to specific treatments and plot configurations; care needed when aggregating across years or sites.
    - Method-specific biases (trapping efficiency, differential detection) should be accounted for in analyses.

- Data access, provenance, and related materials
  - Data availability: provided as a CSV with accompanying metadata and a data dictionary in the Supporting Information.
  - Provenance: linked to the NERC Soil Biodiversity Programme and the Sourhope field experiment; associated with the 2003 SOURHOPE FIELD DATA HANDBOOK and subsequent publications (e.g., 2007–2009 water/soil biodiversity studies).
  - Related datasets and publications: multiple papers exploring insecticide effects, nutrient additions, and multi-trophic interactions; references and links are provided within the documentation.

- Practical guidance for data stewards
  - Ensure consistency of field identifiers (BLOCK, MAIN_PLOT, SUB_PLOT) with other Sourhope datasets.
  - Preserve the explicit data dictionary and taxonomic references to maintain usability across analyses.
  - Maintain licensing and liability statements as provided; note the non-warranty stance in data reuse.
  - Consider publishing a machine-readable data dictionary alongside the CSV to facilitate discoverability and reuse.
  - If integrating with other portaland portals, map treatment codes and sampling types to standardized ontologies and units.

- Additional notes and citations
  - Background and experimental design sources; key methodological references are included in the Supporting Information.
  - Further reading includes several studies on insecticide effects, nutrient inputs, and multi-trophic interactions within the Sourhope ecosystem.