# Campanula rotundifolia: Cytotype determination and common garden study

- Purpose and scope
  - Large-scale study of Campanula rotundifolia combining cytotype determination with a common garden experiment to understand how ploidy levels relate to spatial distribution, phenology, growth, and fecundity.
  - More than 1700 geo-referenced samples collected mainly from Britain and Ireland, with additional context from elsewhere.
  - Data products intended for map-based visualization and spatial analysis, integrating cytotype, phenology, and growth data.

- Geospatial data and provenance
  - Locations stored at 0.01 degree resolution with latitude/longitude from GPS or Ordnance Survey; site anonymity preserved.
  - Samples may come from multiple plants per locality when possible (minimum ~5 m apart to avoid sampling the same clone); some localities yielded single plants.
  - The cytotype results are catalogued in campanula_cytotype.csv (country, location, sample code, coordinates, cytotype). Additional plant material held at CEH Edinburgh with sample codes.

- Cytotype determination methods
  - Flow cytometry following a one-step protocol (Doležel et al. 2007) using Pisum sativum 'Ctirad' as an internal standard and propidium iodide dye.
  - Chromosome counts from previous work used for calibration; flow cytometry results validated and repeated if needed.
  - Quality control: samples with high coefficients of variation (>5%) reanalyzed.
  - Data considerations: time between collection and processing and sample condition can affect results; desiccation and red/brown samples excluded from Cx analyses.
  - Cytotype assignment by genome size (DNA content in pg):
    - Diploid: 2.27–2.71 pg
    - Tetraploid: 4.22–4.96 pg
    - Pentaploid: 5.33–5.65 pg
    - Hexaploid: 6.20–7.14 pg
    - Others classified as aneuploids.

- Common garden study design
  - Clones produced in a glasshouse from cuttings or seeds collected in the preceding two years; planted October 2008 in an external raised bed near CEH Edinburgh (55.86°N, 3.21°W; 190 m a.s.l.).
  - Five randomized blocks including tetraploid, pentaploid, and hexaploid clones, with 55 tetraploid, 1 pentaploid, and 37 hexaploid clones distributed across blocks.
  - Layout is depicted in Figure 1; pollination not restricted; occasional weeding allowed to reduce competition.
  - Data collection included flowering phenology and destructive harvests to assess growth and seed set dynamics across ploidies.

- Data files and variables
  - Campanula_cytotype.csv
    - Country, Location, Sample code, Latitude, Longitude, Cytotype
  - campanula_FFD.csv (phenology)
    - Block number, Clone code, Date of first flowering in 2009, Day number 2009, Plant condition notes 2009, Date of first flowering in 2010, Day number 2010, Plant condition notes 2010
  - Dest_harvest_Aug_2009_blocks_1_and_3.csv (growth/fecundity, stems 1–3)
    - Block number, Clone code, total flowering stems, height of stem 1, seedhead counts, open flowers, flower buds, and comments per stem 1–3, plus plant condition notes
  - Dest_harvest_Sept_2009_blocks_2_and_5.csv (biomass and flowering)
    - Block number, Clone code, total stem dry weight (g), number of flowering stems
  - Additional notes
    - Clone names including 'sd' indicate clones propagated vegetatively from a seedling.
    - Descriptions include data handling conventions (dead or missing data marked with an asterisk).

- Spatial analysis opportunities for GIS
  - Map the geographic distribution of cytotypes and explore associations with geography, environment, and altitude.
  - Visualize phenology (FFD) across clones and ploidy levels; analyze spatial trends in flowering timing.
  - Compare growth and fecundity metrics by ploidy and by location; integrate with environmental layers (e.g., climate, soil).
  - Leverage anonymized coordinates to produce aggregate or hotspot analyses while preserving site confidentiality.
  - Use the common garden layout (block and clone identifiers) to map experimental design and spatial effects within the site.

- Quality, standards, and references
  - Flow cytometry performed with established protocols; DNA content used to assign cytotypes; calibration against previously counted chromosome data.
  - Data quality checks include repeat analyses for ambiguous results and exclusion of compromised samples (desiccated or discolored).
  - Key references include Doležel et al. (2007) for flow cytometry methods and related foundational studies on Campanula rotundifolia.