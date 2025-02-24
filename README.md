# Quota-Hora-Est-
## A NEW METHOD FOR TRACKING SEMANTIC DRIFT with a test case in Latin 
## Abstract:
This project seeks to test a new computational method to track diachronic semantic shift. By utilizing Word2Vec and Cosine similarity, a word list of the top 100 most similar words can be created for every unique word in a Vocabulary. This process can be done multiple times with separated W2V models, each trained on text from different time periods. By repurposing the technique put forward in “Simple, Interpretable and Stable Method for Detecting Words with Usage Change across Corpora”(Gonen et al.2020), inter-model comparisons can then be quickly and accurately made for the same word at different periods by leveraging Jaccard Similarity. The testing of this technique was made on temporally tagged Latin corpus spanning 800 years and proved to be an effective and easily implementable way to find notable semantic shifts en masse.

## Use
The files included should be everything necessary to replicated my results. I will include a brief description of all the code but ultimate they should be set up in such a way that should be easy to run locally. Simply download the repo locally and run the code from there. However, please note that the final_corpus.csv must be unzipped and kept in the same directory in order to run the code.

### LDA_topic_modeling 
This notebook is the Gensim LDA topic model that I used to generate the domains I used for the historical analysis. Unfornately I did not save those outputs, so they are unable to show the original findings. They do, however, demonstrate the methodology of how I built the generated lists from the intersections of those outputs.  The generated wordlist from the original outputs can be found in the Standard Vocab testing list. 

### Word2Vec_lemmas
This notebook carries bulk of the project. It takes the final generated corpus from all the texts and NLP cleaning and applies the Gonen et al. methodology. 
The target domains, words, as well as the words with highest and lowest similarity scores are all available for futher analysis in this notebook 

### T-SNE Visualization 
As in the original Gonen et al. paper, T-SNE visualization were used during the presentation and help illustrate the relations of the target words embeddings across time. This allows for easier and more immediate understanding of the change in the associated words with the target. In the visualizations, each period is associated with a color(Red-the Late Republic, Purple-The Principate, Blue-Late Antiquity). The vector of the target word in each period is also in green to help further illustrate the shift over time.
