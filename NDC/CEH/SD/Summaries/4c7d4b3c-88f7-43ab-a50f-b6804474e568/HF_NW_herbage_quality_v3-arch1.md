# Details of data structure to 'HF_NW_herbage_quality.csv'

- Overview
  - A 13-column, 96-row dataset containing the herbage quality data from grassland fertiliser trials in 2016 at Henfaes Research Station (Bangor University) and North Wyke Research Station (Rothamsted Research).
  - Data provenance: Henfaes samples were pre-dried and sent to Sciantec Analytical (Stockbridge Technology Centre, UK); North Wyke samples were fresh and sent to Trouw Nutrition GB (UK).
  - Analytical method: Dry matter, ADF, ash, crude protein, metabolisable energy (ME), and NDF measured using near-infrared spectrometry.
  - Digestibility metric: D = ME / 0.16.
  - Units: Dry matter, ADF, ash, crude protein are in g kg^-1; ME is in MJ kg^-1; D is in percent. Note: NDF units are ambiguously listed in the text (stated as MJ kg^-1, which is unusual for NDF).

- Dataset structure (columns and meanings)
  - Date: Date of grass cut
  - Site: HF | NW indicating Henfaes or North Wyke
  - N_app: 1 | 2 | 3 indicating fertiliser applications; 1st and 2nd applications are 90 kg ha^-1, 3rd application is 60 kg ha^-1
  - Block: 1 | 2 | 3 | 4; blocking factor of the randomized block design
  - Plot: 1 - 16; plot harvested, with plot size 2 x 6 m
  - Treatment: AN | U | IU | C representing N fertiliser type
    - AN = ammonium nitrate
    - U = urea
    - IU = inhibited urea (agrotain)
    - C = 0N control
  - Dry_matter: g kg^-1
  - ADF: g kg^-1 (acid detergent fibre)
  - Ash: g kg^-1 (total mineral content)
  - Crude_Protein: g kg^-1
  - ME: MJ kg^-1 (metabolisable energy)
  - NDF: Neutral detergent fibre; description provided as part of the dataset (unit ambiguity noted in text)
  - D: D value; digestibility metric in percent

- Context and potential uses
  - The dataset supports analyses of how different N fertiliser types and application schemes affect herbage composition (DM, ADF, NDF, ash, crude protein) and energy/digestibility characteristics.
  - Suitable for correlational analyses and predictive modelling related to fertiliser management and forage quality across two sites.
  - Data processing notes: part of a supplementary document to broader CINAg experiments; careful attention to the NDF unit inconsistency when performing analyses.