# Dataset: Small rodent dynamics at Lathkill Dale SSSI, Derbys, 1971-2005

- A 35-year program of 6-monthly population sampling for bank voles (Myodes glareolus) and wood mice (Apodemus sylvaticus) in a Derbyshire ash woodland.
- Includes annual measurements of ash fruit-fall and a winter severity metric, plus a 4-year experimental ash fruit supplementation in a nearby area.
- Data collected to understand how environmental variables (food supply, climate) and density influence reproductive and population growth, with a focus on long-term dynamics and interspecific differences.

## Aims and relevance for monitoring frameworks

- Demonstrates linking environmental health measures (masting, climate) to small mammal demography to inform policy evaluation and decision-making.
- Uses a state-space modelling approach to separate biological and climatic influences and to quantify lagged effects on population dynamics.
- Highlights the value of long-term, multi-variable data in detecting delayed and density-dependent effects, informing woodland management and biodiversity monitoring.

## Study design and data collection

- Location: Lathkill Dale, Derbyshire; ash-dominated woodland (Fraxinus excelsior); control and experimental study areas.
- Area and sampling: 0.45 ha trapping grid with 90 Longworth traps; sampling conducted over two 24-hour periods at roughly six-month intervals (Dec–Nov and May/June), 1971–2005.
- Species and metrics: population data for bank voles and wood mice, including adults and juveniles; density indices derived from marked individuals; population estimates (Zippin) where applicable.
- Environmental measures:
  - Ash fruit-fall measured as dry weight of edible ash seeds per m2, Sept–Mar or Apr depending on fruit availability.
  - Winter severity represented by mean minimum daily temperature Dec–Mar from Buxton Met Station.
- Experimental manipulation: in 1981–82 and 1984–85, supplementary ash fruit (6.79 g m-2 edible seed) distributed on the experimental grid to assess demographic responses.

## Data files and structure

Six data CSV files accompanying the dataset:
- FlowerdewApodemusData041212csv.csv: wood mouse and environmental data (1971–2005); includes year, winter severity, ash fruitfall sub-totals, trapping dates, adult/juvenile counts, and density estimates.
- FlowerdewApodemusExData040613Controlcsv.csv: wood mouse data on the control area (1981–1985).
- FlowerdewApodemusExData040613Experimentalcsv.csv: wood mouse data on the experimental area (1981–1985).
- FlowerdewMyodesData291112csv.csv: bank vole and environmental data (1971–2005); includes year, winter severity, ash fruitfall, trapping dates, counts, density estimates, and notes.
- FlowerdewMyodesExData040613Controlcsv.csv: bank vole data on the control area (1981–1985).
- FlowerdewMyodesExData040613Experimentalcsv.csv: bank vole data on the experimental area (1981–1985).

Notes on data structure:
- Column definitions cover year of June data collection, timing of trapping (November/December; May/June), counts for adults and juveniles, and density estimates (Zippin) where applicable.
- Environment-related columns include winter severity metrics and ash fruit-fall totals divided into relevant periods (Sept–Dec, Dec–Mar/Apr).
- Experimental and control datasets allow comparisons of demography with and without supplementary fruit.

## Modelling approach and key findings

- Modelling: State-space models applied to the live-trapping data to explain between-year variations in reproductive and population growth rates, with density indices validated against model-generated estimates.
- Key ecological conclusions:
  - September–March ash fruit-fall is the major driver of bank vole spring reproductive rate and population growth, with lasting effects into the following year.
  - Wood mouse responses to fruit-fall are weaker; December–March fruit-fall has a weaker influence on their summer growth; winter severity impacts bank vole winter growth and wood mouse spring reproduction.
  - Density dependence significantly influences growth rates for both species across winter and summer periods.
  - Ash fruit addition experiments confirm the fruit-fall influence on bank vole winter demography, with effects often persisting for a year or more.
  - Long-term dynamics show interspecific variation; notable differences include independent food and weather influences on bank vole demography and delayed, lasting effects of mast events.

## Data quality, metadata and governance

- Comprehensive metadata embedded in column headings and file descriptions; clear provenance of measurements (fruit-fall, temperature, trapping data).
- Data are organized to support replication of the modelling approach and to enable policy-relevant interpretation of how environmental variables drive mammal populations over multiple years.
- The experimental design (control vs. fruit supplementation) strengthens causal inferences about food availability and demographic responses.

## Study location and access

- Study area: Lathkill Dale, Derbyshire, within a 0.45 ha main grid; experimental area located nearby with a similar setup.
- Data were collected between 1971 and 2005, with focused experimental manipulations during 1981–82 and 1984–85 to assess the impact of enhanced ash fruit availability.