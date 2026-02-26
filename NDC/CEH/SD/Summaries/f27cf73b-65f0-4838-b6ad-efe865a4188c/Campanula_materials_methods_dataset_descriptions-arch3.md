# Campanula rotundifolia cytotype and common garden study

- Purpose and scope
  - Describes plant material collection, cytotype determination via flow cytometry, and a common garden experiment to assess phenology, growth, and fecundity across ploidy levels (tetraploid, pentaploid, hexaploid) of Campanula rotundifolia.
  - Includes detailed data descriptors and file formats for downstream use and reuse.

- Plant material (sampling and provenance)
  - >1300 samples (seeds, leaves, stem cuttings) from ~900 geo-referenced locations, focused on Britain and Ireland with additional context from elsewhere.
  - Many samples contributed by volunteers; some from seed suppliers or Botanic Gardens; aim to capture geographic and habitat diversity.
  - Sample storage and propagation: seeds germinated; cuttings rooted in a cool glasshouse; leaf material dried or stored at -20°C; seeds air-dried and stored at 4°C.
  - Sampling strategy to avoid clonal redundancy: where possible, multiple plants per locality separated by at least 5 m; intensified sampling in areas with previous hexaploid observations (Wanlockhead, Teesdale, Cheddar).
  - Metadata and anonymization: cytotype and location details recorded in campanula_cytotype.csv; coordinates given to 0.01° resolution to protect site anonymity; excess material retained at CEH Edinburgh for potential future analysis.

- Cytotype determination (flow cytometry)
  - Cytotypes previously counted cytologically and cross-validated with flow cytometry; conflicting results reanalyzed.
  - Flow cytometry protocol: one-step method with internal standard (Pisum sativum L. 'Ctirad', 2C = 9.09 pg) and propidium iodide dye; QC thresholds include peak coefficient of variation (CV) ≤ 5%.
  - Instrumentation: FACSCalibur or Accuri flow cytometers; data analyzed with Cyflogic or manufacturer software; DNA content inferred from test/standard peak ratios.
  - Quality control and data handling: stored samples may bias DNA content (excluded from mean DNA content calculations); samples analyzed in groups excluded if needed to resolve multiple cytotypes.
  - Data repository: cytotype results stored in campanula_cytotype.csv alongside geographic coordinates and sample codes.

- Common garden study (experimental design)
  - Clonal material created from cuttings/seeds collected in the preceding two years; planted October 2008 in an external raised bed near CEH Edinburgh (site with native tetraploid background).
  - Experimental layout: five randomized blocks with clonal tetraploid, pentaploid, and hexaploid individuals; 55 tetraploid, 1 pentaploid, and 37 hexaploid clones distributed across blocks.
  - Management: no pollination control; occasional weeding; plot maintained to study growth, flowering, and seed set dynamics.
  - Figure 1 illustrates clone layout across blocks and randomization.

- Phenology and growth/fecundity assessments
  - Phenology (3a): daily monitoring in 2009–2010 to record date of first flowering (FFD) when the first flower is bee-accessible; data stored in campanula_FFD.csv.
  - Growth and fecundity (3b): 
    - Aug 2009: counts of total flowering stems per plant; measurements on three randomly selected flowering stems per plant in blocks 1 and 3 (destinations in Dest_harvest_Aug_2009_blocks_1_and_3.csv).
    - Sept 2009: harvest of above-ground material from blocks 2 and 5; recording stem number, height, seedhead metrics, flower counts (in Dest_harvest_Sept_2009_blocks_2_and_5.csv); stems oven-dried for biomass data.

- Data files and structure
  - Campanula_cytotype.csv: location, sample code, and cytotype (country, location, sample code, latitude, longitude).
  - campanula_FFD.csv: block, clone code, first flowering dates for 2009 and 2010, day-number conversions, and plant-condition comments.
  - Dest_harvest_Aug_2009_blocks_1_and_3.csv: block, clone code, total flowering stems, stem heights, seedhead counts, flower counts, and plant-condition comments for stems 1–3.
  - Dest_harvest_Sept_2009_blocks_2_and_5.csv: block, clone code, total stem dry weight and number of flowering stems.
  - Data note: an asterisk (*) indicates dead or missing data; columns are consistently organized across files.

- References and methodology grounding
  - Flow cytometry DNA-content estimation protocols (Doležel et al. 2007) and related nuclear DNA content guidance (Greilhuber et al. 2007).
  - Previous cytotype work and the Biological Flora of the British Isles entry for Campanula rotundifolia (McAllister 1972; Stevens et al. 2012).

- Relevance to environmental monitoring frameworks
  - Demonstrates a comprehensive approach to building an environmental health monitoring dataset: broad geographic sampling, robust data provenance, and explicit metadata practices.
  - Highlights data governance considerations: anonymized location data, explicit data files and column definitions, and transparent quality controls (e.g., CV checks, reanalysis when needed).
  - Addresses data challenges relevant to monitoring: data gaps (volunteer-sourced material), data quality and compatibility (stored vs. fresh samples affecting DNA measures), and the need for careful data transformation and consistent reporting formats.
  - Provides a model for sharing and reuse via structured CSV files with clear documentation of methods, units, and clone/cytotype identifiers, supporting downstream analyses and policy-oriented monitoring decisions.