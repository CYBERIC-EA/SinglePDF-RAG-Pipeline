# PDF-RAG-Pipeline

The main goal of the project is to develop a system capable of retrieving relevant information from a document corpus and generating responses to user queries based on the retrieved information.

Key Components:

PDF Reader: The project utilizes the pypdf library to extract text from PDF documents, enabling the system to access and analyze textual content.
Text Splitter: To manage large documents effectively, the langchain library's CharacterTextSplitter is employed to divide the text into smaller, manageable chunks.

Embedding Documents: The project utilizes the FAISS library to convert text chunks into numerical representations (embeddings), facilitating efficient similarity searches and retrieval of relevant document chunks.

Question Answering (QA) Chain: A pre-trained question answering model, powered by the Ollama language model, is integrated into the pipeline. This model can understand natural language queries and extract relevant information from document chunks.

Workflow:
1. Document Processing: Text is extracted from PDF documents and split into smaller chunks to facilitate efficient processing.
2. Embedding Generation: Converts text chunks into numerical representations using FAISS, enabling similarity-based retrieval.
3. Query Processing: User queries are processed, and relevant document chunks are retrieved using similarity search techniques.
4. Question Answering: The retrieved document chunks, along with the user query, are provided as input to the pre-trained question answering model (Ollama). The model analyzes the input data and generates responses based on the content of the document chunks and the query.
5. Response Generation: The system outputs the generated response, providing answers to user queries based on the analyzed document content.
