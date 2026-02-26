# Description, Experimental Design and Collection

- What the data represent
  - Abundance of parasitoid wasps (parasitic wasps) collected from sticky traps in the center of Brassica napus plant groups under Free-Air Diesel and Ozone Enrichment (FADOE) rings.
  - Focus on two parasitoid groups: Diaeretiella rapae and others.
  - Data collected across two years (Year) and multiple experimental rings (Ring).

- Experimental design
  - Field setup: FADOE rings located in a field of wheat in 2018 (then moved to an adjacent field in 2019).
  - Pollution treatments (Pollutant): diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and a control (CON; natural air).
  - Aphid treatments (Treatment): 50 aphids, 10 aphids, or no aphids inoculated on plants.
  - Replication and runs (Run): one sticky trap placed per ring within groups of plants during three runs (first: 4 plants, second: 7 plants, third: 4 plants); experiments repeated over two years (total of three runs).
  - Trap collection: sticky traps collected at seven weeks, frozen at -20 °C, replaced with new traps; a second collection occurred one week later.
  - Identification: parasitoids identified under a microscope and categorized as Diaeretiella rapae or other.

- Data structure and key variables
  - Year ( Year, Column A )
  - Ring ( Ring, Column B )
  - Pollutant ( Pollutant, Column C )
  - Treatment ( Treatment, Column D )
  - Run ( Run, Column E )
  - D_rapae_counts ( D_rapae_counts, Column F )
  - Others_counts ( Others_counts, Column G )
  - Percentage_D_rapae ( Percentage_D_rapae, Column H ) – share of total parasitoids that were D. rapae
  - Notes: Parasitoid counts and percentage values are pooled across weeks 7 and 8 for each Treatment per Ring per Year.

- Location and timing details
  - Field location: brassica and wheat field locations with specified coordinates for 2018 and 2019.
  - Ring movement: rings moved to an adjacent field in 2019.
  - Measurement window: two-year study with three experimental runs.

- Data quality and reference methodology
  - Quality control measures and full FADOE configuration are described in the cited methodology reference (Ryalls et al. 2022, Environmental Pollution).
  - Parasitoids identified and counted under microscopy; data are organized to enable comparison across pollutant treatments, aphid treatments, runs, and years.

- Potential data products and analyses for data support
  - Dashboards or pivot tables enabling self-serve exploration by Year, Ring, Pollutant, Treatment, and Run.
  - Summary tables of D. rapae counts, other parasitoids, and the percentage of D. rapae per treatment and year.
  - Cross-condition analyses to assess how air pollutants and aphid infestation influence parasitoid abundance and composition.
  - Data integration opportunities with environmental exposure or plant health metrics, using the Ring and Year dimensions.

- Practical considerations for data use
  - Counts are per trap and require aggregation to compare across rings or years (e.g., totals or means per treatment).
  - The data are pooled across two collection weeks within each Year-Treatment-Ring combination.
  - Ensure alignment with the original experimental design when interpreting treatment effects and interactions (Pollutant × Treatment × Run).