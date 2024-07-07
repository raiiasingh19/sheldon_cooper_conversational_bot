## Sheldon Cooper Conversational Bot

This project lets you chat with a simulated Sheldon Cooper from the TV show 'The Big Bang Theory'. It uses a large language model (Gemini Pro) to generate responses in Sheldon's style, based on a provided context. The context is retrieved from a vector database populated with data sourced from a Kaggle dataset, providing information relevant to the conversation. The project leverages libraries like Pathway, LlamaIndex, and Google Generative AI for data processing, embedding, retrieval, and response generation.

## Link to Video Demo

https://www.loom.com/share/262ded553a2b448d8e525c22ca64fd9d?sid=b256fa82-cd45-4b63-86d5-c75aa36d2580


  ## Libraries Used
  
  1. **Llama Index:**
    *  Node Parsing: TokenTextSplitter from llama_index.core.node_parser is used to split the data into smaller chunks (nodes) for efficient processing and embedding.
     * Retrieval: PathwayRetriever from llama_index.retrievers.pathway is used to fetch relevant context from the vector database built using Pathway. This context 
     is then used to generate Sheldon-like responses.
  
  2. **Pathway:**
    * Data Ingestion: pw.io.fs.read is used to read data from the file system.
    * Vector Database: Pathway's VectorStoreServer is used to create and manage the vector database where the embedded data is stored. This allows for efficient          similarity search to retrieve relevant context.
  
  3. **Google Generative AI:**
    * Response Generation: The gemini-pro model from google.generativeai is used to generate responses in Sheldon's style, based on the prompt and the context            retrieved from the vector database.
     

## Instructions for Setting Up and Running

1. **Set up Google Colab:**
   * Create a new Google Colab notebook.
   * Paste the provided code into the notebook.

2. **Install Dependencies:**
   * Run the following pip install commands in a code cell:
     ```
     !pip install llama_index
     !pip install transformers
     !pip install google-generativeai
     !pip install sentence-transformers
     !pip install pathway
     !pip install llama-index-retrievers-pathway
     !pip install llama-index-embeddings-huggingface
     ```

3. **Mount Google Drive:**
   * Run the provided code to mount your Google Drive.
   * Ensure the path to the Big Bang Theory script CSV file (`csv_path`) is correct.

4. **Set Environment Variables:**
   * Store your Google API key in Colab's userdata:
     ```python
     from google.colab import userdata
     userdata.set('GOOGLE_API_KEY', 'YOUR_API_KEY')
     ```

5. **Run the Code:**
   * Execute all code cells in the notebook sequentially.
   * The chatbot will start running in a loop, allowing you to type in queries and receive responses from "Sheldon".

6. **Environment Variables:**

  * GOOGLE_API_KEY: Your API key for accessing the Google Generative AI service. Store this securely in Colab's userdata.


