# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm environmental and phenological data derived from fixed-point repeat photography, 2002-2019.

## Overview
- Documents support for the ECN Cairngorms fixed-point repeat photography dataset.
- Captures timing of snow events and phenological events: Spittlebug spittlemass, heather flowering, Scots pine leaf-flush.
- Temporal coverage: snow/events 2002–2019 (snow 17 years; invertebrate/plant 2010–2019).
- Aids understanding of ecosystem responses to climate change; methods detailed in Andrews and Dick (2020).

## Location and site
- Study area: Allt a’Mharcaidh catchment, Cairngorms National Park, Scotland.
- Targeted slopes: north slopes of Sgoran Dubh Mor (1111 m), NNE slopes of Meall Bhuidhe (960 m), Geal Charn (920 m).
- Coordinates: 57° 6' 28" N, 3° 50' 6" W.
- Elevation range in the visible hillslope: 450–1111 m a.s.l.
- Foreground habitat: dry heath with heather (Calluna vulgaris) and regenerating Scots pine (Pinus sylvestris).

## Data collection and camera system
- Two fixed-point camera systems used since 2002-11-13.
  - Mark I: single daily midday photo.
  - Mark II (from 2009-09-05): time-lapse package with three daily images (09:00, 11:00, 13:00) via solar-powered setup.
- Data gaps bridged with weekly manual photographs when needed.
- Image quality limitations: earlier snow data (Mark I) with lower quality; some phenology data (spittlemass, pine leaf-flush) limited to 2010 onward after Mark II installation.
- Image processing and analysis conducted to extract event timings (see Event-specific sections).

## Detectable events and variables
- Snow presence and duration
  - Snow_form: date of first persistent snow.
  - Snow_melt: date snow persists no longer into spring.
  - Snow_period: duration between form and melt (days).
  - Data gaps bridged with weekly photographs; melt date may have ±3–4 day error when estimated between weekly images.
- Heather flowering phenology
  - Pixel-based color counting on cropped foreground (1200×500 px, bottom-left origin) using colour range around pink/purple.
  - To reduce false positives, flowering considered present when pixel count ≥ 20% of yearly maximum.
  - Fitted flowering curve with GAM; mid-flowering date = 50th percentile; peak duration = 25th–75th percentile.
  - Events: Heather_flowering_Peak_Onset, Heather_flowering_Peak_end, Heather_flowering_Peak_duration.
- Spittlebug (Philaenus sp.) phenology
  - First spittlemass confirmed when two masses visible in a single image.
  - Peak spittlemass date (highest count), end date, and duration between start and end.
  - Events: Spittles_start, Spittles_peak, Spittles_end, Spittles_duration.
- Scots Pine leaf-flush phenology
  - Robustest indicator is pine candle emergence (new needles away from growth stem).
  - Also captured: candle appearance, candles flush, and leaf browning.
  - Cautions: leaf-flush integrates budburst and subsequent growth; may not be directly comparable to budburst-only studies.
  - Events: Pine_candles_appear, Pine_candles_flush, Pine_leaves_browning.

## Data structure, units, and format
- Format: long-format CSV.
- Key columns:
  - Winter: time identifier for winter period (format: YYYY/YY, e.g., 2002/03).
  - Winter_YearEnd: year when the winter ends (e.g., 2002).
  - Event: name of the environmental/phenological event (text).
  - Unit: measurement unit ('days' or 'day_of_year').
  - Value: numeric value (day of year or number of days).
- Event naming conventions:
  - Snow_form, Snow_melt, Snow_period
  - Heather_flowering_Peak_Onset, Peak_end, Peak_duration
  - Spittles_start, Spittles_peak, Spittles_end, Spittles_duration
  - Pine_candles_appear, Pine_candles_flush, Pine_leaves_browning

## Quality control and validation
- Data checked for values outside expected ranges.
- Heather flowering color-count method validated against manual observations (see Andrews & Dick 2020).
- Additional methodological details available in Andrews et al. (2016) and Andrews & Dick (2020).

## References and further reading
- Andrews, C., Ives, S., Dick, J. (2016). Long-term observations of increasing snow cover in the western Cairngorms. Weather, 71(7):178-181.
- Andrews, C., Dick, J. (2020). Utilising repeat photography for long-term monitoring at the Cairngorm Environmental Change Network site: data analysis report. UK Centre for Ecology & Hydrology.
- Weller, H. (2019). Countcolors: Locates and Counts Pixels Within Color Range(s) in Images. R package.