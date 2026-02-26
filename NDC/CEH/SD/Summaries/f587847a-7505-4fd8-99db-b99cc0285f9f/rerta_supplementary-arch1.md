# Nitrous oxide and methane fluxes from different riparian restoration treatments in Oil Palm plantations in Riau, Indonesia 2019-2021

## Aim
- Quantify greenhouse gas fluxes (N2O, CH4, CO2) from four riparian restoration treatments in oil palm landscapes.
- Provide guidance to oil palm growers and policy makers on the environmental impact of different riparian management practices.

## Context and scope
- Oil palm expansion in Southeast Asia linked to deforestation, biodiversity loss, and greenhouse gas emissions; riparian buffers are increasingly required and promoted.
- Limited knowledge on how riparian buffers affect CH4 and N2O emissions; study aims to address this gap.

## Experimental design / Treatments
- Two RERTA sites were established (Kandista and Ujung Tanjung); this greenhouse gas study was conducted at Ujung Tanjung.
- Four treatments across 50 x 400 m river-adjacent zones in a plantation due for replanting:
  1) Immature oil palm – no restoration, replanting to river margin
  2) Mature oil palm – no restoration, 50 m buffer of mature oil palm
  3) Native trees – enrichment planting with forest trees in a 50 m buffer, removal of all mature oil palm
  4) Mature oil palm and native trees – enrichment with forest trees in a 50 m buffer and maintenance of mature oil palm
- 40 static chambers installed: six replicates per treatment (24 chambers) and 16 in the surrounding plantation
- Sampling schedule: monthly from January 2019 to September 2021, with breaks for felling/replanting (April 2019–October 2019) and COVID-19 (January 2021–June 2021)

## Field collection and laboratory instrumentation
- Chamber setup: 40 cm diameter collars inserted to ~7 cm depth; lids sealed; sampling port and pressure compensation used; 100 mL samples collected at 0, 15, 30, and 45 minutes.
- Sample handling: samples transferred to 20 mL glass vials with chlorobutyl septa; shipped to UKCEH Edinburgh for analysis.
- Ancillary measurements: volumetric soil moisture measured near each chamber (depth ~7 cm).
- Permits: foreign research permits issued by Indonesia (RISTEK; two permit numbers covering 2019 and 2020).

## Analytical methods and quality control
- Gas analysis: Agilent 7890B GC with μECD for N2O and FID for CH4 and CO2.
- Calibration: four-point calibration using mixed gas standards; regular calibration after ~20 samples.
- Flux calculation: RCFlux R package using six regression models; flux chosen as the best-fitting model (highest R^2); expressed as µmol m^-2 s^-1 with 95% confidence intervals.
- Data quality: regression plots reviewed; outliers treated conservatively (data flagged invalid only if clearly unreliable); most flux estimates derived from linear or HMR models.

## Data outputs and structure
- rerta_ghg_rcflux.csv
  - Fluxes for each chamber (1–40) across sampling occasions (monthly, 2019–2021)
  - Includes gasName, multiple flux estimates (linear, quadratic, linear2nd, quadratic2nd, asymptotic, HMR, bestfit)
  - Includes 95% confidence intervals and adjusted R^2 values; bestFitMethod and date metadata (year, month, day), chamber identifiers, position, plot type, treatment_zone, treatment, date_installed, soil_moisture, chamber dimensions, and location data
  - NA values indicate missing data or calculations not performed
- rerta_chambers.csv
  - Details for the 40 chambers: RERTA_code, position (east/west), plot (plantation vs riparian buffer), treatment_zone, treatment, date_planted, date_installed, lat, lon, elev, and chamber-specific attributes (e.g., diameter, height, area, volume)

## Additional context
- Data collection spanned multiple years and was interrupted by plantation management activities and the COVID-19 pandemic, which is reflected in the sampling timeline.
- The dataset is intended to be discoverable and usable with metadata, facilitating reuse for comparisons across studies and informing policy and practice in riparian management.