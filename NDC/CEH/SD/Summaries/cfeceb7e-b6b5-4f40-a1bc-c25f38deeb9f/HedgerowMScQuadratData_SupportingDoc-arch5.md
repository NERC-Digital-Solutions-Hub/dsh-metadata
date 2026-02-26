# Plant community basal data from a hedgerow cutting experiment in England, 2016

## Overview
- Data from an MSc project using the hedgerow experiment setup to study how cutting regimes affect species richness of basal flora.
- Used in a Biodiversity and Conservation publication (Stanbury et al., 2020).
- Long-running hedgerow experiments aimed to assess management impacts on wildlife habitat and restoration options, scalable under agri-environment schemes.

## Experimental design and sites
- Experimental framework: randomised block, Experiment 2; full factorial treatments applied with three replicates per treatment per site.
- Field sites (4 total):
  - Woburn, Buckinghamshire (WO) – hawthorn-dominated hedge
  - Waddesdon estate, Oxfordshire (WB) – blackthorn-dominated hedge
  - Waddesdon Estate, Oxfordshire (WC) – mixed-species hedge
  - Yarcombe, Devon (YC) – traditional mixed hedge
- Treatments (13 total, 2 × 2 × 3 design):
  - Time of cutting: Autumn vs. Late winter
  - Intensity of cutting: Standard vs. Incremental (increasing cut height across years)
  - Frequency of cutting: Annual, every two years, every three years
- Treatment period: September 2010 to January/February 2016
- Note: Winter cutting not applied at WB due to site constraints.

## Data collection and measurements
- Vegetation data collected on both sides of each hedgerow plot (except inaccessible sides at WB and WC Block 1).
- Sampling design: two quadrats per side per plot (each 1 m wide × 10 m long).
  - Inner quadrat samples under the hedge (extending ~1 m from hedge center; may include field-margin plants for wider hedges).
  - Outer quadrat samples beside the hedge (outer margin).
- Quadrat placement: approximately 5 m from plot start to minimize edge effects.
- Coverage assessment: species cover estimated in 5% increments from 5–100%, with 1% increments for 1–4%; <1% recorded as 0.1%.
- Sampling scope: vegetation cover measured up to 80 cm height.
- Quality controls: standardized protocol, experienced surveyors, expert checks, and anomaly screening.

## Data structure and file format
- Primary data file: HedgerowMScQuadratData.csv
- Key columns:
  - EXPERIMENT (Experiment number; 2)
  - SITE (Site code: WB, WC, WO, YC)
  - BLOCK_NO (Block number: 1–3)
  - PLOT_NO (Hedge plot number: 1–39)
  - TREATMENT (Treatment code: 1–13; definitions correspond to the experimental design)
  - VISIT_DATE (Sample date; DD/MM/YYYY)
  - VISIT_YEAR (Year of sampling)
  - QUADRAT (Inner or Outer)
  - SPECIES_NAME (Scientific name; includes bare ground and litter)
  - COVER (Percent cover; numeric)
- Data format: CSV with explicit data types described in the accompanying dataset metadata.

## Quality assurance and provenance
- Quality measures:
  - Use of a standard protocol
  - Data collected by trained, qualified field surveyors
  - Expert verification of species lists
  - Consistency checks for anomalous values
- Provenance:
  - Originates from Defra project BD2114; managed by UK Centre for Ecology & Hydrology (UKCEH)
  - MSc student contributions supported by University of Reading; fieldwork support from UKCEH staff

## Publication and references
- Associated publication: Stanbury et al. (2020) in Biodiversity and Conservation (accepted April 2020)
- Related documentation: Defra Defra BD2114 project report; Countryside Survey (Carey et al. 2008) methodology
- Data were used to analyze how cutting regimes influence basal flora richness and Ellenberg indicator profiles within hedgerows.

## Funding and notes for reuse
- Funding: Defra BD2114; MSc funding/travel subsistence for the student; fieldwork support from UKCEH staff
- Reuse considerations:
  - Clear linkage to experimental design, site limitations, and sampling methods
  - Data appears to be structured for re-analysis of species abundance/coverage by plot and treatment
  - Licensing and access terms are not specified in the provided text; users should verify data access rights and citation requirements with UKCEH or the data owners

## Practical implications for data stewards
- Metadata completeness: ensure explicit license, data access restrictions, and usage rights are documented alongside the CSV.
- Provenance clarity: link the dataset to the Defra BD2114 project records and the 2020 publication for traceability.
- Data interoperability: consider tagging species with standard taxonomic authorities and aligning date formats to ISO in future releases.
- Reproducibility: provide a data dictionary with treatment definitions and clearly map all 13 TREATMENT codes to experimental conditions.