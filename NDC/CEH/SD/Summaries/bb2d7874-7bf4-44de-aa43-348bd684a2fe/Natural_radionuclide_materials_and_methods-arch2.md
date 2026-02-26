# Materials and methods for soil, water and sediment data extracted from: Background exposure rates of terrestrial wildlife in England and Wales; Methods for biota data extracted from: Assessment of naturally occurring radionuclides around England and Wales: Application of the G-BASE dataset to estimate doses to non-human species

- Objective and scope
  - Categorise available data on naturally occurring radionuclides in England and Wales according to ICRP reference animals and plants (RAPs) to support radiation dose assessments to non-human species.
  - Review data availability across the UK (not just England and Wales) and assemble data from grey literature, peer-reviewed papers, and internal databases.

- ICRP reference animals and plants (RAPs)
  - Proposed terrestrial RAPs: Reference Deer; Reference Rat; Reference Duck; Reference Frog; Reference Bee; Reference Earthworm; Reference Pine Tree; Reference Wild Grass.
  - Data attribution:
    - Duck → any wild bird
    - Frog → any amphibian
    - Bee → any flying insect
    - Earthworm → any earthworm
    - Pine Tree → any tree
    - Wild Grass → any wild grass or herb (or data labeled as grass)
    - For mammals: data for “any wild mammalian species” plus separate data for Deer and Rat
  - An objective is to evaluate naturally occurring radionuclides in England and Wales against these RAPs and discuss data availability specific to RAP definitions.

- Data sources and data availability
  - Sources include:
    - Grey literature, refereed journals, and in-house databases.
    - RIFE (Radioactivity in Food and the Environment) reports (UK-wide, 1995–2004 sampling; include some wild biota, notably for grass and game species).
    - CEH datasets from studies on radiocaesium deposition (e.g., post-Chernobyl and Sellafield-related work) with gamma data for 40K.
  - Data were allocated to RAPs as described above, noting many data were not originally collected specifically for the defined RAPs.

- Targeted sampling and data collection (2.3)
  - Due to limited data for several RAPs, a targeted sampling campaign was conducted for Duck, Bee, Earthworm, Pine Tree, and Frog.
  - Existing CEH archives used where possible, supplemented by new sampling.
  - Collected samples included:
    - Insects (mixed flying insects, mainly moths) from eight Environmental Change Network sites (England & Wales).
    - Lodgepole pine trunk samples.
    - Grey heron liver samples from Predatory Birds Monitoring Scheme.
    - Earthworms, rabbits, a toad, and mallards.
  - Wales had limited data, so some Welsh samples were sourced from England or mixed from Wales when possible.

- Sample preparation and analyses (2.3.1)
  - Pine trunks: washed, ashed at 450°C.
  - Earthworms: evacuated gut contents, freeze-dried, homogenised.
  - Insects: dried and homogenised.
  - Mallards: plucked; GI tract removed; liver analysed separately; carcasses ashed.
  - Rabbits: skinned; claws and GI tract removed; washed and ashed.
  - Heron and mallard liver: freeze-dried and homogenised.
  - Analytical techniques:
    - Gamma spectrometry on hyperpure germanium detectors to determine gamma-emitting radionuclide concentrations; typically 2-day counts.
    - Calibration with certified reference solutions across relevant energies (59.5–1836 keV).
    - For toads: fresh analysis followed by ashing and total U/Th determination due to small sample size.
    - Total U and Th measured via digestion (HNO3 with HF) and ICP-MS; secular equilibrium assumed between certain U/Th decay products where justified.
  - Sample processing included thorough grinding/powdering and standardized weighing into small vessels for secular equilibrium incubation (about 25 days).

- Derivation of soil and biota activity concentrations (2.4 and related)
  - Soil activity concentrations:
    - Based on G-BASE (Geochemical Baseline Survey of the Environment) data for K, U, and Th in soils.
    - Sampling density: ~one sample per 2 km² (with broader coverage for some elements via supplementary projects).
    - Data normalization:
      - Adjustments for different analytical techniques and sample types (surface vs. subsurface soils; etc.) described in prior work.
      - Linear quantile transformation used to normalize overlapping datasets (e.g., BGS and Wolfson Atlas for K in stream sediments).
      - Extrapolation to cover all of England and Wales using relationships between soils, sediments, and bedrock/superficial geology.
    - Grid-based aggregation:
      - Compute geometric means per 1 km grid square for each element and per parent material (bedrock and superficial geology).
      - Derive 25 km² area-weighted GM values by aggregating the nearest five data points for each parent material within the square.
    - For waters, only geometric mean concentrations were derived where data were available; extrapolation based on geology was not considered sufficiently robust for waters, resulting in more limited coverage than solids.
  - Biota data:
    - Concentrations in terrestrial biota were converted from total element concentrations to radionuclide activity concentrations using specific activity constants:
      - 40K: 31.6 Bq g⁻¹
      - 232Th series: 4.07 Bq mg⁻¹Th
      - 238U series: 12.21 Bq mg⁻¹U
    - Assumptions:
      - 232Th series in approximate equilibrium.
      - 238U series (234U and daughters) in secular equilibrium with 238U; ongoing equilibrium may vary due to differing environmental behaviours.
  - Data outputs intended to support whole-body dose estimates for RAPs and to enable broader environmental radiological assessments.

- Practical output and relevance for monitoring
  - Provides a systematically categorized, QA-verified dataset of naturally occurring radionuclide activity concentrations aligned with RAPs for non-human species.
  - Delineates data gaps and notes the targeted sampling undertaken to fill RAP-specific data needs.
  - Delivers spatially explicit soil and biota activity concentration surfaces (where data permit) to support exposure assessment and monitoring programs.
  - Emphasizes standardized methods, documentation of data provenance, and preparation of datasets suitable for uploading to appropriate data portals and for broader reuse.

- References and data provenance
  - Key source documents and projects cited include:
    - Johnson and Breward on G-BASE; Johnson et al. on G-BASE sampling procedures.
    - Beresford et al. on Assessment of naturally occurring radionuclides around England and Wales.
    - Wolfson Atlas and related geochemical resources for data normalization and extrapolation.
  - Specific datasets and reports (e.g., RIFE series) acknowledged as foundational data sources for RAP attribution and historical radionuclide concentrations.