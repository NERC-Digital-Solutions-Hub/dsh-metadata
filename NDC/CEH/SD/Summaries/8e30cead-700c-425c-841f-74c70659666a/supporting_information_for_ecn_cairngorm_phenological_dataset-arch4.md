# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm environmental and phenological data derived from fixed-point repeat photography, 2002-2019

## Overview
- Provides supporting documentation for the ECN Cairngorms fixed-point repeat photography dataset.
- Temporal coverage: snow events (2002-2019, 17 years) and invertebrate/plant phenology (2010-2019, 10 years).
- Data contribute to understanding ecosystem responses to climate change in the Cairngorms study area.
- Related methods and analyses are detailed in Andrews and Dick (2020) and Andrews et al. (2016); the 2020 report is available online.

## Location and study context
- Target area: north slopes of Sgoran Dubh Mor (1111 m), and north-northeast slopes of Meall Bhuidhe (960 m) and Geal Charn (920 m), Allt a'Mharcaidh catchment, Invereshie and Inshriach National Nature Reserve, Cairngorms National Park, Scotland.
- Elevation range visible to the camera: ~450 m to 1111 m above sea level.
- Foreground habitat: dry heath dominated by heather and regenerating Scots pine.

## Camera systems and data collection
- Two fixed-point repeat photography setups used from 2002 to present:
  - Mark I (2002–2009): one daily image at midday using an Olympus C860, with timer and weatherproof housing.
  - Mark II (from 2009): a custom time-lapse system with Pentax K200D DSLR, 35 mm equivalent lens, DigiSnap controller, waterproof housing and solar power; captures three images daily (09:00, 11:00, 13:00).
- When weather or equipment blocked automatic images, weekly manual photos provided bridging data for snow conditions.
- Some phenological data (spittlemass, pine leaf-flush, heather flowering) start date 2010 onwards due to improved image quality with Mark II.

## Detectable events and their definitions
- Snow presence and duration
  - Snow_form: first date of persistent snow
  - Snow_melt: last date of visible snow before spring melt
  - Snow_period: duration between form and melt (days)
  - Note: bridging data from weekly photos when gaps occurred; melt day estimation can have ±3–4 day error if based on image patches.
- Heather flowering phenology
  - Method: pixel color counting on cropped foreground (1200x500 pixels) from each image; identify pink/purple colors (approx RGB range [0.7, 0.1, 0.7] ±30%); flowering onset/offset determined from flowering curve (GAM) with thresholds to reduce false positives.
  - Peak flowering metrics:
    - Heather_flowering_Peak_Onset: start of peak flowering
    - Heather_flowering_Peak_end: end of peak flowering
    - Heather_flowering_Peak_duration: duration (days)
- Spittlebug (Philaenus spumarius) phenology
  - Spittles_start: date of first detectable spittlemass appearance (requires at least two visible masses in a single image)
  - Spittles_peak: date with the highest spittlemass count
  - Spittles_end: end date of presence
  - Spittles_duration: duration from start to end (days)
- Scots Pine (Pinus sylvestris) leaf-flush phenology
  - Pine_candles_appear: first identifiable pine candles
  - Pine_candles_flush: first leaf flushing
  - Pine_leaves_browning: earliest date of obvious leaf browning
  - Note: leaf flush reflects budburst plus subsequent growth rate; may not be directly comparable to budburst-only studies.

## Data structure and units
- Data are provided in a long-form CSV with the following columns:
  - Winter: time identifier for winter phenology (format: YYYY/YY, e.g., 2002/03)
  - Winter_YearEnd: year in which the winter period ends (e.g., 2002)
  - Event: name of the environmental/phenological event (e.g., Snow_form, Heather_flowering_Peak_Onset)
  - Unit: measurement unit (either days or day_of_year)
  - Value: numeric value for the event (day of year or days)

## Quality control and limitations
- Data screened for values outside expected ranges.
- Heather flowering color-count method validated against manual observations (See Andrews and Dick 2020 for details).
- Potential limitations to consider:
  - Subjectivity in some manual determinations, especially when image quality varies.
  - False positives in flowering detection due to light and weather conditions; mitigated by thresholding (minimum 20% of maximum yearly pixel count).
  - Snow data gaps bridged by weekly photos; ±3–4 day error on certain melt dates.
  - Changes in camera system (Mark I to Mark II) improved temporal resolution and data quality for some events.

## References
- Andrews, C., Ives, S., Dick, J. (2016). Long-term observations of increasing snow cover in the western Cairngorms. Weather, 71(7), 178-181.
- Andrews, C., Dick, J. (2020). Utilising repeat photography for long-term monitoring at the Cairngorm Environmental Change Network site: data analysis report. Edinburgh: UK Centre for Ecology & Hydrology, 34pp. UKCEH Project no. 06953.
- Weller, H. (2019). Countcolors: Locates and Counts Pixels Within Color Range(s) in Images. R package version 0.9.1.