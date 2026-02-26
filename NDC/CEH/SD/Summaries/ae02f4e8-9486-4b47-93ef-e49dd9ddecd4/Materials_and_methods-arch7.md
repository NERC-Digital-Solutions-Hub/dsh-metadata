# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

- Purpose: Compile radionuclide and stable element concentrations across a range of biota and soils, together with estimated dose rates, to support wildlife radiation exposure assessments in a defined reference site within the Chernobyl Exclusion Zone.
- DOI: https://doi.org/10.5285/ae02f4e8-9486-4b47-93ef-e49dd9ddecd4

## Sampling site and design

- Location: Sampling site (0.4 km2) on the western edge of the “Red Forest,” about 5 km WSW of Chernobyl Unit 4; not within the heavily exposed area that caused pine die-off in 1986.
- Inner sampling area: Approximately 0.06 km2 within former kitchen gardens (dacha) with fruit trees; surrounded by deciduous woodland and marsh.
- Soil and habitat context: Predominant soil is soddy-podzolic sandy loam; surrounding habitats include deciduous woodland and marsh.
- Sampling period: May–June 2014 (about 1 month), with additional species analyzed for 90Sr and 137Cs beyond ICRP RAP definitions.

## Sampling by organism groups (and general processing)

- Wild grass (Agrostis gigantea): Grid-based sampling, ~1 cm above ground, air-dried, homogenised.
- Pine trees (Pinus sylvestris): Trunk wood from three mature trees (>28 years, pre-1986), plus needles, cones, branches; dried and homogenised.
- Earthworms (Lumbricidae, likely Eisenia hortensis): Collected from six inner-area sites; rinsed, gut-contents evacuated, sub-samples prepared for radiochemical and stable-element analyses.
- Bees and other insects: Pan traps with water; bees (Xylocopa spp., Bombus spp.) analyzed for stable elements; other insects retained for potential analyses.
- Small mammals: Sherman live traps over five nights; 166 animals of seven species captured; mass, sex, age recorded; most released; nine Apodemus flavicollis euthanised for radiochemical analyses; selective tissues dissected and stored for stable-element analyses.
- Amphibians: Hand-caught and live-monitored; moor frog (Rana arvalis) most common; R. arvalis mostly released after mass measurement; nine individuals ashed for radiochemical analyses; others dissected for comparable tissues.
- Frogs’ spawn: Freeze-dried for stable-element analyses.
- Soils: 15 soil cores per sampled pine tree; additional cores near animal traps and in vicinity; soils dried and homogenised for analyses.

## Live-monitoring and radiological dose assessment

- Live-monitoring: 118 animals monitored in vivo for whole-body 137Cs and 90Sr concentrations using a compact, shielded counting setup with HPGe and NaI detectors; counting times 150–1200 s; typical counting uncertainties <3% (90Sr) and <7% (137Cs).
- Dose assessment: Tier 3 (probabilistic ERICA Tool, version 1.2.1) used to estimate external exposure rates for all organisms.
  - Inputs: Mean/SD of measured activity concentrations for soil (external exposure) and for organisms/plants (fresh mass-based data); trunk wood activity used for P. sylvestris geometry; averaged activity concentrations for bees and Microtus spp.; Pu and Am isotopes treated as 50/50 contributions when both detected.
  - Species geometries: Custom geometries created where necessary (small mammals, amphibians) using measured masses and literature dimensions; default ERICA geometries used for bees, earthworms, and plants.
  - Occupancy factors: Derived from literature/supplementary info; amphibians assumed to spend 100% of time on land; radiation weightings: alpha=10, low-energy beta=3, others beta/gamma=1.
- Analytical focus: Total dose rates and isotope contributions (notably 239,240Pu split assumed equally in the assessment).

## Laboratory analyses and quality control

- Radioanalyses:
  - Gamma spectrometry (Cs-137): HPGe detector; calibration with 152Eu source; detection limits ~0.18 Bq per sample; typical uncertainties 10–15%.
  - Sr-90: Beta spectrometry without radiochemical pretreatment; calibration against mixed standards; uncertainties ~20%.
  - Actinides (Pu, Am): Chemical separation (anion exchange, TRU resin) after acid digestion; alpha spectrometry; typical counting uncertainties <20%.
- Stable and other element analyses:
  - Digestion protocols varied by matrix (soil, plant, animal tissue) with controlled reference materials (NIST SRMs) to assess accuracy.
  - ICP-MS (iCAP-Q) used for multi-element determinations across 29 elements (with internal standards, collision-cell modes, and multiple calibration standards).
  - Iodine: Stable iodine concentrations measured via alkaline extraction (TMAH) or acidic digestion, depending on sample availability.
- Quality control outcomes:
  - Recovery ranges for CRMs generally within 100 ± 15% (most elements); acceptable recoveries within stated CRM ranges for soils and plant materials.
  - Analytical detection limits and uncertainties reported according to extraction form and sample type.

## Data structure and GIS-ready outputs

- Data types included:
  - Radionuclide concentrations: 137Cs, 90Sr, Pu isotopes, Am isotopes in soils, plants, invertebrates, and vertebrates.
  - Stable element concentrations: comprehensive elemental suite across matrices (soil, plants, animals).
  - Dose rates: external exposure estimates per species and per environmental medium (soil, wood, etc.) via ERICA Tool.
- Spatial relevance:
  - Site-level context with inner sampling area and surrounding habitats; soil cores around pines provide micro-scale spatial context.
  - Potential GIS products: layer maps of radionuclide concentrations by species/matrix, soil contamination distributions, and modelled wildlife dose-rate surfaces.
- Data provenance and access:
  - Core dataset linked to the NERC Environmental Information Data Centre; references and methodological details provided for reproducibility and interoperability.

## Data quality, limitations, and considerations for GIS use

- Data quality:
  - Rigorous radiochemical methods with corroborating QA/QC via CRMs; clearly stated detection limits and uncertainties.
  - Multiple matrices and species provide a multi-layered view of contamination and transfer.
- Limitations:
  - Temporal snapshot: May–June 2014 sampling; results represent conditions during that period with some extrapolation for dose modelling.
  - Assumptions in ERICA-based dose assessment (e.g., Pu/Am isotope contributions, occupancy factors, and geometry approximations) influence final dose-rate estimates.
- GIS considerations:
  - When mapping, account for heterogeneity across matrices (soil, biota, air) and align to standard coordinate reference systems; integrate with supplementary spatial metadata (site boundaries, inner-area vs. outer-area distinctions).

## References and related data context

- References include key ERICA tool versions, ICRP reference datasets, and methodological precedents for wildlife radiological assessment.
- The dataset is part of ongoing field/radiological studies in the Chernobyl Exclusion Zone and associated with broader compilations of radionuclide and stable-element data for wildlife exposure modelling.