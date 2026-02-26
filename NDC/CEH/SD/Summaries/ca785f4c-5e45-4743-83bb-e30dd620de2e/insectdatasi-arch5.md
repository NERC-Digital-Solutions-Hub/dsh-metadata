# Data overview

- Purpose and scope
  - Records of insect visitations to flowers in wildflower seed mix trials conducted on two farms (Church Farm, Oxfordshire; Lee Farm, West Sussex)
  - Experimental design: 20 x 5 m contiguous plots with four seed mixes plus a control fallow

- Temporal and geographic coverage
  - Surveys conducted April to August in 2019, 2020, and 2021
  - Eight survey periods per year; farms surveyed on two separate days for each period

- Data collection methods
  - Survey approach: plots walked centrally lengthways; insects visiting flowers within 2 m on either side identified on the wing or captured for lab identification
  - Field lead: Rachel Nichols
  - Taxonomic resolution: insect groups identified to a broad level (Insect.taxa groups) with bees, hoverflies, and butterflies identified to species where possible
  - Quality control: specimens not identifiable in the field sent to experts (Steven Falk for bees; Ellen Rotheray for hoverflies) to ensure accuracy

- Data structure and contents
  - Data file: InsectData.csv containing 14 columns
  - Columns include:
    - Year, Date, Month, Period, Farm, PlotID
    - Mix (seed mix), Replicate (treatment replicate)
    - Flower.family, Flower.species
    - Insect.taxa, Insect.genus, Insect.species
    - Sex of the insect
  - Each row represents a plot-level survey event

- Data quality, provenance, and stewardship
  - Rigorous identification workflow with expert verification for key taxa
  - Clear documentation of data structure and units (counts of insects visiting flowers)
  - Data suitable for sharing to portals and for re-use, with explicit provenance (survey dates, locations, plots, and taxonomic resolution)

- Implications for data governance and stewardship
  - Metadata completeness: ensure explicit units, sampling methods, and taxonomic resolution are maintained across versions
  - Taxonomic standardization: maintain consistent naming conventions and update identifications as needed
  - Data updates: establish a process for incorporating additional years or new plots while preserving historical context
  - Interoperability: consider aligning with broader pollinator datasets and providing access to auxiliary resources (e.g., specimen IDs and expert identification notes)
  - Risk considerations: address potential data gaps due to incomplete user needs, timely data transfer from field teams, and format compatibility when expanding datasets