# Plant material

- Location and origin
  - Plant material vegetatively propagated from Lolium perenne (ryegrass) and Trifolium repens (white clover) from turf samples near Edinburgh, UK (Grid reference NT245642).
  - Plants from different parents were randomized between competition patterns and ozone treatments. Established as individual plants for ~8 weeks before creating monocultures and mixtures for ozone exposure.

- Experimental design
  - Pots: large containers (35.5 cm x 45 cm x 25 cm) with drainage holes, lined to prevent root escape, filled with multipurpose compost.
  - Plant arrangement: each pot contained 12 plants in an even layout—four central Trifolium repens surrounded by eight Lolium perenne.
  - Treatments: three pots for each Lolium monoculture, Trifolium monoculture, and Lolium-Trifolium mixture, randomly allocated to four solardomes.
  - Timeline: exposure to ozone for 12 weeks starting 26 July 2002, with harvests on 6 September (intermediate) and 16 October (final).
  - Watering: well-watered via mist irrigation, with additional hand watering during warm periods.

- Ozone exposure
  - Four solardomes: two controls (ozone in charcoal-filtered air) and two with ozone exposure.
  - Ozone regimes:
    - O3(30): continuous 30 ppb in control domes.
    - O3(30+peaks): episodic rural ozone profile in the other two domes.
  - Concentration pattern: maximum 80 ppb on days 1 and 4; maximum 100 ppb on days 2 and 3.
  - Daily cycle: ozone increased from 30 ppb to daily maximum over 2 hours, held at max for 6 hours, then decreased to 30 ppb over 2 hours; otherwise 30 ppb.

- Visual assessments
  - Injury and senescence assessed visually at the pot level (plants grown together).
  - Classification: leaves categorized as injured or senesced if >25% of the leaf area showed the respective condition; otherwise healthy.
  - Senescence measurement in Lolium perenne: length of the senesced portion measured on a subsample of 20 leaves per pot, from leaf tip along the blade.

- Harvests and biomass
  - Harvests: two harvests after ozone exposure—6 September (6 weeks) and 16 October (12 weeks).
  - Height and layering: plants cut to 7 cm; material harvested in layers—outside the pot, >14 cm above soil, 7–14 cm above soil; after final harvest an additional layer 0–7 cm above soil was included.
  - Processing: plant material sorted by species and health status at harvest; dried at 65°C for at least 4 days to determine biomass.

- Stomatal conductance and chlorophyll measurements
  - Stomatal conductance: measured on Trifolium repens using a porometer (Delta-T AP4) under stable weather after 10–11 weeks of exposure; measurements in upper (sunlit) and inner (shaded) canopy positions; six leaves per pot (two leaves per canopy position).
  - Chlorophyll content: measured with a SPAD meter (chlorophyll a + b) after 1 and 10 weeks; calibration against acetone extraction following Lichtenthaler and Wellburn (1983) to derive chlorophyll content in mg g−1 fresh weight using:
    - Chlorophyll content = (chlorophyll index × 30.448) + 417
  - Calibration context: typical leaves used; some ozone injury present.

- Data analysis
  - Data aggregation: values averaged per solardome before analysis; injury and senescence data arcsine-transformed.
  - Statistical tests:
    - Stomatal conductance: one-way ANOVA (Minitab).
    - Other comparisons: split-plot or split-split-plot ANOVA (Genstat 8).
  - Experimental factors: ozone treatment (main plot), monoculture/mixture (sub-plot), canopy position (sub-sub-plot where applicable).

- Data structure and accessibility
  - Data file: Lolium_and_Trifolium_solardomes_Injury_data.csv
  - Size: 24 rows, 7 columns
  - Columns: Harvest, Species, Monoculture or mixture, part of canopy, Ozone treatment, % leaves that were injured or senesced, standard error.

- Relevance for GIS and map-based data products
  - Provides a structured layout of experimental plots and treatments that could be mapped conceptually (central vs. surrounding species, canopy positions, and ozone exposure zones).
  - Location data (grid reference) enables potential geospatial tagging if integrated with plot-level coordinates; data are primarily time-series and treatment-based measurements rather than geospatial observations.
  - Data quality notes: precise instrumentation and calibration details (porometer, SPAD, chlorophyll calibration) support reproducibility and metadata for GIS-ready datasets.
  - Suitable for creating visualizations of treatment effects across spatially organized plots and for comparative mapping of physiological responses (stomatal conductance, chlorophyll content, injury) under different ozone regimes.