# Substrate utilisation profiles and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland [NERC Soil Biodiversity Programme] - Supporting Information

## Background
- The NERC Soil Biodiversity Thematic Programme (established 1999) focused on understanding soil biota diversity and the functional roles of soil organisms within key ecological processes.
- A large field experiment at Sourhope (Macaulay Land Use Research Institute, now James Hutton Institute) in the Scottish Borders was used to study changes in aboveground productivity, species composition, and relative abundance, with 24 research projects addressing soil structure, soil processes (carbon and nitrogen cycles), and the roles of bacteria, nematodes, protozoa, fungi, micro- and macro-fauna.
- The study specifically investigated bacterial community ecology in Britain’s remaining native grasslands, using temporal and spatial sampling across soil depths and dates, employing BIOLOG-GN substrate utilisation analyses to infer carbon-source utilization patterns of a subset of the bacterial community.

## Site, sampling design, and methods
- Location: Sourhope experimental field site, Scottish Borders (grid NT854 site; NT854196 for the sampling point); temperate upland grassland (Soil Survey of Scotland series SH).
- Soils: shallow, organic-rich brown forest soil over glacial till derived from andesitic lava; unimproved grazed pasture dominated by Agrostis capillaris.
- Sampling schedule: three sampling dates over a week in July 1999 (8, 10, 14 July), plus later dates: 5 October 1999, 3 April 2000, and 30 August 2000.
- For each date: three replicate cores were collected with a 2.5 cm diameter corer to ~20 cm depth.
- Core processing: cores were separated into four 5-cm depth increments (0–5, 5–10, 10–15, 15–20 cm). The upper 0–5 cm layer contained litter and varying organic material; deeper increments spanned organic to mineral horizons.
- Sample preparation: for each replicate, 1 g soil was weighed for dry weight; the remainder was stored at −70°C prior to nucleic acid extraction and BIOLOG analyses.
- Subsampling scope: sampling outside the main plots was conducted for the BIOLOG analyses.

## BIOLOG-GN substrate utilisation analyses
- Preparation: 9 ml of a 0.5% soil suspension was washed and re-suspended in PBS; 100 μl aliquots dispensed into each well of BIOLOG GN plates.
- Incubation and measurement: plates incubated at 18°C until colour development ceased; presence/absence of colour change scored for each substrate well.
- Moisture assessment: soil moisture content determined as the mean of three replicate cores after oven drying at 105°C for 24 hours.

## Data structure and files
- Two CSV data files are provided:
  - P2136_Biolog_Utilisation.csv: Substrate utilisation profiles for BIOLOG GN plates, covering the 1999 and 2000 cores taken from untreated soil outside the main plots. Three cores per sample date, across four soil depths. Key fields include:
    - SAMPLING_DATE, MAX_DEPTH (cm), BIOLOG_CELL, SUBSTRATE, SUBSTRATE_TYPE, UTILISATION (1 if colour change observed, 0 otherwise)
  - P2136_Soil_Moisture.csv: Moisture content data for the same cores and dates, measured as mean of three replicate cores. Key fields include:
    - SAMPLING_DATE, MAX_DEPTH (cm), PERCENTAGE_MOISTURE
- Metadata and structure notes:
  - Sampling dates span 1999–2000; data are tied to specific depths (0–5, 5–10, 10–15, 15–20 cm) and to cores taken from outside main plots.
  - Each data row reflects a substrate test result (0/1) per BIOLOG cell, enabling analyses of depth- and time-associated shifts in substrate utilisation patterns.

## References and related information
- Griffiths, R. I., Whiteley, A. S., O'Donnell, A. G., & Bailey, M. J. (2003). Influence of depth and sampling time on bacterial community structure in an upland grassland soil. FEMS Microbiology Ecology, 43:35-43.
- Related materials:
  - Sourhope Field Data Handbook 2003 (Sourhope Field Data Handbook 2003) via EIDC catalogue record.
  - Usher, M.B., Sier, A.R., Hornung, M. & Millard, P. (2006). Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme. Applied Soil Ecology, 33(2), 101-113. doi:10.1016/j.apsoil.2006.03.006

## Usage notes and caveats
- Data are subject to quality assurance, but NERC does not guarantee accuracy or fitness for a particular purpose; no liability for loss or damage arising from use of these data.
- The dataset represents a specific site (Sourhope) and a subset of the bacterial community (as inferred by BIOLOG-GN) from untreated soil outside main plots; caution is advised when extrapolating to other plots, sites, or broader microbial communities.

## Relevance for analyses
- Enables investigation of temporal and depth-related patterns in bacterial substrate utilisation and soil moisture within upland grassland soils.
- Facilitates correlation analyses between substrate utilisation profiles and moisture content across depths and sampling dates.
- Can be combined with cited literature (e.g., depth/time effects on bacterial community structure) to interpret observed patterns and to inform predictive modeling of soil microbial functional potential under environmental change.