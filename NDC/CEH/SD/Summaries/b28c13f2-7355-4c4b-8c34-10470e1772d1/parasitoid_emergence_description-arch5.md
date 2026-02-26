# Description, Experimental Design and Collection

- This dataset records the abundance of parasitic wasps (Diaretiella rapae) that emerged from cabbage aphids (Brevicoryne brassicae) collected from sticky traps placed on Brassica napus plants within Free-Air Diesel and Ozone Enrichment (FADOE) rings. Full FADOE configuration and quality control details are described in the referenced methodology.
- Sampling occurred over two years (Year). Each FADOE ring has an identifier (Ring) and was allocated to one of four pollution treatments (Pollutant): diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control (CON; natural air).
- Field layout: rings were located in a wheat field in 2018 (lat/long given) and moved to an adjacent field in 2019 (lat/long given).

## Experimental Design and Treatments

- OPEN treatment: plants at five weeks old were inoculated with 10 Brevicoryne brassica aphids and netted; nets were removed for one week to allow parasitism, then re-netted and a sticky trap placed inside each net to capture emerging parasitoids.
- Replication and runs: there were four, seven, and four replicate plants in the first, second, and third experimental runs, respectively, across the two-year period.
- Collection timing: sticky traps inside the nets were collected 10 days after nets were placed for the OPEN plants to assess parasitoid emergence.

## Data Collected and Metadata

- Primary measure: number of parasitoids emerged (Parasitoids_emerged) identified and counted, with Diaretiella rapae being the dominant parasitoid species observed.
- Key columns/fields (examples): Year, Ring, Pollutant, Treatment, Plant_ID, Run, Parasitoids_emerged.
- Geographic and contextual details: precise field locations are provided through lat/long coordinates; the dataset references the FADOE methodology paper for full configuration details.
- Data provenance: methodology and quality control are documented in the cited reference [Ryalls et al., 2022].

## Data Quality, Standards, and Provenance

- Quality control and experimental protocol are governed by the FADOE configuration and QC measures described in the primary methodology reference.
- For data stewardship, ensure consistent metadata for columns (names, data types, units), clear linkage to Ring, Pollutant, Treatment, and Run, and preservation of the temporal sequence across Year.

## Data Management, Sharing, and Reuse

- Data should be uploaded to appropriate data portals and catalogues with complete metadata and documentation linking back to the FADOE configuration and the referenced publication.
- Maintain transparency of treatments, replication, and collection timing to support reproducibility and cross-study comparability.
- Useful reuse directions: study the effects of air pollutant treatments on parasitoid emergence, cross-reference with open data on pollination and insect-mediated processes, and integrate with related environmental exposure datasets.

## Considerations and Limitations

- The dataset captures a specific parasitoid community (predominantly Diaretiella rapae) from a controlled OPEN treatment under multiple pollutant regimes; other parasitoid species may be underrepresented.
- Multi-year field relocation and varying plant replication per Run may introduce variability that requires careful statistical handling.
- As with similar datasets, timely data capture and adherence to metadata standards are essential to maximize usability and interoperability.