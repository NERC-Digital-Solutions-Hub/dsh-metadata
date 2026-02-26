# Enteric virus concentrations and chemical properties of wastewater, water, sediment and shellfish samples collected along the Conwy River and estuary, North Wales.

## Aim and scope
- Assess concentrations of enteric viruses and associated chemical properties across wastewater, surface water, sediments, and shellfish along the Conwy River and estuary.
- Generate data to inform environmental health monitoring and policy decisions.

## Sampling regime and collection methods
- Timeframe: four-weekly sampling from 17 May 2016 to 1 August 2017.
- Sample types and amounts:
  - Surface water: 10 L per sample
  - Sediment: 10 g per sample
  - Mussel tissue: 20 individuals per sample
  - Wastewater influent and effluent: provided by Welsh Water
- Sampling locations:
  - Wastewater treatment plants: Ganol (GI), Betws-y-Coed (BI/BE), Llarwst (LI/LE), Tal-y-Bont (TI/TE)
  - Surface waters: SW1–SW4 (including Betws-y-Coed and Conwy area)
  - Shellfish beds: Llandudno and Conwy
- Sample handling and storage: 4°C storage up to 24 h; top sediment layer sampled during low tide; coordinates and site details documented in Table 1.
- Documentation: detailed sample codes and site descriptions accompany the dataset.

## Laboratory instrumentation and basic measurements
- On-site/field measurements:
  - pH (pH meter)
  - Turbidity (NTU)
  - Conductivity (mS)
- Water concentration processing: Tangential Flow Filtration System (KrosFlo) for viral concentration.

## Nucleic acid extraction and molecular quantification
- Extraction: NucliSENS MiniMag system; manual steps for preparation and purification; additional equipment for handling and processing nucleic acids.
- Quantification targets and methods:
  - Norovirus GI and GII, Sapovirus GI, Hepatitis A (HAV), Hepatitis E (HEV), Sapovirus GI, Mengovirus (MgV) as process control
  - Human Adenovirus (AdV), JC and BK polyomaviruses (JCV, BKV)
  - Detection and quantification via one-step qRT-PCR or qPCR assays (triplex/qRT-PCR formats; SYBR Green for AdV; multiplex probe-based assays for others)
- Assay details:
  - Primers/probes and reaction conditions outlined (annealing temperatures 56–60°C; 60 min RT; 40–45 cycles)
  - Table 2 lists primers and probes used
- Capsid integrity assay for Norovirus:
  - Porcine gastric mucin-conjugated magnetic beads (PGM-MBs) used to assess capsid integrity of Norovirus in water and sediment concentrates
  - Mussel samples excluded from this assay due to prior sample treatment

## Quality control and validation
- Validation approaches:
  - Spiking experiments to assess recovery in sediment (80–100%) and surface water (10–100%)
  - Use of process control MgV to evaluate recovery across samples
  - Duplicates and controls (non-template controls) included in each run
- Detection and quantification limits:
  - NoV GI/GII, HAV, HEV, SaVGI, MgV, AdV, JCV, BKV with specified detection limits (e.g., ~100 gc/L for water, ~10 gc/g for sediment, ~200 gc/g for shellfish)
  - Quantification limits correspond to approximately 200 gc/L water, 100 gc/g sediment, and 500 gc/g shellfish
- Overall data quality: validated extraction methods and spike-recovery data support representativeness of reported concentrations

## Data structure and metadata
- Data format: a single CSV dataset
- Metadata fields (examples):
  - Sample_code, Date, Time_GTM, Volume, pH, Turbidity (NTU), Conductivity (mS)
  - Virus concentrations: NoVGI, NoVGII, HaV, HEV, SaV, AdV, JCV, BKV (gc/UnitVol)
  - NoVGI_PGM and NoVGII_PGM (capsid integrity indicators)
- Notes:
  - Some measurements (e.g., BKV in wastewater) were only targeted in specific sampling rounds (March 2016)
  - Empty fields indicate missing values
- Dataset provenance:
  - Links to methodological references for primers/probes and assay validation
  - Data suitable for monitoring framework applications and policy-informed decision making

## Usage and implications for monitoring and policy
- Provides a comprehensive methodological blueprint for environmental monitoring of enteric viruses across wastewater, surface water, sediments, and shellfish
- Demonstrates integration of field sampling, laboratory workflows, QA/QC, and structured data management
- Facilitates assessment of pollution pathways, environmental health risks, and seafood safety through standardized, transparent reporting
- Supports data governance needs by openly detailing data collection, processing, and quality assurance procedures, enabling replication and comparability across programs

## Acknowledgements and references
- Acknowledges Welsh Water for wastewater samples and the field team
- References include foundational methods for real-time PCR assays and prior related work on environmental virology and method validation