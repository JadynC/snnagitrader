/snnagitrader/

│

├── main.ipynb                         # Single runtime notebook for training, testing, and evaluation

├── README.md                          # Project overview and usage instructions

├── requirements.txt                   # Python dependencies for local/Delta setup

├── .gitignore                         # Standard ignores for Python + Colab

│

├── /data/                             # Order book data (or streamed data API connectors)

│   ├── sample_orderbook.csv           # Example data file or placeholder

│   └── preprocessor.py                # Preprocessing raw LOB to usable input format

│

├── /spike_encoder/                    # Spike encoding logic

│   ├── __init__.py

│   ├── rate_encoder.py                # Rate-based encoding

│   ├── latency_encoder.py             # Latency-based encoding

│   └── event_encoder.py               # Event-triggered encoder

│

├── /snn/                              # Spiking neural network architecture

│   ├── __init__.py

│   ├── layers.py                      # Core neuron model (e.g., LIF neurons)

│   ├── network.py                     # Full SNN architecture setup

│   └── plasticity.py                  # STDP and R-STDP learning rules

│

├── /environment/                      # Simulated trading environment

│   ├── __init__.py

│   ├── lob_simulator.py               # Matching engine, fills, queue logic

│   ├── latency_model.py               # Models execution/response latency

│   └── reward_function.py             # All reward/penalty shaping

│
├── /agent/                            # Agent class wrapper (connects SNN to environment)

│   ├── __init__.py

│   └── trader_agent.py                # Main agent loop: observe → encode → spike → act

│

├── /evaluation/                       # Evaluation and strategy discovery tools

│   ├── __init__.py

│   ├── logger.py                      # Tracks agent behaviour, trades, firing activity

│   ├── clustering.py                  # Feature extraction + dimensionality reduction + clustering

│   └── strategy_analysis.py           # Compares clusters to known strategies, visualizes

