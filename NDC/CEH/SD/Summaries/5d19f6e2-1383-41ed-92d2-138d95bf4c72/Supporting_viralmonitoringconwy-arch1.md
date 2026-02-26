# Enteric virus concentrations and chemical properties of wastewater, water, sediment and shellfish samples collected along the Conwy River and estuary, North Wales.

## Study design and sampling regime
- Four-weekly sampling from 17 May 2016 to 1 August 2017.
- Sample types per site: surface water (10 L), sediment (10 g), mussel tissue (20 individuals).
- Wastewater influent and effluent provided by Welsh Water.
- Sampling points and site codes include:
  - Wastewater: Ganol (GI influent; GE effluent), Betws-y-Coed (BI influent; BE effluent), Llarwst (LI influent; LE effluent), Tal-y-Bont (TI influent; TE effluent).
  - Surface waters: SW1–SW4 (Betws-y-Coed Afon Llugwy; River Conwy; Llarwst; Conwy Beacon).
  - Sediments and shellfish beds: Sed1/Sed2/Sed4; SF1/SF2 (Conwy and Llandudno shellfish beds).
- Sediment sampling targeted the top 1–2 cm; mussels collected at low tide.

## Analytical methods and measurements
- On-site measurements: pH (pH meter), turbidity (NTU), conductivity (mS).
- Water concentration: Tangential Flow Filtration system used for virus concentration.
- Laboratory instrumentation: pH meter, turbidity meter, conductivity meter, filtration system, nucleic acid purification and qPCR/qRT-PCR equipment.
- Calibration: standard solutions and procedures for pH, turbidity, and qPCR assays; duplicates and negative controls included.

## Sample processing and concentration
- Water: two-step concentration to ~50 mL concentrate.
  - Initial concentration with 100 kDa tangential flow filter; backwash with sodium polyphosphate.
  - Elute with beef extract/NaNO3; precipitate with PEG 6000/NaCl; resuspend in PBS.
- Sediment: elution with beef extract/NaNO3; aliquots stored at -80°C.
- Mussel tissue: ISO/TS 15216-1:2013 method; digestive tissue from 20 mussels spiked with Mengovirus as process control.
- Nucleic acid extraction: from 0.5 mL concentrate; final extract ~0.1 mL.

## Viral targets and quantification
- Target viruses and controls: NoV GI and GII, HAV, HEV, SaVGI, Mengovirus (MgV) as process control, Adenovirus (AdV), JC polyomavirus (JCV), BK polyomavirus (BKV).
- Quantification methods:
  - NoV GI/GII, SaVGI, HAV, HEV, MgV: triplex or singleplex one-step qRT-PCR assays.
  - Adenovirus, JC, BK: qPCR or qRT-PCR depending on assay; SYBR Green used for AdV.
- Reagents and cycling details provided for each assay (primer/probe sets, reaction mixes, annealing temperatures, cycle conditions).
- Detection limits and quantification limits:
  - NoV and other viruses reported as genome copies per liter (water) or per gram (sediment/mussel).
  - Detection limits: ~100 gc/L water, 10 gc/g sediment, 200 gc/g mussel.
  - Quantification limits: ~200 gc/L water, 100 gc/g sediment, 500 gc/g shellfish.
- Primers/probes compiled in Table 2; references listed for assay design.

## Capsid integrity assay
- Norovirus capsid integrity assessed using porcine gastric mucin-conjugated magnetic beads (PGM-MBs).
- Process: concentrate diluted; incubated with PGM-MGs; magnetic separation; heated; RNA quantified by qRT-PCR.
- Mussel samples excluded due to prior proteinase K treatment affecting particles.

## Quality control and validation
- Spiking controls: sediment recoveries 80–100%; surface water recoveries 10–100% (varies by matrix).
- Process control MgV recovery >10% in all cases, indicating efficient concentration/extraction.
- Calibration/controls included for qPCR/qRT-PCR; non-template controls or dilution series used.

## Data structure and accessibility
- Data stored in a single CSV file; column definitions described (Table 3).
- Key columns include Sample_code, Date, Time_GTM, Volume, pH, Turbidity, Conductivity, and virus concentration columns (e.g., NoVGI_(gc/UnitVol), NoVGII_(gc/UnitVol), HAV, HEV, SaV, AdV, JCV, BKV) plus corresponding PGM-adjusted values where applicable.
- Units and interpretation:
  - pH reported without units.
  - Turbidity in NTU; Conductivity in mS.
  - Virus concentrations in genome copies per liter (water) or per gram (sediment/mussel); “Negative” indicates below detection limit; “Detected” indicates above detection but below quantification limit.
- Data notes:
  - BKV targeted only in March 2016 wastewater samples.
  - Table 3 and metadata describe field descriptions and data handling.
- References and acknowledgment sections provide context and attribution.

## Potential analyses and insights for data-driven questions
- Correlations between viral concentrations and water quality parameters (pH, turbidity, conductivity).
- Comparison of concentrations in influent vs. effluent wastewater, and downstream river/estuary dynamics.
- Spatial patterns across sites (WWTPs and surface water sites) and across matrices (water, sediment, shellfish).
- Capsid integrity results to distinguish potentially infectious (intact) viruses from degraded particles.
- Assessment of method performance across matrices via recovery rates and detection limits.
- Foundation for local risk assessments of shellfish safety and wastewater management; enable predictive modelling of contamination under varying environmental conditions.
- Limitations to consider: four-week sampling cadence; detection/quantification limits; some missing data points (e.g., BKV across time); matrix-specific variability.