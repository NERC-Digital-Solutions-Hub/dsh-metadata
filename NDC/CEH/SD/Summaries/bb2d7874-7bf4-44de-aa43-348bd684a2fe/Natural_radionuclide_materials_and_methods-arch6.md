# Materials and methods for soil, water and sediment data extracted from: Background exposure rates of terrestrial wildlife in England and Wales N.A. Beresford, C.L. Barnett, D.G. Jones, M.D. Wood, J.D. Appleton, N. Breward, D. Copplestone. Journal of Environmental Radioactivity 99 (2008) 1430-1439. doi: 10.1016/j.jenvrad.2008.03.003.

## Overview
- Describes the identification, compilation, and processing of data on naturally occurring radionuclides in terrestrial biota and environmental media (soil, water, sediment) in England and Wales.
- Aims to categorize available data according to ICRP reference animals and plants (RAPs) to support radiation-dose assessments for non-human species.
- Draws on multiple data sources, including grey literature, peer-reviewed papers, in-house databases, and national monitoring programs.

## ICRP reference animals and plants (RAPs)
- ICRP RAPs used for terrestrial ecosystems: Reference Deer; Reference Rat; Reference Duck; Reference Frog; Reference Bee; Reference Earthworm; Reference Pine Tree; Reference Wild Grass.
- Objective: classify available naturally occurring radionuclide data for England and Wales by RAPs to support dose assessments.
- Data attribution approach:
  - Reference Duck: any wild bird
  - Reference Frog: any amphibian
  - Reference Bee: any flying insect
  - Reference Earthworm: any earthworm
  - Reference Pine Tree: any tree
  - Reference Wild Grass: any wild grass/herb or grass data
  - For mammalian RAPs: data for “any wild mammalian species,” plus separate data for Deer and Rat
- Although RAP-based categorisation was primary, effects on availability of RAP-specific data are discussed.

## Review of available data
- Scope: mostly England and Wales, with UK-wide data collated due to limited England/Wales-specific data.
- Data sources include:
  - Grey literature
  - Refereed journal papers
  - In-house databases
- Key data sources:
  - RIFE (Radioactivity in Food and the Environment) reports: annual UK-wide radionuclide concentrations in biota (predominantly non-edible components; grass is included as edible in some contexts).
  - CEH (Centre for Ecology & Hydrology): analyses of biota for anthropogenic radionuclides and gamma-active samples, including data from Chernobyl fallout and Sellafield discharges.
- Data attribution and RAP alignment:
  - Where species did not perfectly map to RAPs, data were allocated to the closest RAP category (e.g., any bird to Reference Duck, any amphibian to Reference Frog, etc.).
  - Two mammalian RAPs: Deer and Rat, plus data for “any wild mammalian species.”
- Data availability outcomes informed the targeted sampling plan (see below).

## Sampling and analyses
- Rationale: limited existing data for several RAPs; implemented targeted sampling to fill gaps for Duck, Bee, Earthworm, Pine Tree, and Frog.
- Sampling strategy:
  - Leveraged CEH sample archives where possible; plus targeted new sampling.
  - Sample types collected:
    - Mixed flying insect sample (1–2 g dry weight) from eight Environmental Change Network sites in England and Wales
    - Five lodgepole pine (Pinus contorta) trunk samples
    - Twenty grey heron (Ardea cinerea) liver samples from Predatory Birds Monitoring Scheme archive
    - Six earthworm samples
    - Four rabbits (Oryctolagus cuniculus)
    - One toad (Bufo spp.)
    - Five mallards (Anas platyrhynchos)
- Wales data limitations:
  - All rabbit samples, four mallards, three pine samples, and two earthworms sourced from Wales due to paucity of Welsh data for other RAPs.
- Targeted sampling locations and context were chosen to enhance representation of RAPs across the England/Wales region.

## Sample preparation and analyses
- Preparation steps (varied by specimen type):
  - Lodgepole pine: washed and ashed at 450°C
  - Earthworms: two days on moist tissue to evacuate guts; freeze-dried and homogenised
  - Insects: supplied dry, homogenised prior to analyses
  - Mallards: plucked; gastrointestinal tract removed; liver separated for analysis
  - Rabbits: skinned; claws and GI tract removed; carcasses washed and ashed
  - Heron and mallard liver: freeze-dried before homogenisation
  - Toad: analysed fresh, then ashed for total U and Th
- Analytical techniques:
  - Gamma spectrometry using hyperpure germanium detectors for gamma-emitting radionuclides; 2-day count times; spectra analysed with Canberra Genie-VMS.
  - Detector calibration using certified reference solutions; density considerations for dried ground vegetation.
  - Total U and Th determinations:
    - 0.5 g sample digested with 10 ml concentrated HNO3 and two drops HF in a microwave digestor; dried and brought up to 10 ml of 10% HNO3
    - ICP-MS used for U and Th concentrations; typical detection limits ~10^-2 mg/kg (Th) and 10^-3 mg/kg (U)
  - For U and Th total activity concentrations: specific gamma-emission activities used to estimate radionuclide concentrations (with secular equilibrium assumptions for U-series in biological samples; equilibrium within decay chains treated cautiously for others due to different environmental/biological behaviours)
- Whole-body considerations:
  - For some tissues, results were combined or manipulated to provide whole-body or trunk/organ estimates as applicable.

## Derivation of soil activity concentrations
- Data source: G-BASE geochemical baseline survey of the environment (UK-wide): regular measurements of K, U, and Th in soils, stream sediments, and waters.
- Sampling density and normalization:
  - Soils: approx. one sample per 2 km²
  - Stream sediments and waters: approx. one sample per 1.5–2 km²
  - Large, complex dataset: almost complete coverage for K in stream sediments combined from BGS data and Wolfson Atlas; U and Th data normalized between datasets and survey methods
  - Normalization methods described in detail in Beresford et al. (2007)
  - Spatial data handling:
    - Bedrock and superficial geology codes mapped to samples
    - Geometric means computed for each 1 km grid square using the nearest five samples for each parent material
    - Extrapolated surfaces computed for 25 km² grid squares (5 × 5 km) via area-weighted geometric means
    - For waters, only geometric means were derived where data allowed; extrapolation across geology was not as robust for waters
- Activity concentration derivations:
  - For solids (soils, sediments): 40K, 232Th, and 238U activity concentrations derived from total element concentrations using standard specific activities (K = 31.6 Bq g⁻¹ per kg of K; Th = 4.07 Bq mg⁻¹; U = 12.21 Bq mg⁻¹)
  - Assumptions:
    - 232Th series radionuclides assumed to be in approximate secular equilibrium
    - 238U series assumed equilibrium among 238U and 234U and intervening decay products; subsequent equilibrium may not hold for other members due to differing chemical/biological behaviours
- Output and data structure:
  - Terrestrial biota data tabulated with fields including species name, Latin name, RAP assignment, use in whole-body calculations, grid coordinates (Easting/Northing), sampling location and date, and reported activity concentrations (with related metadata and notes on detection limits)

## Data handling and references
- The study integrates data from published literature, national monitoring programs, and targeted new measurements to populate RAP-based datasets.
- Metadata and references are provided to support traceability for all incorporated data, including specific references for biota and environmental media data sources.