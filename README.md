# Business_Project
BEMM466 Business Project: Analysing Public Discourse on the Anticipated U.S. 2025 Tariff Policy: A Topic Modeling Approach
All files are sample dataset and sample codes.
  - Sample dataset is posts from X from 2 April to 3 April 2025 with 500 rows. (Real dataset will be approximately 30,000 rows)
  - 2 sample codes of performing LDA model and BERTopic model
    Step 0 - The data cleaning process is performed in Jupyter Notebook (LDA_Test.ipynb file). After the process of text lemmatized, cleaned data is exported as cleaned_data.csv file for further applying in BERTopic model.
    Step 1 - The LDA model is continously performed in Jupyter Notebook. You can see the code in LDA_Test.ipynb file.
    Step 2 - Due to errors of conflict between versions of some libraries in performing both LDA and BERTopic models that occurred in Jupyter Notebook, I decides to perform the BERTopic model in different program (Google Colab). The reason why I choose to use Google Colab is that it gives me free GPU, which are faster in performing sentence-transformers in BERTopic.
    ** All BERTopic codes might be invisible in Github, but you can download BERTopic_Test.ipynb file to see the codes.

