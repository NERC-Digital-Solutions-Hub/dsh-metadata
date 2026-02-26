# Loch Leven long-term monitoring data

- A long-running dataset from Loch Leven, a lowland Scottish lake, collected as part of a national long-term monitoring programme beginning in 1968 and continuing through the time of writing.
- Data collection and processing supported by multiple organisations within the Natural Environment Research Council (NERC) and the UK Centre for Ecology & Hydrology, under project UK-SCAPE WP7 LEVEN.
- Aimed at describing data nature, sampling/analysis methods, data processing, and output formats to enable data use and re-use.

## Sampling regime and sites

- Fortnightly sampling schedule with two main sites: Reed Bower (RB) and Sluices/Outflow (L/Sl8).
- Reed Bower is boat-accessible; Sluices can be sampled by boat or from shore.
- Sampling can be disrupted by resource limits, weather, or ice; in some cases only Sluices is sampled, or neither site is visited.
- Site codes used in data: Harbour (Site_H), Reed Bower (Site_RB), Sluices (Site_L).

## Measurements, sampling, and analyses

- In situ measurements: conductivity, pH, temperature (via hand-held probes); Secchi depth measured at Reed Bower.
- Water samples collected in duplicate per site; different collection methods for Reed Bower (integrated PVC sampler) vs. Sluices (bottle 10 cm below surface).
- Laboratory analyses on filtered and unfiltered subsamples for: soluble reactive phosphorus (SRP), total soluble phosphorus (TSP), total phosphorus (TP), soluble reactive silicate, total diatom silica, chlorophyll a.
- Phosphorus measurements follow established methods (Murphy & Riley; Wetzel & Likens) with digestion steps for TP/TSP.
- Weather data (cloud cover, wind direction/force) logged at Reed Bower when possible; wind force mapped to Beaufort scale with a detailed lookup table.

## Crustacean and zooplankton component

- Densities (ind/L) of crustacean zooplankton taxa at RB and L sites, including Daphnia, Eudiaptomus, Cyclopidae, Cyclops spp., Bosmina, Leptodora, Bythotrephes, Chydoridae, Ceriodaphnia, Polyphemus pediculus, etc.
- Sampling methods differ by site (4 m net haul at RB; 30 L surface water through 120 µm net at L); preservation and lab counting procedures described.
- Counts converted to densities per litre; most taxa identified to species level where possible.
- As of 2022, column names updated; two new taxa added at dataset end: Ceriodaphnia_sp. and Polyphemus pediculus.

## Data processing

- Data processed with an R import script that standardises and cleans incoming data.
- Wind force: when ranges are provided (e.g., 4-5), the first value is used.
- Probe replicates (conductivity, pH, DO) filtered using Median Absolute Deviation (MAD); samples with replicates outside MAD are handled with defined rules; pH values are converted to 10^pH for median/MAD calculations, then back-transformed for final reporting; certain values are rounded (pH/DO to 2 dp; conductivity and temperatures to 1 dp).
- Inter-calibration: HQ4300 replaced HQ30d; calibration performed to maintain consistency; column names updated accordingly.

## Quality assurance

- Automated and manual data checks performed to catch entry errors and out-of-range values.
- Suspect values investigated and corrected where appropriate.

## Data format and metadata

- Data stored as a single CSV file with comprehensive columns describing determinands, sites, units, and conditions.
- Missing values represented as NA.
- Column descriptions provide detailed metadata, including date, site, week of year, various water quality parameters, and crustacean/zooplankton counts.
- 2023 dataset updates: internal naming harmonised (e.g., litres to L, micro (µ) to u, degrees to deg); Ceriodaphnia_sp. added; overall column order preserved.

## References and further reading

- References for measurement methods and analytical techniques (e.g., Golterman et al.; Murphy & Riley; Wetzel & Likens) and related monitoring reports and compilations.
- Additional information and historical context available in related Hydrobiologia issues and Scottish Natural Heritage reports.

## Practical notes for data use

- Temporal coverage from 1968 onward; two long-term sampling sites with periodic gaps due to weather or logistics.
- Rich dataset including lake chemistry, water quality, weather context, and detailed crustacean/zooplankton community data.
- Useful for dashboards, self-serve data exploration, trend analyses, and cross-site comparisons; requires attention to unit conventions and updated column naming when merging with older records.