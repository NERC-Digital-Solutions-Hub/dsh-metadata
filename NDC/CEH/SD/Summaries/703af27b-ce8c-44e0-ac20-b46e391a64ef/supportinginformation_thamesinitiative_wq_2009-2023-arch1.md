# Brief description of the dataset

- Weekly water quality monitoring data for eight River Thames sites and sixteen major tributaries.
- Time range: March 2009 to December 2023.
- Measured parameters include phosphorus and nitrogen species, dissolved reactive silicon, temperature, pH, Gran alkalinity, suspended solids, chlorophyll, and major dissolved anions (fluoride, chloride, bromide, sulfate).
- Major cations (sodium, potassium, calcium, magnesium, boron) measured 2009–October 2016; dissolved and total iron, manganese, zinc, and copper measured August 2010–February 2013.

## Data collection and sampling

- Bulk samples collected from the main flow on Monday or Tuesday each week.
- In-field measurements (2013–present): water temperature, pH, conductivity, redox potential.
- Dissolved oxygen measured immediately after sampling (since July 2018).
- Subsamples filtered in the field through 0.45 μm membranes; samples stored in the dark at 4°C before laboratory analysis.
- Missing data appear as blanks; samples below detection limits marked nd (not detectable).

## Analytical methods

- pH: laboratory measurement with Radiometer pH meter; calibration with pH 4, 7, 10 buffers (NIST-traceable).
- Gran alkalinity: acidimetric titration to pH 4 and 3 using 0.5 N H2SO4.
- Suspended solids: filtration, drying, and reweighing of pre-dried filter papers.
- Chlorophyll a: filtration, acetone extraction, spectrophotometric quantification (Marker et al. 1980).
- Total phosphorus (TP) and total dissolved phosphorus (TDP): digestion with acidified potassium persulphate; blue molybdenum complex quantified at 880 nm.
- Soluble reactive phosphorus (SRP): filtered sample analyzed by phosphomolybdenum blue method (Murphy & Riley; Neal et al. 2000).
- Dissolved reactive silicon: molybdate-based method with tin(II) reduction; spectrophotometric measurement.
- Ammonium: indophenol-blue colorimetric method.
- Dissolved organic carbon (DOC) and total dissolved nitrogen (TDN): thermal oxidation method (Thermalox) up to 2010; Elementar Cube from 2011.
- Major dissolved anions: fluoride, chloride, nitrite, nitrate, sulfate by ion chromatography (Dionex).
- Cations: total and dissolved concentrations determined by ICP-OES after acidification (unfiltered for total, filtered for dissolved).
- Flow data: mean daily river flow from the National River Flow Archive (NRFA); gauging stations linked to sites via SiteLocations_2009_2023.

## Nature and units of recorded values

- Date/time format: day/month/year; sampling time in hour:minute.
- Concentration and concentration-like units:
  - Total phosphorus, dissolved phosphorus: micrograms P per litre.
  - Soluble reactive phosphorus: micrograms P per litre.
  - Chlorophyll a: micrograms per litre.
  - Suspended solids: milligrams dry solids per litre.
  - Gran alkalinity: micro-equivalents per litre.
  - Dissolved/total metals (Fe, Mn, Zn, Cu): micrograms per litre.
  - Ammonium: milligrams NH4+ per litre.
  - Dissolved silica, nitrogen, carbon species: mg or mg/L as specified.
  - Major cations/ions: mg/L or μg/L as specified.
  - Conductivity: microsiemens per centimetre.
  - Redox potential: millivolts.
  - Dissolved oxygen: percent saturation and mg/L.
- TP and TDP are totals for unfiltered and 0.45 μm filtered samples, respectively; SRP is filterable/reactive phosphorus.
- Some parameters have multiple measurement conventions (e.g., total vs dissolved, unfiltered vs filtered).

## Data quality and quality control

- All analyses (except suspended solids) carried out with reference Aquacheck QC standards (LGC Standards).
- Data presented in monitoring site-order, then ascending date order.

## Data structure, access, and documentation

- Site locations and relevant gauging stations referenced in supporting documents (SiteLocations_2009_2023).
- Data include missing values (blanks) and non-detects (nd).
- References for analytical methods provided (embedded in dataset metadata).

## References

- Eisenreich, S. J., Bannerman, R. T., & Armstrong, D. E. (1975). A simplified phosphorus analytical technique.
- Leeks, G. J. L., Neal, C., Jarvie, H. P., Casey, H., & Leach, D. V. (1997). The LOIS river monitoring network: strategy and implementation.
- Marker, A. F. H., Nusch, E. A., Rai, H., & Riemann, B. (1980). The measurement of photosynthetic pigments in freshwaters.
- Mullin, J. B., & Riley, J. P. (1955). Colorimetric determination of silicate.
- Murphy, J., & Riley, J. P. (1962). Modified method for phosphorus in natural waters.
- Neal, C., Neal, M., & Wickham, H. (2000). Phosphate measurement and interference issues in natural waters.