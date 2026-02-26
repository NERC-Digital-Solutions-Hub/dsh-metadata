# SARS-CoV-2 qPCR and water chemistry data from wastewater at six sites in England and Wales between March and July 2020, with associated Covid-19 positive test and related-death data collated from other sources

## Data access, licensing and citation
- Accessible via DOI: 10.5285/ce40e62a-21ae-45b9-ba5b-031639a504f7
- Licensed under Open Government Licence (OGL)
- Must cite the dataset: Hillary et al. (2021), NERC Environmental Information Data Centre

## Data description
- Two CSV files provided:
  - data_table.csv: main dataset with weekly and sample-level measurements
  - cases.csv: clinical testing data aligned to wastewater sampling period
- Key columns in data_table.csv include: Week, Date, Site_Name, Flow, SARS-CoV-2 genome copies (gc) per 100 mL for N1 and E assays, CrAssphage gc/100 mL, CrAssphage recovery, NO3, NH4, PO4, pH, EC, Deaths, Deaths_100k, Daily_Cases_100k, Population_Equivalent, Rolling_Sum_100k, Local_Authority_Population, cov_class/cov_detect, E_class/E_cov data
- Key columns in cases.csv include: Site_Name, Date, Local_Authority_Population, Daily_Cases, Cumulative_Cases, Rolling_Sum, Daily_Cases_100k, Rolling_Sum_100k, Week

## Data collection and sampling
- Six wastewater treatment plants (WWTPs) across Wales and Northwest England (Gwynedd, Cardiff, Liverpool, Manchester, Wirral, Wrexham) serving ~3 million people
- Sampling period: weekly influent samples March–July 2020 (grab samples on weekdays 08:00–09:00; Wirral also collected as a 24-hour composite)
- Treated effluent sampled periodically at the same times
- Samples transported on the same day or next day on ice; stored at 4 °C and processed within 24 h
- Aliquots frozen at -80 °C for downstream analyses

## Wastewater physicochemical analyses
- Analytes measured: ammonium (NH4), nitrate (NO3), molybdate-reactive phosphate (MRP), electrical conductivity (EC), pH
- Methods: colorimetric analyses for NH4 and NO3; MRP by Murphy & Riley; EC and pH measured with standard meters
- Analyses performed in 96-well format

## Concentration and nucleic acid extraction
- Influent: duplicate 50–100 mL samples centrifuged; supernatant concentrated to 500 µL
- Effluent: large-volume concentration via tangential flow ultrafiltration (100 kDa) followed by Centricon concentration
- Extraction controls: samples spiked with murine norovirus (MNV) to monitor extraction efficiency
- Nucleic acids extracted with NucliSENS MiniMag system; elution buffer 50–100 µL
- Extractions and q(RT-)PCR setups conducted in separate BSC-equipped labs to minimize contamination
- Extracted nucleic acids stored at -80 °C prior to q(RT-)PCR

## qPCR and qRT-PCR assays
- Targets: SARS-CoV-2 N1 and E gene; Murine Norovirus (MNV) as extraction control; CrAssphage as human fecal loading marker
- Assay formats: duplex (N1) or triplex (N1 + E) q(RT-)PCR; CrAssphage quantified separately
- Instruments and reagents: QuantStudio Real-Time PCR System; specified reaction mixes and primers/probes
- Replicates: data used are means of duplicate reactions
- Controls: negative controls included; MNV recovery used to check inhibition/cross-contamination
- Standards: plasmid controls for SARS-CoV-2 targets; synthetic controls for MNV and CrAssphage
- Assay performance: LoD and LoQ established prior
  - LoD: N1 1.7 gc/µL; E 3.8 gc/µL; MNV 3.1 gc/µL
  - LoQ: N1 11.8 gc/µL; E 25.1 gc/µL; MNV 32.1 gc/µL

## Data processing, quality assurance and documentation
- Data points used in analysis derive from q(RT-)PCR assays on extracted RNA (5 µL input)
- MNV recovery monitored; samples with recovery <1% re-tested with adjusted input, noting impact on sensitivity
- CrAssphage used as a proxy for human fecal loading to contextualize SARS-CoV-2 signals
- Documentation and supplementary materials provide detailed sequences, parameters and references for all assays
- Data stored with traceable processing steps and QA measures to support reuse and reproducibility

## Governance, provenance and limitations
- Data governance aligned with data stewardship goals: licensing, citation requirements, clear data description, and provenance (sampling, methods, and QA)
- Dataset includes metadata about sampling sites, calendar week alignment, and population context
- Potential limitations for reuse:
  - Temporal and spatial coverage limited to six sites and March–July 2020
  - Use of grab samples (except Wirral) may affect comparability; composite sampling only at one site
  - Heavy reliance on standardized laboratory methods; any changes in protocols over time are not described here
  - Data processing choices (e.g., handling of inhibition, replication strategy) influence downstream analyses

## References
- Includes extensive references for CDC and Corman et al. RT-PCR methods, CrAssphage benchmarking, and methodological precedents used in extraction and qPCR procedures