# Agentic Database Creator

**⚠️ Warning: This project is still under active development. APIs and configurations may change.**

## 📜 Overview

The Agentic Database Creator is a powerful, multi-agent system designed to build structured datasets from the web. It employs two distinct approaches for data collection: a systematic, keyword-based search and an autonomous, agentic search. While currently focused on Indian agriculture, the system is designed to be generalized for any domain through a simple configuration file.

This tool is ideal for researchers, data scientists, and developers who need to create specialized datasets for tasks like training Retrieval-Augmented Generation (RAG) models.

### Key Features

*   **Dual Approaches:** Choose between a precise, keyword-based search or a broad, autonomous exploration.
*   **Highly Configurable:** Easily adapt the system to your specific needs.
*   **Scalable:** Run multiple agents in parallel to accelerate data collection.
*   **Data Validation:** Built-in tools to ensure data quality and relevance.
*   **Extensible:** Designed to be easily extended with new data sources and processing logic.
*   **Comprehensive Documentation:** Includes detailed guides and diagrams to get you started.

## 🏛️ System Architecture

The system is composed of two main components, each with its own set of agents and configurations:

```
                      +-------------------------+
                      |   Internet Sources      |
                      +-----------+-------------+
                                  |
                      +-----------v-------------+
                      |     Search Engines      |
                      +-----------+-------------+
                                  |
          +-----------------------+-----------------------+
          |                                               |
+---------v-----------+                         +---------v-----------+
|  Keyword-Based      |                         |  Autonomous Agent   |
|  Search System      |                         |  Search System      |
+---------------------+                         +---------------------+
          |                                               |
          +-----------------------+-----------------------+
                                  |
                      +-----------v-------------+
                      |   Content Processing    |
                      +-----------+-------------+
                                  |
                      +-----------v-------------+
                      |   Data Structuring      |
                      +-----------+-------------+
                                  |
                      +-----------v-------------+
                      |   JSONL Dataset Output  |
                      +-------------------------+
```

## 🚀 Getting Started

### Prerequisites

*   Python 3.9+
*   8GB+ RAM (16GB+ recommended for the autonomous agent approach)
*   A stable internet connection

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/agentic-database-creator.git
    cd agentic-database-creator
    ```

2.  **Install the dependencies:**
    ```bash
    chmod +x setup/install_dependencies.sh
    ./setup/install_dependencies.sh
    ```
    Alternatively, you can install the dependencies manually from the `requirements.txt` files in the `keyword_based_search` and `autonomous_agent_search` directories.

### Running the System

You can run either of the two approaches depending on your needs.

**1. Keyword-Based Search**

This approach is ideal for targeted data collection when you have a clear idea of the topics you want to cover.

```bash
cd keyword_based_search
python src/agriculture_data_curator.py
```

**2. Autonomous Agent Search**

This approach is best for comprehensive, exploratory data collection when you want to build a large and diverse dataset.

```bash
cd autonomous_agent_search
python src/autonomous_agriculture_curator.py
```

## ⚙️ Configuration

Both approaches can be configured by editing their respective `config.yaml` files.

*   **Keyword-Based Search:** `keyword_based_search/config/config.yaml`
*   **Autonomous Agent Search:** `autonomous_agent_search/config/autonomous_config.yaml`

These files allow you to control the number of agents, search parameters, and other settings.

## 🌐 Generalization

While the current focus is on Indian agriculture, the system is designed to be easily generalized to any other domain. In the future, you will be able to specify the domain, search queries, and other parameters in a central configuration file to create datasets for any topic.

## 🤝 Contributing

Contributions are welcome! If you have any ideas for new features, improvements, or bug fixes, please open an issue or submit a pull request.

## 📄 License

This project is licensed under the **Creative Commons Zero v1.0 Universal**. See the `LICENSE` file for more details.
