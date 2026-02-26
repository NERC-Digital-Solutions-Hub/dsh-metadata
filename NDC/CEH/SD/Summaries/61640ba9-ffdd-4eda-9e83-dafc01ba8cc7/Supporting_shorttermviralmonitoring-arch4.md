# Enteric virus concentrations, pH and turbidity in wastewater discharged to the Conwy River and estuary, North Wales (2016-2017)

## Overview
- Aim: quantify enteric viruses, pH, and turbidity in wastewater discharged to the Conwy River and estuary during 2016–2017.
- Study sites: three major wastewater treatment plants (Betws-y-Coed, Llanrwst, Ganol) discharging to the Conwy River.
- Data scope: measurements include pH, turbidity (NTU), and concentrations of multiple viruses (norovirus GI and GII, sapovirus GI, hepatitis A and E, adenovirus) expressed as genome copies per litre (gc/L) of wastewater.

## Sampling regime and collection methods
- Sampling equipment: ISCO automatic water samplers.
- Sampling points: at plant discharge pipes (Betws-y-Coed and Llanrwst) or WWTP influent (Ganol).
- Regime: samples collected every second hour for three days per site (36 samples per site); samples collected daily and transported to the laboratory.
- Sample types and timing: combinations of influent and effluent samples across seasons (summer, autumn, winter) with site-specific codes (e.g., Betws-y-coed_summer effluent, Ganol_autumn influent).
- Geographic data: recording of site coordinates for each sample.

## Laboratory instrumentation
- pH measurements: S2K922 Waterproof pocket-sized pH meter.
- Turbidity measurements: T-100 Handheld Turbidity meter.
- Concentration and filtration: KrosFlo Research IIi Tangential Flow Filtration System.
- Nucleic acid extraction: NucliSENS MiniMag Nucleic Acid Purification System; Gilson Safe Aspiration station.
- Mixing/handling: ThermoMixer Compact.
- Quantification: Flex 6 Quant Studio Real-time PCR system.

## Nature and units of recorded values
- pH: unitless.
- Turbidity: Nephelometric Turbidity Units (NTU).
- Viral data: genome copies per litre (gc/L) for water samples; also noted for sediment/mussel in some contexts (noted as gc per gram in some descriptions).
- Detection/quantification limits: detection limit 100 gc/L; quantification limit ≈ 200 gc/L.
- Negative/Below-detection: reported when concentrations are below detection limit.

## Wastewater concentration
- Method: two-step concentration.
  - Initial concentration with KrosFlo tangential flow filtration (100 kDa) to reduce volume from sample to concentrate (~50 mL).
  - Elution with 3% beef extract with 2 mM NaNO3 (pH 5.5), followed by PEG 6000/NaCl precipitation.
  - Final resuspension in 2–4 mL phosphate-buffered saline (pH 7.4).
- Storage: concentrates stored at 4°C for up to 24 hours, then at -80°C.

## Viral nucleic acid extraction
- Extraction from 0.5 mL of viral concentrate, following manufacturer guidelines.
- Final nucleic acid volume: 0.1 mL.

## Viral nucleic acid quantification
- Targets and methods:
  - RNA viruses quantified by singleplex or triplex one-step qRT-PCR (NoV GI, NoV GII, Sapovirus GI, Hepatitis A, Hepatitis E) using RNA Ultrasense kits and specific primers/probes.
  - Adenovirus DNA quantified by SYBR Green qPCR.
- Reaction details: 20 µL total volume with specified enzyme mixes, primers, probes, BSA; cycling conditions with appropriate annealing temperatures per assay.
- Primers/probes: listed in the document (Table 2) with references.
- Quality controls: duplicates per run; non-template controls; dilution series of target DNA/RNA; inclusion of a plasmid-based standard.
- Process controls: samples spiked with Mengovirus (VMC0) to assess recovery.

## Data structure
- Dataset format: a single CSV spreadsheet.
- Key columns (examples):
  - Sampling_event: site and season description (e.g., Betws-y-coed_summer_effluent).
  - Sample_type: untreated influent or treated effluent.
  - Date_Time(GMT): date and time of sampling.
  - pH: pH value (unitless).
  - Turbidity_NTU: turbidity in NTU.
  - NoVGI_gc/l, NoVGII_gc/l, SaV_gc/l, HAV_gc/l, HEV_gc/l, AdV_gc/l: virus concentrations in gc/L.
- Metadata context: detailed description of sampling events, sites, and sample types (Table 1 and Table 3 references in the document).

## Acknowledgements and references
- Acknowledgements: thanks to Welsh Water for influent sampling assistance; thanks to individuals for sample processing support.
- References: includes foundational methods and primers/probes literature (e.g., Da Silva et al. 2007; Chan et al. 2006; Costafreda et al. 2006; Loisy et al. 2005; Kageyama et al. 2003; Pinto et al. 2009; others).