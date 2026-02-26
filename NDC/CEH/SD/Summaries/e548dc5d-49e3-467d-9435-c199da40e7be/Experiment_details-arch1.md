# Overview of data

- Dataset: pigAMRgenecounts.csv containing quantitative PCR (qPCR) readouts of antimicrobial resistance gene (AMRG) assays and associated metadata. Reported values are mean gene copies per microlitre of DNA extract.

- Origin and scope of samples:
  - Collected from a single British commercial pig unit.
  - Sample types: faecal (sow housing barn, pig growing houses, piglet pen) and environmental (slurry tanks) samples; plus random stratified environmental sampling of the farm and surrounding land.
  - Studies: a main study (Oct 19, 2016 – Apr 5, 2017) and a depopulation study (Jun 19, 2017 – Nov 13, 2017).
  - Data generation window: Aug 1, 2017 – May 1, 2018.

- Objective: monitor dynamics of antimicrobial resistance gene dynamics on-farm in response to antimicrobial administration and management practices, including partial depopulation.

- Missing data: some samples missing due to material absence or access issues; assumed missing completely at random.

- Investigators: Alexander Corbishley (PI), David Gally (co-I), Mike Hutchings (co-I), Jolinda Pollock (postdoc), Geoffrey Mainda (postdoc) involved in collection; interpretation by AC, JP, and colleagues.

- Experimental design and sampling regime:
  - Farm: 600-sow farrow-to-finish unit.
  - Weaner piglets received acidified water for 2 weeks, chlortetracycline in feed, then tylosin in-feed during growing/finishing.
  - Replication: three pen replicates; weekly faecal sampling from each pen; sow barn sampling for background AMR levels; slurry sampling for pooled on-farm AMR levels.
  - Sample counts: 329 faecal/environmental samples in the main study; 45 additional samples in the depopulation study.
  - Early missing samples explained (e.g., lack of faeces from piglets, access issues), considered random.

- Sample handling, storage, and processing:
  - On-farm collection protocols for farrowing crates, sow barns, slurry, and weaning/growing/finishing pens.
  - Immediate on-site storage at -20°C, transport on dry ice to the lab, storage at -80°C prior to processing.
  - Detailed handling protocols to maintain sample integrity and prevent cross-contamination (gloves, sterile containers, validated stock reagents, avoidance of PCR-amplified DNA areas).

- Quality control and laboratory practices:
  - Use of PCR-grade water, a microbiological safety cabinet, disposable consumables, filter tips, fresh lab coats and gloves, and separation from PCR-amplified DNA areas.
  - Thawing on wet ice before processing.
  - Dry matter assessment and standardized handling to ensure consistency.

- Faecal sample handling and DNA extraction:
  - Homogenization, precise weighing of 250 mg for DNA extraction; desiccation step for dry matter calculation; storage of remaining samples at -80°C.
  - DNA extraction via PowerSoil (MoBio) kit with a detailed lysis and inhibitor-removal workflow (including C1–C6 reagents and multiple spin-filter steps) to maximize yield and purity.
  - Emphasis on removing humic substances and inhibitors to improve downstream qPCR performance.

- DNA quantification and storage:
  - Eluted DNA divided into five 20 µL aliquots; concentration and purity assessed by NanoDrop (260/280, 260/230); samples stored at -80°C.
  - Care taken to track aliquots opened outside a tissue culture hood.

- Quantitative PCR (qPCR) methodology:
  - Instrument: Agilent Mx3005p; absolute quantification using standard curves from cloned plasmids (range 10^7 to 10^1 copies/µL); all reactions run in triplicate with appropriate no-template controls.
  - Reagents: Brilliant Ultra Fast Master Mix; optimized primers/probes; 20 µL reaction volumes.
  - Cycling: 95°C denaturation, 60°C annealing/extension; 40 cycles; fluorescence detection during extension.
  - Target genes and controls: tetB, ermA, ermB, dfrA1, tetQ, and 16S rRNA (with specific forward/reverse primers and probes listed); fragment sizes provided.
  - Standards and controls implemented to ensure accurate copy number estimation.

- Data processing and structure:
  - Analysis software: MxPro for qPCR data (standard curves used to calculate gene copy numbers in unknown samples).
  - Data integration: imported into Microsoft Excel; paired with sample metadata.
  - Output: mean gene copies per microlitre of DNA extract; standardization possible via percent dry matter (%DM) or 16S copy numbers.
  - Dataset description: single CSV file (pigAMRgenecounts.csv) with 24 columns covering sample identifiers, descriptions, metadata, and gene copy counts.

- Dataset variables (example structure):
  - Column 1: Shortened sample identifier; Column 2: Sample description (faeces, soil); Column 3: Full sample ID; Column 4: Category of pigs (sow, piglet); Column 5: Date of sampling; Column 6: Sampling site; Column 7: DNA box ID; Column 8: DNA concentration; Column 9: Sample wet weight (g); Column 10: Sample dry weight (g); Column 11: % dry matter; Column 12: Distance from sow barn (environmental samples); Column 13-18: Copies/µL for tetB, ermA, ermB, dfrA1, tetQ, 16S; Column 19: Experiment type (main or depopulation); Column 20: Sample type; Column 21: Pig type; Column 22: Pig age; Column 23: Pen ID; Column 24: Antibiotic used (none, acidified water, chlortet, tylosin, etc.).
  - Reference to methodology and kit: PowerSoil DNA Isolation Kit protocol (2014) and associated supplier details.

- Documentation and references:
  - Protocols and procedures cited from PowerSoil kit guidelines; associated vendor contact details provided.
  - References for qPCR primer/probe sets and prior similar methods cited (Schmidt et al., Boeckelmann et al., Clifford et al., Maeda et al.).

- Practical notes for use:
  - Data can be standardized to (%DM) or 16S copies to account for sample mass and microbial load.
  - The dataset enables analysis of AMR gene dynamics across production stages, sample types, and treatment regimens, including the depopulation event.