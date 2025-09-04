# BEMM466 Business Project 
**Project Title:** *Analysing Public Discourse on the Anticipated U.S. 2025 Tariff Policy: A Topic Modeling Approach*

This repository contains the dataset, preprocessing scripts, topic modeling code, and output files of the project.  

The workflow was implemented in **Python (Jupyter Notebooks)** and uses both **LDA** and **BERTopic** for topic modeling.  

## Dataset 

The dataset (`X_fulldataset.csv`) is raw dataset of 31,624 posts collected from **X (Twitter)** via **Apify**, covering the period **2 April – 1 July 2025 (90 days)**.  

## Code Files (Jupyter Notebooks)

There are **4 files** of code: `Data_cleaning.ipynb`, `EDA.ipynb`, `Text_preprocessing+LDA Model.ipynb`, and `BERTopic Model.ipynb` in this project.

#### Run notebooks in the following order:
  1. `Data_cleaning.ipynb`
  2. `EDA.ipynb`
  3. `Text_preprocessing+LDA Model.ipynb`
  4. `BERTopic Model.ipynb`

### 1. Data_cleaning.ipynb
- Input file: `X_fulldataset.csv`
- Cleans and structures the raw dataset.  
- **Output files (Export from the code)**  
  - `posts_table.csv` – Structured table of posts data
  - `users_table.csv` – Structured table of users data  
  - `hashtags_table.csv` – Structured table of extracted hashtags data

### 2. EDA.ipynb
- Input file: `post_table.csv`, `users_table.csv`, and `hashtags_table.csv`
- Perform **Exploratory Data Analysis (EDA)**.  
- Include visualisations of hashtag usage, posting frequency per user, users following and follower, verified accounts, and post engagement in the file.  

### 3. Text_preprocessing+LDA Model.ipynb
- Input file: `post_table.csv`
- Text Preprocessing:  
  - Remove URLs, mentions, emojis, punctuation, numbers
  - Remove punctuation  
  - Converts text to lowercase
  - Remove stop words
  - Lemmatize texts
  - **Output files (Export from the code):** `cleaned_text.csv` - Cleaned text after text pre-processing for further analysis in BERTopic model
    
- **Latent Dirichlet Allocation (LDA)**
  - Run topic modeling via **LDA model** with lemmatized texts
  - **Output files (Export from the code):** `lda_visualization.html` - Interactive visualisations for interpreting topics

### 4. BERTopic_Model.ipynb 
- Input file: `cleaned_text.csv`
- Run **BERTopic Model** for topic modeling
- **Output files (Export from the code):** 
  - `Topic_freq.csv`- Topic frequency and keywords result
  - `BERTopic_intertopic_distance_map.html`- Interactive intertopic distance map
  - `BERTopic_topic_word_scores.html`- Interactive bar chart of topic word scores
  - `document_info.csv`- Document-topic assignment table
  - `data_topic_samples.csv`- 5 documents sample from each topic for further topic labeling
  - `topics_over_time.html`- Interactive line graph of topics over time
- **Additional file:** `topic_labels.xlsx`-	5 representative posts from each topic with labels, which manually assigned by the author

#### Note: All visualisation are in `.html` format. They can be downloaded and opened in any browser to interact with the plots for better clarity.
  

 


   
