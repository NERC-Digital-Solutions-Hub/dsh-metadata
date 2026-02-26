# Enteric virus concentrations, pH and turbidity in wastewater discharged to the Conwy River and estuary, North Wales (2016-2017)

## Study design and sampling regime
- Three wastewater treatment plants (WWTPs): Betws-y-Coed, Llanrwst, Ganol (Llandudno Junction) discharging to the Conwy River.
- Sampling method: ISCO automatic water samplers collecting wastewater.
- Betws-y-Coed and Llanrwst: samples taken from the discharge pipe entering the river (effluent); Ganol: sampler at WWTP capturing influent.
- Sampling schedule: every two hours for three days, yielding 36 samples per site; sampling conducted across three seasons (summer, autumn, winter).
- Sample coding includes site, wastewater type, and season (e.g., Betws-y-coed_summer, Betws-y-coed_autumn, Ganol_winter).

## Laboratory measurements and instrumentation
- Physicochemical measurements:
  - pH measured with S2K922 Waterproof pocket pH meter.
  - Turbidity measured with T-100 Handheld Turbidity meter (NTU).
- Viral concentration and processing:
  - Concentration by KrosFlo tangential flow filtration to ~50 mL concentrate.
  - Elution with 3% beef extract + 2 mM NaNO3 (pH 5.5); PEG 6000 precipitation; final resuspension in 2–4 mL PBS (pH 7.4).
  - Nucleic acid extraction from 0.5 mL concentrate; final extraction volume 0.1 mL.
- Viral targets and quantification:
  - Norovirus GI, GII; Sapovirus GI; Hepatitis A (HAV); Hepatitis E (HEV); quantified by triplex or singleplex one-step qRT-PCR (RNA Ultrasense kit) with specified annealing temps (56°C for some assays, 60°C for others).
  - Adenovirus DNA quantified by SYBR Green qPCR (QuantiFast kit).
  - Process controls: Mengovirus (strain VMC0) spiked into autumn/winter samples; recovery >10%.
- Assay details:
  - Primers/probes listed in Table 2; multiplexing adjustments noted (fluorescent dyes replaced for multiplex development).
  - Reaction mixes, cycling conditions, and quality controls (no-template controls, plasmid standards, duplicate runs).

## Data types and units
- pH: unitless (no units reported).
- Turbidity: Nephelometric Turbidity Units (NTU).
- Viral concentrations: genome copies per liter (gc/L) for concentrated wastewater samples (NoVGI, NoVGII, SaVGI, HAV, HEV, AdV); detection limit 100 gc/L; quantification limit ≈ 200 gc/L.
- Negative results: below detection limit; Detected vs. Not Quantified distinctions explained.

## Data structure and accessibility
- Data stored in a single CSV file (Dataset) with standardized columns:
  - Sampling_event
  - Sample_type (untreated influent or treated effluent)
  - Date_Time(GMT)
  - pH
  - Turbidity_NTU
  - NoVGI_gc/l
  - NoVGII_gc/l
  - SaV_gc/l
  - HAV_gc/l
  - HEV_gc/l
  - AdV_gc/l
- Column definitions described in Table 3 (values n.m. indicate not measured for some events).
- Dataset format supports reuse and linkage to outputs (maps, charts, reports) and facilitates cross-study comparisons.

## Quality control and data reliability
- Process control (mengovirus) recovery validated; recovery >10% across autumn/winter samples.
- All qPCR/qRT-PCR runs included duplicates, non-template controls, and plasmid standards for calibration.
- Calibration details:
  - pH meter calibrated with 7.0 pH buffer.
  - Turbidity meter calibrated with standard NTU solutions (800, 100, 20, 0.02 NTU).
  - qPCR/qRT-PCR calibration performed with background noise checks and dye-specific calibration; samples run in duplicates.

## Context and usage
- Recent publications cite the dataset as part of studies on seasonal and spatial dynamics of enteric viruses in wastewater and receiving waters.
- Data structure and QC enable integration with other environmental datasets and support standardised cross-site and temporal comparisons.

## Key relevance for environmental monitoring analysts
- Demonstrates a standardised workflow from field sampling to molecular quantification suitable for environmental health monitoring.
- Provides a structured, high-quality dataset linking physicochemical parameters (pH, turbidity) with enteric virus concentrations across multiple sites and seasons.
- Emphasises data provenance, QA/QC, and data-sharing readiness to enhance reuse and policy-relevant insights.