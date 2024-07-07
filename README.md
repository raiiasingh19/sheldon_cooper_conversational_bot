##### ## **# Sheldon Cooper Conversational Bot**

This project lets you chat with a simulated Sheldon Cooper from the TV show 'The Big Bang Theory'. It leverages a large language model (Gemini Pro) and a vector database (Pathway) to store and retrieve relevant context from a dataset of Big Bang Theory scripts.

## Steps to Run

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

## Environment Variables

* **GOOGLE_API_KEY:** Your API key for accessing the Google Generative AI service. Store this securely in Colab's userdata.

Link to Video Demo:

https://www.loom.com/share/262ded553a2b448d8e525c22ca64fd9d?sid=b256fa82-cd45-4b63-86d5-c75aa36d2580
