# Healthcare Supply Chain Optimization

> **Note:** Despite the repository name, this project is **not** an accounting application. It implements healthcare supply chain optimization using generative AI, reinforcement learning, route optimization, and blockchain smart contracts.

## Overview

A Python desktop application (Tkinter GUI) that orchestrates a multi-step pipeline for healthcare supply chain management:

1. Collect patient and healthcare data via forms
2. Preprocess disease patterns, seasonal fluctuations, and patient address data
3. Train models using Conditional GANs (CGAN) with Krill Herd Optimization (KHO)
4. Apply Q-learning for inventory and supply chain decisions
5. Optimize delivery routes with Dijkstra's algorithm (NetworkX)
6. Interact with Ethereum smart contracts for supply chain transparency (Ganache)

## Components

| Module | Purpose |
|--------|---------|
| `Main_View.py` | Tkinter GUI orchestrating the pipeline |
| `Data.py`, `Data1.py`, `Data2.py` | Patient demographics and healthcare data collection |
| `Preprocess.py` | Data cleaning and formatting |
| `Train_the_Model.py` | CGAN + KHO model training (TensorFlow/Keras) |
| `Q_learning.py` | Q-learning agent for supply chain inventory decisions |
| `Route_Optimization.py` | Dijkstra's algorithm for delivery route optimization |
| `Consensus_mechanism.py` | Ganache/Ethereum RPC interaction |
| `contracts/` | Solidity smart contracts (`SupplyChain.sol`, `Products.sol`, `Users.sol`) |
| `data/` | CSV datasets (patient addresses, disease patterns, seasonal fluctuations) |

## Tech Stack

- Python (pandas, scikit-learn, TensorFlow/Keras, NetworkX, PySpark, tkinter)
- Solidity smart contracts (Truffle/Ganache)
- Ganache local Ethereum node (`http://127.0.0.1:7545`)

## Prerequisites

- Python 3 with dependencies: pandas, scikit-learn, tensorflow, networkx, matplotlib, seaborn, pyspark, plyer, tkcalendar
- [Node.js](https://nodejs.org/) and [Truffle](https://trufflesuite.com/) for smart contract deployment
- [Ganache](https://trufflesuite.com/ganache/) running locally for blockchain features

## Usage

```bash
# Start Ganache, then deploy contracts
truffle migrate

# Run the main application
python Main_View.py
```

The GUI provides buttons to step through data collection, preprocessing, model training, Q-learning, route optimization, and consensus mechanisms.

## Data

Sample CSV files in `data/` include patient addresses, disease patterns, and seasonal fluctuation records used for preprocessing and analysis.
