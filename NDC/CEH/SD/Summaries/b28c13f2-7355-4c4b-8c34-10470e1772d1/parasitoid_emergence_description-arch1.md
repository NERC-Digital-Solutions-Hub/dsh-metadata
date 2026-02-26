# Description, Experimental Design and Collection

- Objective: Quantify the abundance of parasitoids (Diaretiella rapae) emerging from cabbage aphids (Brevicoryne brassicae) on Brassica napus plants under different air pollution treatments, to examine potential effects of pollutants on parasitoid-mediated interactions.

- Experimental setup
  - FADOE rings placed in a field of wheat in 2018 and moved to an adjacent field in 2019.
  - Pollutant treatments: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and a natural air control (CON); two rings assigned to each treatment.
  - OPEN treatment: five-week-old plants inoculated with 10 B. brassicae aphids and netted; nets later removed for one week to allow parasitoid activity, then re-netted with a sticky trap inside each net to capture emerging parasitoids.
  - Sampling: sticky traps collected 10 days after trap placement to count parasitoids emerged.
  - Parasitoid focus: Diaretiella rapae, the dominant parasitoid species parasitizing B. brassicae in this setup.

- Experimental runs and replication
  - Three experimental runs across two years.
  - Replication per run: 4, 7, and 4 replicate plants in the first, second, and third runs, respectively.
  - Ring-level replication: two rings per pollutant treatment per year (total design spread across the two fields and two years).

- Data structure (columns)
  - Year
  - Ring
  - Pollutant (D, O3, D+O3, CON)
  - Treatment (OPEN)
  - Plant_ID
  - Run
  - Parasitoids_emerged (count of Diaretiella rapae)

- Location and provenance
  - Field coordinates provided for 2018 (latitude 51.482853, longitude -0.897749) and 2019 (latitude 51.482374, longitude -0.895855).
  - Full methodological details and quality controls described in the referenced FADOE configuration study.

- Data interpretation considerations
  - Only Diaretiella rapae was found in abundance; other parasitoid species were not reported at meaningful levels.
  - The dataset is designed to support analyses of correlations between pollutant exposure and parasitoid emergence, as well as predictive modelling of pollutant effects on biological control dynamics, with careful attention to multi-year and multi-ring structure.