# Enteric virus concentrations, pH and turbidity in wastewater discharged to the Conwy River and estuary, North Wales (2016-2017)

- Overview
  - Dataset of enteric virus concentrations, pH and turbidity in wastewater discharged to the Conwy River and estuary, North Wales, during 2016-2017.
  - Collected at three wastewater treatment plants: Betws-y-Coed, Llanrwst, and Ganol (Llandudno Junction).
  - Sampling regime involved automatic ISCO samplers, with 36 samples per site over the study period (every second hour for three days per event).
  - Measurements include pH, turbidity (NTU), and concentrations of multiple viruses (Norovirus GI and GII, Sapovirus GI, Hepatitis A and E, Adenovirus) expressed as genome copies per liter; an internal process control (mengovirus) was used to assess recovery.
  - Data structure: a single CSV with concentration and metadata fields, and extensive methodological details to support reproducibility and data governance.

- Data collection regime
  - Sites and sampling: Betws-y-Coed (effluent), Llanrwst (effluent), Ganol (influent) wastewater discharge into the Conwy River.
  - Sampling method: ISCO automatic water sampler; samples collected twice daily for three days per event, yielding 36 samples per site.
  - Sample codes denote site, season (summer, autumn, winter), and wastewater type; sample coordinates are recorded.
  - Data captures seasonal and spatial dynamics relevant to environmental virology.

- Measurements and data types
  - Physicochemical measurements: pH (unitless), turbidity (NTU).
  - Viral metrics: concentrations of NoV GI, NoV GII, Sapovirus GI, HAV, HEV, and Adenovirus, expressed as genome copies per liter (gc/L) of the concentrated wastewater.
  - Detection and quantification: detection limit ~100 gc/L; quantification limit ~200 gc/L; ‘Negative’ indicates below detection limit; ‘Detected’ indicates detectable but below quantification limit.
  - Data columns (example): Sampling_event, Sample_type (influent/effluent), Date_Time(GMT), pH, Turbidity_NTU, NoVGI_gc/l, NoVGII_gc/l, SaV_gc/l, HAV_gc/l, HEV_gc/l, AdV_gc/l.

- Laboratory methods and calibration
  - Instrumentation:
    - pH: S2K922 Waterproof pocket-sized pH meter.
    - Turbidity: T-100 Handheld Turbidity meter.
    - Filtration: KrosFlo Research IIi Tangential Flow Filtration System for concentration.
    - Nucleic acid extraction: NucliSENS MiniMag Nucleic Acid Purification System; Gilson Safe Aspiration station; Thermomixer.
    - Quantification: Flex 6 Quant Studio Real-time PCR system.
  - Calibration and controls:
    - pH calibration with manufacturer-provided pH buffers before use.
    - Turbidity calibration with standard NTU solutions (800, 100, 20, 0.02 NTU).
    - qRT-PCR/qPCR calibration: background noise and dye-specific calibrations; runs include duplicates, no-template controls (NTCs), and plasmid-based standards.
  - Assay details:
    - Viral targets quantified by one-step qRT-PCR (triplex or singleplex) for NoV GI/GII, SaV, HAV, HEV, and MgV; Adenovirus quantified by SYBR Green qPCR.
    - Reaction parameters, primer/probe sets, and annealing temperatures provided (with references).
  - Data processing:
    - Sample concentrates stored at 4°C up to 24 hours, then at -80°C.
    - Nucleic acids extracted from 0.5 mL of concentrate, final volume 0.1 mL.
    - qRT-PCR setup, cycle conditions, and validation steps described for reproducibility.

- Data structure and metadata
  - Dataset format: a single CSV file containing concentration data and metadata.
  - Column headings (metadata description) include:
    - Sampling_event, Description = site, season, and event details.
    - Sample_type, Description = wastewater type (untreated influent or treated effluent).
    - Date_Time(GMT), Description = sampling date/time (GMT).
    - pH, Turbidity_NTU = physicochemical measurements.
    - NoVGI_gc/l, NoVGII_gc/l, SaV_gc/l, HAV_gc/l, HEV_gc/l, AdV_gc/l = viral concentrations (gc/L) for respective targets.
  - Additional dataset context: sample codes and site coordinates are described in the accompanying sample-code table; relevant primers and probes are listed in Table 2 (primers/probes; multiplexing notes).

- Quality assurance and control
  - Process controls: Mengovirus (VMC0) spiked into autumn and winter samples; recovery >10% across tests, indicating reliable extraction and concentration.
  - QC measures: samples run in duplicates; inclusion of no-template controls; use of plasmid standards and internal dyes in qPCR assays.
  - Data interpretation: negative results indicate concentrations below detection limit; detected results indicate quantifiable or near-quantifiable concentrations per defined limits.

- Data governance, stewardship, and reuse notes
  - Data provenance: detailed description of sampling, concentration, extraction, and quantification workflows supports traceability and reproducibility.
  - Metadata richness: site, season, sampling type, timing (GMT), and coordinates enable spatial-temporal analyses and data discovery.
  - Data licensing and sharing: the document does not specify a data sharing license or repository; governance steps should apply (e.g., institutional policies) before public release.
  - Potential reuse: suitable for environmental virology studies, wastewater-based epidemiology, and relationships between virus concentrations, pH, and turbidity, with explicit measurement limits and QC context informing interpretation.
  - Acknowledgements and references: funding/assistance acknowledged; references provided for assay designs and related methodological work.

- Limitations and caveats
  - Detection/quantification limits constrain interpretation of low-concentration results.
  - The Multiplexing approach and primer/probe details require careful reproducibility considerations when reusing the data.
  - No published reuse examples listed in the document; future analyses should cite the original methodological framework and data structure.