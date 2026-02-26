# Description, Experimental Design and Collection

- Purpose: Describe an dataset documenting the abundance of parasitoid wasps (Diaeretiella rapae and others) collected from sticky traps placed among Brassica napus plants under Free-Air Diesel and Ozone Enrichment (FADOE) treatments.

- Spatial and temporal scope:
  - Collected over two years (Year 1 and Year 2).
  - FADOE rings distributed within a field of wheat in 2018 (field location: latitude 51.482853, longitude -0.897749) and moved to an adjacent field in 2019 (latitude 51.482374, longitude -0.895855).

- Experimental treatments:
  - Pollutant treatments (Column C): diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control (CON; natural air).
  - Aphid inoculation treatments (Column D): 50 aphids, 10 aphids, or no aphids.
  - Each FADOE ring was assigned to one pollutant treatment; aphid inoculation varied by Ring.

- Experimental design and replication:
  - Three experimental runs across the two years (Run 1, Run 2, Run 3).
  - One sticky trap per Ring per Run.
  - Plant group sizes around each trap varied by Run: Run 1 surrounded by 4 plants, Run 2 by 7 plants, Run 3 by 4 plants (replicates per Run).

- Sampling procedure:
  - Sticky traps collected when plants were seven weeks old; traps frozen at -20 °C.
  - After one week, a second set of sticky traps collected and frozen (-20 °C).
  - Parasitoids identified under a microscope and classified into two groups: Diaeretiella rapae (D_rapae) and others (Others).

- Data structure and variables (Columns):
  - Year (A): sampling year.
  - Ring (B): FADOE ring identifier.
  - Pollutant (C): treatment type (D, O3, D+O3, CON).
  - Treatment (D): aphid inoculation level (50 aphids, 10 aphids, or none).
  - Run (E): experimental run (1, 2, or 3).
  - D_rapae_counts (F): count of D. rapae parasitoids per trap.
  - Others_counts (G): count of other parasitoid species per trap.
  - Percentage_D_rapae (H): percentage of total parasitoids identified as D. rapae.

- Data processing notes:
  - Parasitoid counts from weeks seven and eight were pooled for each combination of Treatment, Ring, and Year.
  - Percentage_D_rapae computed as the share of D. rapae among total counted parasitoids.

- Identification and quality control:
  - Parasitoids identified and counted using microscopy.
  - Full FADOE configuration and quality control details are described in the referenced methodology ( Ryalls et al., 2022 ).

- Reference:
  - Ryalls, J.M.W., Langford, B., Mullinger, N.J., Bromfield, L.M., Nemitz, E., Pfrang, C. & Girling, R.D. 2022. Anthropogenic air pollutants reduce insect-mediated pollination services. Environmental Pollution 297, 118847. (doi:10.1016/j.envpol.2022.118847).

- GIS relevance and applications:
  - Enables map-based visualization of parasitoid abundances by Ring, Year, Pollutant, and Aphid treatment.
  - Suitable for spatial analyses of how air pollutant exposures relate to D. rapae prevalence.
  - Geolocational context (two fields with precise coordinates and ring relocation between years) supports spatial trend analysis and field-level management insights.