# Langchain Lamma2 Bot
This README will guide you through the setup and usage of the Langchain with Llama 2 model for pdf information retrieval using Chainlit UI.

## Prerequisites

- Python 3.9 or higher
- Required Python packages (you can install them using pip):
    - langchain
    - chainlit
    - sentence-transformers
    - faiss
    - PyPDF2 (for PDF document loading)

## Installation

1. Clone this repository to your local machine.

    ```bash
    git clone https://github.com/d-t-n/llama2-langchain-chainlit-pdf.git
    cd llama2-langchain-chainlit-pdf
    ```

2. Create virtual environment (conda recommended):

    ```bash
    conda create -n langllmpdf python=3.10
    conda activate langllmpdf 
    ```

3. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Use your HuggingfaceHub API key (from this [URL](https://huggingface.co/settings/tokens)) in the .env file
   ```
   HUGGINGFACEHUB_API_TOKEN=your_huggingface_api_token
   ```

5. Put your pdf files in the data folder and run the following command in your terminal to create the embeddings and store it locally:
   ```
   python ingest.py
   ```

6. Run the following command in your terminal to run the app UI (to choose ip and port use --host IP and --port XXXX):
   ```
   chainlit run main.py -w --host 127.0.0.1 --port 9001
   ```

7. Ask any question about the pdfs