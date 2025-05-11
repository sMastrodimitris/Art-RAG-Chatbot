# Art-RAG-Chatbot
A Langchain RAG-LLM Bot, using a ChromaDB created from Wikipedia Articles about Art. All in a nice gradio packaging.

![My Logo](images/Gradio/Gradio7.png)



### This project was done as practice in the use of VectorDBs, Langchain, Retrieval-Augmented-Generation(RAG) and different LLM APIs. 

## The project can be analysed in 3 different steps.
### Step1: Using WikipediaAPI to crawl automatically to create a document. An Information Corpus from where we can pull requests. (wikipedia_art_corpus_document)

### Step2: Load, Split, vectorise the document into a Choma Vector Database (document_to_vectordb)

### Step3: Use a retreiver and and a LLM to provide natural, accurate and informed answers (art_claude_rag). Take it a step further by changing the LLm and create a simple Gradio App. (art_GPT_gradio_implementation)


#### Because Github is a bit silly i only could providde the code but not the prints. 
#### Below you can find some example that i saved by hand.


### Here is the query using the VectorDB without a informed retreiver.
![My Logo](images/Vector.png)


#### Here is the RAG results for questioning about Stained glass

#### Here is the RAG results with Claude
![My Logo](images/Claude/Claude1.png)
#### Here is the RAG results with GPT-3.5 Turbo
![My Logo](images/GPT/GPT1.png)



#### Here is the RAG results for questioning about Stained glass

#### Here is the RAG results with Claude
![My Logo](images/Claude/Claude2.png)
#### Here is the RAG results with GPT-3.5 Turbo
![My Logo](images/GPT/GPT2.png)



#### Here is the RAG results for questioning about Stained glass

#### Here is the RAG results with Claude
![My Logo](images/Claude/Claude3.png)
#### Here is the RAG results with GPT-3.5 Turbo
![My Logo](images/GPT/GPT3.png)


