# Vegetation change at whim Moss (2002 -2016) Materials and methods

## Overview and Field Site
- Study conducted at Whim bog in the Scottish Borders (3 ◦ 16' W, 55 ◦ 46' N) on 3–6 m deep peat.
- Climate: mean air soil temperatures ~7.9 °C (air) and 7.6 °C (10 cm depth); annual rainfall ~1141 mm (range 734–1486 mm).
- Water table typically ~10 cm below peat surface (dry year 2013: ~24 cm).
- Hummock–hollow topography with Calluna vulgaris–Eriophorum vaginatum blanket mire community; bog includes mosaics of Calluna vulgaris, Sphagnum spp. (capillifolium, fallax, papillosum), Erica tetralix, Hypnum jutlandicum, Pleurozium schreberi.
- Vegetation not burned or grazed, leading to variable age/stature.

## Experimental Design and Treatments
- Nitrogen deposition applied in two systems: dry NH3 deposition and wet NH4+/NO3− deposition.
- Timeline: treatments began June 2002 and continued year-round except near freezing.
- Dry deposition: free-air NH3 release system using a cylinder of NH3 diluted with ambient air; releases when wind from SW quadrant, above freezing, wind speed >2.5 m s−1; created a downwind deposition gradient. NH3 measured with passive samplers at multiple distances (0.1 m above vegetation) and vertical/horizontal gradients profiled.
- Wet deposition: replicated plots with a randomized block design using a rainwater sprayer system. Concentrated NH4Cl or NaNO3 solutions added to rainwater to achieve target deposition rates; phosphorus and potassium added at lowest and highest N treatments in PK ratio 1:14 to match amino-acid P:N.
- Treatment levels: three N deposition rates (1.6, 3.2, 6.4 g N ha−1 y−1) plus ambient control (0.8 g N ha−1 y−1); PK additions applied where specified.
- Experimental layout: four blocks; eleven treatment combinations per block (1 control, 3 NH4+ without PK, 2 NH4+ with PK, 3 NO3− without PK, 2 NO3− with PK) for a total of 44 plots.
- Application cadence: sprayer triggered automatically ~every 15 minutes when conditions permitted; ~120 applications y−1, distributed across the year with a winter pause.
- Data collected on soil water chemistry from dipwells in all plots monthly from 2006 onwards; ions measured by ion chromatography with detection limits of 0.014 mg L−1 for NH4+-N and 0.062 mg L−1 for NO3−-N.

## Vegetation Survey
- In each plot, three permanent quadrats (40 × 40 cm) established before treatments (2002) and subdivided into sixteen 10 × 10 cm sub-quadrats.
- Vegetation surveys conducted approximately every two years.
- For each survey, percent cover of all species recorded at the sub-quadrat level; sub-quadrat values averaged to yield mean cover per quadrat.
- Species list is bespoke to this study.

## Nature and Units of Recorded Values
- Dataset: Whim_veg_2002-2006.csv (vegetation data, 2002–2006).
- Key fields include:
  - year (Year of survey)
  - PLOT (plot identifier)
  - QUADRAT (quadrats per plot)
  - ASSESSMENT.DATE (date of vegetation survey)
  - SPECIES.LIST.NUMBER (species code)
  - SPECIES.LIST.NAME (Latin name)
  - SUB.SQUARE.1-16 (percent cover for each species in each sub-square)
  - distance_m (distance from NH3 source for transect plots)
  - Expt (form of N-deposition: "Wet" or "Dry")
  - PK (PK addition: "PLUSPK" or "0"/"MINUSPK")
  - BLOCK (experimental block ID)
  - TREATMENT (code for N-form, dose, PK)
  - FORM (substrate: "Ammonia", "Nitrate" or "Ammonium")
  - Fnh3, Fnh4, Fno3 (fluxes of NH3, NH4+, and NO3− to each plot; kg N ha−1 y−1)
  - DOSE (total N deposition to each plot, kg N ha−1 y−1)
- Data types and units: year (year), distance_m (meters), fluxes (kg N ha−1 y−1), DOSE (kg N ha−1 y−1); other fields primarily identifiers and descriptive text.
- The dataset includes a species list with coded numbers and Latin names, plus descriptive fields for deposition form, dose, PK status, and plot design.

## Data Quality, Provenance, and Governance Considerations
- Provenance anchored in well-documented field methods and references (e.g., Cape et al. 2008; Leith et al. 2004; Sheppard et al. 2004; Leeson et al. 2017; Tang et al. 2001; Rodwell 1998).
- Rich metadata supporting reuse: explicit descriptions of deposition methods (dry vs wet), treatment codes, PK additions, block structure, and measurement approaches.
- Important for data stewardship:
  - Standardization of units and coding (Expt, FORM, PK, TREATMENT) to enable interoperability with related datasets.
  - Bespoke species list requires careful documentation for cross-study comparisons.
  - Time-series aspects: vegetation surveys every two years; soil nutrient data monthly from 2006; deposition data ongoing beyond 2006 (documented through references).
  - Data gaps: dataset excerpt covers 2002–2006 vegetation data; broader 2002–2016 context exists in the study.
- Reuse considerations:
  - Potential for integrating with climate, hydrology, and nutrient deposition datasets due to linked methods and locations.
  - Attention to data versioning and linking to related deposition measurements (Fnh3, Fnh4, Fno3, DOSE) and transect distances for spatial analyses.
  - Documentation of detection limits and measurement methods essential for downstream analysis and comparability.

## Access, Usage, and Further Information
- Data are associated with a field experiment at Whim bog, with published methodological references and deposition treatments.
- For full context and reproducibility, users should consult the cited references detailing deposition methods, sampling, and data processing.

## References
- Cape, J., Jones, M., Leith, I., Sheppard, L., van Dijk, N., Sutton, M. & Fowler, D. (2008) Estimate of annual NH3 dry deposition to a fumigated ombrotrophic bog using concentration-dependent deposition velocities. Atmospheric Environment 42 6637-6646.
- Leeson, S.R., Levy, P .E., van Dijk, N., Drewer, J., Robinson, S., Jones, M.R., Kentisbeer, J., Washbourne, I., Sutton, M.A. & Sheppard, L.J. (2017) Nitrous oxide emissions from a peatbog after 13 years of experimental nitrogen deposition. Biogeosciences 14, 5753-5764.
- Leith, I.D., Sheppard, L.J., Fowler, D., Cape, J.N., Jones, M., Crossley, A., Hargreaves, K.J., Tang, Y.S., Theobald, M. & Sutton, M.R. (2004) Quantifying Dry NH3 Deposition to an Ombrotrophic Bog from an Automated NH3 Field Release System. Water, Air, & Soil Pollution: Focus 4, 207-218.
- Rodwell, J.S. (1998) British Plant Communities. Cambridge University Press
- Sheppard, L.J., Crossley, A., Leith, I.D., Hargreaves, K.J., Carfrae, J.A., van Dijk, N., Cape, J.N., Sleep, D., Fowler, D. & Raven, J.A. (2004) An Automated Wet Deposition System to Compare the Effects of Reduced and Oxidised N on Ombrotrophic Bog Species: Practical Considerations. Water, Air, & Soil Pollution: Focus 4, 197-205.
- Tang, Y.S., Cape, J.N. & Sutton, M.A. (2001) Development and Types of Passive Samplers for Monitoring Atmospheric NO2 and NH3 Concentrations. The Scientific World Journal 1, 513-529.