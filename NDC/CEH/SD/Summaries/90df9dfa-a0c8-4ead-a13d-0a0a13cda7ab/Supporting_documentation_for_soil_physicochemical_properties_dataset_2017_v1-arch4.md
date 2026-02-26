# Details of data structure to CINAg_digestate_experiment_2017_Soil_physicochemical_properties.csv

## Summary
- Supplement describing the data structure of the CINAg_digestate_experiment_2017_Soil_physicochemical_properties.csv dataset from a digestate trial conducted in 2017.
- The dataset comprises 35 columns and 180 rows and captures soil physicochemical properties measured after digestate treatments.

## Dataset scope and design
- Source: Digestate experiment 2017.
- Rows: 180 observations.
- Columns: 35 data columns (plus headers explaining each column).
- Structure supports comparison across treatment, depth, site, and sampling time.

## Experimental design and sampling context
- Sites: NW = North Wyke, HF = Henfaes Farm.
- Treatments: C = Control, D = digestate, ADNI = acidified digestate with nitrification inhibitor DMPP.
- Depths: 0-15 cm, 15-30 cm, 30-60 cm.
- Sampling times: T1 (beginning of the experiment after digestate application) and T2 (last harvest).
- Plot identifiers and a Year field indicate when samples were taken.

## Data columns and key variables (with units)
- Sample_ID: unique sample identifier (Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths).
- Year: year when samples were taken.
- Site: farm platform (NW or HF).
- Sampling_date: date of sampling (dd/mm/yyyy).
- Sampling_time: T1 or T2.
- Plot: plot numbers.
- Treatment: C, D, or ADNI.
- Depth_cm: sampling depth (cm) corresponding to the depth categories.
- NH4_mgN_per_kg_soil: soil extractable ammonium (mg N per kg dry soil).
- NO3_mgN_per_kg_soil: soil extractable nitrate (mg N per kg dry soil).
- DOC_mgC_per_kg_soil: dissolved organic carbon (mg C per kg dry soil).
- DON_mgN_per_kg_soil: organic nitrogen (mg N per kg dry soil).
- Aminoacids_mgN_per_kg_soil: nitrogen in amino acids (mg N per kg dry soil).
- Peptides_and_proteins_mgN_per_kg_soil: nitrogen in peptides and proteins (mg N per kg dry soil).
- MBC_mgC_per_kg_soil: microbial biomass carbon (mg C per kg dry soil).
- MBN_mgN_per_kg_soil: microbial biomass nitrogen (mg N per kg dry soil).
- Aggr_b20µm_perc: aggregates < 20 µm (%).
- Aggr_b250µm_perc: aggregates < 250 µm (%).
- Aggr_b2000µm_perc: aggregates < 2000 µm (%).
- Sand_perc, Silt_perc, Clay_perc: soil texture fractions (%).
- Soil_moisture_perc: soil moisture content (%).
- LOI_perc: loss-on-ignition as soil organic matter (%).
- pH_deionised_water: pH in deionised water (unitless).
- pH_CaCl2: pH in calcium chloride extract (unitless).
- EC_µS_per_cm: electrical conductivity (µS cm^-1).
- POXC_mgC_per_kg_soil: permanganate oxidisable carbon (available carbon) (mg C per kg dry soil).
- PO4.P_mgP_per_kg_soil: citric acid extractable phosphorus (plant available P) (mg P per kg dry soil).
- totC_perc: total soil carbon content (%).
- totN_perc: total soil nitrogen content (%).
- CN_ratio: soil carbon-to-nitrogen ratio (unitless).
- totP_mgP_per_kg: total soil phosphorus content (mg P per kg dry soil).
- Olsen_P_mgP_per_kg_soil: Olsen-phosphorus (mg P per kg dry soil).

## Data governance and usefulness
- Explicit column headers and units enhance discoverability, interoperability, and reuse.
- Data enables analysis of how digestate treatments influence a broad range of soil physicochemical properties across depths, sites, and timepoints.
- Serves as a structured data asset within the CINAg experimental framework, supporting replication, meta-analyses, and cross-study comparisons.