# Business-Intelligence-Insights-using-GenAI
___________________________________________________

## Project Overview: 

This project implements a Question-Answering (QA) system that extracts financial insights from web articles. Leveraging modern natural language processing techniques, it retrieves the most relevant content from financial news and provides concise answers based on user queries. The system integrates document embedding, retrieval mechanisms, and large language models like Llama for generating accurate responses.


## Features: 

1. Web Scraping: Automatically fetches financial news articles from provided URLs.
2. Document Processing: Splits articles into smaller, manageable chunks for better indexing.
3. Embedding Generation: Uses Sentence Transformers to encode documents and user queries into high-dimensional vectors.
4. Similarity Matching: Computes cosine similarity between query embeddings and document embeddings to find the most relevant content.
5. Question Answering: Employs Llama (via Groq) to generate concise answers from retrieved documents.
6. Source Attribution: Ensures answers are traceable to the original articles.


## Why Llama 3 over OpenAI?

In our AI-based Business Intelligence tool, we chose to integrate Llama 3 instead of OpenAI for several key reasons:

1. **Cost-Effectiveness**: Llama 3 provides a more affordable solution compared to OpenAI, especially for handling large-scale data and analysis without incurring high API usage costs.

2. **Open-Source Flexibility**: Llama 3 is open-source, allowing us greater flexibility in customizing the model for our specific use case and ensuring better control over the integration and updates.

3. **Data Privacy**: Llama 3 provides more control over data privacy, especially when dealing with sensitive business intelligence data. It eliminates concerns regarding data being processed externally or used to train other models.

4. **Performance & Efficiency**: Llama 3 offers high performance with faster processing speeds, which is crucial for delivering real-time insights in our Business Intelligence tool.

5. **Customization for Domain-Specific Needs**: Llama 3 can be fine-tuned for specific industries and domains, making it a more tailored fit for our business intelligence requirements, allowing us to optimize the model based on the nature of our datasets.

In conclusion, Llama 3 was chosen for its cost-effectiveness, flexibility, performance, and ability to ensure privacy and customization for our AI-driven insights.


## Technologies Used:

1. Programming Language: Python



## Libraries:

1. LangChain: For document loading and QA chains.
2. Unstructured: For processing text from URLs.
3. Sentence Transformers: For embedding generation.
4. FAISS: For vector similarity search.
5. Groq: For using Llama as the QA model.


   
## Model:
1. Sentence Transformer: all-MiniLM-L6-v2
2. Llama Model: llama3-70b-8192


## Setup and Installation: 

### Clone the repository:
``` bash
git clone https://github.com/anshsrivasta/Business-Intelligence-Insights-using-GenAI/tree/main
cd <repository-folder>
```
### Install the dependancies:
```bash
pip install langchain unstructured sentence-transformers faiss-cpu langchain-groq transformers
```


## Usage

### Load Financial News

Update the UnstructuredURLLoader with your desired financial news article URLs. The script automatically processes and chunks the data.

### Generate Embeddings

The system generates embeddings for both documents and user queries using the SentenceTransformer model.


## Ask a Question

Update the query in the script:

```bash
query = "Tell me about Tesla's Market Value."
```

##Customization

Modify the prompt variable to tailor the response style or focus on specific types of data (e.g., financial figures, trends, or sentiment).
Add or remove URLs to process multiple news sources here:
```bash
loaders = UnstructuredURLLoader(urls=[
    "https://www.moneycontrol.com/news/business/markets/wall-street-rises-as-tesla-soars-on-ai-optimism-11351111.html"
])
```
_____________________________________________________________________________

#### License
This project is licensed under the MIT License.

Acknowledgments
Inspired by advancements in NLP and retrieval-augmented generation techniques.






