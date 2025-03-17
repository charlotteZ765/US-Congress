# US-Congressional Speech Analysis
An NLP Analysis of Lexical and Semantic Variation in US Congressional Speeches

## Overview
This project aims to analyze the stylistic, lexical, and semantic variations in speeches made by elected members of Congress. Using **Natural Language Processing (NLP)** techniques, we quantify differences in speech complexity, word choice, and semantic meaning across various dimensions such as political affiliation, gender, and time.

The main goal is to gain insights into political communication patterns while also providing hands-on experience with NLP methodologies.

## Data Sources
We utilize two primary datasets:

1. **U.S. Congressional Speeches (2001-2010)**  
   - Sourced from the *Congressional Record*  
   - Processed using Optical Character Recognition (OCR)  
   - Available at: [Stanford Congress Text](https://data.stanford.edu/congress_text)

2. **U.K. Parliamentary Speeches (2001-2010)**  
   - Sourced from *Hansard Speeches*  
   - Available at: [Hansard Dataset](https://evanodell.com/projects/datasets/hansard-data/)

Both datasets have been preprocessed to:
- Convert text to lowercase
- Remove speeches shorter than 100 characters
- Tokenize speech segments

## Methodology
We analyze congressional speeches using the following NLP techniques:

### **1. Stylistic Variation Analysis**
   - Metrics used:
     - **Mean characters per word**
     - **Words with at least 6 or 7 characters**
     - **Mean syllables per word**
   - Research Questions:
     - Are Republican speeches less complex than Democrat speeches?
     - Do speeches by women have higher complexity than those by men?
     - Is speech complexity decreasing over time?
     - Are U.K. parliamentary speeches more complex than U.S. congressional speeches?

### **2. Lexical Variation Analysis**
   - Metrics used:
     - **Exclusive word usage by political party/gender**
     - **Over/underrepresentation of words using Pointwise Mutual Information (PMI)**
   - Research Questions:
     - Which words are uniquely used by Republicans vs. Democrats?
     - How does word usage differ between male and female speakers?
     - What words have been abandoned or introduced over time?

### **3. Semantic Variation Analysis**
   - Approach:
      - Used **pretrained embeddings** from `"glove-wiki-gigaword-100"`
     - **Trained new Word2Vec models** by updating our pretrained model with congressional speech data
     - Extracted semantic differences using similarity and vector-based transformations
       
   - Research Questions:
     - How do meanings of words shift between political parties?
     - How does word meaning evolve over time?
     - How do semantic interpretations differ between U.S. and U.K. politicians?

## Tools & Libraries
- **Python** (for NLP processing)
- **NLTK** / **spaCy** (for tokenization and linguistic analysis)
- **Gensim** (for word embeddings)
- **Pyphen** (for syllable counting)
- **Scikit-learn** / **Statsmodels** (for statistical analysis)

## Results & Findings
Key insights and results are presented in the codebook [US Congress v2](./US%20Congress%20v2.ipynb) and the [Project Report](./analysis%20report.pdf).

The report summarizes:
- Speech complexity trends
- Lexical distinctions between groups
- Semantic shifts in political language
- Visualization of findings using tables and graphs

## References
Benoit, K., Conway, D., Lauderdale, B. E., Laver, M., & Mikhaylov, S. (2019). "Simple, Interpretable and Stable Method for Detecting Words with Usage Change across Corpora". Available at: [DOI link](https://doi.org/10.18653/v1/2020.acl-main.51)

Grieve, J. (2007). "Quantitative Methods in Lexical Variation". Linguistics Research Series. Available at: [DOI link](https://doi.org/10.1093/llc/fqm020)



