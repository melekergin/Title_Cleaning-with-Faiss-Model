**FAISS Job Title Similarity and Speed Comparison Notebook**

This notebook is designed to perform similarity searches on job titles using the FAISS library and includes a comparison of search speeds between two different FAISS index types.

**Sections**
**Title Cleaning**: The notebook begins by cleaning job titles from a CSV file, standardizing the text for more accurate vector representation.

**Single Title Search with IndexFlatL2**: It demonstrates a nearest neighbor search for a single title using the IndexFlatL2 index, which is precise but may not be the fastest for large datasets.

**Speed Measurement with IndexFlatL2**: The speed of the search using IndexFlatL2 is measured to provide a baseline for comparison.

**Speed Comparison with IndexIVFFlat**: The notebook compares the search speed using IndexIVFFlat, which is faster than IndexFlatL2 due to its use of an inverted file system and quantization. However, it requires training on a subset of the data (2000 training points) and may trade off some accuracy for speed.

**Conclusion**
The notebook serves as a practical guide for cleaning job titles, encoding them into vector space, and performing efficient similarity searches with FAISS. It also provides insights into the trade-offs between search accuracy and speed by comparing two different types of FAISS indices.
