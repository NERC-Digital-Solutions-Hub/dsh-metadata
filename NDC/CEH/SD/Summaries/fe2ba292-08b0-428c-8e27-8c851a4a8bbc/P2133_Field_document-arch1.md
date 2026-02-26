# Measurements of microarthropod community structure and diversity from an upland grassland experimental site [NERC Soil Biodiversity Programme]

## Context and Aim
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focusing on soil biota diversity and their functional roles in key ecological processes.
- Large field experiment at Sourhope, Scotland, investigating how microarthropod communities relate to soil fertility and ecosystem function (e.g., C/N cycles, productivity).
- 24 projects funded across soil structure, processes, and microfauna/flora; emphasis on linking diversity to soil function and management effects.

## Site description, design, and treatments
- Location: Sourhope field site in the Cheviot Hills, south-east Scotland; semi-improved upland grassland, ~350 m altitude.
- Climate: annual rainfall ~1117 mm; air temperature ~3.8–12.2°C.
- Plant community: Agrostis capillaris, Festuca ovina, Poa pratensis, Anthoxanthum odoratum.
- Soil: humic brown (Sourhope series).
- Experimental design: five replicate blocks downslope; each block contains six plots (12 x 20 m) with randomised treatments.
- Treatments: nitrogen (N) as ammonium nitrate, lime as calcium carbonate, both N and lime, and control (no fertilisation).
- Application schedule: N May 1999, Sept 1999, Apr 2000, May 2000; Lime May 1999 and Apr 2000.
- Management: site mowed five times per growing season (June–Sept) to ~6 cm, cuttings removed.
- Sampling: soil cores collected at four dates (Nov 1999, Feb 2000, May 2000, Aug 2000). In August, paired cores additionally used for soil condition and other measurements. Sampling across all five blocks for each treatment; total cores: 80 (Nov/Feb/May) and 120 (Aug).

## Data collected and measurements
- Microarthropods: abundance and species identification (mites and Collembola); extraction via Berlese-Tullgren funnels (96 h); storage in preservative; counts and identifications used to compute diversity and biomass.
- Diversity and functional indices: Shannon-Wiener diversity (H), evenness (J), cumulative species richness (R); separate indices for mites + Collembola and for each group; functional diversity indices for predatory vs non-predatory mites.
- Biomass estimates: microarthropod community biomass estimated using published conversion factors.
- Above-ground productivity: annual above-ground biomass (ANPP) estimated from dry weight in quadrats (0.25 m^2 x 4 per plot across five mowing events).
- Soil and root analyses (August data emphasized for paired samples): 
  - Root biomass: dry weight per core.
  - Total soil and root C and N contents (Dumas method, Carlo Erba NA 1500).
  - Soil moisture (percent), pH (wet method with deionised water), organic matter (loss on ignition).
  - Microbial biomass C: fumigation-extraction (CHCl3) with 0.5 M K2SO4 extractant; biomass C calculated using kEC = 0.35.
  - Microbial activity: soil basal respiration via CO2 measurement after 24 h incubation at 25°C.
- Soil and microarthropod datasets include depth details: cores typically 8 cm diameter to 10 cm depth; August paired cores extended to include additional measurements; depth metrics included in datasets.

## Datasets and data structure
- Dataset 1040: Plant species data (P2133_FIELD_BOTANICAL_PERCENT.csv)
  - Variables include sampling unit identifiers (SUID), block, main plot, sub-plot, cell coordinates (CELL_X, CELL_Y), treatment, sampling date, surface area, species name, and percent cover per core/plot.
- Dataset 1041: Field microarthropod population density data (P2133_FIELD_MPOD_NUMBERS.csv)
  - Variables include SUID, sampling date, block, main plot, sub-plot, cell, treatment, sample type (core), surface area, mite and Collembola counts (per m^2 to 5 cm depth), depth metrics.
- Dataset 1042: Field microarthropod species abundance data (P2133_FIELD_MPOD_SPECIES.csv)
  - Variables include SUID, sampling date, block, main plot, sub-plot, cell, treatment, sample type, surface area, species name, and counts per core.
- Dataset 1043: Field soils data (P2133_FIELD_SOILS.csv)
  - Variables include SUID, sampling date, block, main plot, sub-plot, cell, treatment, sample type, surface area, and soil/roots measurements: biomass C, respiration, pH, LOI, root biomass, soil C/N, root C/N, soil moisture, depthFrom/to, etc.
- Data notes: datasets include detailed field/method metadata, measurement units, and sampling design descriptors to support reproducibility and cross-dataset integration.

## Processing, analysis, and quality assurance
- Data processing: standardized logging of samples via unique sampling unit identifiers (SUID) and consistent depth and plot coordinates to enable multi-dataset linkage.
- Analytical methods: 
  - Microarthropods identified to species where possible; dominating taxa used for diversity metrics.
  - Biomass and chemical analyses performed using established methods (Dumas for C/N; CHCl3 fumigation for microbial biomass C; soil respiration via headspace CO2).
- Quality control: numeric range checks, data formatting checks, and logical integrity checks performed; NERC provides QA assurances but does not warrant data accuracy or fitness for a specific use; data users bear responsibility for suitability and interpretation.

## References and supporting materials
- Foundational sources on methods and interpretation (e.g., Hopkin for Collembola taxonomy; Krantz for acarology; Luxton and Petersen for biomass and calorimetry of microarthropods; Jenkinson & Powlson for microbial biomass methods; Begon et al. for ecological indices).
- Related data handbooks and regional soil biodiversity studies cited for methodological context and data usage guidelines.

## How to use the data
- Suitable for analyses linking microarthropod community structure/diversity with soil fertility manipulations (N and lime), soil microbial activity, and above-ground productivity.
- Enables multivariate analyses of diversity, biomass, and functional roles in relation to soil chemistry and physical properties.
- Enables cross-dataset integration across plant community data (1040), microarthropod densities and species data (1041–1042), and soil/root chemistry data (1043) to examine below-ground–above-ground linkages.
- Important caveats: dataset quality is subject to QA procedures; no guaranteed accuracy or fitness for a particular use; consider potential scale limitations and context when extrapolating beyond experimental plots.