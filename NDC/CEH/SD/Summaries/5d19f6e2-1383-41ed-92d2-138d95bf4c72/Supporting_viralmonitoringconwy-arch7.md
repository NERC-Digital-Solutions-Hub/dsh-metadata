# Enteric virus concentrations and chemical properties of wastewater, water, sediment and shellfish samples collected along the Conwy River and estuary, North Wales.

- A study detailing concentrations of enteric viruses and chemical properties in wastewater, surface water, sediments, and shellfish along the Conwy River and estuary, North Wales.
- Timeframe: four-weekly sampling from 17 May 2016 to 1 August 2017.

## Scope and sampling regime

- Sample types and sites
  - Wastewater: Ganol (GI—influent; GE—effluent)
  - Wastewater: Betws-y-Coed (BI—influent; BE—effluent)
  - Wastewater: Llarwst (LI—influent; LE—effluent)
  - Wastewater: Tal-y-Bont (TI—influent; TE—effluent)
  - Surface water: SW1 Betws-y-Coed, Afon Llugwy; SW2 Betws-y-Coed, River Conwy; SW3 Llarwst; SW4 Conwy, Beacon
  - Sediment/shellfish: Sed1 Llandudno shellfish bed; Sed2 Conwy shellfish bed; Sed4 Conwy, Beacon; SF1 Llandudno shellfish bed; SF2 Conwy shellfish bed
- Sampling frequency and methods
  - Surface water (10 L), sediment (10 g), and mussel (20 individuals) collected every four weeks; storage at 4°C for up to 24 h before processing
  - Detailed sample codes and coordinates provided (Table 1 in the original)
- Geographic details
  - Coordinates for wastewater plants and water/shellfish sampling sites are recorded (e.g., Ganol: 53°16'43.6"N, 3°47'32.9"W; Betws-y-Coed: 53°05'44.0"N, 3°48'01.8"W; etc.)

## Analytical workflow and instrumentation

- In-field and sample processing
  - pH: S2K922 waterproof pH meter
  - Turbidity: T-100 handheld turbidity meter
  - Conductivity: 4520 Conductivity meter
  - Filtration/concentration: KrosFlo tangential flow filtration system for initial concentration
- Nucleic acid handling
  - Extraction: NucliSENS MiniMag system; Gilson Safe Aspiration; Thermomixer compact
  - Quantification: Flex 6 Quant Studio Real-time PCR system
- Quality controls and calibration
  - Regular calibration for pH, turbidity, and qPCR/qRT-PCR assays
  - Duplicate runs with non-template controls and plasmid standards
  - Calibration and dye-specific adjustments for multiplex assays

## Viral targets and quantification

- Viruses quantified
  - Norovirus GI (NoVGI) and GII (NoVGII)
  - Sapovirus GI (SaVGI)
  - Hepatitis A (HAV) and Hepatitis E (HEV)
  - Mengovirus (MgV) as process control
  - Adenovirus (AdV), JC polyomavirus (JCV), BK polyomavirus (BKV)
- Assay types and conditions
  - NoVGI, NoVGII, SaVGI, HAV, HEV quantified via triplex or duplex qRT-PCR assays
  - MgV quantified via qRT-PCR
  - AdV, JCV, BKV quantified via qPCR or qRT-PCR with specific primer/probe sets
  - Primers/probes (Table 2) used as described in prior work; different annealing temperatures per assay
- Units and interpretation
  - Virus concentrations reported as genome copies (gc) per liter for water or per gram for sediment/mussel
  - “Detected” indicates below quantification limit; “Negative” indicates below detection limit
  - Detection limits: ~100 gc/L (water), ~10 gc/g (sediment), ~200 gc/g (shellfish); quantification limits ~200 gc/L (water), ~100 gc/g (sediment), ~500 gc/g (shellfish)

## Capsid integrity assay (Norovirus)

- Capsid integrity assessed for NoV positives using porcine gastric mucin-conjugated magnetic beads (PGM-MBs)
- Protocol notes
  - Mussel samples excluded due to prior processing steps
  - Dilution and magnetic separation steps followed by RNA extraction and qRT-PCR

## Data handling, quality control, and structure

- Data validation
  - Process and method validations conducted with spiking experiments
  - Recovery ranges: 80–100% for sediment; 10–100% for surface water
  - Process control MgV recovery > 10% across samples
- Data structure and availability
  - Data stored in a single CSV file; columns described in Table 3 of the original
  - Missing values represented as empty fields
  - BKV targeted only in March 2016 wastewater samples; not pursued subsequently
- Metadata and reproducibility
  - Comprehensive methodological details enable cross-site spatial analysis and temporal trend assessment
  - Clear documentation of sampling points, dates, volumes, and analytical parameters supports GIS-based visualization

## GIS-relevant considerations and potential data products

- Spatial visualization
  - Coordinate data for all sampling sites enables mapping of viral and chemical properties along the Conwy River and estuary
  - Ability to create layer groups: wastewater influent/effluent, surface water sites, sediments, and shellfish beds
- Temporal analysis
  - Four-weekly sampling over more than a year allows for seasonal/water-quality trend mapping
- Data integration
  - Multi-parameter dataset (pH, turbidity, conductivity, and viral gc/g) supports composite indicators and risk mapping
  - Dataset structure (CSV with standardized column headers) facilitates import into GIS platforms for spatial statistics and visualization
- Data standards and provenance
  - Detailed method descriptions, calibration notes, and QA/QC provide traceability for data consumers and GIS analysts

## Acknowledgements and references

- Acknowledges Welsh Water for wastewater samples and team members involved in collection and processing
- References listed for methodological primers and related studies (e.g., Farkas et al., 2017-2018; various primer/probe sources) to support data interpretation and reproducibility