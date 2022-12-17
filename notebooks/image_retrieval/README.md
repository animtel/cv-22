This homework consists of several consecutive notebooks:

- 00_dataset_preprocessing - responsible for downloading data, unpacking and cutting video from the dataset into frames. 
Result: directory with frames.
- 01_embed_images - responsible for computing image embeddings using CLIP and store it into pickle file.
Result: pickle file with embeddings for img files.
- 02_cluster_embeddings - experimental and core notebook that consists image deduplication by dimensionality reduction using UMAP and clustering using DBSCAN, after that it finds medoids (the most representative sample in claster) and store them into pickle file. This notebook is core because image retrieval quality depends on database quality, and database should consists unique but representative data samples.
Result: pickle pandas dataframe with medoids. Dataframe properties: filename | emb | cluster_id
- 03_image_retrieval - code that use FAISS library to index and search in database. It takes image embedding as input and find closest embedding indexes in database, than finds filename by corresponding indexes.
- 04_fiftyone_image_search - using fiftyone library implemented image search by CLIP embeddings.

What can be improved:
- There are many ways to find image features that will provide better search, but it depends from end project goal.
- I used UMAP + DBSCAN to reduce duplicates in the data, but didnt experement with parameters of this approach. Also there are more advanced methods of dataset cleaning with different clustering methods, I think there is big field to research.