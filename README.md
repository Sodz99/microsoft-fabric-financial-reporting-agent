# Microsoft Fabric Project to Build a Financial Reporting Agent

The primary aim of this project is to utilize Microsoft Fabric for consolidating wealth and financial data into a centralized warehouse, enabling seamless data integration, storage, and retrieval.

## Overview
The project is designed to leverage the powerful capabilities of Microsoft Fabric to streamline and modernize financial data handling and analysis in the wealth management domain. Microsoft Fabric's unified platform offers tools for centralizing diverse financial datasets—ranging from client portfolios and transaction histories —into a centralized OneLake data warehouse. This consolidation not only simplifies data management but also ensures seamless access to structured and unstructured data through its versatile lakehouse and warehouse architecture. Using Dataflow Gen2, the project automates the transfer of data from disparate sources into Fabric’s data warehouse, enabling scalable and efficient storage.

## Data
The dataset includes comprehensive financial information crucial for wealth management:

1. Wealth Assets Data: Details of client portfolios, including asset classes such as stocks, bonds, real estate, and alternative investments.
2. Financial Records: Transaction histories, and investment portfolios for a complete financial overview.

_Data is not included in this repository._

## Approach
- Set Up the Microsoft Fabric Environment
- Data Preparation and Consolidation ○ Use Dataflow Gen2 to copy and import data from the database into Microsoft Fabric ○ Organize data into a format within OneLake (lakehouse and warehouse architecture)
- Data Storage in Microsoft Fabric ○ Create views and tables in the data warehouse to represent structured data (e.g., portfolio summaries, transaction details) ○ Link the data lakehouse and warehouse for data querying
- Integration with SQL and Python ○ Set up an SQL connection string for querying data from Microsoft Fabric ○ Write Python scripts to connect to the SQL engine and retrieve data using the connection string
- Build a Retrieval-Augmented Generation (RAG) System ○ Build a RAG system using the data schema from the Fabric warehouse to contextualize large language models (LLMs) ○ Use LLMs (e.g., GPT-4) to enable natural language understanding of financial data ○ Validate data accuracy and consistency across OneLake and the data warehouse
- Develop a Querying Interface ○ Implement a text-to-SQL conversion layer using Vanna AI for natural language queries ○ Use Python to process SQL queries, interact with the Fabric warehouse, and retrieve results ○ Visualize query outputs using the Vanna AI dashboard

Modular code overview:

Once you unzip the modular_code.zip file, you can find the following: ├─ CreateDataWarehouse │   ├─ Insert to SQL.py │   ├─ InsertToSQL.py │   └─ SQL │       ├─ create_tables.sql │       ├─ create_views_sql.sql │       ├─ Proc.json │       ├─ stored_procedures.sql │       ├─ Tables.json │       └─ Views.json ├─ LangchainFabrics │   ├─ LangChainFabrics.py │   └─ TestConnectionFabrics.py ├─ RAGToSQL │   ├─ chroma.sqlite3 │   ├─ FabricsRAG.py │   ├─ Helper │   │   ├─ Credentials.py │   │   ├─ FabricsConnection.py │   │   ├─ VannaObject.py │   │   ├─ __init__.py │   ├─ InferenceRAG.py │   ├─ TrainingRAG-Artifact │   │   ├─ .DS_Store │   │   ├─ Documentation.txt │   │   ├─ Proc.json │   │   ├─ Tables.json │   │   ├─ training_summary.csv │   │   └─ Views.json │   ├─ training_summary.csv │   ├─ TrainRAG.py │   └─ VisualizeRAG.py ├─ Readme.md └─ requirements.txt

Here is a brief information on the files:

## Tech stack
➔ Language: Python 3.10 ➔ Libraries: pandas, numpy, Azure, langchain, Open AI, Vanna AI ➔ Cloud Platform Components: Microsoft Fabric (OneLake, LakeHouse, Fabrics Datawarehouse) ➔ Model: Retrieval-Augmented Generation (RAG) with GPT-4

➔ Cloud Platform: Azure ➔ Dashboard Framework: Vanna AI integrated with Microsoft Fabric

## How to run
```bash
pip install -r Code Folder/requirements.txt
```

## Project structure
```
.gitignore
Code Folder/
  CreateDataWarehouse/
    Insert to SQL.py
    InsertToSQL.py
    SQL/
  LangchainFabrics/
    LangChainFabrics.py
    TestConnectionFabrics.py
  RAGToSQL/
    FabricsRAG.py
    Helper/
    InferenceRAG.py
    TrainRAG.py
    VisualizeRAG.py
  Readme.md
  requirements.txt
README.md
```

## Credits
Based on a ProjectPro guided project.
