# Topsoil carbon concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

- Purpose and scope
  - Provides modelled estimates of topsoil carbon concentration (0–15 cm) across Great Britain for 2007 at 1 km² resolution.
  - Based on Countryside Survey data and intended as a key indicator of soil health and ecosystem services.

- Data and modeling approach
  - Data origin: soil carbon measurements from 2,446 locations, with samples nested within 1 km² survey squares.
  - Statistical method: Generalized Additive Mixed Model (GAMM) using a Tweedie distribution (variance power = 1.99) to handle non-Gaussian data.
  - Model structure: includes random effects for 1 km² square nesting; non-linear smoothing for climate and atmospheric deposition variables; two-dimensional tensor product smooths for spatial location (latitude/longitude) to capture broad spatial variation.
  - Predictors included (from Table 1): climate (5-year mean summer temperature and precipitation; 5-year mean spring temperature; 5-year mean winter temperature), atmospheric deposition (3-year mean SO4, NH4, NO3), broad habitat/land cover, soil/parent material factors (including soil group and parent material), and spatial terms.
  - Data sources for predictors: Met Office (climate), CBED (deposition), Land Cover Map 2007, British Geological Survey soil/parent material models, among others.
  - Data product: NetCDF file named CS_topsoil_carbon_gam.nc; modeled mean soil carbon concentration (Soil_OrgC_Conc) with associated variability (VAR).

- Key data product details
  - Variable: Soil_OrgC_Conc – mean topsoil carbon concentration in g kg⁻¹ for 2007.
  - Uncertainty: VAR – standard error associated with Soil_OrgC_Conc divided by the predicted mean (dimensionless ratio).
  - Spatial attributes: x (Easting) and y (Northing) in OSGB 1936 / British National Grid (meters); coordinate reference system defined as transverse Mercator.
  - Resolution and scope: 1 km² spatial resolution across Great Britain; temporal focus on 2003–2007 climate/ deposition ranges for predictors, but the target is 2007 modeled carbon concentration.

- Sampling, calibration, analytical methods and QA
  - Sampling protocol: soil cores 15 cm long, 5 cm diameter; LOI (loss on ignition) measured on 10 g subsamples after sieving to 2 mm.
  - Carbon estimation: soil carbon concentration estimated by multiplying LOI by a factor of 0.55, derived from regression against total soil carbon measurements; method aligned with CEH UKAS accredited SOP SOP3102.
  - Quality control and governance: following Defra/NERC Joint Codes of Practice; QA details documented in accompanying technical reports and peer-reviewed sources.

- Data attributes and documentation
  - Dataset attributes and metadata described for CS_topsoil_carbon_gam.nc, including units (g kg⁻¹ for Soil_OrgC_Conc, dimensionless ratio for VAR), and coordinate information.
  - Full methodological documentation provided in Reynolds et al. (2013) and Emmett et al. (2008, 2010), with the GAMM approach detailed in Thomas et al. (2020).

- Considerations for data use and governance (Data Leaders perspective)
  - Data governance: a well-documented, model-derived national soil carbon product with explicit metadata, units, and coordinate system; still anchored to 2007 data and 0–15 cm depth.
  - Data quality and reproducibility: transparent modeling approach (GAMM, random effects, smoothing terms) and cited methodological references; software used (R mgcv package) noted.
  - Data discoverability and interoperability: single NetCDF data product with clear variable naming and attributes; accessible via provided references; compatible with environmental and soil health analyses.
  - Gaps and limitations: temporal limitation to 2007 as the target year; spatial resolution fixed at 1 km²; potential limitations in extrapolation beyond the 2446 calibration locations; depth restricted to 0–15 cm.
  - Opportunities for data strategy: can support retrospective soil carbon assessments, integration with other Countryside Survey datasets, and (where available) guiding updates or validation studies with newer surveys or higher-resolution data.

- Supporting references
  - Thomas, A. et al. (2020). Patterns and trends of topsoil carbon in the UK: Complex interactions of land use change, climate and pollution. Science of the Total Environment.
  - Reynolds, B.A. et al. (2013). Countryside Survey: National 'Soil Change' 1978–2007 for Topsoils in Great Britain—Acidity, Carbon, and Total Nitrogen Status. Vadose Zone Journal.
  - Emmett, B.A. et al. (2008, 2010). Countryside Survey technical reports on soils manual and soils from 2007.
  - Henrys, P.A. et al. (2012). Model estimates of topsoil carbon — Countryside Survey.
  - Morton, R.D. et al. (2014). Land Cover Map 2007.
  - Dore, A.J. et al. (2015). Atmospheric Environment — model inter-comparison for deposition estimates.