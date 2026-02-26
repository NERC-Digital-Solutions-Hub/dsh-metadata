# SARS-CoV-2 qPCR and water chemistry data from wastewater at six sites in England and Wales between March and July 2020, with associated Covid-19 positive test and related-death data collated from other sources

## Overview
- A dataset of SARS-CoV-2 concentrations in wastewater from six UK wastewater treatment plants (WWTPs) across Wales and Northwest England, collected March–July 2020.
- Linked to Covid-19 clinical data (positive tests and related deaths) aggregated at local authority level from external sources.
- Aimed at enabling correlations, trend analyses, and predictive insights relating wastewater signals to clinical outcomes.

## Data Access and Licensing
- Access via doi: 10.5285/ce40e62a-21ae-45b9-ba5b-031639a504f7
- Available under the Open Government Licence (OGL).
- Must cite: Hillary et al. (2021), NERC Environmental Information Data Centre dataset.

## Data Description
- Two CSV files are provided:
  - data_table.csv (main dataset)
    - Key variables: Week, Date, Site_Name, Flow, gc_100ml (SARS-CoV-2 N1), E_gene_100ml (E gene), Crass_gc_100, Crass_Recovery, NO3, NH4, PO4, pH, EC, Deaths, Deaths_100k, Daily_Cases_100k, Population_Equivalent, Rolling_Sum_100k, Local_Authority_Population, cov_class, cov_detect, E_class.
    - Additional rolling and population-adjusted metrics (e.g., Rolling_Sum_100k, Deaths_100k).
  - cases.csv (clinical testing data for the same period)
    - Key variables: Site_Name, Date, Local_Authority_Population, Daily_Cases, Cumulative_Cases, Rolling_Sum, Daily_Cases_100k, Rolling_Sum_100k, Week.
- Data cover six WWTPs serving Gwynedd, Cardiff, Liverpool, Manchester, Wirral, and Wrexham, with a combined population ~3 million.

## Sampling Sites and Protocols
- Six WWTPs in Wales and Northwest England; population served approx. 3 million.
- Sampling period: weekly influent samples from March–July 2020; Wirral site also collected as a 24-hour composite.
- Sample timing: grab samples on weekdays 08:00–09:00; treated effluent collected periodically.
- Sample handling: transported same day or next day on ice; stored at 4 °C and processed within 24 h; aliquots frozen at -80 °C for further analyses.

## Wastewater Physicochemical Analyses
- Measured: ammonium (colorimetric), nitrate (colorimetric), molybdate-reactive phosphate, electrical conductivity (EC), and pH.
- Analyses performed in 96-well plate format using microplate spectrophotometry.

## Nucleic Acid Concentration and Extraction
- Concentration: duplicate 50–100 mL samples; centrifuged; supernatant concentrated to 500 µL; for effluent, initial concentration by tangential flow ultrafiltration followed by Centriprep concentration.
- Internal process controls: murine norovirus (MNV) spike-in (~4×10^5 gc) for extraction efficiency; cross-contamination checks with negative/positive controls.
- Extraction: NucliSENS MiniMag Nucleic Acid Purification System; elution buffer volume 50–100 µL; extracts stored at -80 °C.
- Laboratory workflow: extractions and qPCR setups conducted in separate biosafety cabinets to minimize contamination.

## qPCR and qRT-PCR Assays
- SARS-CoV-2 targets: N1 (duplex qRT-PCR) and E gene (triplex with N1 if applicable); CrAssphage used as a human fecal marker; MNV as extraction control.
- Assay setup: 25 µL reactions with specified reagents and 2–5 µL RNA extract; duplicates performed; 5 µL extracts used for each run.
- Standards and quantification: serial dilutions with plasmid or oligo DNA standards; Ct-based quantification against standards.
- Performance metrics: limit of detection (LoD) and limit of quantification (LoQ) established prior to analysis.
  - LoD: N1 = 1.7 gc/µL, E = 3.8 gc/µL, MNV = 3.1 gc/µL.
  - LoQ: N1 = 11.8 gc/µL, E = 25.1 gc/µL, MNV = 32.1 gc/µL.
- CrAssphage assay: used as a normalization indicator for human fecal load; detailed primer/probe sequences and qPCR conditions provided.

## Assay Details and Primers
- SARS-CoV-2 (N1) primers and probe with specified sequences and qPCR parameters.
- SARS-CoV-2 (E) primers and probe with specified sequences and qPCR parameters.
- MNV primers and probe with qPCR parameters.
- CrAssphage Q56 primers and probe with qPCR parameters.
- All assays included appropriate negative controls; data used in analysis derived from extracts tested in duplicate.

## Data Processing and Quality Assurance
- Data points derived from multiple laboratory procedures, with internal controls (MNV and CrAssphage) to monitor extraction efficiency and human fecal loading.
- Duplicate measurements and standardized protocols help ensure comparability across sites and time.
- Data points and methods are described with reference to supplementary materials and established protocols.

## Potential Analyses and Applications
- Correlate wastewater SARS-CoV-2 concentrations (N1 and E gene) with local clinical case data (daily and 7-day rolling sums, per 100k population).
- Normalize SARS-CoV-2 signals using CrAssphage loading to account for human fecal content variability.
- Assess temporal relationships and potential lead-lag effects between wastewater signals and reported cases/deaths.
- Comparative site analyses to explore differences in viral load relative to population served and flow.
- Integration with physicochemical parameters to explore associations with wastewater quality and viral persistence.

## Licensing, Citation and References
- Data licensed under Open Government Licence; cite the dataset according to the provided reference.
- References included in the document provide assay protocols and validation (CDC N1, E gene assays; Corman et al.; CrAssphage studies; MNV controls).

## Summary of Purpose and Value
- This dataset enables researchers to investigate the relationship between SARS-CoV-2 RNA in community wastewater and clinical COVID-19 indicators across multiple UK sites, offering a basis for early warning, trend analysis, and modelling of the likely impact of public health actions. It includes robust QA/QC measures, standardised sampling and analysis procedures, and linked clinical data to support integrated epidemiological analyses.