# Vegetation change at whim Moss (2002 -2016) Materials and methods

## Field site
- Location: Whim bog in the Scottish Borders (3°16'W, 55°46'N), a transition between lowland raised bog and blanket bog on 3–6 m of deep peat.
- Climate and hydrology: mean air and soil temperatures (10 cm) ~7.9°C and 7.6°C; annual rainfall ~1141 mm; water table ~10 cm below surface in hollows (drought in 2013 reduced to ~24 cm); hummocks ~20 cm higher than hollows.
- Peat and vegetation: very acidic peat (pH ~3.4). Vegetation classified as Calluna vulgaris Eriophorum vaginatum blanket mire (M19), with M15, M17, M18 also present. Dominated by Calluna vulgaris; mosaic of hummocks/hollows with various Sphagnum species and other common taxa.

## Experimental Design and Treatments
- Nitrogen manipulation: two systems for N inputs — dry deposition of NH3 and wet deposition of NH4+ and NO3− in solution.
- Timing: treatments began June 2002 and continued year-round except near freezing.
- Dry NH3 deposition: free-air release system delivering NH3 from liquid NH3 diluted with ambient air; release only when wind direction 180–215°, temperatures above freezing, wind speed >2.5 m s−1; created a downwind gradient measured at 0.1 m above vegetation along transects (8–60 m from source). Deposition calculated from concentration measurements; deposition at permanent quadrats interpolated by ordinary kriging assuming spatially homogeneous deposition velocity.
- Wet NH4+/NO3− deposition: replicated plots in a randomised block design using a sprinkler system. Rainwater collected on a 178 m2 surface; concentrated NH4Cl or NaNO3 solutions diluted in rainwater and distributed to plots via a central sprayer. Three treatment levels aimed for total N deposition of 1.6, 3.2, and 6.4 g N ha−1 y−1, plus a control (0.8 g N ha−1 y−1 ambient). PK added with NH4+ treatments at the two extremes in a P:N ratio of 1:14. NH4+ and NO3− treatments increased precipitation by ~10%.
- Experimental layout: four blocks with eleven treatment combinations each (1 control, 3 NH4+ without PK, 2 NH4+ with PK, 3 NO3− without PK, 2 NO3− with PK) for a total of 44 plots.
- Application cadence: sprayer activated roughly every 15 minutes whenever rainwater and weather conditions permitted (~120 applications per year), distributed over most of the year except mid-winter.
- Measurements associated with deposition: NH3 deposition measured via concentration-dependent deposition velocities and related methods; NH3 deposition modeled per Cape et al. (2008).

## Vegetation survey
- Sampling design: within each experimental plot, three permanent quadrats (40 × 40 cm) established pre-treatment (2002), each subdivided into 16 sub-quadrats (10 × 10 cm).
- Data collected: percent cover of all species in each sub-quadrat; mean cover per species per quadrat computed from sub-quadrat data; bespoke species list used for this study.
- Survey frequency: typically every two years.

## Nature and Units of recorded values
- Dataset: Whim_veg_2002-2006.csv (data described for 2002–2006).
- Key variables:
  - Year, PLOT, QUADRAT, ASSESSMENT.DATE
  - SPECIES.LIST.NUMBER, SPECIES.LIST.NAME
  - SUB.SQUARE.1–16: percent cover of each species in each sub-square
  - distance_m: distance from NH3 source (for transect plots)
  - Expt: form of N-deposition ("Wet" or "Dry")
  - PK: PK addition status ("PLUSPK" or "0"/"MINUSPK")
  - BLOCK, TREATMENT, FORM: treatment metadata
  - Fnh3, Fnh4, Fno3: fluxes of NH3, NH4+, and NO3− to plots (kg N ha−1 y−1)
  - DOSE: total N deposition to each plot (kg N ha−1 y−1)
- Soil and chemical data: soil water concentrations of detectable ions (NH4+-N, NO3−-N) via ion chromatography; detection limits provided (0.014 and 0.062 mg N L−1, respectively).

## Soil measurements
- Soil water sampling: monthly from 2006 onwards using dipwells in all plots.
- Analyses: ion chromatography following standard titration; data used to track soil N dynamics in response to deposition treatments.

## Analysis-ready data considerations
- Outputs include spatial deposition profiles (NH3), plot-level N deposition fluxes, and vegetation responses over time.
- The study design supports analysis of treatment effects (NH3 dry vs NH4+/NO3− wet), dose–response across multiple N levels, and PK interactions.
- Data are structured for integration with other environmental datasets (e.g., climate, soil chemistry), with explicit metadata on treatments, plots, and sampling dates.
- Methods reference established deposition estimation and interpolation approaches (e.g., Cape et al. 2008; Leith et al. 2004; Tang et al. 2001; ordinary kriging).

## References
- Cape, J., Jones, M., Leith, I., Sheppard, L., van Dijk, N., Sutton, M., & Fowler, D. (2008). Estimate of annual NH3 dry deposition to a fumigated ombrotrophic bog using concentration-dependent deposition velocities. Atmospheric Environment, 42, 6637-6646.
- Leeson, S.R., Levy, P.E., van Dijk, N., et al. (2017). Nitrous oxide emissions from a peatbog after 13 years of experimental nitrogen deposition. Biogeosciences, 14, 5753-5764.
- Leith, I.D., Sheppard, L.J., Fowler, D., et al. (2004). Quantifying Dry NH3 Deposition to an Ombrotrophic Bog from an Automated NH3 Field Release System. Water, Air, & Soil Pollution: Focus, 4, 207-218.
- Rodwell, J.S. (1998). British Plant Communities. Cambridge University Press.
- Sheppard, L.J., Crossley, A., Leith, I.D., et al. (2004). An Automated Wet Deposition System to Compare the Effects of Reduced and Oxidised N on Ombrotrophic Bog Species: Practical Considerations. Water, Air, & Soil Pollution: Focus, 4, 197-205.
- Tang, Y.S., Cape, J.N., & Sutton, M.A. (2001). Development and Types of Passive Samplers for Monitoring Atmospheric NO2 and NH3 Concentrations. The Scientific World Journal, 1, 513-529.