Academic RAG Agent: Your Personal Course Assistant
An end-to-end Retrieval-Augmented Generation (RAG) pipeline built to automate the retrieval of information from dense academic materials. This agent acts as a high-fidelity expert tutor, answering complex university-level questions while citing specific source documents.




🚀 Features

Automated Academic Research: Eliminates the manual task of searching through hundreds of pages of textbooks and lecture slides.


RAG Architecture: Integrates external knowledge retrieval with a fine-tuned "Generator" model to ensure answers are based solely on your documents.



Deep Document Processing: Ingests 14 PDF files (971 pages) , splitting them into 2,739 distinct text chunks for granular search.


Vector Search: Utilizes a local FAISS database for high-speed similarity searches using all-MiniLM-L6-v2 embeddings.




LLM-as-a-Judge Evaluation: Features an automated evaluation suite to measure groundedness and helpfulness.

🛠️ Tech Stack

Orchestration: LangChain 


Generative Models: Google Gemini 2.5 Flash (Preview) 


Vector Database: FAISS (Facebook AI Similarity Search) 


Embeddings: all-MiniLM-L6-v2 


PDF Parsing: PyMuPDF 

📂 Project Structure

NOtes.ipynb: The main project notebook containing the pipeline, fine-tuning data, and evaluation suite.



my_course_notes_db/: Local vector database containing the indexed document chunks.


tutor_finetuning_data.jsonl: Curated dataset for training the model to act as a grounded expert tutor.


Source Data: 14 integrated PDFs covering Chemical Engineering (Reactor Design, Process Control) and AI Ethics.

📊 Evaluation Metrics
The system uses a strict "LLM-as-a-Judge" framework to score responses on a scale of 1-5:


Average Groundedness: 5.0/5.0 — The agent successfully avoids hallucinations by sticking strictly to the context.



Average Helpfulness: 4.75/5.0 — The agent provides complete and direct answers to academic queries.
