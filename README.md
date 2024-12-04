# PDF-Text-Embedding-Generator

## Project Description  
This project demonstrates an end-to-end solution for extracting text from PDF files stored in **Azure Blob Storage** and generating embeddings using open-source **LLMs** in an **Azure Databricks** environment. It integrates Azure services with natural language processing capabilities, offering a scalable and efficient workflow.

---

## Prerequisites  

Ensure you have the following prerequisites before running this project:  
- **Azure Databricks workspace**  
- **Azure Blob Storage account**  
- **Python 3.x** installed  
- Required Python packages:
  - `PyPDF2`
  - `sentence-transformers`
  - `azure-storage-blob`

---

## Configuration  

```python
# Storage Account Details
storage_account_name = "genaicertificationsa"
container_name = "gen-ai-container"
mount_point = "/mnt/gen-ai-container"
```

---

## Features  
- **Azure Blob Storage Mounting** on Databricks  
- **PDF Text Extraction** using PyPDF2  
- **Text Embedding Generation** using Sentence Transformers  
- Robust **Error Handling and Validation**:
  - Mount point verification  
  - PDF file existence checks  
  - Text extraction and embedding validation  

---

## Installation  

Follow these steps to set up the project:

1. Clone this repository to your local machine:  
   ```bash
   git clone https://github.com/<your-username>/PDF-Text-Embedding-Generator.git
   cd PDF-Text-Embedding-Generator
    ```
2. Configure Azure Blob Storage credentials in your Databricks environment.

3. Mount the Blob Storage container to Databricks using the mount_storage.py script.

4. Install the required Python dependencies:
   ```bash
    pip install PyPDF2 sentence-transformers azure-storage-blob
   ```


Here’s the comprehensive README.md file with proper structure and flow:



# PDF-Text-Embedding-Generator

## Project Description  
This project provides an end-to-end pipeline for extracting text from PDF files stored in **Azure Blob Storage** and generating text embeddings using open-source **LLMs** in an **Azure Databricks** environment. It demonstrates the integration of Azure services with natural language processing techniques, making it a scalable and efficient solution.

---

## Features  
- **Azure Blob Storage Mounting** on Databricks.  
- **PDF Text Extraction** using PyPDF2.  
- **Text Embedding Generation** using Sentence Transformers.  
- Robust **Error Handling and Validation**:
  - Mount point verification.  
  - PDF file existence checks.  
  - Text extraction and embedding validation.

---

## Installation  

Follow these steps to set up the project:

1. **Clone this repository**:  
   ```bash
   git clone https://github.com/<your-username>/PDF-Text-Embedding-Generator.git
   cd PDF-Text-Embedding-Generator
2. Configure Azure Blob Storage credentials in your Databricks environment.

3. Mount the Blob Storage container to Databricks using the `mount_storage.py` script.

4. Install the required Python dependencies:
   
```bash
pip install PyPDF2 sentence-transformers azure-storage-blob
```

## Usage

1. Upload PDF files to the specified Azure Blob Storage container.

2. Mount the Blob Storage container by executing the mounting script:

```python
# Example:
mount_blob_storage(storage_account_name, container_name, mount_point)
Run the text extraction function from text_extraction.py to extract text from the uploaded PDF files.
```

3. Run the text extraction function from text_extraction.py to extract text from the uploaded PDF files.

4. Generate embeddings using `embedding_gen.py`.
   
5. Process the results as per your application’s requirements.

## Project Structure

```text
├── mount_storage.py      # Storage mounting functions
├── text_extraction.py    # PDF text extraction
├── embedding_gen.py      # Embedding generation
└── validation.py         # Validation functions
```

## Error Handling

The project includes robust error handling mechanisms to ensure a seamless workflow:

1. **Mount Point Validation**: Ensures that the Blob Storage container is mounted successfully.
2. **PDF File Existence Check**: Verifies that PDF files exist in the Blob Storage container.
3. **Text Extraction Verification**: Validates successful extraction of text from PDF files.
4. **Embedding Generation Validation**: Confirms the integrity of generated embeddings.
