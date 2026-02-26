# VIRAQUA survey

- Purpose and scope
  - A 15-minute survey designed to gather opinions from a broad target group about upset stomachs and bugs that cause them.
  - Conducted by researchers at Bangor University and the University of Manchester; responses are confidential and used for academic research only.

- Structure of data collection
  - Demographics: self-identified gender, age, and household income earner occupation classification.
  - Dietary and environmental exposure:
    - Filter-feeding shellfish consumption (locations, frequency, and forms such as raw, cooked, ready meals, and pickled shellfish).
    - Contact with UK recreational waters in the last year (activities and settings).
  - Health experience assessment:
    - Upset stomach experiences in the last 12 months, including links to eating shellfish and water contact.
    - Behavioral changes following illness (e.g., dietary changes, avoidance of shellfish, cooking precautions).
  - Guidance and information sources:
    - Whether respondents sought advice for upset stomachs, where they looked for guidance, and perceived sufficiency of government information.
  - Knowledge of pathogens:
    - Awareness of specific bugs (MRSA, Cryptosporidium, Norovirus, E. coli, Perginella, C. difficile, Listeria, Shigella, Campylobacter, Rotavirus) with “Never heard of / Heard of but know nothing / Know a little / Know a lot” scales.
  - Hazards of Life module:
    - Sets of four hazards presented repeatedly; respondents indicate which hazard they fear the most and the least (fear assessment).
    - Later sections assess perceived control over hazards (most control / least control).
  - Personal impact and experience:
    - Whether respondents or close others have experienced listed hazards (e.g., terrorist attack, dementia, car accident, heart attack, diabetes, etc.).
  - Final prompts and wrap-up:
    - Reflection on ease of understanding and making choices, and an option to provide additional thoughts.
    - Completion acknowledgment with a notice about data usage and privacy.

- Data nuances and instrumentation
  - Extensive use of coded variables (e.g., effs_r1, wsfsf, fear_1_b) to capture granular responses across multiple sections.
  - Mixed data types: structured multiple-choice items, Likert-like scales, and free-text comment boxes.
  - Progress indicators and section navigation built into the instrument (e.g., “Hazards of Life” sections, multiple rounds of choices).

- Data governance and ethics
  - Explicit statement that data are for academic research and not for private marketing; responses are confidential.
  - Participants are asked about government information sources and may provide feedback on accessibility and usefulness.

- Data quality considerations for Data Leaders
  - Potential data quality risks:
    - Heterogeneous question formats and heavily coded variable naming may complicate data harmonization.
    - Some response options and labels appear inconsistent or incomplete in places (e.g., placeholders and mixed tokens).
    - Complex skip patterns and multi-part questions require careful parsing to preserve relationships between variables.
  - Opportunities for governance and improvement:
    - Standardize variable naming conventions and metadata to improve discoverability and interoperability.
    - Document skip logic and mapping between coded responses and their semantic meaning.
    - Implement data quality checks to handle incomplete or ambiguous responses and to normalize scales across sections.
    - Ensure clear metadata around privacy, purpose, and data provenance for downstream users.

- How this aligns with data strategy and practice for Data Leaders
  - Demonstrates the importance of end-to-end data stewardship: from demographics and exposures to health outcomes and knowledge of pathogens.
  - Highlights need for data discoverability (metadata and discoverability updates) and proper data formatting (uniform scales, consistent coding).
  - Underlines the value of feedback loops (user guidance perceptions, information-source usefulness) to inform data product design and outreach.
  - Emphasizes cross-cutting data collaboration and audience segmentation (demographics, behavioral responses, hazard perception) relevant for wider data ecosystems.

- Takeaways for action
  - When designing data-gathering programs, ensure clear, consistent instrumentation with thorough metadata.
  - Balance rich, granular data collection with standardized schemas to enable interoperability across networks.
  - Build in governance for discoverability, data quality, and privacy to support reuse by policy colleagues and partner communities.
  - Leverage the survey’s findings to improve data products and guidance around public health information and risk communication.