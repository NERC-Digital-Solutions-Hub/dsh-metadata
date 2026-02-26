# SARS-CoV-2 qPCR and water chemistry data from wastewater at six sites in England and Wales between March and July 2020, with associated Covid-19 positive test and related-death data collated from other sources

## 1. Data access, licensing and citation
- Data are accessible via the DOI provided and released under the Open Government Licence (OGL).
- Proper citation required: Hillary et al. (2021), SARS-CoV-2 qPCR and water chemistry data from wastewater at six sites in England and Wales between March and July 2020, with associated Covid-19 positive test and related-death data collated from other sources. NERC Environmental Information Data Centre.

## 2. Data description
- Datasets record SARS-CoV-2 concentrations at six wastewater treatment sites in the UK from March–July 2020, alongside Covid-19 clinical data.
- Two CSV files are included:
  - data_table.csv: main dataset with wastewater and physico-chemical measurements per site and time.
  - cases.csv: clinical testing data for the same period, aligned to sites/dates where available.
- Key measurement types include genome copy concentrations (gc) per 100 mL for SARS-CoV-2 targets (N1, E), CrAssphage as a human fecal loading marker, and wastewater physico-chemical parameters (NO3, NH4, PO4, pH, EC), plus flow and population-related metrics.
- Associated clinical data include daily and rolling counts of Covid-19 tests and deaths, local authority population, and population-adjusted metrics.

## 3. 3.1 data_table.csv - main dataset
- Time and site identifiers:
  - Week, Date, Site_Name
- Water and wastewater flow:
  - Flow (m3 population equivalent-1)
- Viral and marker concentrations:
  - gc_100ml (SARS-CoV-2 N1), E_gene_100ml (SARS-CoV-2 E gene)
  - Crass_gc_100 (CrAssphage concentration), Crass_Recovery (CrAssphage recovery %)
- Physico-chemical parameters:
  - NO3 (mg/L), NH4 (mg/L), PO4 (mg/L), pH, EC (μS/cm)
- Epidemiological context:
  - Deaths, Deaths_100k
  - Daily_Cases_100k
  - Rolling_Sum_100k (7-day)
  - Local_Authority_Population
  - Population_Equivalent
  - Local_Authority_Covariates: cov_class, cov_detect, E_class (classification for N and E assays)
- Data quality and usage notes:
  - Measurements include replicates; extraction and PCR details support QA; some classifications indicate detection limits or non-detects for N gene and E gene.

## 3. 3.2 cases.csv - clinical testing data for the same period
- Site and time alignment:
  - Site_Name, Date
- Population context:
  - Local_Authority_Population
- Covid-19 clinical data:
  - Daily_Cases, Cumulative_Cases
  - Rolling_Sum (7-day)
  - Daily_Cases_100k, Rolling_Sum_100k
- Temporal framing:
  - Week (calendar week)

## 4. 4.1 Sampling sites and wastewater sampling
- Six WWTPs located in Wales and Northwest England (Gwynedd, Cardiff, Liverpool, Manchester, Wirral, Wrexham), serving ~3 million people.
- Sampling regime:
  - Untreated influent sampled weekly (Mar–Jul 2020); Wirral site used a 24-hour composite sample; others used grab samples.
  - Grab samples collected on weekdays 08:00–09:00; treated effluent sampled periodically.
- Sample handling:
  - Transport within same day or overnight on ice; stored at 4 °C; processed within 24 h; aliquots frozen at -80 °C for later analyses.

## 5. 4.2 Wastewater physicochemical analyses
- Analytes and methods:
  - Ammonium (colorimetric via Mulvaney 1996), Nitrate (colorimetric via Miranda et al. 2001), Molybdate-reactive phosphate (Murphy & Riley 1962)
  - Measurements conducted in 96-well format with a microplate reader; EC (conductivity) and pH measured with standard meters.
- Equipment:
  - PowerWave XS Microplate Spectrophotometer; Jenway conductivity meter; Hanna pH meter.

## 6. 4.2.1 Wastewater concentration and nucleic acid extraction
- Concentration workflow:
  - Inflow samples concentrated via Centriprep 50 kDa for influent; effluent concentrated by tangential flow ultrafiltration (100 kDa) plus Centriprep cleanup.
- Nucleic acid controls:
  - Murine Norovirus (MNV) spike-in as an extraction control; positive/negative extraction controls and cross-contamination checks.
- Extraction and storage:
  - Nucleic acids extracted with NucliSENS MiniMag system; elution buffers 50–100 μL; extracts stored at -80 °C; separate labs for extraction and qPCR setups to minimize contamination.

## 7. 4.3 q(RT-)PCR and qPCR assays
- Targets and platform:
  - SARS-CoV-2 N1 and E gene quantified using duplex/qtriplex q(RT-)PCR; MNV as extraction/inhibition control; CrAssphage quantified by singleplex qPCR.
- Assay setup:
  - 25 μL reactions with specified enzyme mix, primers, probes, and sample input (5 μL extracted RNA per run; inhibition retests with 2 μL if MNV recovery <1%).
- Quality and controls:
  - Duplicate runs for samples, standards, and controls; use of plasmid standards for SARS-CoV-2 targets; serial dilutions spanning relevant copy numbers.
- Performance metrics:
  - LoD (N1: 1.7 gc/μL; E: 3.8 gc/μL; MNV: 3.1 gc/μL), LoQ (N1: 11.8 gc/μL; E: 25.1 gc/μL; MNV: 32.1 gc/μL) established in prior validation.

## 8. 5. qPCR and q(RT)-PCR assay details
- Primers and probes:
  - SARS-CoV-2 N1 and E gene primer/probe sequences and references provided; multiplexing configurations described.
  - CrAssphage and MNV primer/probe sets described with respective cycling parameters.
- Cycling and reaction specifics:
  - Detailed thermal profiles and reagent compositions laid out for each target; modifications documented to accommodate QuantStudio system compatibility.

## 9. 6. References
- CDC (2020) and Corman et al. (2020) assay references.
- Farkas et al. (2019, 2021) CrAssphage and SARS-CoV-2 methodological papers.
- Kitajima et al. (2010), Miranda et al. (2001), Mulvaney (1996), Murphy & Riley (1962), Stachler et al. (2017, 2018) for markers and methods.