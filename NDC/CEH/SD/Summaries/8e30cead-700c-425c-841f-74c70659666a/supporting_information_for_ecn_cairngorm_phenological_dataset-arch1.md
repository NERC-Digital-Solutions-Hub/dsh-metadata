# Supporting information for the dataset:
UK Environmental Change Network (ECN) Cairngorm environmental and phenological data derived from fixed-point repeat photography, 2002-2019.

- Purpose and scope
  - Provides supporting documentation for fixed-point repeat photography-derived phenological data from the Cairngorms ECN site.
  - Tracks timing of snow events and phenological events: Spittlebug spittlemass, heather flowering, and Scots pine leaf-flush.
  - Time coverage: snow events (2002-2019, 17 years); invertebrate and plant events (2010-2019, 10 years).
  - Related methods are detailed in Andrews and Dick (2020); further information in Andrews et al. (2016).

- Location
  - Site: Allt a’Mharcaidh catchment, Invereshie and Inshriach National Nature Reserve, Cairngorms National Park, Scotland.
  - Targeted hillslopes: north slopes of Sgoran Dubh Mor (~1111 m), north-north-east slopes of Meall Bhuidhe (960 m) and Geal Charn (920 m).
  - Elevation range across the visible hillslope: ~450–1111 m above sea level.
  - Dominant foreground habitat: dry heath with heather and regenerating Scots pine.

- Camera system
  - Mark I (2002–2009): single daily midday photo using Olympus C860; weatherproof housing and shutter solenoid.
  - Mark II (from 05 Sep 2009): three daily images (09:00, 11:00, 13:00) using a custom time-lapse package with a Pentax K200D, 18-55 mm lens, DigiSnap 2100 controller, in waterproof housing with a 5 W solar panel.

- Detectable events and data streams
  - Snow events
    - Snow_form: date of first persistent snow
    - Snow_melt: date snow persists until melt in spring
    - Snow_period: duration (days) between form and melt
    - Gaps/bridging: manual weekly photos used to bridge gaps due to weather or system failures; melt-date estimates may have ±3–4 day error when inferred from remnant patches.
  - Heather flowering (Calluna vulgaris)
    - Method: pixel colour counting on cropped foreground, using RGB range to identify pink/purple hues; proportion of coloured pixels relative to background used to build flowering curves.
    - Flowering dates derived by applying a GAM to flowering curve; mid-flowering date = 50th percentile; peak duration = 25th–75th percentile span.
    - Threshold to reduce false positives: flowering considered started/ended when daily colour count ≥20% of the year’s maximum.
  - Spittlebug (Philaenus spumarius) phenology
    - Spittles_start: date of first observable spittlemass (requires two masses in a single image for reliability)
    - Spittles_peak: date with the highest count of spittlemasses
    - Spittles_end: end of spittlemass presence
    - Spittles_duration: duration between start and end (days)
  - Scots Pine (Pinus sylvestris) leaf-flush phenology
    - Focus on the first identifiable “candles” and subsequent leaf flushing; note that leaf flush integrates budburst timing and growth rate
    - Pine_candles_appear: date of first identifiable pine candles
    - Pine_candles_flush: date of first leaf flushing
    - Pine_leaves_browning: earliest date of leaf browning
  - Data format
    - Long-format CSV with columns: Winter, Winter_YearEnd, Event, Unit, Value
    - Winter uses a YYYY/YY format; Winter_YearEnd is the year the winter ends (for snow)
    - Event contains the specific metric (e.g., Snow_form, Heather_flowering_Peak_Onset, Spittles_start, Pine_candles_flush)
    - Unit indicates Day_of_Year or days; Value provides the numeric date or duration

- Data structure, units, and processing methods
  - Data organization: long-format CSV with clear event naming, units, and values
  - Heather flowering processing: image cropping (1200x500 px from bottom-left), color quantization to 256 colors; pink/purple pixels counted with CountColors in R; flowering curve fitted with GAM
  - Snow data handling: first persistent snow date and last visible snow date; snow duration calculated between these dates; when data gaps occurred, bridging from weekly manual photos
  - Spittlebug and pine phenology: set rules to ensure robust detection (e.g., two spittlemasses required for start)

- Quality control and limitations
  - Range checks performed to identify outliers; validation of color-based flowering against manual records (Andrews and Dick, 2020)
  - Early snow camera (Mark I) had lower image quality, limiting some phenology observations to 2010 onward after Mark II deployment
  - Potential for false positives in color-based flowering during certain light/weather conditions; mitigated by requiring a minimum 20% of yearly maximum for onset/end
  - Data gaps due to obscuring weather, camera downtime, or data processing steps; bridging data with weekly photos helps but residual uncertainty remains, including ±3–4 day error on melt estimates

- Accessibility and references
  - Related data analysis report: Andrews and Dick (2020) – Utilising repeat photography for long-term monitoring at the Cairngorm Environmental Change Network site
  - Foundational methods: Andrews, Dick (2016); Countcolors R package (Weller, 2019) used for color detection
  - Primary data source and dataset context available via UK Centre for Ecology & Hydrology and NERC portals (eprint link provided in 2020 report)

- Purpose for analysts
  - Provides long-term, sensor-free phenological data derived from fixed-point photography to examine climate-driven ecological change
  - Enables correlation analyses between snow timing and plant/invertebrate phenology, with explicit documentation of methods, data structure, and uncertainties to support reproducible analyses.