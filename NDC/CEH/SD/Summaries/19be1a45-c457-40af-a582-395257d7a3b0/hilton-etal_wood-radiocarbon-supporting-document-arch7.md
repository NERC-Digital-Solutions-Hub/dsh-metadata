# Radiocarbon measurements on river wood deposits, Mackenzie River, Canada

- Purpose and scope
  - Study to constrain the source and age of wood carried by the Mackenzie River delta draining into the Arctic Ocean.
  - Field campaign in August 2019 visiting 42 wood deposits across multiple depositional environments (lake shores, coastal embayments, inland floodplains, riverbanks).
  - Up to three large wood samples collected per site to capture environmental diversity; systematic sampling to achieve robust spatial coverage (longitudes ~132°W to ~135°W, latitudes ~67°N to ~69°N).

- Geospatial data and dataset structure
  - Each sample recorded with precise latitude and longitude (decimal degrees).
  - Dataset includes: sample identifier, measurement batch, regional site descriptor, wood dimensions (diameter in cm, length in m), carbon content of cellulose, stable carbon isotope (δ13C, VPDB), percent modern radiocarbon activity (pMC) and 1σ uncertainty, Fraction Modern (F14C) and 1σ, radiocarbon age (years BP) and 1σ, and calibrated ages (upper and lower bounds, 2σ, 95% confidence) with AD year ranges; calibration method depends on F14C value (IntCal20 for F14C<1; Bomb21NH1 for F14C>1).
  - Additional descriptors: sample type (large log, small pieces, buried, river cut bank), vegetation cover, depositional landform, and depositional environment.
  - Data packaged as a CSV with 77 rows (A–Y), enabling map-based representations and spatial analyses.

- Methods and laboratory workflow
  - Collection methodology: outermost wood (2–5 cm) from large wood pieces using an axe due to weathering; field sites chosen to maximize environmental representativeness.
  - Sample processing to cellulose: sequential digestion and purification steps (HCl, KOH, de-humification with acidified sodium chlorite) to isolate cellulose; final preparation involved filtration and freeze-drying.
  - Radiocarbon measurement: combustion to CO2, conversion to graphite, AMS dating at SUERC; results reported as conventional radiocarbon years BP and Fraction Modern (F14C), each with 1σ uncertainties.
  - Isotopic correction: δ13C values corrected to VPDB = -25‰ using dual inlet MS measurements.

- Calibration and age modelling
  - Calibration performed with OxCal v4.4.
  - For F14C < 1: IntCal20 calibration curve used.
  - For F14C > 1: Bomb-curve (Bomb21NH1) used.
  - Outcome: upper and lower calibrated wood ages reported in AD with 95% confidence (2σ), reflecting the range of plausible calendar ages.

- Quality control and data interpretation
  - Quality control conducted at NEIF Radiocarbon Facility with blanks and analytical standards; reported uncertainties are 1σ.
  - All measured cellulose radiocarbon ages and F14C values were modelled in OxCal to produce calendar-year age ranges.
  - The dataset and methods are discussed in detail in Sendrowski et al., 2023 (Wood-Based Carbon Storage in the Mackenzie River Delta: The World's Largest Mapped Riverine Wood Deposit, Geophysical Research Letters).

- Practical considerations for GIS applications
  - The dataset provides georeferenced samples with associated age ranges and environmental metadata, enabling spatial visualization of wood age distribution, depositional environments, and river-transport dynamics.
  - Can be integrated with other spatial layers to analyze wood-derived carbon storage and transport pathways within the Mackenzie River delta region.

- Related publication
  - Data and methodology underpinning the study published in Geophysical Research Letters, 2023 (Sendrowski et al.).