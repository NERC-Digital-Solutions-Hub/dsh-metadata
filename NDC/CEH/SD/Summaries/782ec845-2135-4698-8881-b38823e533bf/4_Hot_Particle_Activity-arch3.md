# Metadata for 4_Hot_Particle_Activity.csv

## Purpose and relevance for monitoring frameworks
- Provides a comprehensive metadata schema for hot particle measurements related to Chernobyl fallout.
- Supports environmental health monitoring, policy scrutiny, and informing future decisions by enabling isotope-specific risk assessment, spatial analysis, and temporal comparison.
- Documents particle-level characteristics, isotopic composition, radiological activities with uncertainties, and provenance to support transparent reporting and governance.

## Key data elements (data dictionary highlights)
- Identification and sampling context
  - Code / Identifier: unique IDs and labels for each particle or record.
  - STRUCT, TYPE: descriptors of particle structure and hot particle type (e.g., fuel vs. condensed; Warsaw or Mikolajki sampling sites noted).
  - DIST_km: distance from a central point (ChNPP); Angle_degree: polar angle around ChNPP (0° North, clockwise).
  - DIST_km notes: includes approximation for some samples (e.g., ~500 km for Polish samples).

- Particle characteristics
  - MAXSIZE_um / MINSIZE_um: particle size range (micrometers).
  - VIEW / COLOR / FORM: visual and physical descriptors of the particle.
  - GROUP A/B/C: Poland-specific isotope composition groups, with Group A dominated by Ru-103/Ru-106, Group B richer in multiple isotopes, and Group C similar to B with more Ru.

- Measurement dates and timing
  - DATE_Gamma: date of gamma measurement (with a two-format enumeration).
  - DATE_Alpha / DATE_Beta: dates of alpha and beta measurements.
  - TOTAL_alpha_activity_Bq: total alpha activity (Bq).

- Radiological activities and uncertainties (Bq with uncertainties)
  - Activity_of_95Zr_Bq, Activity_of_95Nb_Bq, Activity_of_106Ru_Bq, Activity_of_125Sb_Bq, Activity_of_134Cs_Bq, Activity_of_137Cs_Bq, Activity_of_144Ce_Bq, Activity_of_154Eu_Bq, Activity_of_155Eu_Bq, Activity_of_54Mn_Bq, Activity_of_60Co_Bq, Activity_of_241Am_Bq, Activity_of_90Sr_Bq.
  - STD_of_<isotope>_Bq: standard deviations (uncertainties) for each isotope activity.
  - DATE_Gamma / DATE_Alpha: contextual timing for gamma and alpha measurements.

- Burnup and interpretation
  - Burnup_MW_d_kg-1: burnup value derived from activity ratios of low-mobile refractory radionuclides and Cs isotopes; categorized into 17 groups.
  - References linked to burnup derivation and particle classification (e.g., Kuriny et al., Kashparov et al.).

- Additional descriptive fields
  - VIEW notes: reference for classification visual representations (Dabrowska et al., 1989).
  - STRUCT notes: location-based notes (e.g., Mikolajki, Warsawa, Lomza, Bialystok, Suwalki) and HP type (fuel vs. condensed).
  - DATE_Alpha / DATE_Gamma / DATE_Beta formats indicate data recording conventions (e.g., dd-mmm-yyyy).

- References
  - Core scholarly sources underpinning particle characterization, aging, and classification (e.g., Begichev et al. 1990; Kashparov et al. 1996, 1997; Kuriny et al. 1993; Zhurba et al. 2009).

## Data quality, access, and governance considerations
- Metadata completeness and clarity: includes many fields with explicit explanations, though some units are unspecified (units often listed as blank).
- Data provenance and transparency: dataset draws on established studies and provides a bibliographic trail for interpretation (numerous Russian and international sources).
- Data sharing and openness: metadata acknowledges the potential barrier to publicly sharing underlying datasets; emphasizes the importance of data governance, storage, and up-to-date metadata.
- Transformations and interoperability: several fields note that data may require transformation or normalization (e.g., units for activities and uncertainties, coordinate systems).

## Practical implications for monitoring and policy evaluation
- Enables targeted radiological risk assessment by isotope, with quantified activities and uncertainties at the particle level.
- Supports spatial analysis of hot particle distribution around the ChNPP, including distance and angular positioning.
- Facilitates policy evaluation on remediation, monitoring intensity, and public communication by providing clear particle classifications and temporal measurement contexts.
- Provides a structured basis for reporting dashboards, charts, and policy-oriented summaries that align with environmental health monitoring aims.

## References and data lineage
- Key foundational works informing particle classification, burnup interpretation, and historical context:
  - Begichev et al., 1990
  - Kashparov et al., 1996, 1997
  - Kuriny et al., 1993
  - Zhurba et al., 2009
- These references underpin the dataset’s burnup interpretation, isotopic groupings, and qualitative classifications of hot particles.