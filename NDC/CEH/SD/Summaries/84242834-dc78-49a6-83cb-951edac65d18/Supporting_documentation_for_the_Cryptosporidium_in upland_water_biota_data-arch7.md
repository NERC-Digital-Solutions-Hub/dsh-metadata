# Supporting documentation for the Cryptosporidium in Welsh upland water biota data (2012-2015)

## Overview
- A sample survey within the DURESS project testing Cryptosporidium in Welsh upland water biota.
- No field treatments or replication during sampling; laboratory controls present, but none during sampling.
- Targets: Cryptosporidium in gills, gut contents, and faeces from fish; also faeces from land/aquatic mammals (otters) and filter-feeding invertebrate larvae.
- Data are tied to the DURESS sampling frame, with some deviations for otters; results include molecular testing and sequencing.

## Sampling and Data Collection
- Fish sampling (2012):
  - 74 fish from 11 Welsh upland river sites; electrofished and culled; gut contents scraped and gills dissected for testing.
  - Species: salmon, brown trout, bullhead; paired gut and gill samples for a subset (16 salmon, 17 gills; 41 brown trout; 16 bullhead).
  - Samples stored frozen at -20°C.
- Fish faeces sampling (2013):
  - 117 fish from 8 sites; live fish anaesthetised and faecal samples collected during gut massage; samples stored frozen at -20°C.
- Otter faeces sampling (2013-2015):
  - 41 faecal samples collected in riparian zones; animal source identified where possible.
  - Additional otter samples (92) from otters found dead across England/Wales (2011-2015) tested due to otter host potential.
- Invertebrate larvae sampling (2012):
  - 290 larvae from genera including Baetis, Rhithrogena, Leuctra, Hydropsyche, Simulium, and others; collected from upland rivers around Llyn Brianne; preserved in absolute ethanol.
- Sample processing:
  - DNA extraction methods varied by sample type (tissue-based kits for gut/gill, stool kit for faeces, Gentra Puregene for larvae); invertebrate larvae ground in liquid nitrogen and processed.
  - Molecular testing via nested PCR targeting the ssu rRNA gene; gp60 genotyping for C. parvum and C. hominis on positive samples; real-time PCR for C. hominis on invertebrates with internal inhibition control.
  - Positive/negative controls included; testing accredited at the Cryptosporidium Reference Unit (CRU), now ISO15189; sequencing outsourced to Source Bioscience.

## Data Structure and Files
- Two main CSV data files:
  - Results_Invertebrate_Larvae.csv
    - Key fields: Site, Sample_group, Host, Sample_Type, CRU_Ref, n18S_result, GP60, Sequencing.
    - n18S_result indicates nested ssu rRNA PCR result; GP60 and Sequencing provide subtype/sequence outcomes.
    - Site references link to geographic context via a separate site description file.
  - Results_Biofilm_Fish_Mammals.csv
    - Key fields: Site, Sample_group, Host, Sample_Type, CRU_Ref, n18S_result, GP60, Sequencing.
    - Includes details on fish (e.g., trout, salmon) and mammal-associated samples; some hosts may be unidentified (marked with a question mark, e.g., Mink?).
- Site descriptions:
  - Site coordinates and descriptions are provided in a separate file: DURESS_CU_site_description.csv (references in the data files point to this).
- Data content scope:
  - Temporal span: 2012–2015 sampling activities; laboratory analysis and sequencing conducted within CRU framework.
  - Provides presence/absence and genotype information for Cryptosporidium across aquatic and riparian biota.

## Data Quality, Standards and Provenance
- Laboratory QA:
  - Nested PCR and sequencing performed with appropriate positive/negative controls.
  - gp60 genotyping performed on C. parvum and C. hominis positive samples.
  - Invertebrate samples screened for C. hominis with an internal control to detect inhibition.
  - Sequencing outsourced; analysis completed at CRU.
- Accreditation:
  - CRU methods accredited under Clinical Pathology Accreditation at the time; currently ISO15189.
- Data provenance:
  - Data linked to the CRU accession numbers (CRU_Ref) for traceability.
  - Some host identifications are uncertain and may be annotated with a question mark when ambiguous.

## GIS and Mapping Considerations for Use
- Geospatial linking:
  - Site-level data can be geolocated via DURESS_CU_site_description.csv; use Site identifiers to join coordinates for mapping.
  - Two CSV files allow separate mapping of aquatic invertebrate results and fish/mammal-associated results, which can be combined for comprehensive spatial analyses.
- Data interpretation:
  - n18S_result indicates presence/absence of Cryptosporidium DNA; GP60 and Sequencing provide species/subtype information where available.
  - Ch_Ct_value and IC_Ct_value (invertebrate real-time PCR) offer a quantitative sense of assay performance and inhibition risk in those samples.
- Robustness and caveats:
  - Some host sources may be unidentified; use caution when aggregating by host species.
  - Otter samples originate from a broader study and may not align perfectly with catchment-level sampling.
  - The data reflect field sampling linked to the DURESS project, with methodology and sample types described to enable appropriate spatial analyses and integration with other DURESS data.

## References
- Alves, M., Xiao, L., Sulaiman, I., Lal, A.A., Matos, O., Antunes, F., 2003. Subgenotype analysis of Cryptosporidium isolates from humans, cattle, and zoo ruminants in Portugal. J. Clin. Microbiol. 41, 2744-2747.
- Hadfield, S.J., Robinson, G., Elwin, K., Chalmers, R.M., 2011. Detection and differentiation of Cryptosporidium spp. in human clinical samples using real-time PCR. J. Clin. Microbiol. 49, 918-924.
- Jiang, J., Alderisio, K.A., Xiao, L., 2005. Distribution of Cryptosporidium genotypes in storm event water samples from three watersheds in New York. Appl. Environ. Microbiol. 71, 4446-4454.