# Dialogue Decoded: Humans & LLMs

Large Language Models (LLMs) are advanced machine learning models that XXX. The goal of this project is to explore and understand what people ask LLMs and which models humans think do the best in specific contexts. We sample real conversation data from [Chatbot Arena](https://lmarena.ai), a website available for anyone to chat with two unknown AIs and vote which one they think has a better response.



This repository is the result of a collaboration between MIT's Break Through Tech AI program and the MIT IBM Watson AI Lab.



Contributors:

[Kat Canavan](https://github.com/thegalaxykat), Jane Liu, [Sarah Simmons](https://github.com/SarahSimmmons), Nida Chacar-Palubinskas, & Dilanur Bayraktar.

Thank you to Mikhail Yurochkin and Felipe Maia Polo for advising this project.



## Method (Instructions)

This project is split across three python notebooks with a pickle file saved and loaded between each notebook. This was done for two reasons. First, the notebooks needed to be compatible with single-use Google Colab runtime environments. Additionally, since this involves a several heavy and somewhat random processes, such as UMAP embedding and clustering using methods such as BERTopic, each pickle file acts as a checkpoint in the process such that embeddings only need to be computed once, clusters once, etc.



Required libraries can be found at the top of each notebook. Everything is compatible with Google Colab notebooks.



### Notebook 1

This notebook covers the data preprocessing steps, including embedding user prompts into vectors.



### Notebook 2

This notebook clusters user prompts for Large Language Models (LLMs) into categories using three different methods:

- KMeans

- BERTopic

- 2D Grid approach

After clustering, it labels each cluster using an LLM (we used ChatGPT 4o) for further analysis. We did not have access to a free API with enough tokens to label all clusters so we took a manual approach. More details are provided in the notebook.



### Notebook 3

This notebook calculates metrics for our research questions, specifically which topics have the most ties and which topics small models tie/ win the most in. Results and analysis can be found here.
