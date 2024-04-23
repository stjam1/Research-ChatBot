
# Latest Trends ChatBot Tool

This is a easy to use tool to seek necessary information from news articles such as stock prices, sales and market trends. Users can provide URLs of articles they wish and then can provide questions to the chatbot to get necessary insights.

![alt text](ChatBot.jpg)

## Features

- Load URLs or upload text files containing URLs to fetch article content.
- Process article content through LangChain's UnstructuredURL Loader
- Construct an embedding vector using OpenAI's embeddings and leverage FAISS, a powerful similarity search library, to enable swift and effective retrieval of relevant information
- Interact with the LLM's (Chatgpt) by inputting queries and receiving answers along with source URLs.


## Demo

1. Run the Streamlit app by executing:
```bash
streamlit run main.py

```

2.The web app will open in your browser.

- On the sidebar, you can input URLs directly.

- Initiate the data loading and processing by clicking "Process URLs."

- I have used the following URLs 
  - https://www.theguardian.com/technology/2024/apr/21/tesla-sales-price-cuts-elon-musk
  - https://www.bloomberg.com/news/features/2024-04-21/tesla-tsla-cybertruck-recall-is-latest-setback-to-stock-s-rough-2024
  - Have not loaded 3rd URL to save open API tokens and charges for embedding :)

- Observe the system as it performs text splitting, generates embedding vectors, and efficiently indexes them using FAISS.

- The embeddings will be stored and indexed using FAISS, enhancing retrieval speed.

- The FAISS index will be saved in a local file path in pickle format for future use.
- One can now ask a question and get the answer based on those news articles


## Project Contents

- main.py: The main Streamlit application script.
- requirements.txt: A list of required Python packages for the project.
- faiss_store_openai: folder that contains pickle file for FAISS index.
- .env: Configuration file for storing your OpenAI API key.
  
# Note:
- change the .env file with the your openAI API key for running the project manually or with the following command 
```bash
  OPENAI_API_KEY=your_api_key_here
```