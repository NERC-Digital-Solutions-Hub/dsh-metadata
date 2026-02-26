# Overall sampling design

## Aim and study context
- Aimed to characterize seasonal and geology-related changes in the functional microbial community involved in carbon and nitrogen cycling.
- Measurements are paired within columns to relate process rates to functional genes; sampling across sites uses a consistent transect design.

## Sampling design
- At each site: nine soil samples taken within a 40 x 40 m transect at 20 m intervals.
- Sub-samples prepared and stored differently depending on the intended analysis.
- Focus on measuring process rates (mineralization, nitrification, denitrification, N2O production) to address hypotheses about seasonal and geological influences.

## Methodologies (measurements and core procedures)
- Soil water content and soil pH: measured using Rowell 1994 methods.
- Mineralization and nitrification: rates estimated by isotope dilution, using Kirkham and Bartholomew (1954) equation.
  - Small soil cores (10 ml syringes with distal ends removed) collected from 0–10 cm depth for these measurements.
- Denitrification: measured by a 15N enrichment technique (Nielsen 1992) with 15N-enriched soils incubated in situ for 2 days.
  - About 3 g of 15N-enriched soil used per exetainer (12.5 ml) in 12 exetainers.
- Nitrous oxide (N2O) production: measured via gas chromatography with an electron capture detector, following Robinson (1997) approach.
  - 3 g of 15N-enriched soil per exetainer incubated in situ for 2 days.
- Ammonium and nitrate: extracted with 2 M KCl.
  - NH4+: analyzed colorimetrically; nitrate: UV absorption at 220 nm.
  - Extraction specifics: 8 g wet-weight soil for NH4+ extraction; 4 g wet-weight soil for NO3− extraction.

## Sample handling and incubation details
- Incubations conducted at in situ temperature for 2 days for denitrification and N2O measurements.
- Aliquots prepared as described; exetainers and precise incubation conditions maintained to ensure comparability.

## Data and metadata structure
- Identifying information:
  - Year, measurement definitions for year/date/month; site.name stores a short site name encoding underlying geology and river information (e.g., GA2 = River Avon; CW2 = River Wylye; AS2 = River Sem).
  - geology field indicates sub-catchment underlying geology (Clay, Chalk, Greensand).
- Measured variables and units:
  - Mineralisation: µg N g-1 dry weight soil day-1.
  - Nitrification: µg N g-1 dry weight soil day-1.
  - Denitrification niche variables: in situ and saturated moisture contents (percent).
  - N2O production moisture context: in situ and saturated moisture contents (percent).
  - Soil pH; soil temperature (°C); soil water content (percent).
  - Ammonium: µmol NH4 g-1 dry weight soil day-1.
  - Nitrate: µmol NO3 g-1 dry weight soil day-1.
- Quality control: Measurements validated by the Centre for Ecology & Hydrology, Lancaster.

## Quality control and provenance
- QC validation performed by CEH Lancaster to ensure data reliability.
- Detailed documentation of methods and materials enables reproducibility and cross-study comparability.
- Isotopic enrichment (approximately 40% 15N) specified for denitrification and N2O experiments to ensure interpretability of rates.

## Data governance and stewardship considerations
- Clear metadata definitions for year, date, site, geology, and measurement types to support discoverability and reuse.
- Standardized units and measurement definitions across analyses facilitate interoperability.
- Documentation of analytical protocols and QC steps supports data traceability and quality assurance.
- Data sharing readiness is enhanced by explicit identifiers (site codes, geology) and method references, enabling accurate data integration into portals and catalogs.

## Key considerations for Data Stewards
- Ensure comprehensive metadata capture (site names, geology encoding, measurement definitions, units, and date fields) to enable discovery and reuse.
- Maintain provenance by storing method references (Rowell 1994; Kirkham & Bartholomew 1954; Nielsen 1992; Robinson 1997) and precise incubation conditions.
- Prescribe and enforce standardized data formats and unit conventions to support interoperability across datasets and analyses.
- Capture quality control status and validation sources (e.g., CEH Lancaster) to communicate data reliability.
- Anticipate challenges such as aligning metadata with user needs, handling large datasets from multiple analyses, and ensuring timely data availability across sites and time points.