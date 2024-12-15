# Deep Text Search - AI Based Text Search & Recommendation System
<p align="center">
**Deep Text Search** is an AI-powered multilingual **text search and recommendation engine** with state-of-the-art transformer-based **multilingual text embedding (50+ languages)**.



## Features
- Faster Search.
- High Accurate Text Recommendation and Search Output Result.
- Best for Implementing on python based web application or APIs.
- Best implementation for College students and freshers for project creation.
- Applications are Text-based News, Social media post, E-commerce Product recommendation and other text-based platforms that want to implement text recommendation and search.

## Installation

This library is compatible with both *windows* and *Linux system* you can just use **PIP command** to install this library on your system:

```shell
pip install DeepTextSearch
```

## How To Use?

We have provided the **Demo** folder under the *GitHub repository*, you can find the example in both **.py** and **.ipynb**  file. Following are the ideal flow of the code:

### 1. Importing the Important Classes
There are three important classes you need to load **LoadData** - for data loading, **TextEmbedder** - for embedding the text  to data, **TextSearch** - For searching the text.

```python
# Importing the proper classes
from DeepTextSearch import LoadData,TextEmbedder,TextSearch
```

### 2. Loading the Texts Data

For loading the Texts data we need to use the **LoadData** object, from there we can import text data as python list object from the CSV/Text  file.

```python
# Load data from CSV file
data = LoadData().from_csv("../your_file_name.csv")
# Load data from Text file
data = LoadData().from_text("../your_file_name.txt")
```
### 3. Embedding and Saving The File in Local Folder

For Embedding we are using state of the art multilingual Sentence Transformer Embedding, We also store the information of the Embedding for further use on the local path **[embedding-data/]** folder.

You can also use the **load embedding()** method in a **TextEmbedder()** class to load saved embedding data.

```python
# To use Serching, we must first embed data. After that, we must save all of the data on the local path.
TextEmbedder().embed(corpus_list=data)

# Loading Embedding data
corpus_embedding = TextEmbedder().load_embedding()
```
### 3. Searching

We compare Cosian Similarity for searching and recommending, and then the corpus is sorted according to the similarity score:

```python
# You must include the query text and the quantity of comparable texts you want to search for.
TextSearch().find_similar(query_text="What are the key features of Node.js?",top_n=10)
```

## Complete Code

```python
# Importing the proper classes
from DeepTextSearch import LoadData,TextEmbedder,TextSearch
# Load data from CSV file
data = LoadData().from_csv("../your_file_name.csv")
# To use Serching, we must first embed data. After that, we must save all of the data on the local path
TextEmbedder().embed(corpus_list=data)
# You must include the query text and the quantity of comparable texts you want to search for
TextSearch().find_similar(query_text="What are the key features of Node.js?",top_n=10)
```



**More cool features will be added in future. Feel free to give suggestions, report bugs and contribute.**
