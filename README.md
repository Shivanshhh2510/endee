# SentinelAI — AI Data Copilot using Endee Vector Database

SentinelAI is an AI-powered Business Intelligence assistant that enables users to ask questions about datasets in natural language and automatically generate insights, visualizations, and machine learning predictions.

This project integrates the **Endee Vector Database** to power semantic search and retrieval for AI-driven analytics using a Retrieval Augmented Generation (RAG) architecture.

The goal is to make advanced data analysis accessible to non-technical users through natural language interaction.

---

# Project Overview

Traditional data analysis tools require technical knowledge of SQL, Python, or BI platforms. SentinelAI removes this barrier by allowing users to simply ask questions about their data.

Examples:

- "Show sales by region"
- "Which category has highest profit?"
- "Show monthly sales trend"
- "Show profit distribution"

The system automatically:

- Understands the intent of the question
- Retrieves relevant dataset context using vector search
- Generates charts
- Produces AI insights and explanations

---

# Key Features

### AI Data Copilot
Users can ask natural language questions about their dataset and receive charts, insights, and explanations instantly.

### Automated Visualization Engine
The system dynamically generates multiple chart types:

- Bar charts
- Line charts
- Scatter plots
- Histograms
- Pie charts
- Area charts
- Heatmaps

### Intelligent Dataset Profiling
Automatic analysis of:

- Numeric columns
- Categorical columns
- Missing values
- Duplicate rows
- High-cardinality features

### AutoML Model Training
Automatically detects the target variable and trains multiple ML models to identify the best performing one.

### AI Insights Generation
Charts are accompanied by AI-generated explanations so non-technical users can easily understand the findings.

### Dashboard Builder
Users can save generated charts and combine them into reusable dashboards.

### RAG-based Query Engine
SentinelAI uses **Retrieval Augmented Generation** to retrieve relevant dataset context and generate accurate responses.

---

# How Endee Vector Database is Used

Endee is used as the vector database powering semantic retrieval.

Workflow:

1. Dataset content is converted into embeddings
2. Embeddings are stored in the Endee vector store
3. User queries are converted into embeddings
4. Endee retrieves the most relevant dataset context
5. The AI engine generates insights using retrieved context

This allows SentinelAI to perform intelligent data exploration and question answering.

---

# System Architecture
User
│
│ Natural Language Question
▼
Streamlit Frontend (UI)
│
▼
FastAPI Backend
│
├─ Intent Detection
├─ Chart Generator
├─ Query Engine
│
▼
Embedding Generator
│
▼
Endee Vector Database
│
▼
RAG Query Engine
│
▼
AI Copilot Response
│
▼
Charts + Insights + Suggestions


---

# Project Structure
SentinelAI
│
├── app/
│ ├── ai/ # AI copilot logic
│ ├── analytics/ # chart & query engine
│ ├── automl/ # model training
│ ├── chat/ # intent detection & planner
│ ├── ingestion/ # dataset loader
│ ├── rag/ # retrieval engine
│ ├── vector/ # Endee vector integration
│ └── routes/ # API endpoints
│
├── frontend/
│ └── app.py # Streamlit UI
│
├── data/ # sample datasets
├── models/ # trained ML models
├── reports/ # generated reports
├── storage/ # database storage
│
├── requirements.txt
└── README.md


---

# Tech Stack

### Backend
- Python
- FastAPI

### Frontend
- Streamlit

### Machine Learning
- Scikit-learn
- XGBoost

### Visualization
- Plotly

### Vector Search
- Endee Vector Database
- FAISS

### Data Processing
- Pandas
- NumPy

---

# Installation

Clone the repository:


git clone https://github.com/YOUR_USERNAME/endee.git

cd endee


Install dependencies:


pip install -r requirements.txt


---

# Running the Backend

Start the FastAPI server:


python app/main.py


or


uvicorn app.main:app --reload


Backend will run on:


http://127.0.0.1:8000


---

# Running the Frontend

Start the Streamlit app:


streamlit run frontend/app.py


The app will open at:


http://localhost:8501


---

# Example Queries

Users can ask questions like:

- Show sales by region
- Which category has highest profit
- Show monthly sales trend
- Show profit distribution
- Show correlation between sales and profit

---

# Example Output

SentinelAI generates:

- Interactive visualizations
- AI-generated insights
- Suggested follow-up questions
- Automated dashboards

This allows users to quickly understand complex datasets without writing code.

---

# Use Cases

SentinelAI can be used for:

- Business intelligence
- Sales analytics
- Data exploration
- Automated reporting
- Decision support systems

---

# Future Improvements

- Multi-dataset analysis
- Real-time data streaming
- Advanced AI reasoning agents
- Enterprise dashboard export
- Natural language SQL generation

---

# Author

Shivansh Mishra

BTech Computer Science Engineering

AI / Data Science / Machine Learning

---

# License

This project builds upon the Endee open-source vector database.

Original repository:
https://github.com/endee-io/endee
