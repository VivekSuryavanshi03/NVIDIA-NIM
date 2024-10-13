# NVIDIA NIM Demo with LangChain and FAISS

This project demonstrates the integration of NVIDIA AI Endpoints, LangChain, and FAISS to build a document retrieval system. The app ingests a PDF file (in this case, the 2013-2014 budget for India) and allows users to ask questions based on the contents of the PDF. The app then retrieves relevant chunks from the document and provides an answer using NVIDIA’s language model.

## Features
- **Document Ingestion**: Load and process PDF documents, chunking them for efficient retrieval.
- **NVIDIA AI Integration**: Utilizes NVIDIA’s language models for natural language understanding and response generation.
- **Vector Search**: FAISS is used to create embeddings of document chunks for efficient retrieval.
- **Streamlit Interface**: A simple UI for users to input questions and get responses based on the document content.

## Tech Stack
- **LangChain**: For document chaining, vectorization, and prompt management.
- **NVIDIA AI Endpoints**: Used to embed and process document content and for large language model (LLM) responses.
- **FAISS**: For fast vector similarity search on document chunks.
- **Streamlit**: For building the web-based interface.

## Installation

### Prerequisites
Make sure you have the following installed on your machine:
- Python 3.10.0 or later
- NVIDIA API Key (added in `.env` file)

### Steps

1. **Clone the repository**:
    ```bash
    https://github.com/VivekSuryavanshi03/NVIDIA-NIM.git
    cd nvidia-nim-demo
    ```

2. **Set up the environment**:
    Create a `.env` file in the root of the project and add your NVIDIA API key:
    ```bash
    NVIDIA_API_KEY="your-nvidia-api-key"
    ```

3. **Install dependencies**:
    Install the required Python packages listed in `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```

4. **Prepare the PDF document**:
    Place your PDF documents inside the `pdf` folder. For this demo, the **2013-2014 Budget of India** is used.

5. **Run the application**:
    Run the Streamlit app using the following command:
    ```bash
    streamlit run finalapp.py
    ```

6. **Using the application**:
    - Upload the PDF (budget of India 2013-2014) into the `pdf` directory.
    - Click on the **Documents Embedding** button to process the PDF and create embeddings.
    - Enter a question in the text input based on the document, such as "What was the total expenditure in 2013?".
    - The app will display the answer and show relevant document chunks for reference.

## Example Question
Example question you can ask based on the budget document:
- "What was the allocation for the healthcare sector in 2013-2014?"

## File Overview
- **finalapp.py**: The main application code integrating NVIDIA AI, LangChain, FAISS, and Streamlit.
- **requirements.txt**: Contains all the Python dependencies needed to run the app.
- **.env**: (Not included) Your environment file for storing sensitive information like the NVIDIA API key.
- **pdf/**: Directory where you can place the PDF documents for ingestion.

## Technologies Used
- **Python**: Backend language.
- **LangChain**: For document processing and prompt management.
- **NVIDIA AI**: For language model and embeddings.
- **FAISS**: For document vectorization and similarity search.
- **Streamlit**: For building the UI.

## License
This project is licensed under the MIT License.
