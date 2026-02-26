# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm environmental and phenological data derived from fixed-point repeat photography, 2002-2019

- Overview
  - Fixed-point repeat photography dataset capturing environmental and phenological timing.
  - Covers snow events (timing and duration) and phenology of invertebrates and plants (spittlebug spittlemass, heather flowering, Scots pine leaf-flush).
  - Snow data: 2002–2019 (17 years); invertebrate/plant phenology: 2010–2019 (10 years).
  - Aims to enhance understanding of ecosystem response to climate change; methodology documented in Andrews & Dick (2020).

- Location and site
  - Cairngorms National Park, Scotland: north slopes of Sgoran Dubh Mor (1111 m) and north-northeast slopes of Meall Bhuidhe (960 m) and Geal Charn (920 m).
  - Allt a’Mharcaidh catchment, Invereshie and Inshriach National Nature Reserve.
  - Elevation range 450–1111 m, foreground dry heath dominated by heather and regenerating Scots pine.

- Camera system
  - Mark I (2002–2009): single daily midday photograph using Olympus C860, timer, weatherproof housing.
  - Mark II (from 2009): three daily images (09:00, 11:00, 13:00) using a dedicated time-lapse package with Pentax K200D, 35 mm lens, DigiSnap controller; solar-powered for continuous operation.
  - Transition increased image availability and reduced occlusion by weather.

- Detectable events and measurement methods
  - Snow timing and duration
    - Snow_form: date of first persistent snow.
    - Snow_melt: date when persistent snow melts.
    - Snow_period: duration in days between form and melt.
    - Bridging data: weekly manual photos used when automatic system obscured by weather or failed; melt date between weekly images estimated with ±3–4 day error.
  - Heather flowering phenology
    - Pixel colour counting on cropped foreground area (1200x500 px) to identify pink/purple flowering pixels.
    - Flowering onset/end constrained by at least 20% of maximum yearly colour count to reduce false positives.
    - Flowering curve modeled with GAM; mid-flowering date = 50th percentile; peak duration = 25th–75th percentile.
  - Spittlebug phenology
    - Spittlemass onset when two masses visible in a single image (to avoid outliers).
    - Peak date = date with highest count of spittle masses.
    - Spittlemass duration = between first and last observable spittle masses.
  - Scots Pine leaf-flush phenology
    - Focus on candle development (new needles); also records of candle appearance and leaf flush, with browning noted.
    - Caveat: leaf-flush dates reflect both budburst and subsequent growth rate; comparisons to budburst-only studies should be cautious.

- Data structure and units
  - Long-format CSV
  - Columns: Winter (YYYY/YY), Winter_YearEnd (YYYY), Event (text), Unit (Day_of_Year or Days), Value (numeric).
  - Example events: Snow_form, Snow_melt, Snow_period; Heather_flowering_Peak_Onset/End/Duration; Spittles_start/Peak/End/Duration; Pine_candles_appear/Flush/Browning.

- Quality control
  - Out-of-range value checks.
  - Validation of the pixel-count method for Heather flowering against manual records.
  - Documentation references (see Sources) for detailed QC procedures.

- References (for methods and context)
  - Andrews, C., Ives, S., Dick, J. (2016). Long-term observations of increasing snow cover in the western Cairngorms.
  - Andrews, C., Dick, J. (2020). Utilising repeat photography for long-term monitoring at the Cairngorm Environmental Change Network site: data analysis report.
  - Weller, H. (2019). Countcolors: R package for color-based pixel counting.