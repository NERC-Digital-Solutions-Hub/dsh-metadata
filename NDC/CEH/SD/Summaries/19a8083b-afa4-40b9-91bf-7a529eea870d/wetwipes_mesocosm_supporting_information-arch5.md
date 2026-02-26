What has been recorded and what form does the data take?

- Five CSV files comprise the dataset, documenting a mesocosm study on the persistence of wet wipes in beach sand and the survival of E. coli on their surfaces:
  - Dry_weight_sand_used_in_wet_wipes_mesocosm.csv
  - Background_bacterial_concentrations_in_wet_wipes_mesocosm.csv
  - Water_characteristics_used_in_wet_wipes_mesocosm.csv
  - Tensile_strength_of_wet_wipes_in_wet_wipes_mesocosm.csv
  - Bacterial_concentrations_in_wet_wipes_mesocosm.csv
- Each file uses replicates consistent across data files; data fields cover weight, bacterial concentrations, water characteristics, tensile strength, and contamination counts.

Study location and timeframe

- Location: Mesocosm study conducted at the University of Stirling.
- Period: May to August 2023.
- Experimental scope: Three wet wipe brands with different advertised compostability categories were tested (A: non-compostable with plastic; B: home compostable; C: commercially compostable). Wipes were cut into 7 × 7 cm squares and subjected to a sequence of treatments to simulate disposal and environmental exposure from bathroom to beach.

Experimental design and data collection

- Experimental flow:
  - Wipes flushed in a setup with tap water and added E. coli inoculum to simulate toilet passage.
  - Transferred to glass beakers with WWTP effluent and additional E. coli inoculum.
  - Incubated, then moved to seawater, and subsequently to beach sand mesocosms.
  - Beach sand mesocosms prepared from drainpipes packed with sand.
- Sampling and measurements (weekly, 15 weeks total):
  - Four wipes per type sampled each week; loosely adhering sand removed; wipes processed in PBS, vortexed, and E. coli counted via membrane filtration on selective media (MLGA) after incubation.
  - Tensile strength of each wipe measured with a digital force meter after drying.
- Study purpose:
  - To investigate sewage-associated plastic waste as reservoirs for fecal bacteria, potential human pathogens, and antimicrobial resistance genes.
  - To fulfill UKRI NERC grant requirements related to microbial hitchhikers of marine plastics.

Data collection details and responsible party

- Principal data collector/analyst: Rebecca Metcalf.
- Data completeness: Checked for anomalous data; no data were reported as missing.
- Data provenance: Data reflect controlled mesocosm experiments designed to mimic the environmental journey of wipes from use to beach exposure.

Data fields, structure and metadata

- File contents and variable types (high-level):
  - Dry weight of sand used in mesocosms.
  - Background bacterial concentrations used in mesocosms.
  - Water characteristics of water types used in mesocosms (pH, salinity, etc.).
  - Tensile strength of wet wipes (N) by week.
  - Bacterial concentrations of E. coli on wipes (CFU per mL or per wipe) by week.
- Common metadata and units:
  - Replicate identifiers (Rep), Week, Date, Wipe_type, Timepoint, and relevant measurements (CFU, CFU_per_wipe, Tensile Strength in Newtons, pH, Salinity, etc.).
  - Units include grams (for weights), CFU (colony-forming units), Newtons, percentages for salinity, and date stamps.
- Notes on variable descriptions:
  - Some columns are described with paired labels (e.g., Rep, Week, Date, Wipe_type, CFU_per_ml, CFU_per_wipe, Tensile Strength (N)).
  - The dataset includes both per-wipe and per-wipe-folder measurements, and differentiates between the various water types and replicates.

Data governance, reuse, and maintenance

- Governance and usability:
  - Metadata provides clear descriptions and units to support discoverability and reuse by data stewards and researchers.
  - Data are organized to support cross-file integration by replicates and timepoints.
- Update and interoperability considerations:
  - The study design was fixed (15-week mesocosm, weekly sampling); updates would require new sampling cycles or extended mesocosm configurations.
  - Data were stored as CSVs with consistent replication schemes across files, aiding interoperability with common data platforms.
- Funding and provenance:
  - Linked to UKRI NERC grants on microbial hitchhikers of marine plastics, ensuring alignment with funded project data management practices.

Contact and stewardship

- Primary contact for the dataset: Rebecca Metcalf.
- Intended use: Evaluation of persistence and transfer of microbes and genes associated with sewage-derived plastic waste in coastal environments; supports data-driven governance of environmental microbiology datasets.