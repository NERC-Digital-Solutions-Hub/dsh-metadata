# Weekly water quality monitoring data of eight sites along the River Thames, UK, and sixteen of its major tributaries (2009-2023)

## Overview
- A long-term dataset of weekly water quality measurements from eight River Thames sites and sixteen major tributaries.
- Coverage: March 2009 to December 2023.
- Parameters include nutrients (phosphorus species, nitrogen species), dissolved silicon, temperature, pH, alkalinity, suspended solids, chlorophyll, major dissolved anions (fluoride, chloride, bromide, sulfate), major dissolved cations (Na, K, Ca, Mg, B) (measured 2009–Oct 2016), and dissolved/total metals (Fe, Mn, Zn, Cu) (measured Aug 2010–Feb 2013). Additional measurements and methods described below.

## Scope and Coverage
- Sites: 8 Thames sites + 16 tributaries.
- Sampling frequency: weekly bulk samples from main flow, collected on Mondays or Tuesdays.
- Data organization: monitoring site order, then ascending date.

## Data Collection and Handling
- In-field measurements (Mar 2013–present): water temperature, pH, conductivity, redox potential; dissolved oxygen measured post-sampling since July 2018.
- Subsampling: field filtration through 0.45 μm membranes; samples stored in the dark at 4°C until analysis.
- Data gaps and notes: missing data shown as blanks; samples below detection limits marked nd (not detectable).

## Analytical Methods and Measurements
- pH: laboratory measurement with a calibrated pH meter (pH 4, 7, 10 buffers; traceable to NIST).
- Alkalinity: acidimetric titration to pH 4 and 3 with 0.5N H2SO4.
- Suspended solids: gravimetric determination via filtration and drying/weighing.
- Chlorophyll a: filtration, acetone extraction, spectrophotometric measurement per Marker et al. 1980.
- Phosphorus:
  - Total phosphorus (TP) and total dissolved phosphorus (TDP): digestion with acidified potassium persulfate and colorimetric detection at 880 nm.
  - Soluble reactive phosphorus (SRP): filtered sample with phosphomolybdate colorimetry (Murphy & Riley; Neal et al. 2000); SRP analyzed within 48 hours.
- Dissolved reactive silicon: molybdate reaction and reduction to produce silicomolybdenum blues; spectrophotometric quantification.
- Ammonium: indophenol-blue colorimetric method.
- DOC and TDN: thermal oxidation methods; DOC/TDN measured with Thermalox until 2010 and with a Elementar Vario Cube from 2011 onward.
- Major anions: fluoride, chloride, nitrite, nitrate, sulfate by ion chromatography.
- Major cations: total (unfiltered) and dissolved (filtered) concentrations after acidification, by IC-OES.
- Quality control: analyses (except suspended solids) run with Aquacheck QC standards.

## Temporal and Spatial Details
- Date/time format: day/month/year; sampling time in hour:minute.
- Additional data reference: mean daily river flow available from the National River Flow Archive (NRFA).
- Gauging stations: most sites near Environment Agency gauging stations; relevant stations listed in SiteLocations_2009_2023 (supporting documents).

## Data Quality and Organization
- Data quality controls include QC standards with analyses (except SS).
- Data are organized by monitoring site, then by date.
- Documentation includes methods, units, and references for analytical approaches.

## Units and Variable Definitions
- Concentrations reported as appropriate units per parameter (e.g., TP, TDP, SRP in μg P/L; chlorophyll a in μg/L; ammonium in mg NH4+/L; various metals in mg/L or μg/L as specified in the dataset; pH is unitless; temperature in °C; conductivity in μS/cm; DO as % saturation or mg/L depending on measurement).

## References and Method Details
- Eisenreich, Bannerman, Armstrong (1975) – simplified phosphorus analytical technique.
- Leeks et al. (1997) – LOIS river monitoring strategy.
- Marker et al. (1980) – chlorophyll pigment measurement standardization.
- Mullin & Riley (1955) – silicate colorimetric method.
- Murphy & Riley (1962) – phosphorus determination colorimetry.
- Neal et al. (2000) – SRP measurement considerations (silica interference).
- Additional instrument and method notes for the Auto Analyser 3 and IC-OES processes.

## Practical Considerations for Data Support
- Longitudinal potential: suitable for trend analysis, seasonal patterns, and watershed-scale assessments.
- Data preparation needs: handle missing data; flag nd values; harmonize units across years where method changes occurred (e.g., cation/metal measurements, DOC/TDN methods).
- Data integration opportunities: combine with NRFA flow data for flux calculations; align with site locations in supporting documents for spatial analyses.
- Data products to consider: time-series dashboards, self-serve tables, dashboards comparing sites, and exportable CSV/JSON datasets for downstream analytics.

## Potential Data Products and Uses
- Dashboards capturing temporal trends of key nutrients, metals, and chlorophyll across sites.
- Time-series analyses of TP, SRP, TDP, and nitrogen species to assess eutrophication risk.
- Flow-normalized interpretations by integrating NRFA river flow data.
- Public-facing summaries of water quality status and changes over the 2009–2023 period.