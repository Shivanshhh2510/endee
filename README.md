# SentinelAI — AI Data Copilot using Endee Vector Database

SentinelAI is an AI-powered Business Intelligence assistant that enables users to ask questions about datasets in natural language and automatically generate insights, visualizations, and machine learning predictions.

This project integrates the **Endee Vector Database** to power semantic search and retrieval for AI-driven analytics using a **Retrieval Augmented Generation (RAG)** architecture.

The goal is to make advanced data analysis accessible to non-technical users through natural language interaction.

---

# Project Overview

Traditional data analysis tools require technical knowledge of SQL, Python, or BI platforms. SentinelAI removes this barrier by allowing users to simply ask questions about their data.

Example queries:

- Show sales by region  
- Which category has highest profit  
- Show monthly sales trend  
- Show profit distribution  

The system automatically:

- Understands the intent of the question
- Retrieves relevant dataset context using vector search
- Generates charts and visualizations
- Produces AI insights and explanations

---

# Key Features

## Dataset Upload

- Upload **CSV or Excel datasets**
- Automatic **data profiling**

Detection includes:

- Numeric columns
- Categorical columns
- Datetime columns
- Missing values
- High cardinality features

---

## AutoML Model Training

Automatically trains multiple machine learning models:

- Logistic Regression
- Random Forest
- Extra Trees
- XGBoost
- LightGBM

SentinelAI automatically:

- Detects the problem type
- Selects the target column
- Evaluates model performance
- Displays feature importance

---

## AI Data Copilot

Users can ask questions about their dataset.

Examples:

- Show sales by region
- Which category has highest profit
- Explain this dataset

The system performs:

1. Intent detection  
2. Analytical query execution  
3. RAG retrieval from the vector database  
4. AI reasoning using an LLM  

---

## Dashboard Builder

Users can save generated charts into custom dashboards.

Features:

- Save charts generated from AI insights
- Create multiple dashboards
- Persistent storage using SQLite

---

# System Workflow

1. User uploads a dataset (CSV or Excel)
2. SentinelAI performs automatic dataset profiling
3. Dataset context is embedded and stored in the vector database
4. User asks a question in natural language
5. Relevant dataset context is retrieved using vector search
6. Analytical queries generate insights and charts
7. AI produces explanations using an LLM

---

# Project Architecture

```
Frontend
   │
   │ Streamlit UI
   ▼
FastAPI Backend
   │
   ├── Authentication
   ├── Dataset Ingestion
   ├── AutoML Engine
   ├── Analytical Query Engine
   └── RAG Query Engine
          │
          ▼
Vector Database (Endee)
          │
          ▼
LLM Reasoning (Gemini API)
```

---

# Application Screenshots

## Dataset Upload and Model Training


<img width="1184" height="1009" alt="image" src="https://github.com/user-attachments/assets/91f98a5c-6127-4e06-bf53-9c46305ff49d" />

---

## Dataset Intelligence and Model Insights


<img width="1600" height="1043" alt="image" src="https://github.com/user-attachments/assets/80456bc2-2e03-4ab4-bce4-0dfcb8ec12f2" />

<img width="1600" height="588" alt="image" src="https://github.com/user-attachments/assets/f2819727-6d09-4c70-a3d6-e6ea983e8183" />

<img width="1600" height="561" alt="image" src="https://github.com/user-attachments/assets/c86a2fd4-0dca-490d-bde5-45efa2235dbc" />

<img width="1600" height="650" alt="image" src="https://github.com/user-attachments/assets/fc5ab99b-54ee-4a8f-91a1-64d04034ac62" />

<img width="1600" height="697" alt="image" src="https://github.com/user-attachments/assets/a1da1eea-9067-4625-8ae4-6891257f9c2f" />


---


## AI Data Copilot Query Interface


<img width="1474" height="845" alt="image" src="https://github.com/user-attachments/assets/abde026a-e7cb-4c88-b450-088886288af5" />

<img width="1600" height="733" alt="image" src="https://github.com/user-attachments/assets/53c2b26f-15ce-4510-aba3-7475554e8486" />

<img width="1600" height="624" alt="image" src="https://github.com/user-attachments/assets/84266d3d-faa7-47d2-a216-bf044ae96259" />

<img width="1600" height="560" alt="image" src="https://github.com/user-attachments/assets/cff68975-2139-49da-be3d-652c14e96393" />

<img width="1600" height="527" alt="image" src="https://github.com/user-attachments/assets/2ab617be-1271-40bf-ab26-dcf09c529cf5" />

---


## Custom Dashboard Builder


<img width="1600" height="754" alt="image" src="https://github.com/user-attachments/assets/f71280e5-f85d-49c6-a912-da9254aac91e" />


---

# Tech Stack

## Frontend

- Streamlit  
- Plotly  
- Pandas  

## Backend

- FastAPI  
- Python  

## Machine Learning

- Scikit-Learn  
- XGBoost  
- LightGBM  
- Optuna  
- SHAP  

## AI + RAG

- Gemini API  
- Vector Embeddings  
- Retrieval Augmented Generation  

## Vector Database

- Endee Vector DB (Docker)

## Storage

- SQLite

---

# How to Run the Project Locally

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/sentinelai.git
cd sentinelai
```

---

## 2. Create Virtual Environment

```bash
python -m venv venv
```

Activate environment:

**Windows**

```bash
venv\Scripts\activate
```

**Mac / Linux**

```bash
source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 4. Run Endee Vector Database (Docker)

Make sure **Docker Desktop is running**.

```bash
docker run -p 8080:8080 endeeio/endee-server
```

---

## 5. Set Environment Variables

Create a `.env` file:

```
GEMINI_API_KEY=your_gemini_api_key
```

---

## 6. Start Backend Server

```bash
uvicorn app.main:app --reload
```

Backend runs at:

```
http://127.0.0.1:8000
```

---

## 7. Run Streamlit Frontend

```bash
cd frontend
streamlit run app.py
```

Open in browser:

```
http://localhost:8501
```

---

# Project Structure

```
sentinelai
│
├── app
│   ├── ai
│   ├── analytics
│   ├── automl
│   ├── ingestion
│   ├── rag
│   ├── routes
│   └── vector
│
├── frontend
│   └── app.py
│
├── storage
│
├── requirements.txt
└── README.md
```

---

# Future Improvements

- Multi-dataset support  
- Chat history persistence  
- User workspace dashboards  
- Advanced chart recommendations  
- Streamlit Cloud deployment  

---

# Author

**Shivansh Mishra**  
AI / Data Science Engineer  
B.Tech Computer Science  

---

⭐ If you like this project, consider giving the repository a star on GitHub.
