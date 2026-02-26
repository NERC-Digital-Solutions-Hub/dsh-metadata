# Enteric virus concentrations and chemical properties of wastewater, water, sediment and shellfish samples collected along the Conwy River and estuary, North Wales.

## Overview
- Study of concentrations of enteric viruses and chemical properties across wastewater, surface water, sediment, and shellfish along the Conwy River and estuary (North Wales).
- Sampling regime: four-weekly collections from 17 May 2016 to 1 August 2017.
- Data include physical-chemical measurements (pH, turbidity, conductivity) and viral nucleic acid concentrations for multiple pathogens, plus a capsid integrity assay for Norovirus.

## Sampling regime, sites and sample types
- Sample types: wastewater influent/effluent, surface water, sediment, and mussels/shellfish.
- Key site codes:
  - Ganol wastewater treatment plant: GI (influent), GE (effluent)
  - Betws-y-Coed wastewater treatment plant: BI (influent), BE (effluent)
  - Llarwst wastewater treatment plant: LI (influent), LE (effluent)
  - Tal-y-Bont wastewater treatment plant: TI (influent), TE (effluent)
  - Surface waters: SW1–SW4 (various locations including Betws-y-Coed, Conwy)
  - Sediment and shellfish: Sed1, Sed2, Sed4; SF1, SF2
- Georeferenced coordinates accompany each sample code; sample volumes are reported in liters or grams as appropriate.

## Data collected and units
- Physical-chemical measurements:
  - pH (unitless in this dataset)
  - Turbidity (NTU)
  - Conductivity (mS)
- Virological data (genome copies per unit):
  - Norovirus GI (NoVGI), GII (NoVGII)
  - Sapovirus GI (SaVGI)
  - Hepatitis A (HAV), Hepatitis E (HEV)
  - Sapovirus GI (SaVGI)
  - Adenovirus (AdV)
  - JC polyomavirus (JCV), BK polyomavirus (BKV)
  - MgV (mengovirus) used as process control
  - Units: gc per liter for water, gc per gram for sediment and mussel; “Negative” indicates below detection; quantification limits stated (e.g., ~200 gc/L for water, 100 gc/g for sediment, 500 gc/g for shellfish)
- Capsid integrity: Norovirus capsid integrity assessed for positive water/sediment samples using porcine gastric mucin-conjugated magnetic beads; results expressed as gc per unit after the integrity assay.

## Laboratory methods and quality control
- Concentration and extraction:
  - Two-step concentration for water/sediment samples (tangential flow filtration, backwash, PEG precipitation)
  - Shellfish viruses extracted following ISO/TS 15216-1:2013
- Nucleic acid detection and quantification:
  - NoVGI/GII, SaVGI, HAV, HEV quantified by triplex or duplex qRT-PCR assays
  - AdV, JCV, BKV quantified by respective qPCR/qRT-PCR assays
  - Primers and probes (Table 2) and assay conditions provided; multiple controls included (non-template control, plasmid standards, dilution series)
- Calibration and QA:
  - pH and turbidity calibration solutions and standards used
  - qPCR/qRT-PCR runs performed in duplicates with appropriate controls
  - Process controls (MgV) spiked into samples; recovery assessments
  - Reported recoveries: 80–100% for sediment NoVGII (indicating method suitability); 10–100% for surface waters (suitable for environmental matrices); MgV recovery >10% in all cases
- Capsid integrity assay:
  - Fivefold diluted positive samples tested with PGM-MG beads; RNA quantified post-assay to infer intact capsids

## Data structure and accessibility
- Data stored in a single CSV spreadsheet.
- Columns correspond to metadata and viral/chemical measurements (as described in Table 3: Sample_code, Date, Time_GTM, Volume, pH, Turbidity NTU, Conductivity mS, NoVGI, NoVGII, HAV, HEV, SaVGI, AdV, JCV, BKV, MgV controls, and PGM-assisted concentrations where applicable).
- Some fields are missing (empty cells); wastewater conductivity not measured due to near-zero values; BKV targeted only in March 2016.
- The dataset explicitly links sample codes to site details and sampling dates/times.

## Data quality considerations and limitations
- Patchy data across formats and environments; measurement gaps reflect real-world field variability.
- Detection and quantification limits influence interpretation of “Detected” vs. “Quantified” results.
- Capsid integrity results are not available for mussel samples due to processing steps degrading intact virions.
- Data accuracy depends on spiking recoveries; methodology validated with spiking experiments to ensure representativeness.

## Potential data products and insights for data support
- Time-series dashboards showing viral concentrations by site and sample type (wastewater, surface water, sediment, shellfish) over the study period.
- Spatial heatmaps of viral contamination along the Conwy River and estuary, contrasting receiving waters with wastewater inputs.
- Comparative analyses of viral loads vs. physico-chemical properties (pH, turbidity, conductivity) to explore associations.
- Self-serve data tools (pivot tables, filters) enabling end users to query by virus, sample type, or location.
- Integration with QA metrics (recovery rates) to contextualize observed concentrations and support risk assessment.

## References and provenance
- Methodological references and primers/probes details are provided (Farkas et al., 2017b; Farkas et al., 2018; related virus detection and assay development literature).
- Acknowledges Welsh Water for sample provision and field/processing contributors.