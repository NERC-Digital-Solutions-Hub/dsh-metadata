# Description, Experimental Design and Collection

## Data overview
- Represents the abundance of parasitic wasps (Diaretiella rapae) that emerged from cabbage aphids collected from sticky traps on Brassica napus plants within Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Data cover two years (Year) and are organized by ring (Ring) and pollution treatment (Pollutant) with four levels: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control (CON).
- Plants in the OPEN treatment were inoculated with aphids and netted; parasitoids were allowed to parasitize aphids and trapped using sticky traps inside nets.
- Replication: four, seven, and four plants per Run for the first, second, and third experimental runs, respectively, across the two years.
- Emergent parasitoids were counted from traps inside nets; the dataset records the number of Diaretiella rapae parasitoids emerged (Parasitoids_emerged).

## Experimental design
- Location and timing: Field of wheat in 2018 (later moved to an adjacent field in 2019); precise coordinates provided. Rings were assigned to four pollutant treatments (D, O3, D+O3, CON).
- OPEN treatment procedure: Plants five weeks old were inoculated with 10 Brevicoryne brassica aphids and netted. Nets were removed after two weeks to allow free-living parasitoids to attack aphids, then re-netted after one additional week.
- Sampling mechanism: A sticky trap was placed inside the net of each plant to capture emerging parasitoids; traps inside nets were collected 10 days later.
- Target species: Diaretiella rapae, the predominant parasitoid species observed in this setup.

## Data structure and variables
- Year (Column A)
- Ring (Column B)
- Pollutant (Column C): D, O3, D+O3, CON
- Treatment (Column D): OPEN (netted/open condition during sampling)
- Plant_ID (Column E)
- Run (Column F): 1st, 2nd, 3rd experimental run
- Parasitoids_emerged (Column G): count of Diaretiella rapae emerged
- Location details: Field coordinates for 2018 and movement to adjacent field in 2019
- Reference methodology: Full FADOE configuration and quality control described in Ryalls et al. 2022 ( Environmental Pollution )

## Data quality and provenance
- Methodology and quality control are documented in the referenced 2022 Environmental Pollution article.
- Data are tied to a defined experimental framework (FADOE) with replicated rings and plants across multiple runs and years, enabling analysis of treatment effects and temporal variation.

## Potential analyses and data products
- Compare parasitoid emergence counts across pollutant treatments (D, O3, D+O3, CON) and over years.
- Assess effects of Run and Plant_ID as random or fixed effects to account for replication and within-ring variation.
- Visualization-ready data for dashboards and reports to communicate how air pollutants influence aphid–parasitoid interactions.
- Data can support broader analyses of plant–insect interactions under environmental stressors and aid in communicating findings to stakeholders.