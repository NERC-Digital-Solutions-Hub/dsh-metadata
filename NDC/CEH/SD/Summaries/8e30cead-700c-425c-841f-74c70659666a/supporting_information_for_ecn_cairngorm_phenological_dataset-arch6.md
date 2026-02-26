# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm environmental and phenological data derived from fixed-point repeat photography, 2002-2019

## Overview
- Provides supporting documentation for a fixed-point repeat photography dataset capturing environmental and phenological events in the Cairngorms.
- Covers snow timing (start, end, duration) across 2002–2019 (17 years) and invertebrate/plant phenology (2010–2019, 10 years), contributing to understanding ecosystem responses to climate change.
- Methods and quality checks draw on Andrews and Dick (2020) with additional details in Andrews et al. (2016).

## Location and site
- Site: Allt a’Mhárcaidh catchment, Cairngorms National Park, Scotland.
- Targeted area: north slopes of Sgoran Dubh Mor (1111 m) and Meall Bhuidhe (960 m) and Geal Charn (920 m).
- Habitat: dry heath foreground with heather (Calluna vulgaris) and regenerating Scots pine (Pinus sylvestris).

## Camera system and data collection
- Two fixed-point systems in use since 13 November 2002:
  - Mark I (2002–2009): single daily midday photo (Olympus C860) with timer and shutter solenoid.
  - Mark II (from 5 September 2009 onward): time-lapse package (Habortronics) with Pentax DSLR, 3 daily images (09:00, 11:00, 13:00), solar-powered.
- Data bridging: when automated images were obscured or failed, weekly manual photos provided bridging data for snow conditions.
- Clear event definitions and data extraction depend on image quality, with higher resolution data available from the Mark II system.

## Detectable events and methods
- Snow timing (2002–2019): start of persistent snow, end of persistent snow, and snow duration.
  - Persistent snow: first date of non-melting snow and last visible snow date in spring.
  - Snow duration: days between form and melt dates.
  - Handling gaps: bridging data from manual photographs; melt day estimated ±3–4 days if gaps occurred between weekly images.
  - Event names: Snow_form, Snow_melt, Snow_period.
- Heather flowering (Calluna vulgaris) phenology:
  - Objective: minimize subjectivity by color-based pixel counting rather than manual date assignment.
  - Image processing: crop foreground to 1200×500 px, convert to 256 colors; identify pink/purple pixels (RGB ~ [0.7, 0.1, 0.7] ±30%) using CountColors in R; compute colored-to-background pixel proportion.
  - Mitigations for false positives: flowering considered started/ended when pixel count ≥20% of yearly maximum.
  - Analysis: general additive model (GAM) to produce yearly flowering curves; mid-flowering date is the 50th percentile; peak duration is 25th–75th percentile.
  - Event names: Heather_flowering_Peak_Onset, Heather_flowering_Peak_end, Heather_flowering_Peak_duration.
- Spittlebug phenology (Philaenus spumarius):
  - Start of spittlemass: defined as first appearance visible as two spittle masses in a single image (to avoid overinterpretation).
  - Peak spittlemass: date with the highest observed count.
  - Duration: days between first and last observable spittlemass.
  - Event names: Spittles_start, Spittles_peak, Spittles_end, Spittles_duration.
- Scots Pine leaf-flush phenology:
  - Focus on robustly identifiable growth point (pine candles) and subsequent leaf flushing, with caution about comparing to budburst-only studies.
  - Additional events tracked: Pine_candles_appear, Pine_candles_flush, Pine_leaves_browning.
  - Event names: Pine_candles_appear, Pine_candles_flush, Pine_leaves_browning.

## Data structure and units
- Data format: long-format CSV.
- Key fields:
  - Winter: time identifier for winter phenology (format YYYY/YY, e.g., 2002/03).
  - Winter_YearEnd: year of occurrence/end of winter period (format YYYY, e.g., 2002).
  - Event: name of environmental or phenological event (text, e.g., Pine_candles_flush).
  - Unit: measurement unit ('days' or 'day_of_year').
  - Value: numeric value (day of year or number of days).
- Period coverage:
  - Snow data: 2002–2019 (17 winters).
  - Heather, spittlebug, and pine phenology: 2010–2019 (limited by camera capability for earlier years).

## Quality control
- Data checked for values outside expected ranges.
- Heather flowering color-count method cross-validated against manual recordings (details in Andrews and Dick 2020).

## Related references
- Andrews, C., Ives, S., Dick, J. (2016). Long-term observations of increasing snow cover in the western Cairngorms. Weather, 71(7):178-181.
- Andrews, C., Dick, J. (2020). Utilising repeat photography for long-term monitoring at the Cairngorm Environmental Change Network site: data analysis report. UK Centre for Ecology & Hydrology, 34pp. http://nora.nerc.ac.uk/id/eprint/529051/
- Weller, H. (2019). Countcolors: Locates and Counts Pixels Within Color Range(s) in Images. R package version 0.9.1. https://cran.r-project.org/web/packages/countcolors/countcolors.pdf