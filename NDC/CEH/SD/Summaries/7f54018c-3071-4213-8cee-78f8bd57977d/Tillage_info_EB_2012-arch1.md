# Nitrous oxide fluxes from an intensively managed grazed grassland in Scotland

- Objective and setting
  - Investigates fluxes of N2O from two adjacent fields in Easter Bush, Scotland, before and after tillage on May 1, 2012.
  - Climate: temperate maritime; ~921 mm annual rainfall; ~9°C average temperature (2001–2011).
  - Soils: clay loam, imperfectly drained Macmerry soil; pH ~5.1; drainage system present but not functioning well.
  - Land use: intensive livestock production for ≥20 years; grazing by sheep; average stocking density ~0.7 LSU ha-1; fertilisation ~200 kg N ha-1 y-1 (NH4NO3 or NPK).

- Field setup and management
  - Two fields (~5.4 ha each): South field tilled in May 2012; North field remained un-tilled.
  - Management events (highlights):
    - Feb 16, 2012: North field grazed; South field to be tilled.
    - Apr 27, 2012: Glyphosate (1.5 L ha-1) applied to South field.
    - May 1, 2012: South field ploughed to 30 cm; May 3: harrowed, rolled, sown with ryegrass.
    - May 28, 2012: North field receives 70 kg-N ha-1 (Nitram).
    - Aug 9, 2012: Both fields receive 70 kg-N ha-1; South field also fertilised post-til lage.
    - Sep 19, 2012: Both fields grazed (continuous).
  - Footprints and timing focused on capturing N2O responses to tillage and subsequent management.

- Measurement approaches
  - Eddy covariance (EC)
    - Installed March 27, 2012 at field boundary; height 2.4 m.
    - Instrumentation: 3-axis WindMaster Pro anemometer; quantum cascade laser (QCL) gas analyser for N2O, H2O, CO2.
    - Data: 10 Hz sampling; fluxes computed at 30 min intervals using covariance between N2O mixing ratio and vertical wind speed.
    - Data processing: double coordinate rotation, spike removal, block averaging, time-lag removal via covariance maximisation; frequency loss and density fluctuation corrections; quality control per Foken et al. (2005); initial data separation by wind direction to assign to tilled vs un-tilled field; data outside instrument footprint discarded.
  - Chamber measurements
    - Static chambers: PVC cylinders (38 cm ID, 22 cm height) inserted 5 cm; closed for 40 min; three 100 mL samples taken; gas analysed by GC with ECD.
    - Dynamic chambers: 39 cm ID, 22 cm high, connected to QCL via tubing; closed system with ~6–7 L/min flow; fluxes computed from 1 Hz data over 3 minutes using linear and non-linear asymptotic regression; best-fit method chosen per measurement.
    - Coverage: 10 static chambers per field; chambers occasionally moved to minimize microclimate bias; measurements typically between 09:00–15:00.
  - Flux calculations
    - Static: F = (dC/dt) × (ρ V) / A, where dC/dt is concentration change over time; ρ is air density, V chamber volume, A ground area.
    - Dynamic: fluxes derived from chamber–instrument data with appropriate regression models.
  - Data and files
    - Easter_Bush_EddyC_Tillage_2012: EC data file containing fluxes, meteorology (wind, L, L-d)/L, CO2, H2O, N2O, etc., with accompanying wind direction and quality metrics.
    - Easter_Bush_Chambers_Tillage_2012: Chamber data file with fluxes, air temperature, soil temperature, soil water content, rainfall, PAR, etc.
    - Table 1: Field management events for tilled and un-tilled fields in 2012.

- Analytical and QA considerations
  - Cross-validation: EC and chamber methods provide complementary coverage of N2O fluxes.
  - Data quality and limitations:
    - Footprint separation relies on wind direction; data outside clear separation excluded due to potential obstruction.
    - Java-like issues with data alignment across methods and scales; standard corrections applied to account for instrument and environmental effects.
  - Relevance to data challenges:
    - Addresses common data issues for environmental flux studies: local-scale management effects (tillage), sparse high-quality data streams (EC vs chambers), and need for careful QA in complex landscapes.