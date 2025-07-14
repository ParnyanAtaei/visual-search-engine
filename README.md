# visual-search-engine
To build a visual search engine, we first need to convert each image in our collection (specifically, the COCO 2017 dataset in this case) to extract high-dimensional numerical "feature vectors" (embeddings).

Next, a FAISS index is created from these image embeddings. FAISS (Facebook AI Similarity Search) is a specialized library for efficient similarity search and clustering of dense vectors, optimized for rapidly searching through millions or even billions of high-dimensional vectors.

Afterward, each query (whether an image or text) is also converted to an embedding. This query embedding then undergoes L2 normalization. Subsequently, a search is performed within the FAISS index to identify and retrieve the top 5 most similar images corresponding to the query (through inner product).

The results of image_query as below:
<table style="width:100%;">
  <tr>
    <td style="width:50%; text-align:center;">
      <img src="images/result_cat.PNG" alt="serach based of cat image" style="width:100%;">
      <br>
      <em>Top 5 images similar to query image</em>
    </td>
    <td style="width:50%; text-align:center;">
      <img src="images/result_dog.PNG" alt="serach based of dog image" style="width:100%;">
      <br>
      <em>Top 5 images similar to query image</em>
    </td>
  </tr>
</table>

And for text_query:
![Application Screenshot](images/result-car.PNG " Top 2 image similar to text query")

The short video of how this visual search engine work:
