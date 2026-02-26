# Enteric virus concentrations, pH and turbidity in wastewater discharged to the Conwy River and estuary, North Wales (2016-2017)

## Overview
- Study monitors enteric virus concentrations, pH, and turbidity in wastewater discharged to the Conwy River estuary, North Wales, at three WWTPs: Betws-y-Coed, Llanrwst, and Ganol (Llandudno Junction) during 2016–2017.
- Data collection includes multiple viruses (NoV GI/GII, SaV GI, HAV, HEV, AdV, Mengovirus as process control) and physical-chemical parameters (pH, turbidity).

## Sampling regime and data collection
- Sampling method: ISCO automatic water samplers at each site.
- Sample type and collection: effluent sampled at Betws-y-Coed and Llanrwst; influent sampled at Ganol; 1 L effluent and 0.7 L influent collected every second hour for three days per event, totaling 36 samples per site.
- Seasons and site codes described (summer, autumn, winter for Betws-y-Coed and Llanrwst; autumn/winter for Ganol).

## Laboratory instrumentation and calibration
- pH measurements: S2K922 pocket pH meter.
- Turbidity measurements: T-100 Handheld Turbidity meter.
- Nucleic acid extraction: NucliSENS MiniMag; Safe Aspiration station; Thermomixer.
- Quantification: Flex 6 Quant Studio Real-time PCR system; calibration and quality controls described.
- Calibration practices:
  - pH: 7.0 calibration solution used before each use.
  - Turbidity: NTU standards used for calibration.
  - qRT-PCR/qPCR: background noise checked quarterly; dye/pipeline calibration annually; runs include duplicates, non-template controls, and plasmid dilution standards.

## Nature and units of recorded values
- pH: unitless.
- Turbidity: Nephelometric Turbidity Units (NTU).
- Viral data: genome copies per liter (gc/L) of concentrated wastewater for NoVGI, NoVGII, SaVGI, HAV, HEV, AdV; negative indicates below detection; detection limit ~100 gc/L; quantification limit ~200 gc/L.
- Data interpretation notes: detection/quantification limits referenced to prior work (Farkas et al., 2017, 2018).

## Wastewater concentration and viral nucleic acid quantification
- Concentration method: two-step process using KrosFlo tangential-flow filtration (100 kDa membrane) to ~50 mL concentrate; elution with beef extract and NaNO3; precipitation with PEG 6000 and NaCl; final resuspension in phosphate saline buffer.
- Nucleic acid extraction: 0.5 mL of concentrate processed; final nucleic acid volume 0.1 mL.
- Viral nucleic acid quantification:
  - NoVGI, NoVGII, SaVGI, HAV, HEV, MgV quantified by singleplex or triplex qRT-PCR assays.
  - AdV DNA quantified by SYBR Green qPCR.
  - Assay details include primer/probe sets, reaction mixes, and cycling conditions.
  - Assays run with appropriate controls (no-template, plasmid standards) and duplicates.
- Primer/probe references provided; dyes were adjusted for multiplexing.

## Quality control
- Process control: Mengovirus (VMC0) spiked into autumn/winter samples; recovery >10% across tests, indicating reliable concentration and extraction and representative data.

## Data structure and dataset description
- Dataset stored in a single CSV file.
- Key columns (Table 3) include:
  - Sampling_event, Sample_type (influent or effluent), Date_Time_GMT, pH, Turbidity_NTU, NoVGI_gc/l, NoVGII_gc/l, SaV_gc/l, HAV_gc/l, HEV_gc/l, AdV_gc/l.
- Data notes:
  - n.m. indicates values not measured.
  - Negative values indicate concentrations below the detection limit.
- Data usage: recent example publications cited (N/A for this dataset).

## Data usage notes and potential products
- Data suitable for dashboards and self-serve analysis linking viral concentrations with pH and turbidity across sites and seasons.
- Clear documentation of detection/quantification limits and quality controls supports robust data interpretation.
- Opportunities to extend with regional trends, comparisons across sites, and integration with other water-quality datasets.

## Acknowledgements and references
- Acknowledges Welsh Water and individuals for sampling and processing support.
- References provide sources for primers, assays, and related methodological validation.