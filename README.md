# visual-search-engine
To build a visual search engine, we first need to convert each image in our collection (specifically, the COCO 2017 dataset in this case) to extract high-dimensional numerical "feature vectors" (embeddings).

Next, a FAISS index is created from these image embeddings. FAISS (Facebook AI Similarity Search) is a specialized library for efficient similarity search and clustering of dense vectors, optimized for rapidly searching through millions or even billions of high-dimensional vectors.

Afterward, each query (whether an image or text) is also converted to an embedding. This query embedding then undergoes L2 normalization. Subsequently, a search is performed within the FAISS index to identify and retrieve the top 5 most similar images corresponding to the query (through inner product).

The results are as below:

