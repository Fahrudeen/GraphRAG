# GraphRAG: Graph-based Retrieval Augmented Generation for Supply Chain Management

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fahrudeen/GraphRAG/blob/master/notebooks/graphrag_pipeline.ipynb)

---

## 📝 Project Overview

**GraphRAG** is a demonstration of Graph-based Retrieval Augmented Generation (RAG) for intelligent supply chain management. This project integrates **Neo4j** graph databases with advanced **LLM APIs (Groq)**, enabling natural language queries over a rich supply chain knowledge graph—cars, features, parts, suppliers, and more.

---

## 📁 Directory Structure
```
GraphRAG/
├── data/ # CSV files for graph nodes and relationships
├── notebooks/
│ └── graphrag_pipeline.ipynb
├── requirements.txt
├── .gitignore
├── .env.example
├── LICENSE
└── README.md
```

---

## Features

- **Knowledge Graph Construction** from supply chain data (cars, features, parts, suppliers)
- **Natural Language to Cypher** conversion using Groq’s LLM API
- **Context-Aware LLM Responses** grounded in graph data
- **Modular, Extensible Pipeline** for building and querying supply chain knowledge graphs

---

## Setup & Installation

### 1. Clone the Repository
```
git clone https://github.com/fahrudeen/GraphRAG.git
cd GraphRAG
```

### 2. Configure Environment Variables

Copy `.env.example` to `.env` and fill in your confidential values:
```
NEO4J_URI=bolt://localhost:7687 # Or your AuraDB URI
NEO4J_USERNAME=neo4j
NEO4J_PASSWORD=your_password_here
GROQ_API_KEY=your_groq_api_key_here
DATA_PATH=./data/
```

### 3. Install Python Dependencies
```
pip install -r requirements.txt
```


### 4. Prepare Data

Place all required data CSVs for nodes/edges in the `data/` directory:
- `nodes_car_model.csv`
- `nodes_feature.csv`
- `nodes_part.csv`
- `nodes_supplier.csv`
- `with_feature.csv`
- `is_composed_of.csv`
- `is_supplied_by.csv`

*Ensure filenames match notebook expectations.*

---

## Usage

1. **Open Jupyter or Colab**

   - [Open in Colab](https://colab.research.google.com/github/fahrudeen/GraphRAG/blob/master/notebooks/graphrag_pipeline.ipynb)
   - Or: Launch `notebooks/graphrag_pipeline.ipynb` in Jupyter

2. **Run All Cells**

   Make sure all cells run from top to bottom. Ensure environment variables are set.

3. **Ask Queries**

   At the notebook’s end, use the input cell to ask questions such as:
   - `"What features does Model A have?"`
   - `"Who supplies brake parts?"`
   - `"Compare Model A and Model C"`

4. **Update and Extend**

   Add new CSVs, entities, or relationships as needed and re-run respective notebook cells.

---

## Example Queries

- `"Show all features of car model C1000"`
- `"List suppliers for the ABS part"`
- `"Parts used in the sunroof feature"`

---

## Project Status & Roadmap

**Current:**  
 End-to-end supply chain knowledge graph with LLM-RAG querying.

**Planned:**
- Interactive graph visualization (`NetworkX`, `pyvis`, etc.)
- Enhanced filtering and query expansion
- Support for additional supply chain entities and relationships

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🤝 Contributing

Contributions and suggestions are welcome!  
- Open issues or pull requests.

---

## 📚 References

- [Neo4j Documentation](https://neo4j.com/docs/)
- [Groq API](https://groq.com/)
- [LLM + Knowledge Graph Patterns](https://neo4j.com/developer/)

---

**Contact:** [fahrudeen001@gmail.com](mailto:fahrudeen001@gmail.com)


