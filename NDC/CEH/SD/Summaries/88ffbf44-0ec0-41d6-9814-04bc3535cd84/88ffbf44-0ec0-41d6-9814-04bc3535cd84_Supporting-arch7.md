# Site Description

- Auchencorth Moss is a 3.4 km² low-lying ombrotrophic peatland in SE Scotland (55°47' N, 03°14'W; 249–300 m elevation) with predominantly peat soils (85%). Land use is mainly low-intensity sheep grazing, with a small peat extraction area in the southwest.
- Catchment and hydrology: patchy vegetation over a Sphagnum base with hummock/hollow microtopography; hollows may submerge after heavy rainfall but no permanent water bodies exist. Peats depth ranges from <0.5 m to >5 m; underlying geology includes glacial till and Carboniferous/Devonian sandstone sequences. Mean water-table depth is 12.5 cm (ranging >55 to 4.5 cm above peat). Deposited nutrients include DOC (mean 312 ± 15.9 μg C g⁻¹ dry soil), NO₃⁻ (4.45 ± 0.48 μg N g⁻¹), and NH₄⁺ (21.8 ± 1.85 μg N g⁻¹). Total nitrogen deposition ~0.8 g N m⁻² yr⁻¹.
- Drainage and hydrology: drainage ditches in an area of special scientific interest were blocked by SNH in March 2015 using peat dams (red) and plastic pile dams (blue). The main catchment drains NE via natural tributaries to the Black Burn; total stream length from source to outlet is ~5.2 km with an average width of 0.65 m. The stream shows a rapid (flashy) response to rainfall events.

- GIS visuals: Auchencorth Moss Map 1 (peat dams in red and plastic dams in blue) and Map 2 (same dam locations) accompany the dataset. Table 1 lists blocking dates by ditch.

- Ditch blocking chronology (selected summary): 39 drains were blocked, with peat and plastic dams typically blocked early March 2015 and plastic dams around 18–19 March 2015; some drains show blocking dates between March 2–9, 2015, with multiple drains processed on the same dates.

- Experimental design and sampling regime (2015–early 2016) at three stream water sites:
  - Lower site
  - Tributary site
  - Upper site
  - Site coordinates (degrees): Lower 55°47'13.36"N, 3°15'32.41"W; Tributary 55°47'07.98"N, 3°15'43.62"W; Upper 55°47'04.14"N, 3°15'43.40"W
  - Measurement periods span several data streams dated 2015–2016 (see data tables for exact ranges).

## Spatial Features and GIS-Ready Data

- Sampling sites: three geo-located stream water sites (Lower, Tributary, Upper) with precise latitude/longitude coordinates.
- Ditch and dam features: locations of peat dams and plastic pile dams, mapped for spatial analysis of hydrological modifications.
- Catchment topology: low-relief peatland with hummock/hollow microtopography; drainage network and blocked ditches alter hydrological connectivity within the catchment.
- Maps and figures: Map 1 and Map 2 depict dam locations; Table 1 provides blocking dates per ditch.

## Data Collected and Temporal Coverage

- Continuous data
  - CO2 concentrations at the lower site (15-minute sampling; 0–1% CO2 range; corrected for temperature/pressure; results in mg C L⁻¹).

- Discrete water chemistry and greenhouse gases
  - DOC (daily autosampler samples; 200 mL water samples filtered and analyzed; range 0.1–4000 mg L⁻¹).
  - DIC (manual sampling approximately weekly; 60 mL syringes, filtered; analyzed similarly to DOC; results in mg C L⁻¹).
  - GHGs (headspace method; CO2, CH4, N2O concentrations; two replicate headspace samples plus ambient air; analyzed by GC; results in mg C L⁻¹ or μg C L⁻¹ depending on species).

- Datasets and date ranges
  - CO2_continuous.csv: 11/02/2015 to 03/02/2016
  - DOC_Daily_Autosampler.csv: 20/02/2015 to 05/11/2015
  - DOC_DIC_2weeks_Manual.csv: 04/03/2015 to 17/03/2016
  - GHGs_2weeks_Manual.csv: 04/03/2015 to 07/07/2015

- Units and variables
  - DOC: mg C L⁻¹
  - DIC: mg C L⁻¹
  - CO2: mg C L⁻¹
  - CH4: μg C L⁻¹
  - N2O: μg N L⁻¹
  - Date: dd/mm/yyyy local time
  - Site: Local site identifier (Lower, Tributary, Upper)

## Methods and Calibration

- Continuous CO2
  - Instrument: Vaisala GMT220 NDIR; 15-minute cadence; sensors enclosed in water-tight PTFE membranes; depth- and temperature-corrected to mg C L⁻¹.

- DOC and DIC
  - DOC: 200 mL samples collected daily at the lower site, filtered (0.45 μm) and measured with a PPM LABTOC Analyser (0.1–4000 mg L⁻¹ range).
  - DIC: Manual sampling ~weekly; same filtration and analysis as DOC.

- Dissolved GHGs
  - Headspace method: 40 mL water equilibrated with 20 mL ambient air; two replicates per occasion; GC analysis with ECD (N2O) and FID (CH4/CO2); detection limits ~CO2 10 ppmv, CH4 70 ppbv, N2O 30 ppbv.
  - Concentrations calculated from headspace and ambient air via Henry’s law.

- Calibration
  - Gas chromatograph: 4-point CH4/N2O calibration standards (various ppmv).
  - LABTOC analyser: 3-point 0–50 ppm calibration.

- Data formatting and metadata
  - Records include Date, Site, and concentration values with appropriate units as listed above.

## Data Quality and Standards

- Cross-method data integration involves aligning datasets with different resolutions and time steps; data are corrected/calibrated according to referenced methodological sources.
- Spatial analysis benefits from the mapped dam locations and sampling sites to assess how hydrological modifications influence carbon and greenhouse gas fluxes in the peatland.

## References

- Billett MF, Palmer SM, Hope D, Deacon C, Storeton-West R, Hargreaves KJ, Flechard C, Fowler D (2004) Linking land-atmosphere-stream carbon fluxes in a lowland peatland system. Global Biogeochemical Cycles 18: GB1024
- Dawson JJC, Hope D, Cresser MS, Billett MF (1995) Downstream Changes in Free Carbon-Dioxide in an Upland Catchment from Northeastern Scotland. Journal of Environmental Quality 24(4): 699-706
- Dinsmore KJ, Billett MF, Skiba U, Rees RM, Drewer J, Helfter C (2010) Role of the aquatic pathway in the carbon and greenhouse gas budgets of a peatland catchment. Global Change Biology 16(10): 2750-2762
- Dinsmore KJ, Wallin MB, Johnson MS, Billett MF, Bishop K, Pumpanen J, Ojala A (2013) Contrasting CO2 concentration discharge dynamics in headwater streams: A multi-catchment comparison. Journal of Geophysical Research: Biogeosciences 118(2): 445-461
- Drewer J, Lohila A, Aurela M, Laurila T, Minkkinen K, Penttila T, Dinsmore KJ, McKenzie RM, Helfter C, Flechard C, Sutton MA, Skiba UM (2010) Comparison of greenhouse gas fluxes and nitrogen budgets from an ombotrophic bog in Scotland and a minerotrophic sedge fen in Finland. European Journal of Soil Science 61(5): 640-650
- Johnson MS, Billett MF, Dinsmore KJ, Wallin M, Dyson KE, Jassal RS (2010) Direct and continuous measurement of dissolved carbon dioxide in freshwater aquatic systems - methods and applications. Ecohydrology 3: 68-78