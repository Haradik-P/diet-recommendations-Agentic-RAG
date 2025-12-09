Nutrition RAG Pipeline (LangChain + Chroma + LangGraph)

This project builds a diet recommendation system using:
   1. CSV → Single merged document
   2. OpenAI embeddings
   3. ChromaDB (local vector storage)
   4. LangGraph pipeline (Profiling → Retrieval → Diet Plan Generation)

For Setup
1. Install Dependencies
pip install -r requirements.txt
2. Add API Key
in .env add your api key of open Ai
OPENAI_API_KEY=your_key

#  How It Works

1. Loads 2 CSV files:
nutrition_knowledge_base.csv
diet_recommendations_dataset.csv

2. Converts all rows into one combined document.

3. Creates a local Chroma vector DB:
./chroma_db


4. Builds a LangGraph workflow:
User Profile → Calculate Metrics → Retrieve Docs → Generate Diet Plan


5. Takes user input and give output :
Calculated calories
Custom diet plan
Run

Output Example
Calculated Target Calories: 2100
---------------------------------------------------
<generated diet plan>
