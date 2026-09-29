# neo4ds

Jupyter notebooks for learning Neo4j graph data science with Python — from a first connection all the way to node embeddings and supervised classification on a graph.

## Contents

### `Getting Started Neo4j with Python (For Complete Beginners).ipynb`

The on-ramp. Load a dataset into Neo4j, run graph queries, and visualize results — no prior Neo4j experience assumed. Uses `py2neo` against a local instance.

### `titanic/` — Graphing the Titanic

Builds a knowledge graph out of the Titanic passenger manifest and applies Neo4j Graph Data Science (GDS):

- `titanic/data/` — node and relationship CSVs (`titanic.csv` → one node per passenger, plus derived `nodes.csv` / `relationships.csv`)
- `GraphDataScience.pptx` — deck explaining the modeling choices
- `Graphing the Titanic.ipynb` — the walkthrough: import → project → embed → classify

The interesting part is the feature engineering. Class, sex, and port of embarkation are turned into one-hot graph relationships so the GDS node classifier can work on a plain passenger–passenger similarity graph rather than a flat table.

### `graphml/dallas.graphml`

A road-network graph used as sample input for import experiments.

### `extra/`

Rendered images used by the notebooks.

## Setup

```bash
pip install jupyter neo4j py2neo pandas numpy scikit-learn
```

The GDS section additionally needs the [Graph Data Science library](https://neo4j.com/docs/graph-data-science/current/) installed in your Neo4j instance. Point the notebooks at your database with the connection details at the top of each notebook.

## License

MIT
