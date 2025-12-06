AI Research Agent

AI Research Agent is an intelligent research assistant that automatically analyzes PDF and Word documents, generates structured research plans, and produces concise summaries based on relevant content. It is designed to accelerate literature review, streamline research workflows, and help users extract insights efficiently.

This project is ideal for academics, students, and professionals who need a fast and reliable way to organize information from multiple documents.

Problem Statement

Research often involves sifting through large volumes of documents to extract relevant information, which is time-consuming and prone to human error. AI Research Agent addresses this problem by:

Automatically reading and indexing PDFs and Word documents.

Retrieving the most relevant content for a given query.

Generating a structured research plan and summary for rapid understanding.

Value Proposition

AI Research Agent saves time, reduces manual effort, and provides actionable insights by:

Streamlining document analysis for research projects.

Offering AI-generated plans and summaries to guide research decisions.

Allowing teams to focus on critical thinking rather than manual review.

Project Structure
ai-research-agent/
│
├─ main.py
├─ test_agent_run.py
├─ .env
├─ .env.example
├─ .gitignore
├─ README.md
├─ requirements.txt
├─ agent/
│   ├─ __init__.py
│   ├─ _config.py
│   └─ agent.py
├─ rag/
│   ├─ __init__.py
│   ├─ index_documents.py
│   ├─ openai_embed.py
│   └─ retriever.py
│   ├─ docs/
│   └─ store/
├─ skills/
│   ├─ __init__.py
│   ├─ planner.py
│   └─ summarize.py
├─ vector_store/
│   ├─ __init__.py
│   └─ vector_store.py
└─ venv/

Key Features

Document Indexing: Converts PDFs and Word documents into vector embeddings and stores them in FAISS.

Smart Retrieval: Finds the most relevant documents for any research query.

Research Planning: Generates concise, structured research plans using retrieved content.

Summarization: Produces clear summaries in bullet points or short paragraphs.

Test Mode: A script simulates documents to validate agent workflow without real files.

Technologies and Libraries

Python 3.10+

FAISS for vector storage and search

PyPDF2 for PDF text extraction

python-docx for Word document reading

Semantic Kernel for AI-driven text generation

OpenAI GPT API (optional) for advanced summaries and planning

Installation

Clone the repository:

git clone https://github.com/<your-username>/ai-research-agent.git
cd ai-research-agent


Create a virtual environment:

python -m venv venv
source venv/bin/activate  # Linux / macOS
venv\Scripts\activate     # Windows


Install dependencies:

pip install -r requirements.txt
pip install PyPDF2 python-docx faiss-cpu


(Optional) Add OpenAI API Key:

OPENAI_API_KEY=your_api_key_here

Usage
Running with Real Documents

Place PDF or Word files in rag/docs/.

Execute the agent:

python main.py


Enter a research question.

View the research plan and summary in the console.

Running the Test Script
python test_agent_run.py


Automatically generates example PDF and Word files.

Runs the agent to produce a research plan and summary.

Useful for testing or demonstration purposes.

Example Output
Research question: What are the latest AI techniques for document summarization?

Searching for relevant information...
Retrieved 5 relevant documents.

Generating research plan...
Plan summary:
- Review current AI summarization models
- Compare extractive vs abstractive methods
- Identify datasets commonly used
- Highlight evaluation metrics
- Suggest applications in document research

Producing final report...
Summary:
- Bullet 1: ...
- Bullet 2: ...
- Bullet 3: ...

Impact

By automating research workflows, AI Research Agent allows users to:

Reduce time spent on literature review.

Extract actionable insights efficiently.

Focus on decision-making and analysis rather than manual reading.

This project demonstrates practical AI applications in research and information management.

License

This project is licensed under the MIT License.