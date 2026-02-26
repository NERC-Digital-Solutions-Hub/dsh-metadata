# ECN Frog Spawning Phenology Data

- A phenology-based dataset recording the spawning of Common Frogs in selected pools and ditches, with accompanying water-quality analyses.
- Purpose: support GIS-based data products and spatial analysis of environmental change impacts on frog populations.

## Dataset provenance and governance

- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (ECN data portal available at http://data.ecn.ac.uk; contact ecn@ceh.ac.uk).
- Dataset Owners: UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies.
- Acknowledgement and use: ECN requests acknowledgment in publications and a reprint of any publication citing the data.
- Standards and comparability: ECN has standard operating procedures to ensure comparability across sites; see BF.pdf for data collection procedures.

## Data content and structure

- Methodology:
  - Spawning is recorded through counting egg masses as an indicator of population health.
  - Laboratory analyses are conducted on water samples from observed pools.
  - Users should consult accompanying quality information when using the data.
- Data download structure:
  - SITECODE: Unique ECN Site code.
  - LCODE: Location code (unique within site).
  - FROMDATE: Start date of data applicability.
  - SDATE: Sampling date.
  - FIELDNAME: Variable measured (e.g., spawning-related metrics or water quality parameters).
  - VALUE: Measured value.
- Supporting quality information:
  - ECN_BF_qtext.csv contains site-manager assigned quality codes and optional explanatory text for atypical events (quality code 999 indicates an unusual event).
  - Quality codes (Q1–Q8) accompany the data to describe data quality and processing status.
  - A dedicated quality-code dictionary is provided to interpret codes and their meanings (e.g., data losses, sample issues, laboratory conditions, or unusual events).
- Explanatory material: Site codes and locations are provided to enable precise geospatial interpretation.

## Site codes and locations (examples)

- T01: Drayton — 52°11'37.95"N, 1°45'51.95"W
- T02: Glensaugh — 56°54'33.36"N, 2°33'12.14"W
- T03: Hillsborough — 54°27'12.24"N, 6°04'41.26"W
- T04: Moor House - Upper Teesdale — 54°41'42.15"N, 2°23'16.26"W
- T05: North Wyke — 50°46'54.96"N, 3°55'4.10"W
- T06: Rothamsted — 51°48'12.33"N, 0°22'21.66"W
- T08: Wytham — 51°46'52.86"N, 1°20'9.81"W
- T09: Alice Holt — 51°9'16.46"N, 0°51'47.58"W
- T10: Porton Down — 51°7'37.83"N, 1°38'23.46"W
- T11: Snowdon (Y Wyddfa) — 53°4'28.38"N, 4°2'0.64"W

Note: T07 is not listed; site coverage includes ten named sites with precise coordinates.

## Variables and measurement details

- FIELDNAME examples include (with typical context):
  - Spawning-related: CONGDATE (date frogs first seen congregating), HATCHDATE (date first hatching observed), SPAWNDATE (date of first spawning observed), NEWMASS (number of new spawn masses), SURFAREA (surface area of spawn), STAGE (water level stage).
  - Water quality and chemistry: ALKY (alkalinity, mg/L), CALCIUM, CHLORIDE, COND Y (conductivity), COLOUR, NH4N (ammonium), NO3N (nitrate nitrogen), TOTALN (total nitrogen), TOTALP (total phosphorus), SO4S (sulfate), SODIUM, PH (pH, with multiple readings), PH1–PH3 (daily pH readings), PHAQCS/PH A QCU (pH measurements from AquaCheck), and others.
  - Additional fields cover depth, dissolved organic carbon (DOC), metals (e.g., IRON, MAGNESIUM), and various quality indicators.
- Units: Each variable has described units (e.g., mg/L, pH 1–14, °C, cm, m2, date formats).
- Data richness: The dataset mixes spawning observations with contemporaneous water-quality measurements, enabling multi-parameter spatial analyses.

## Data quality, documentation, and supporting resources

- Quality codes: A comprehensive list (e.g., 100–177, 200–239, 501–513, and 999 for unusual events) indicating issues such as sample loss, equipment problems, environmental interferences, or lab processing notes.
- Quality text: When applicable, site managers provide descriptive text in ECN_BF_qtext.csv explaining the circumstances behind quality codes.
- Documentation: In addition to the quality file, ECN provides BF.pdf describing data collection protocols and other Explanatory Information for site codes and fields.
- Best practices for GIS:
  - Use SITECODE and LCODE for site-based joins with spatial data layers.
  - Incorporate quality codes (Q1–Q8) and accompanying text to filter or annotate data by reliability.
  - Link spawning events (spawn dates, new masses) with location coordinates to map spatial patterns of spawning activity.
  - Acknowledge ECN in any published GIS products and consult accompanying documentation to ensure proper interpretation of quality flags.

## Practical GIS considerations and usage

- Mapping and visualization:
  - Plot sites with coordinates and link to time-series of spawning indicators (e.g., spawn dates, number of spawn masses) and key water-quality parameters.
  - Use quality codes to color-code or filter data by reliability and to attach quality narratives to features.
- Data preparation:
  - Expect data to come from multiple sites with potentially different sampling dates and resolutions; perform harmonization and quality-filtering prior to analysis.
  - Prepare multi-parameter layers by joining SITECODE/LCDOE with field measurements to create composite maps showing both biotic (spawning) and abiotic (water quality) factors.
- End-user considerations:
  - The data are suitable for policy-facing visuals, stakeholder briefings, and public-facing maps that illustrate environmental change impacts on amphibian populations, provided quality indicators are clearly communicated.