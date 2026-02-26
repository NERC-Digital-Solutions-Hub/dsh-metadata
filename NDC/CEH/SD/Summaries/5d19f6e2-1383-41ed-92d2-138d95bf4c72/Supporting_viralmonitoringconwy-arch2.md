# Enteric virus concentrations and chemical properties of wastewater, water, sediment and shellfish samples collected along the Conwy River and estuary, North Wales.

## Overview
- Longitudinal environmental monitoring dataset (2016–2017) assessing enteric viruses and basic chemical properties in wastewater, surface water, sediment, and mussels along the Conwy River and estuary.
- Data generated to support environmental health assessments and policy performance over time.

## Sampling regime and collection methods
- Four-weekly sampling from 17 May 2016 to 1 August 2017.
- Matrices collected: surface water (10 L), sediment (10 g), and mussels (20 individuals); wastewater influent and effluent provided by Welsh Water.
- Sampling points include three wastewater treatment plants (Ganol, Betws-y-Coed, Tal-y-Bont, with corresponding influent/effluent) and multiple surface water and shellfish sites (e.g., Betws-y-Coed area, Conwy, Llandudno).
- Samples stored at 4°C for up to 24 hours prior to processing.
- Detailed sample codes and site coordinates provided (Table 1).

## Laboratory instrumentation and processing
- In-field/bench measurements: pH (pH meter), turbidity (NTU), conductivity (mS), and filtration system for viral concentration.
- Viral concentration: two-step method using tangential flow filtration, backwash, beef extract elution, polyethylene glycol precipitation; final concentrate stored at -80°C.
- Virus elution from sediment and shellfish using standard extraction procedures; shellfish extraction follows ISO/TS 15216-1:2013.

## Nucleic acid extraction and quantification
- Nucleic acid extraction from viral concentrates using commercial purification systems.
- Quantification targets:
  - Norovirus GI and GII, Hepatitis A and E, Sapovirus GI, Mengovirus (process control).
  - Human Adenovirus DNA quantified with SYBR Green qPCR.
  - JC and BK polyomaviruses quantified with TaqMan qPCR.
- qRT-PCR assays as described in referenced literature; two triplex/qPCR configurations and one SYBR Green assay used.
- Primer/probe sequences and assay conditions summarized (Table 2).
- Capsid integrity of Norovirus assessed using porcine gastric mucin-conjugated magnetic beads (PGM-MBs) with subsequent qRT-PCR.

## Quality control and validation
- Method validation via spiking experiments for sediment and water samples; recoveries generally in the 10–100% range for water and 80–100% for sediment, supporting method suitability.
- Process controls (Mengovirus VMC0) with recoveries >10% across samples.
- Duplicates run for each sample; non-template controls included; calibration and background checks performed for qPCR assays.

## Data structure and recorded values
- Dataset compiled into a single CSV file with a comprehensive metadata structure (Table 3).
- Recorded variables include:
  - Sample code, date, time, volume/weight processed, pH, turbidity (NTU), conductivity (mS).
  - Viral concentrations: NoV GI/GII, HAV, HEV, SaVGI, AdV, JCV, BKV with units gc per liter for water or gc per gram for sediment/mussel.
  - PGM-assisted capsid integrity results for NoV where applicable.
- Detection limits: 100 gc/L for water, 10 gc/g for sediment, 200 gc/g for mussel; quantification limits around 200 gc/L for water, 100 gc/g for sediment, 500 gc/g for shellfish.
- Non-detects indicated as below detection limit; some wastewater conductivity measurements omitted due to low values.
- The dataset references prior method validation work (Farkas et al., 2017a, 2017b, 2018) for context and comparability.

## Relevance for environmental monitoring analysts
- Provides standardized, QA’d data across multiple environmental matrices, enabling temporal and spatial trend analyses of human enteric viruses in wastewater and receiving waters.
- Clear documentation of methods, detection limits, and data structure supports data integrity, comparability, and re-use for policy assessment and environmental health monitoring.
- Data can be integrated with other environmental datasets to enhance interpretability and value.

## Data accessibility and stewardship
- Data are structured for storage and potential upload to appropriate data portals, aligning with standard monitoring practices for transparency and accessibility.
- Acknowledges collaboration with Welsh Water and field/processing teams, emphasizing data provenance and operational support.

## Challenges and opportunities for the archetype
- Opportunities to increase data value by integrating these virus and water-chemistry data with complementary environmental datasets (e.g., rainfall, land use, upstream discharges).
- Emphasizes making underlying data more accessible to stakeholders to improve transparency and policy evaluation.