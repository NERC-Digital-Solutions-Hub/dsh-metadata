# Soil bacterial cell counts and moisture content from a water stress experiment [NERC Soil Biodiversity Programme] -Supporting Information

- Purpose and scope
  - Describes a soil biodiversity study focusing on how soil bacterial activity and diversity respond to drying and rewetting in intact soil monoliths from Sourhope, Scotland.
  - Part of the NERC Soil Biodiversity Thematic Programme (established 1999) aiming to understand soil biota diversity and functional roles in ecological processes.
  - Data support analyses of microbial activity under moisture perturbations and provide a basis for studying microbial responses to water stress.

- Study site and context
  - Field site: Sourhope, Scottish Borders (Macaulay/JH Institute), grid reference NT8545019630.
  - Soil type: organic-rich brown forest soil, pH 4.5–5.0.
  - Experimental setup: nine microcosms created from intact grassland monoliths (~15 cm deep; 45 cm diameter pots) planted with standardized vegetation, maintained in open air at Oxford.
  - Experimental duration: July–October 2001, with 11 sampling events (S1–S11).

- Experimental design and treatments
  - Treatments (three regimens, three replicates each):
    - A: continual wetting
    - B: drying
    - C: drying and rewetting
  - Water management:
    - Initial 3 samples with natural rainfall plus regular watering.
    - Rainfall exclusion introduced on 14 August via UV-transparent covers.
    - Drying began after 20 August; continual wetting maintained with ~2 L every 2 days.
    - Rewetting occurred on 18 September after ~1 month of drying.
  - Sampling: regular collection of soil cores (4 cores per pot, ~1 cm diameter, to ~7 cm depth) with homogeneous mixing; samples used for moisture and microbial analyses.

- What was measured
  - Soil moisture content: determined by oven-drying at 105°C for 24 hours.
  - Bacterial cell counts:
    - Culturable cells: soil dispersed in PBS, serial dilutions plated on TSBA (full-strength and 1/10-strength) and PSA media with cycloheximide; incubated 10 days at 18°C; colony counts used to estimate culturability.
    - Total cells: flow cytometry after density-based extraction and staining with SYBR Green II; cells counted by FACS Calibur.
  - Media and methods aimed to compare culture-dependent and culture-independent estimates of bacterial abundance.

- Data files and structure (GIS-relevant tabular data)
  - P2136_Culturable_cells.csv
    - MICROCOSM_ID, TREATMENT, SAMPLING_DATE, MEDIA_USED, CELL_COUNT
    - MEDIA_USED: psa, tsba, and 1/10 tsba
    - CELL_COUNT: cells per gram dry weight soil; numeric
  - P2136_Microcosm_Soil_Moisture.csv
    - MICROCOSM_ID, TREATMENT, SAMPLING_DATE, MOISTURE_CONTENT
    - MOISTURE_CONTENT: percentage water content; numeric
  - Data notes
    - Both files derived from the same nine microcosms with three replicates per treatment.
    - Sampling spanned 23 July 2001 to 26 October 2001 (moisture measured by oven-dry method).

- GIS-ready considerations
  - Spatial context: site location and grid reference enable integration with soil maps and land-use layers; potential to map microcosm locations within Sourhope field layout.
  - Temporal context: multi-date sampling allows creation of time-series layers showing moisture dynamics and microbial abundance over the drying–rewetting cycle.
  - Data integration: links between moisture content and microbial counts can be joined by MICROCOSM_ID and sampling date for spatial-temporal analyses.
  - Potential outputs: map-based visualizations of microbial responses to moisture regimes; choropleth maps of moisture content by microcosm over time; correlation surfaces between moisture and culturability/total cell counts.

- Data quality, limitations, and rights
  - Quality assurance applied, but data providers (NERC) do not warrant accuracy or fitness for any particular use; no liability for misuse or errors.
  - Data originate from controlled microcosm experiments and may require careful interpretation when extrapolating to field conditions.
  - Resolution and scope: data are aggregates for 9 microcosms under 3 treatments; spatial heterogeneity beyond microcosm level is not captured.
  - Related literature and resources provided for context and methodology (e.g., Whiteley et al. 2003; Griffiths et al. 2003) and a field data handbook.

- References and related materials
  - Whiteley, A. S., Griffiths, R. I., Bailey, M. J. 2003. Analysis of microbial functional diversity via flow cytometry and CTC+ sorting.
  - Griffiths, R. I., Whiteley, A. S., O'Donnell, A. G., Bailey, M. J. 2003. Physiological and community responses of soil bacteria to water stress.
  - Sourhope Field Data Handbook 2003 and related UK soil biodiversity literature for broader context.

- Access and liability
  - Data are provided subject to QA but without warranty of accuracy; no liability for outcomes arising from use of the data.