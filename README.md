The notebook consists of several cells that perform the following tasks:

Data Loading: A CSV file containing job titles is loaded into a pandas DataFrame. The DataFrame is expected to have at least two columns: 'Title' and 'Cleaned_Title'.

Encoding: The preprocessed titles are encoded into numerical vectors using the SentenceTransformer model. This model converts each title into a high-dimensional vector that captures semantic meaning.

FAISS Index Creation: A FAISS index (IndexFlatL2) is created to facilitate efficient similarity searches. The index is compatible with L2 distance, which measures the Euclidean distance between vectors.

Vector Normalization and Indexing: The title vectors are normalized to unit length and added to the FAISS index. Normalization is crucial for meaningful distance comparisons.

Search Query Encoding: A search query (e.g., 'Director of People Operations') is encoded using the same SentenceTransformer model to ensure consistency with the indexed vectors.

Nearest Neighbor Search: The FAISS index is queried with the search vector to find the k-nearest neighbors (where k is a user-defined parameter, such as 5).

Results Processing: The distances returned by the FAISS search are converted into similarity scores, and the results are merged with the original DataFrame to display the corresponding job titles.

Output: The top k results are displayed, showing the most similar job titles to the search query based on the similarity scores.

Usage
To use this notebook, you need to have a CSV file with job titles and follow the steps outlined in the cells. The notebook is designed to be modular, allowing for easy adaptation to different datasets or search queries.

Requirements
pandas
re (regular expressions)
SentenceTransformer
numpy
faiss-cpu or faiss-gpu (depending on your hardware)
