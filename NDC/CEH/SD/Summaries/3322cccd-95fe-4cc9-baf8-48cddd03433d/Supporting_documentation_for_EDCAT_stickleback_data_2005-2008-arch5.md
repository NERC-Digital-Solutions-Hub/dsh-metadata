# EDCAT stickleback data 2005-2008. Pottinger, T. G., Cook, A., Matthiessen, P. (2017)

## Overview
- Dataset from three-spined sticklebacks (Gasterosteus aculeatus L.) collected in the River Ray (southwest England) near Rodbourne WWTW before (2005–2007) and after (2008) remediation with granular activated carbon (GAC) tertiary treatment; plus samples from neighboring reference rivers (River Ock, Childrey Brook).
- Aim to assess physiological and biomarker responses; VTG and spiggin analyses reported elsewhere.
- Tissue processing included weighing, length measurement, heart/kidney dissection, tissue homogenization, and storage for subsequent assays.

## Sampling regime and collection methods
- Fish captured with a hand net; humane euthanasia with 2-phenoxyethanol (1:1000); individually labeled tubes; frozen in a liquid nitrogen dry shipper for transport to CEH Lancaster; stored at -80°C.
- On thawing, each fish weighed and measured; ventral incision for heart/kidney collection; remaining tissue homogenized in Tris-HCl buffer with glycerol/EDTA/DTT; homogenate stored at -20°C until analysis.
- All sampling and dissection steps performed prior to and during the 2005–2008 period; standard protocols applied with a noted deviation (see Analytical Methods).

## Analytical methods
- EROD (cytochrome P4501A activity) measured in liver homogenate using a microplate assay (96-well plates); excitation 530 nm, emission 590 nm; protein quantified via fluorescamine assay.
- Cortisol extracted from homogenate with ethyl acetate and quantified by radioimmunoassay (RIA); dextran-coated charcoal used in the assay buffer (noted as the only deviation from published methods).
- Glucose quantified in homogenate using a hexokinase-based microplate assay.
- Nucleic acids extracted with 1% sarcosyl; total nucleic acids measured with RiboGreen; after RNase treatment, RNA and DNA quantified by difference.

## Data structure
- Data provided as a CSV with columns:
  - Sampling_date; Description
  - River; Description
  - Site_within_river; Description
  - Fish_code; Description
  - Length_mm; Description
  - Weight_mg; Description
  - Sex; Description
  - KF; Description
  - EROD_pmol_min_mg_protein; Description
  - RNA_DNA_ratio; Description
  - Whole_body_cortisol_ng_g; Description
  - Whole_body_glucose_mg_g; Description

## Sampling locations
- River Ray sites:
  - Rodbourne WWTW (grid SU128865; 51.577 N, -1.817 W; 0.2 km from WWTW)
  - Elborough Bridge (SU121872; 51.584 N, -1.827 W; 1.8 km)
  - Tadpole Bridge (SU111896; 51.605 N, -1.841 W; 5.9 km)
  - Seven Bridges (SU119925; 51.631 N, -1.829 W; 9.5 km)
- River Ock sites:
  - Charney Basset (SU381944; 51.647 N, -1.451 W)
  - Garford (SU438962; 51.663 N, -1.368 W)
- Childrey Brook:
  - Venn Mill (SU434948; 51.650 N, -1.374 W)
  - Marcham Mill (SU448954; 51.656 N, -1.354 W)

## Data provenance, quality, and deviations
- Explicit note of methodological deviation: dextran-coated charcoal formulation in cortisol assay.
- Methods and references aligned with established publications (e.g., Hodson et al., 1996; Lorenzen & Kennedy, 1993; Pottinger & Carrick, 2001; Gorokhova & Kyle, 2002).
- Data generated across multiple years and sites, enabling comparisons of pre- vs post-remediation and reference conditions.

## Usage, governance, and publications
- This dataset has been used in multiple publications (e.g., Katsiadaki et al. 2012; Pottinger et al. 2011–2012), illustrating anti-androgen biomarkers and stress/chemical exposure indices.
- Metadata and variable definitions accompany the data structure; suitable for integration into data portals and cross-study analyses.
- Clear documentation of sampling regime, analytical methods, and site coordinates supports reproducibility and data discovery.

## References
- Gorokhova E, Kyle M. (2002). J Plankton Res.
- Hodson PV, et al. (1996). J Toxicol Environ Health.
- Lorenzen A, Kennedy SW. (1993). Anal Biochem.
- Pottinger TG, Carrick TR. (2001). Hormones and Behavior.
- Katsiadaki I, et al. (2012). Aquatic Toxicology.
- Pottinger TG, Cook A, et al. (2011–2012). Various journals (Environment International; Journal of Fish Biology).