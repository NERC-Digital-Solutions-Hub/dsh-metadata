# Metadata for 4_Hot_Particle_Activity.csv

## What this dataset is
- A data dictionary describing per-particle measurements of Chernobyl hot particles, including location, morphology, and detailed radioisotope activities.
- Covers sampling around ChNPP (ChNPP center; “Shelter” or sarcophagus for some samples) and distant Polish samples (approx. 500 km noted).
- Includes classifications for Polish particles (Group A, B, C) based on isotope contents and similarities to defined groups.
- Intended to support analysis, visualization, and self-serve exploration of hot-particle data, with emphasis on data quality, transformation, and product creation.

## Key data fields (highlights)
- Code: unique dataset serial number.
- Identifier: UIAR label (chemical analysis number).
- Angle_degree: angular position in a clockwise polar system (0°/360° = North) around ChNPP.
- DIST_km: distance from the ChNPP center in kilometers (note about approximate 500 km for Polish samples).
- MAXSIZE_um / MINSIZE_um: particle size range in micrometers.
- Burnup_MW_d_kg-1: burnup category derived from activity ratios, classified into 17 groups; references provided.
- VIEW: visual representation category; linked notes provide details.
- COLOR / FORM / STRUCT: particle appearance, inclusions, and structural notes (with location notes for sampling sites).
- DATE_Gamma / DATE_Alpha / DATE_Beta: dates of gamma/alpha/beta measurements (formats noted).
- Activity_of_[isotope]_Bq: total activity of various isotopes (e.g., 95Zr, 95Nb, 106Ru, 125Sb, 134Cs, 137Cs, 144Ce, 154Eu, 155Eu, 54Mn, 60Co, 241Am, 90Sr).
- STD_of_[isotope]_Bq: standard deviation of the respective activity measurements at 95% confidence.
- Total_alpha_activity_Bq: total alpha activity.
- DATE_Beta and RELATED: beta measurement date fields.
- Representative notes: some fields include explanatory notes (e.g., grouping definitions, sample locations).

## Geography, sampling context, and grouping
- Sampling context includes ChNPP center references, with some particles sampled from the Shelter/sarcophagus area.
- Distances and angles place particles in a polar coordinate framework around the plant.
- Polish samples are grouped into three categories (Group A, B, C) based on their isotope contents; Group characteristics emphasize Ru isotopes and cesium/ruthenium signatures, with Group B showing broader isotope presence compared to Group A and C.

## Measurements and data types
- Per-particle radioisotope activities are provided in bequerels (Bq) with associated standard deviations (STD) at 95% confidence.
- Multiple isotopes are covered, including both fission products and activation products (e.g., Ru, Cs, Sb, Ce, Eu, Mn, Co, Am, Sr).
- Dates accompany measurement data to enable temporal analyses.
- Several fields may have non-standard naming in the raw text (e.g., spaces in some column names), reflecting the metadata nature of the dataset.

## Data quality and caveats
- Described as a dataset with patchy data and a variety of formats, likely requiring harmonization across sources.
- Some notes indicate approximations or location-specific details (e.g., 500 km Polish samples; sampling points like Warsaw/Mikolajki).
- Complex isotopic data require careful interpretation and potential simplification for broader communication.
- Information may reside in multiple publications; provenance is provided via references.

## Potential data products and use cases (Data Support perspective)
- Self-serve dashboards filtering by angle, distance, size, or burnup group to compare particle signatures.
- Visualization of per-particle isotopic profiles, including size and morphological attributes.
- Cross-particle analyses by location (Poland vs local sites) and by burnup group.
- Aggregations by isotope activities, with uncertainty (STD) propagation for summary insights.
- Data cleaning pipelines to harmonize field names, units, and date formats for integration with other systems.
- Prototyping and sharing early outputs to gather feedback and drive better data creation practices.

## References
- Begichev S. N. et al.: Preprint IAE-5268/3: Reactor Fuel of Unit 4 of the Chernobyl NPP (brief handbook). 1990.
- Kashparov V. A. et al.: Formation of Hot Particles During the Chernobyl NPP Accident. Nuclear Technology, 1996.
- Kashparov V. A. et al.: Assessment of maximal temperature and annealing duration of Chernobyl fuel particles during the accident. Radiokhimiya, 1997.
- Kuriny V. D. et al.: Particle associated Chernobyl fall-out in local and intermediate zones. Annals of Nuclear Energy, 1993.
- Zhurba M. et al.: The 'hot particles' data base. Radioactive Particles in the Environment, 2009.