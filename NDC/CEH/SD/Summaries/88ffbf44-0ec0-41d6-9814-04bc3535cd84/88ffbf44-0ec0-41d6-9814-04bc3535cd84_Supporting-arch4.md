# Site Description

- Auchencorth Moss is a 3.4 km2 peatland in SE Scotland (55°47' N, 3°14'W) with low-intensity sheep grazing and a small area of peat extraction in the southwest.
- The catchment features a patchy vegetation cover above a Sphagnum-dominated base, with hollows that can flood after heavy rain but no permanent pools.
- Peat depths range from <0.5 m to >5 m; underlying geology includes glacial till and Lower Devonian sandstones with minor limestone and coal.
- Hydrology is freshwater-dominated with drainage NE through natural tributaries and overgrown drainage ditches into the Black Burn; total stream length ~5.2 km and a typically flashy hydrograph.
- Ditch blocking across the catchment (peat dams and plastic piling dams) occurred in March 2015 to restore hydrological connectivity; 36 blocking events documented (dates vary by site).

## Experimental context and sites

- Timeframe: measurements conducted in 2015 through early 2016.
- Three stream water sites: Lower, Tributary, and Upper with precise coordinates provided (latitude/longitude for each site).
- Data collection focuses on carbon and greenhouse gas dynamics in stream water pre- and post-ditch blocking.

## Data types and sampling regime

- CO2 flux data: Continuous CO2 concentrations collected at the lower site.
- Dissolved organic carbon: Daily DOC concentrations at the lower site (autosampler) and periodic DIC measurements (manual).
- Dissolved inorganic carbon and GHGs: Manual sampling for DOC, DIC, CO2, CH4, and N2O (headspace method) across the three sites.
- Datasets and time spans:
  - CO2_continuous.csv: 11/02/2015 to 03/02/2016
  - DOC_Daily_Autosampler.csv: 20/02/2015 to 05/11/2015
  - DOC_DIC_2weeks_Manual.csv: 04/03/2015 to 17/03/2016
  - GHGs_2weeks_Manual.csv: 04/03/2015 to 07/07/2015

## Collection and Analytical Methods

- Continuous CO2 concentrations
  - Instrument: Vaisala GMT220 NDIR CO2 transmitters
  - Frequency: 15-minute intervals
  - Setup: sensors under water in a perforated sleeve; connected to a datalogger
  - Calibration/Corrections: corrected for temperature and pressure (atmospheric and water depth)
  - Output: CO2 in mg C L-1

- Daily DOC concentrations
  - Sample collection: 200 mL samples at the lower site daily; sampling typically weekly
  - Filtration: 0.45 µm syringe filters
  - Analysis: PPM LABTOC Analyser
  - Range: 0.1–4000 mg L-1

- Manual sampling for DOC and DIC
  - Frequency: ~weekly March–July 2015, then ~biweekly
  - Methods: 60 mL syringe, 0.45 µm filtration, cooled transport to CEH Edinburgh
  - Analysis: LABTOC Analyser (as above)

- Manual sampling for CO2, CH4 and N2O
  - Method: headspace technique
  - Procedure: 40 mL water samples equilibrated with 20 mL ambient air; two replicate headspace samples plus ambient air
  - Analysis: GC (HP5890 Series II) with ECD for N2O and CH4; FID (with methaniser) for CO2
  - Detection limits: CO2 10 ppmv, CH4 70 ppbv, N2O 30 ppbv
  - Calculation: dissolved gas concentrations derived from headspace using Henry’s law

- Calibration
  - Gas chromatography: 4-point CH4/N2O calibration standards (provided concentrations)
  - LABTOC: 3-point zero-to-50 ppm calibration

## Data format and units

- Recorded fields
  - Date: dd/mm/yyyy (local time)
  - Site: site identifier (Lower, Tributary, Upper)
  - DOC: mg C L-1
  - DIC: mg C L-1
  - CO2: mg C L-1
  - CH4: µg C L-1
  - N2O: µg N L-1

## Location and drainage context

- Three sampling sites located along the Auchencorth Moss drainage network:
  - Lower site
  - Tributary site
  - Upper site
- Drainage modification: multiple drains were blocked in March 2015 using peat dams and plastic dams; blocking dates are detailed in accompanying tables and figures.

## References and context

- Methodological and environmental context drawn from a body of literature focusing on peatland carbon fluxes, dissolved inorganic/organic carbon, and aquatic greenhouse gas budgets, including work by Billett et al., Dawson et al., Dinsmore et al., and Johnson et al.