# Enteric virus concentrations, pH and turbidity in wastewater discharged to the Conwy River and estuary, North Wales (2016-2017)

## Overview
- Study of wastewater chemistry and enteric virus concentrations at three WWTPs discharging to the Conwy River: Betws-y-Coed, Llanrwst, and Ganol (Llandudno Junction).
- Timeframe: 2016–2017, capturing seasonal variation (summer, autumn, winter).
- Data collected include pH, turbidity (NTU), and concentrations of multiple viruses (norovirus GI and GII, sapovirus GI, hepatitis A and E, and adenovirus, plus Mengovirus as a process control).
- Designed to support analyses of correlations, spatial/temporal patterns, and potential predictive relationships between water quality parameters and viral loads.

## Sampling regime and collection methods
- Sampling sites and wastewater types:
  - Betws-y-Coed: effluent entering the river.
  - Llanrwst: effluent entering the river.
  - Ganol: influent at the Ganol WWTP.
- Sampling apparatus: ISCO automatic water sampler.
- Sampling protocol:
  - For Betws-y-Coed and Llanrwst: 1 L effluent and 0.7 L influent collected every two hours for three days (36 samples per site).
  - Ganol: sampler at WWTP, collecting influent prior to treatment.
- Seasonal sampling codes (per site/date) include Betws-y-coed_summer, Betws-y-coed_autumn, Betws-y-coed_winter, Llanrwst_summer/autumn, Ganol_autumn/winter, with exact start dates and coordinates provided.
- Detailed sample metadata included in a table of sample codes, sites, wastewater type, and geographic coordinates.

## Laboratory instrumentation and measurements
- pH measurements: S2K922 Waterproof pocket-sized pH meter.
- Turbidity measurements: T-100 Handheld Turbidity meter.
- Water concentration: KrosFlo Tangential Flow Filtration system for viral concentration.
- Nucleic acid extraction: NucliSENS MiniMag system; Gilson Safe Aspiration station; Thermomixer for processing.
- Quantification: Flex 6 Quant Studio Real-time PCR system.
- Calibration and quality checks:
  - pH calibration with manufacturer-provided buffer solutions before use.
  - Turbidity calibration with standard NTU solutions (800, 100, 20, 0.02 NTU).
  - qPCR/qRT-PCR calibration for background noise and dye specificity; runs performed in duplicates; inclusion of non-template controls and a plasmid-based dilution series.
- Viruses targeted and detection approach:
  - Norovirus GI and GII, sapovirus GI, hepatitis A virus, hepatitis E virus, and mengovirus (MgV) quantified by triplex/qRT-PCR assays.
  - Human adenovirus (AdV) DNA quantified by SYBR Green qPCR.
  - Sample volumes and reaction conditions detailed (20 μL reactions; specific primer/probe sets and annealing temperatures; reverse transcription steps for RNA viruses; duplex/triplex assay configurations).
- Probes and primers:
  - Primers/probes for NoV GI/GII, SaV GI, HAV, HEV, MgV, with references.
  - AdV primers/probe listed; note that original dye labels were modified for multiplexing.
- Quality control:
  - Process control (mengovirus) spiked into autumn and winter samples; recovery >10% in all cases, indicating efficient concentration and extraction.

## Data structure, units, and quality indicators
- Data structure: a single CSV spreadsheet containing all measurements.
- Columns (primary examples):
  - Sampling_event (site + season), Sample_type (influent or effluent), Date_Time (GMT).
  - pH, Turbidity_NTU.
  - NoVGI_gc/l, NoVGII_gc/l, SaV_gc/l, HAV_gc/l, HEV_gc/l, AdV_gc/l.
- Units and interpretation:
  - pH: unitless (as reported).
  - Turbidity: Nephelometric Turbidity Units (NTU).
  - Viral data: genome copies per liter (gc/l) of concentrated wastewater; 'Negative' indicates below detection limit; 'Detected' indicates below quantification limit.
  - Detection limit: 100 gc/L; Quantification limit: approximately 200 gc/L.
- Data usage notes:
  - Data entries are organized by sampling event, site, and wastewater type, enabling correlation analyses across time, space, and physico-chemical parameters.

## Data processing and reproducibility
- Viral concentration and extraction followed described two-step protocol (tangential flow concentration, beef extract elution, PEG precipitation, final resuspension).
- Nucleic acid extraction performed per manufacturer instructions with strict adherence to volumes and final nucleic acid yield.
- qRT-PCR/qPCR assays run with duplicate reactions, appropriate controls, and standard curves to enable relative and absolute quantification.
- Process-control recovery (>10%) supports representativeness of the measured concentrations.

## Data availability and usage notes
- Recent example publications referencing these datasets are not listed (N/A).
- The dataset is structured to support analyses of seasonal and spatial dynamics of enteric viruses in wastewater and receiving waters.
- Acknowledgments indicate collaboration with Welsh Water and individuals assisting with sampling and processing.
- References provide methodological context for the assays and primer/probe design used.

## Acknowledgments and key references
- Acknowledgements: Welsh Water; Daffydd E Peters; John D Maloney.
- Key methodological references include publications on real-time RT-PCR assays for norovirus, sapovirus, hepatitis A and E viruses, and adenovirus, as well as standardization and validation studies for these assays.