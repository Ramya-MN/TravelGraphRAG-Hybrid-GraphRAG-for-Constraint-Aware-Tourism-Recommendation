# Graph-RAG Module

This folder contains the **Graph-RAG (GRAG) component** of **TravelGraphRAG: Hybrid Graph-RAG for Constraint-Aware Tourism Recommendation**.

The module performs constraint-aware retrieval by combining **semantic similarity with knowledge-graph-based retrieval** to identify relevant tourism destinations from the structured travel knowledge graph.

## Pipeline

```text
User Query
    ↓
Query & Constraint Extraction
    ↓
Semantic Retrieval + Graph Retrieval
    ↓
Hybrid Score Fusion
    ↓
Constraint Validation
    ↓
Evidence Path Extraction
    ↓
Final Ranked Destinations
```

## Main Components

* **Knowledge Graph Construction**
  Builds the tourism knowledge graph from destination attributes and relationships.

* **Semantic Retrieval**
  Retrieves destinations based on query–destination similarity.

* **Graph Retrieval**
  Uses graph relationships and explicit travel constraints to retrieve structurally relevant destinations.

* **Hybrid Retrieval**
  Combines semantic and graph-based retrieval scores for ranking.

* **Constraint Validation**
  Filters candidates that do not satisfy the required travel constraints.

* **Evidence Extraction**
  Identifies graph paths supporting the retrieved destinations.

## Input

A natural-language tourism query containing preferences or constraints such as:

* Location
* Season
* Budget
* Trip type
* Accessibility
* Activities

Example:

```text
Suggest a budget-friendly winter adventure destination in South India.
```

## Output

The GRAG module returns a ranked set of candidate destinations together with:

* Retrieval score
* Constraint satisfaction
* Supporting graph evidence
* Evidence paths

## Scope

This folder contains **only the Graph-RAG retrieval component** of the TravelGraphRAG framework.

The following components are **not included**:

* LLM-based generation
* Prompt engineering
* LLM fine-tuning
* Response generation

## Running

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Run the Graph-RAG pipeline:

```bash
python <main_grag_script>.py
```

The implementation retrieves and ranks destinations using the hybrid Graph-RAG approach described in the paper.

## Reference

This implementation corresponds to the Graph-RAG methodology described in:

**TravelGraphRAG: Hybrid Graph-RAG for Constraint-Aware Tourism Recommendation**
