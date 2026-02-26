# The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport

- Study aim and context
  - Assess the effects of street lighting on moths and nocturnal pollen transport.
  - Location: 20 lit/unlit site pairs within 40 km of Wallingford, Oxfordshire, UK.
  - Period: May–September 2014; results linked to a Global Change Biology paper (in press).

- Experimental design and site pairing
  - 20 lit sites paired with hedgerow sections serving as unlit controls.
  - Lit sites required adjacent high-pressure sodium street lights; unlit sites >100 m from any street lights.
  - Within-pair distance: mean 207 m (range 120–330 m); between-pair nearest neighbor distance ~6 km.
  - Matching criteria covered road, verge/hedge, and field characteristics to control for habitat variables.

- Sampling regime and methods
  - Sampling windows divided into three six-week periods: spring, early summer, late summer.
  - Weather criteria for sampling: dry conditions, wind ≤ Beaufort 3, minimum temperature ≥ 12°C.
  - Methods conducted at each site pair:
    - Night-time transects: 25 m transects with lit/unlit halves; three repeats per visit; red-filtered floodlight to reduce moth disturbance.
    - Overhead flight-activity surveys: counts (1 minute per replicate) with a bright torch to quantify higher-altitude activity.
    - Light-traps: Heath-style traps with 8 W actinic bulbs; operated ~8 hours from dusk; separate nights for transects and traps to avoid interference.
  - Sampling timing: transects and overhead surveys on the same night; traps on a separate night; all pairs observed per season when feasible.

- Light and environmental measurements
  - Light intensity measured at lit site centers using a CEM DT-1300 lux meter.
  - Unlit sites recorded 0 lux; lit sites had a median around 2.3 lux (range 0.2–12.1 lux).

- Data collection and structure
  - Four spreadsheets (F1–F4) capturing complementary data:
    - F1_sites.csv: site-level metadata per pair (Site_Number, Site_Name, Lit_Site_Grid_Ref, Hedge_Height, Lamp_Height, Margin_Width, Crop, Distances to habitation and to unlit site, number of nearby lights, light meter lux).
    - F2_moths.csv: individual moth records (Date, Site, Method, Treatment [Lit/Unlit], Reference, BinomialName, EnglishName, Family, Group [Macro/Micro]).
    - F3_overhead.csv: overhead survey counts (Date, Site, Treatment, FirstCount, SecondCount, ThirdCount).
    - F4_pollen.csv: pollen data on proboscises (MothReference linked to F2; BinomialName; 28 morphotypes with counts across columns, plus taxonomic notes).
  - Pollen analysis: moths euthanized and pollen swabbed from proboscides using fuchsin jelly; slides examined at 400x; morphotypes identified via standard pollen keys and local reference collections.
  - Data linkage: moth records connect to site and pollen data via moth/moth reference identifiers.

- Key variables and measurements
  - Habitat and site variables: hedge height, hedge/field-margin widths, crop type, distance to habitation, distance between lit and unlit sites, and proximity to other lights.
  - Light exposure: lux readings at lit sites; explicit separation of lit vs unlit treatments.
  - Moth data: species identification (BinomialName, EnglishName, Family), body-size grouping (Macro/Micro), sampling method (Transect vs Trap), and treatment (Lit vs Unlit).
  - Flight activity: counts from overhead surveys across three replicates.
  - Pollen transport: per-moth morphotype counts across 28 morphotypes, enabling analysis of floral sources via proboscis pollen loads.

- Analytical potential and scope for analysts
  - Compare moth abundance, species richness, and functional groups between lit and unlit sites across seasons and methods.
  - Assess whether street lighting alters nocturnal pollen transport by examining pollen load and morphotype diversity on moth proboscides.
  - Integrate habitat and light data to model drivers of moth activity and pollen transport disruption.
  - Use cross-file keys to link individual moth data with site characteristics and pollen outcomes for multivariate analyses.
  - Explore seasonal dynamics (spring to late summer) and method-specific detectability.

- Limitations and considerations
  - Quality control not explicitly documented; some overhead counts may include non-moth insects.
  - Pollen analysis relies on morphotype identifications, which may group multiple species under single morphotypes.
  - Some data may be missing or limited by weather conditions affecting sampling across seasons.
  - Calibration steps are not detailed beyond standard equipment descriptions.

- Publication and data provenance
  - Dataset underpinning Macgregor, C.J.; Evans, D.M.; Fox, R.; Pocock, M.J.O. (in press) The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport. Global Change Biology.