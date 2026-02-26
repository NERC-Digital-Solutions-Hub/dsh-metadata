# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm environmental and phenological data derived from fixed-point repeat photography, 2002-2019.

- Purpose and scope
  - Provides supporting documentation for a long-term fixed-point repeat photography dataset covering snow events and phenology (invertebrates and plants) in the Cairngorms.
  - Snow timing data cover 2002–2019 (17 years); invertebrate and plant phenology cover 2010–2019 (10 years).
  - Aims to improve understanding of ecosystem responses to climate change; method details are elaborated in Andrews and Dick (2020).

- Study site and camera setup
  - Location: north slopes of Sgoran Dubh Mor, Meall Bhuidhe, and Geal Charn, Allt a’Mharcaidh catchment, Invereshie and Inshriach NNR, Cairngorms National Park, Scotland.
  - Habitat: dry heath foreground with heather and regenerating Scots pine.
  - Camera systems:
    - Mark I (2002–2009): one daily image at midday using an Olympus C860; weatherproof housing with shutter timer.
    - Mark II (2009–present): three daily images (09:00, 11:00, 13:00) using a purpose-built time-lapse setup with a Pentax K200D, solar-powered controller.

- Detectable events and how they were derived
  - Snow presence and duration
    - Observed as persistent winter snow in images; dates recorded for first persistent snow and final melt in spring.
    - Snow_duration = days between first persistent snow and melt date.
    - When images were obscured or failed, bridging data from weekly manual photos were used; melt dates sometimes estimated from image patches with an ±3–4 day error.
  - Heather (Calluna vulgaris) flowering phenology
    - Used pixel color counting on cropped foreground area (1200×500 px) focusing on pink/purple tones; colors identified with CountColors in R.
    - To reduce false positives, flowering was flagged when daily pixel counts reached at least 20% of that year’s maximum.
    - Flowering curves per year were GAM-fitted; mid-flowering date = 50th percentile; peak duration = 25th to 75th percentile.
  - Spittlebug (Philaenus spumarius) phenology
    - Start when two spittle masses are visible in a single image; peak date is the date with the highest observed count; duration from first to last observation.
  - Scots pine (Pinus sylvestris) leaf-flush phenology
    - Focused on robust indicators: first appearance of the “candles” (new needles) and subsequent leaf flushing; also recorded leaf browning.
    - Data provide dates for Candle appearance, Candle flush, and Browning onset.

- Data structure and units
  - Long-format CSV with columns:
    - Winter (time identifier, format YYYY/YY)
    - Winter_YearEnd (year the winter ends, format YYYY)
    - Event (name of environmental/phenological event)
    - Unit (Day_of_Year or days)
    - Value (numeric; day of year or number of days)
  - Event names include Snow_form, Snow_melt, Snow_period; Heather_flowering_Peak_Onset/End/Duration; Spittles_start/peak/end/duration; Pine_candles_appear/flush; Pine_leaves_browning.

- Data quality, processing, and validation
  - Quality checks performed to identify out-of-range values.
  - Pixel-based flowering method validated against manual methods (details in Andrews & Dick 2020).
  - Bridging data from weekly site visits used to mitigate gaps due to weather or camera issues; acknowledged measurement uncertainties (e.g., ±3–4 days for melt dates).

- Related documentation and references
  - Andrews, C., Ives, S., Dick, J. (2016). Long-term observations of increasing snow cover in the western Cairngorms.
  - Andrews, C., Dick, J. (2020). Utilising repeat photography for long-term monitoring at the Cairngorm Environmental Change Network site: data analysis report.
  - Weller, H. (2019). Countcolors: R package for color-based pixel counting.

- Usage and context for monitoring frameworks
  - Demonstrates a structured approach to identifying and documenting environmental health indicators via fixed-point repeat photography.
  - Provides explicit event definitions, data transformation steps, and quality control measures essential for informing monitoring decisions and policy evaluation.
  - Highlights data gaps, bridging strategies, and potential limitations (e.g., image quality, ocean of data gaps, need for metadata to ensure reuse).