# The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport

- Overview of the dataset
  - Details moths captured at paired lit and unlit sites near Wallingford, Oxfordshire, UK, during May–September 2014.
  - Three sampling methods used: night-time transects, light-trapping, and overhead flight-activity surveys.
  - Pollen sampled from the proboscides of captured moths to assess nocturnal pollen transport.
  - Dataset is complete; analysis published (in press) in Global Change Biology.

- Experimental design and sampling regime
  - 20 lit site pairs, each lit site paired with a nearby hedgerow (unlit site) to control habitat variables.
  - Lit sites feature at least one nearby high-pressure sodium street light; unlit sites are >100 m from any street light.
  - Within-pair distance: mean 207 m (range 120–330 m); between-pair nearest-neighbour distance: mean 6.0 km (range 2.2–14.0 km).
  - Habitat and site characteristics matched across pairs (road orientation/width, verge/field margin, hedge, crop type, etc.).
  - Sampling periods: spring, early summer, late summer; weather criteria required (dry, wind ≤ Beaufort 3, temp ≥ 12°C).
  - Each pair sampled once per method per season; transects and overhead surveys on the same night; light-traps on a separate night.
  - Weather and practical constraints limited replication (e.g., six pairs sampled per method in spring).

- Data collection methods and instruments
  - Night-time transects
    - 25 m transects with a street light at the lit transect midpoint; red-filtered floodlight to reduce moth attraction.
    - Moths sampled for a total of 1 minute per 5 m section, in three replicates per night (lit and unlit transects alternated).
  - Overhead flight-activity surveys
    - 1-minute counts of moths flying 3–12 m above ground, using a bright LED torch at transect midpoint; counts repeated three times per session.
  - Light-traps
    - Heath-style traps with 8 W actinic bulbs; traps deployed at lit and unlit sites, active ~8 hours overnight; traps rotated between lit and unlit sites across nights.

- Data structure and file specifics
  - F1_sites.csv - site data
    - Key fields include: Site_Number, Site_Name, Lit_Site_Grid_Ref, Hedge_Height_m, Lamp_Height_m, Margin_Width_m, Crop, Distance_Lit_site_To_Habitation_m, Distance_Lit_to_Unlit_site_m, Distance_to_Nearest_Extrapair_Neighbour_Site_km, Number_of_lights_within_100m, Lit_site_Light_Meter_reading_lux.
  - F2_moths.csv - moth data
    - Each row: Date, Site, Method (Transect or Trap), Treatment (Lit or Unlit), Reference, BinomialName, EnglishName, Family, Group (Macro or Micro).
  - F3_overhead.csv - overhead flight-activity data
    - Each row: Date, Site, Treatment, FirstCount, SecondCount, ThirdCount.
  - F4_pollen.csv - pollen data
    - Each row links to a moth (MothReference) and includes BinomialName; counts for 28 morphotypes (columns labeled for each morphotype) representing pollen grains found on the moth proboscis.
  - Pollen analysis notes
    - Pollen swabbed from proboscides after relaxing the moths; slides prepared and morphotyped using standard references; morphotypes may group multiple species when resolution is limited.
  - Light intensity measurements
    - Night-time light levels recorded with lux meter for lit and unlit sites (0 lux at unlit sites; median ~2.3 lux at lit sites).

- Pollen transport and processing
  - All retained moths examined for pollen between Nov 2014 and Mar 2015.
  - Pollen collected via fuchsin jelly swabs from proboscises only.
  - Morphotyped pollen identified using established keys and local reference materials; some morphotypes remain at higher taxonomic levels due to identification limits.

- Data quality, limitations, and considerations for reuse
  - Moth captures per site per night are relatively low (median 6; range 0–26), with 46 paired observations per method across seasons.
  - Weather and methodological constraints led to incomplete replication across all pairs and periods for each method.
  - Pollen morphotype identifications are morphological groupings and may not resolve to species for all morphotypes.
  - The dataset provides a rich, multi-method view of light-attraction effects and nocturnal pollen transport, suitable for analyses of lighting impact, moth activity patterns, and pollination networks linked to nocturnal visitors.

- Provenance and references
  - Original dataset described in Macgregor, C.J., Evans, D.M., Fox, R. and Pocock, M.J.O. (in press) The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport. Global Change Biology.
  - Data files named F1–F4 correspond to site, moth, overhead, and pollen data respectively.