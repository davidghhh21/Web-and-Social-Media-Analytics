# Web-and-Social-Media-Analytics
# Network Analysis of Academic Collaborations

## Overview
This repository contains an in-depth analysis of **academic collaboration networks** using graph theory and network science techniques. The project focuses on analyzing relationships between researchers based on their collaborations in various research projects. It utilizes **NetworkX**, **community detection algorithms**, and **centrality measures** to gain insights into the structure of academic networks.

## Table of Contents
- [Introduction](#introduction)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Network Construction](#network-construction)
- [Graph Analysis & Community Detection](#graph-analysis--community-detection)
- [Results & Findings](#results--findings)
- [Limitations & Future Work](#limitations--future-work)
- [How to Use](#how-to-use)
- [Dependencies](#dependencies)

## Introduction
Understanding academic collaborations can help institutions and researchers identify **influential contributors, emerging research communities, and interdisciplinary connections**. This project builds and analyzes a network graph where **nodes represent researchers** and **edges represent collaborations** in academic projects.

## Data Preprocessing
The dataset consists of two files:
- **collab_edges.csv**: Contains collaboration data (`Source`, `Target`, `Weight`, `Project`).
- **depart_nodes.csv**: Contains researcher details (`Person`, `Role`).

Data preprocessing steps include:
- Loading datasets into **Pandas DataFrames**.
- Checking for missing values and duplicates.
- Ensuring correct data types for nodes and edges.
- Extracting and formatting key features such as collaboration strength and researcher roles.

## Exploratory Data Analysis (EDA)
EDA was performed to understand:
- **Distribution of collaborations** across different research projects.
- **Role-based participation** (Professors, Associate Professors, Assistant Professors).
- **Network density and connectivity** metrics.

## Network Construction
A **graph-based representation** of the dataset was built using **NetworkX**:
- **Nodes**: Represent researchers with attributes (roles).
- **Edges**: Represent collaborations with weights (strength of collaboration).
- **Graph visualization**: Created using `spring_layout()` and customized for clarity.

## Graph Analysis & Community Detection
Several network science techniques were applied:
- **Degree Centrality**: Identifies researchers with the most collaborations.
- **Betweenness Centrality**: Finds key connectors bridging different groups.
- **Clustering Coefficient**: Measures local collaboration density.
- **Shortest Path Analysis**: Computes communication efficiency between researchers.
- **Community Detection Algorithms**:
  - **Louvain Method** (detects modularity-based research groups)
  - **Girvan-Newman Algorithm** (hierarchical community detection)
  - **Label Propagation** (unsupervised classification of research clusters)

## Results & Findings
Key insights derived from the analysis:
- **Top Collaborators**: Researchers with the highest number of connections.
- **Key Influencers**: Individuals acting as bridges between disciplines.
- **Most Connected Fields**: Research areas with high interdisciplinary participation.
- **Network Structure**: The presence of tightly knit communities vs. loosely connected researchers.

## Limitations & Future Work
- **Data Limitations**: Collaboration data may not capture informal or unpublished work.
- **Scalability**: Larger networks may require optimized algorithms.
- **Future Enhancements**:
  - Expanding dataset to include more institutions.
  - Applying **temporal analysis** to track network evolution over time.
  - Using **Graph Neural Networks (GNNs)** for predictive insights.

## How to Use
1. Clone this repository:
   ```sh
   git clone https://github.com/YOUR_USERNAME/MARK1294-Network-Analysis.git
   cd MARK1294-Network-Analysis
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:
   ```sh
   jupyter notebook
   ```
   Open `MARK1294_Network_Analysis.ipynb` and execute the cells.

## Dependencies
- Python 3.x
- Jupyter Notebook
- Pandas, NumPy
- NetworkX
- Matplotlib, Seaborn
- Community Detection Libraries

## License
This project is under the MIT License.

## .gitignore
```
# Ignore Jupyter notebook checkpoints
.ipynb_checkpoints/

# Ignore temporary files
*.pyc
*.pyo
*.pyd
__pycache__/

# Ignore virtual environment
venv/
.env/

# Ignore dataset files
*.csv
*.xlsx
