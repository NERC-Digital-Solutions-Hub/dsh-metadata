# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm environmental and phenological data derived from fixed-point repeat photography, 2002-2019.

- Purpose and scope
  - Documents supporting information for a dataset covering snow timing and various phenological events (invertebrate and plant) derived from fixed-point repeat photography in the Cairngorms.
  - Time coverage: snow 2002-2019; invertebrate and plant events 2010-2019.
  - Aims to enhance understanding of ecosystem responses to climate change in the study area.
  - Related methods report available (Andrews and Dick, 2020); additional methods details in Andrews et al. (2016).

- Study site and location
  - Allt a’Mharcaidh catchment, Cairngorms National Park, Scotland.
  - Targeted hillslopes: north slopes of Sgoran Dubh Mor, Meall Bhuidhe, and Geal Charn.
  - Elevation range from 450 m to 1111 m; foreground dry heath with heather and regenerating Scots pine.

- Data collection and camera systems
  - Two fixed-point repeat photography systems used since 2002:
    - Mark I (2002–2009): single daily image at midday with an Olympus C860.
    - Mark II (from 2009): time-lapse setup capturing three images daily (09:00, 11:00, 13:00) using a Pentax K200D and solar-powered controller.
  - Data continuity supported by weekly manual photographs when automated system data were missing or obscured.

- Detected events and definitions
  - Snow timing and duration
    - Snow_form: first persistent snow date (snow that remains until spring).
    - Snow_melt: last visible snow date in spring.
    - Snow_period: duration between form and melt (in days).
    - Data often bridged with manual weekly photos; melt day sometimes estimated if gaps occurred.
    - Error for melt estimation: ±3–4 days.
  - Heather (Calluna vulgaris) flowering phenology
    - Pixel color counting method applied to cropped foreground area (1200x500 px) to identify pink/purple tones.
    - Flowering onset/end defined when daily colored-pixel count ≥ 20% of year’s maximum to reduce false positives.
    - Flowering curve modelled with GAM; mid-flowering date is 50th percentile; peak duration is 25th–75th percentile spread.
  - Spittlebug phenology (Philaenus spumarius)
    - First spittlemass: defined when two spittlemasses are visible in a single image.
    - Peak spittlemass date: date with highest observed count.
    - Spittlemass duration: days between first and last appearance.
  - Scots Pine leaf-flush phenology
    - Focus on robust growth point (candles) and subsequent leaf flush.
    - Recorded events: Pine_candles_appear (first candles), Pine_candles_flush (first leaf flush), Pine_leaves_browning (earliest browning).

- Data structure and units
  - Data stored in a long-format CSV with fields:
    - Winter: time identifier for winter phenological periods (format YYYY/YY, e.g., 2002/03).
    - Winter_YearEnd: year the winter period ends (YYYY, e.g., 2002).
    - Event: name of the measured event (text).
    - Unit: measurement unit (either days or day_of_year).
    - Value: numeric value (day of year or number of days).

- Data processing and quality control
  - Quality checks for out-of-range values.
  - Heather flowering quantified via image processing; validated against manual records.
  - Documentation notes potential subjective elements in date assignments (e.g., snow melt) and steps taken to minimize bias (color thresholding, 20% criterion, GAM smoothing).
  - Where data gaps existed, bridging data from weekly manual photographs used to maintain continuity.

- Documentation, references, and further information
  - Key references:
    - Andrews, C., Ives, S., Dick, J. (2016). Long-term observations of increasing snow cover in the western Cairngorms. Weather.
    - Andrews, C., Dick, J. (2020). Utilising repeat photography for long-term monitoring at the Cairngorm Environmental Change Network site: data analysis report. UK Centre for Ecology & Hydrology.
    - Weller, H. (2019). Countcolors R package (for the pigment counting method).
  - Additional background and methods details available in the cited reports (notably Andrews & Dick, 2020) for deeper methodological understanding.

- Practical considerations and limitations
  - 2010 onward: improved data quality and capabilities with Mark II camera; earlier snow data (and some phenology) had lower image quality, affecting later event detection.
  - Potential false positives in color-based flowering detection due to light conditions; mitigated by thresholds and year-specific analysis.
  - Subjective estimation steps (e.g., melt day) introduce uncertainty (±3–4 days) acknowledged in the dataset.

- Usage notes for data stewards
  - Clear event naming conventions and units to support interoperability and discovery.
  - Long-format CSV structure facilitates integration with metadata-driven data catalogs.
  - Documentation of bridging procedures and uncertainty aids transparent reuse and replication.
  - Primary sources for deeper metadata and processing workflows: Andrews and Dick (2020) data analysis report and Andrews et al. (2016).