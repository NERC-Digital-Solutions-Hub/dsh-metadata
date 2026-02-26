# UrineComposition.csv

## Overview
- Dataset of Welsh Mountain ewe urine chemical composition with associated metadata from the Uplands-N2O project.
- Samples filtered on ice, stored at -20°C; various biochemical measurements performed using standard analytical methods.
- Includes detailed headers describing collection context (season, site, sheep, date, time) and a broad panel of urine constituents.

## Data Content and Structure
- Headers capture: Season, Site, Sheep, Date, Time, Vol, TOC, TN, pH, EC, Urea, Nitrate, Ammonium, AA, Allantoin, Creatinine, Uric, Hippuric, Benzoic, Ca, Na, K.
- Units (as listed in headers): Vol (ml), TOC (g C l-1), TN (g N l-1), pH (dimensionless), EC (mS cm-1), Urea (g urea-N l-1), Nitrate (mg NO3--N l-1), Ammonium (mg NH4+-N l-1), AA (mg amino acid-N l-1), Allantoin (g compound l-1), Creatinine (mg compound l-1), Uric (mg compound l-1), Hippuric (g compound l-1), Benzoic (mg compound l-1), Ca (mg Ca l-1), Na (mg Na l-1), K (g K l-1).
- Context: Season refers to spring, summer, or autumn; Site indicates semi-improved or improved pasture; Date in dd/mm/yyyy; Time approximate.

## Data Collection & Measurement Methods
- Sample processing: urine filtered on ice through Whatman No.1 (11 μm) before freezing.
- pH and electrical conductivity measured with standard electrodes.
- TOC and TN measured with Multi N/C 2100S analyzer.
- Urea measured enzymatically (Orsenneau et al., 1992).
- Nitrate and Ammonium measured colorimetrically (Miranda et al., 2001; Mulvaney, 1996).
- Free amino acids determined fluorometrically (Jones et al., 2002).
- Allantoin, Creatinine, Uric acid, Hippuric acid, and Benzoic acid measured by HPLC with a C18 column; detection at 218 nm; specific mobile phases and flow rate described.
- K+, Na+, Ca2+ measured by flame photometer (Sherwood Model 410).
- Sample preparation for some analyses involved dilution in mobile phase A as needed.

## Variables and Units
- Key variables include: TOC, TN, pH, EC, Urea, Nitrate, Ammonium, AA, Allantoin, Creatinine, Uric, Hippuric, Benzoic, Ca, Na, K.
- Temporal and spatial metadata: Season, Site, Sheep, Date, Time, Vol.
- Data are suitable for per-sample cross-tabulation across chemical constituents and urine volume.

## Data Quality, Provenance, and Licensing
- Provenance: Authors and grant details provided; data intended to be fully cited if reused.
- References for methods: Jones et al. 2002; Miranda et al. 2001; Mulvaney 1996; Orsenneau et al. 1992.
- Note on reuse: ensure full citation of data in any downstream work.

## How Data Supports Analysis and Product Creation (Data Support perspective)
- Enables self-serve exploration of urine chemistry across seasons and pasture types, with per-sample granularity.
- Supports creation of dashboards or pivot-table based dashboards to compare constituents by season/site/sheep.
- Data cleaning opportunities: unify date formats, handle missing or partial data, harmonize units if combining with other datasets.
- Data products to consider: data dictionary, validation checks, sample-level QC reports, and reusable scripts for calculating summary statistics (means, medians, variance) and correlations between urinary constituents.
- Potential integrative analyses: linking urine chemistry to pasture type, environmental variables, or animal health metrics; exploring diurnal/temporal patterns via Date/Time.

## Practical Considerations for Reuse and Integration
- Maintain citation and acknowledgment per the dataset’s guidelines.
- Be prepared to align formats with other data sources (e.g., unit harmonization).
- Consider data access controls if integrating with other organisational datasets; document data lineage and transformations.