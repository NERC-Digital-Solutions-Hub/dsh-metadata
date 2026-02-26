# Summary (a brief description/overview of the data)

- What the data are
  - Outcomes from questionnaire surveys of greenspace users regarding perceptions of experimentally manipulated urban meadows (varying diversity and vegetation height of sown wildflower meadows) and associated respondent socio-economic data.
  - Experimental sites located in Bedford and Luton; originally collected in 2014 under the Fragments, functions and flows NERC BESS project; subsequently re-analysed for the 2021 paper by Jones et al. (People and Nature).
  - Data resource consists of one CSV file with 1020 rows and 21 columns (Data_Phase 2_AsUsed_ForPublicArchive.csv).

- Experimental design and sampling
  - Nine experimental meadows per site, defined by a 3-level diversity × 3-level height matrix (total of 9 meadow types).
  - Four sites (locations in Bedford and Luton); 30 greenspace users surveyed per site.
  - Data include perception scores and categorical responses from the questionnaire.

- Collection and transformation methods
  - Greenspace users were surveyed via questionnaire after providing informed consent.
  - Ethical approval obtained; responses checked during data entry; answers not matching categorical options were excluded.

- What is recorded (Nature and units)
  - Perceptual and social variables such as:
    - Q1_PerceivedDiversity: perceived number of plant types in each plot.
    - Q2_PrefScore: 1–10 scale of liking for each plot (1 = strongly dislike, 10 = strongly like).
    - plantid_EcoKnowledge: number of correctly identified plants from a list.
    - ecoCentrism-related measures (e.g., biodiversity/wildlife features in gardens).
    - Visit-related measures: visitlength (minutes), visitfreq, othergsfreq, visitcount.
    - Demographics: gender, age, income, employment, edu, ukresident, ethnic.
  - Treatment descriptors:
    - Diversity level, Height level, and a 9-level combined Treatment description (combinations of height and diversity).

- Data structure details
  - Variables encoded with codes (e.g., SITE, Sample, SampNo, Diversity, Height, Treatment description) and a description for each.
  - Categorical and numerical fields reflect respondent answers, with NA indicating no response.

- Analytical methods used with this data resource (context)
  - The presented data resource itself has not undergone analytical processing within this description.
  - Prior work (Southon et al. 2017, 2018) analyzed similar data using multivariate analyses and mixed-effects models in R to relate meadow characteristics to user responses.
  - The 2021 Jones et al. paper used mixed-effects models and Bayesian modelling to evaluate how different user characteristics shape perceptions of greenspace meadows within a cultural services framework.

- Quality control and provenance
  - Ethics: Approved by the University of Sheffield Research Ethics Committee (Landscape Architecture Ethics Panel).
  - Data integrity: Responses checked during data entry; responses outside categorical options excluded.
  - Provenance: Data originally from the Fragments, functions and flows project; later re-analyzed for a peer-reviewed article (Jones et al., in press 2021).

- Important considerations for use
  - Dataset is self-reported and cross-sectional; potential biases in perception measures.
  - Some variables are derived (e.g., age and income mid-points from brackets); many socio-economic factors are included for modelling.
  - The data enable exploration of relationships between meadow design (diversity and height) and perceived value, as well as how respondent characteristics influence perceptions.

- References and related materials
  - Southon, G.E. et al. (2017, 2018) on aesthetic value, perceived richness, and well-being impacts.
  - Jones, L. et al. (2021, in press) Can we model cultural ecosystem services, and are we measuring the right things? People and Nature.