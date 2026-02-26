# Abstract

- The dataset comes from Loch Leven’s long-term monitoring programme in Scotland, UK, collected as part of UK-SCAPE WP7 LEVEN; sampling began in 1968 and continues.
- Collected and processed by NERC/CEH staff; data processing and output described in this document.
- Covers multiple determinands for lake chemistry, physical conditions, and crustacean zooplankton; includes sampling methods, lab analyses, data processing, and CSV output format.

## Sampling regime and sites

- Fortnightly sampling with two main sites per occasion: Harbour (Site_H), Reed Bower (Site_RB), and Sluices/Outflow (Site_L).
- Reed Bower accessible by boat; Sluices accessible by boat or shore; “Outlet” samples labeled as “Sluices” in dataset.
- Sampling can be disrupted by weather, ice, or resource constraints; extreme cases may result in only one or neither site being sampled.
- Site coordinates provided (UK National Grid); sites encoded in data by site IDs (H, RB/RB5, L/Sl8).

## Measurements, sampling, and analyses

- In situ measurements: conductivity, pH, temperature; Secchi depth measured at Reed Bower.
- Water samples collected as duplicates from each site; Reed Bower uses integrated column sampling; Sluices uses surface sampling.
- Laboratory analyses include soluble reactive phosphorus (SRP), total soluble phosphorus (TSP), total phosphorus (TP), soluble silica, total diatom silica, chlorophyll a; analyses follow established methods and storage protocols.
- Weather data recorded at Reed Bower when possible; wind force described via a Beaufort-based scale with a detailed lookup table.

## Crustacean & Zooplankton data

- Densities (ind/L) for a suite of zooplankton taxa (e.g., Daphnia, Eudiaptomus, Cyclopidae, Bosmina, Leptodora, Bythotrephes, Chydoridae, Polyphemus pediculus).
- Zero values indicate non-detection at sampling/analytical resolution; NAs indicate missing data.
- As of 2022, some column names updated for consistency; two new taxa added at dataset end (Ceriodaphnia sp., Polyphemus pediculus).
- RB sampling used a 4 m angled net (120 µm); L sampling used 30 L of surface water through a 120 µm net; preservation with 4% formaldehyde.
- Laboratory identification and counting performed on multiple sub-samples; counts converted to ind/L.

## Data processing

- An R-based import script processes data before database entry, with documented decisions.
- Wind force: when ranges appear (e.g., 4-5), the first value is used.
- Probe replicates (conductivity, pH, DO, and associated temperatures) are filtered using median absolute deviation (MAD); median/transformations applied for pH and related values; final values rounded (pH/DO to 2 dp; conductivity and temperatures to 1 dp).
- Inter-calibration: HQ30d to HQ4300 adjustment for the Hach probe to maintain consistency.
- Data undergo both automated and manual quality checks; unusual values investigated and corrected when appropriate.

## Format of stored data and metadata

- Data stored in a single CSV file; missing values marked as NA.
- Columns include site conditions, lake chemistry, and crustacean/zooplankton counts; units and sites indicated where relevant.
- Column descriptions provide detailed mapping of each determinand to site, date, week, depth, weather, and analytical results (e.g., conductivity, temperature, DO, pH, TP, SRP, TSP, chlorophyll, and zooplankton taxa).
- Core reference for column meanings is Table 3 (detailed descriptions of determinands, sites, and units).

## References and additional reading

- Method references for analyses (e.g., Murphy & Riley methods for phosphorus; Wetzel & Likens for digestion methods).
- Additional information and context available in related Hydrobiologia issues and Scottish Natural Heritage reports.
- 2022 dataset updates include terminology tweaks and addition of new taxa to the crustacean zooplankton dataset.