# Relationship between the concentrations of dissolved organic matter and polycyclic aromatic hydrocarbons in a typical U.K. upland stream.

## Study design and sampling context
- Location: River Wyre, northwest England, spanning upland and agricultural areas with organic-rich soils.
- Sites: five sampling sites along the river.
- Timeline: four sampling events (19 Aug 2010; 6 Dec 2010; 6 Mar 2011; 6 Jun 2011).
- Sample types and volumes: 5 L water samples for PAHs; 100 mL samples for DOC per site per event.
- Storage and handling: samples kept at 5 °C and processed within 48 hours; stability of dissolved PAHs and DOC confirmed in preliminary tests.

## DOC analysis
- Method: DOC concentrations determined by UV absorbance at 270 and 350 nm using an algorithm from Tipping et al. 2009.
- Filtration: samples filtered through a 0.45 µm filter prior to analysis.

## PAH analysis and fractionation
- Sample division: each sample split into two sub-samples for total dissolved PAHs and freely dissolved PAHs.
- Isolation of freely dissolved PAHs:
  - Precipitate DOC and DOC-associated PAHs with Al2(SO4)3 (0.4 g in 5 mL water) at pH 6.
  - Flocculation and removal of DOC via GF-F filter.
  - Al2(SO4)3 effectively removes DOC and associated PAHs, preserving freely dissolved PAHs.
- Total dissolved PAHs: measured in raw sample filtered through a GFF filter.
- DOC-associated PAHs: calculated indirectly as (total dissolved PAHs) minus (freely dissolved PAHs).
- Quality controls: laboratory blanks included.

## PAH extraction and instrumental analysis
- Extraction: samples split, liquid–liquid extraction with dichloromethane (DCM) three times; extracts pooled and dried.
- Clean-up: reduced to ~1 mL, desiccated with sodium sulfate, cleaned on alumina column.
- Internal standards: spiked with d10-acenaphthene and d12-benz[a]anthracene.
- Target compounds: 28 PAHs analyzed (recovery compounds monitored).
- Naphthalene: initially included but excluded from reporting due to high/variable blank levels.
- Instrumentation: GC-MS (Agilent 6890N + 5973N) with EI-mode and selected ion monitoring.
  - Injection: 20 µL in solvent vent mode; HT8 column; helium carrier gas.
  - Temperature program: detailed ramping and holds culminating at 330 °C.
  - Data: quantification of 28 target PAHs and recovery compounds.

## Data outputs and structure for GIS use
- Variables per site per event:
  - DOC concentration (from UV absorbance method).
  - Freely dissolved PAH concentrations.
  - Total dissolved PAH concentrations.
  - DOC-associated PAH concentrations (calculated as difference between total and freely dissolved).
  - Possibly the 28 PAH concentrations reported (excluding naphthalene).
- Temporal and spatial resolution:
  - Spatial: five river sites.
  - Temporal: four sampling events across 2010–2011.
- Data quality considerations:
  - Use of blanks, deuterated internal standards, and recovery checks to ensure data reliability.
  - Exclusion of naphthalene due to analytical blanks.

## Considerations for GIS integration
- Data can be mapped as spatial distributions of DOC, freely dissolved PAHs, total PAHs, and DOC-associated PAHs by site and time.
- Enables cross-site comparisons and time-series analyses to explore relationships between DOC and PAH fractions.
- Documentation needed: site coordinates, sampling timestamps, unit definitions, and QA/QC flags to ensure consistent GIS layering and analysis.

## References
- Tipping, E.; Corbishley, H. T.; Koprivnjak, J. F.; et al. Quantification of natural DOM from UV absorption at two wavelengths. Environ. Chem. 2009.
- Laor, Y.; Rebhun, M. Complexation-flocculation: A new method to determine binding coefficients of organic contaminants to dissolved humic substances. Environ. Sci. Technol. 1997.