# AdaptiveAI — Self-Learning Autonomous Agent Framework

AdaptiveAI is a self-learning autonomous agent system built in Python. It features episodic memory storage, self-evaluating execution rewards, dynamic strategy selection (balancing exploration and exploitation using ML models and contextual multi-armed bandit strategies), and an interactive web interface.

## Features

- **Autonomous Agent Execution Engine:** Executes tasks across code execution, web search, mathematical calculations, and data processing.
- **Episodic Memory & Reward System:** Logs execution metrics, execution time, and evaluates composite reward scores for continuous reinforcement learning.
- **ML Strategy Predictor:** Dynamically retrains machine learning models to choose the optimal reasoning and execution strategy per domain category.
- **Web UI & REST API:** Interactive dashboard built with HTML5, CSS3, and JavaScript, powered by a Python backend server.
- **Automated Benchmarking:** Built-in benchmark suite to demonstrate learning progression over sequential task batches.

## Tech Stack

- **Backend:** Python, FastAPI
- **Frontend:** HTML, CSS, JavaScript
- **Machine Learning:** scikit-learn, NumPy, joblib
- **Data Storage:** SQLite
- **Testing:** pytest

## Directory Structure

```text
├── backend/
│   ├── agent.py
│   ├── app.py
│   ├── core/
│   ├── learning/
│   ├── memory/
│   └── tools/
├── frontend/
│   ├── index.html
│   ├── styles.css
│   └── app.js
├── models/
│   └── ml_strategy_model.pkl
├── tests/
│   └── test_adaptive_agent.py
├── run_demo.py
├── requirements.txt
├── README.md
└── .gitignore
```

## Getting Started

### Prerequisites

- Python 3.8 or later
- Git

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/rajaryan26940-del/AdaptiveAI-Improved.git
   cd AdaptiveAI-Improved
   ```

2. Install dependencies:

   ```bash
   python -m pip install -r requirements.txt
   python -m pip install pytest
   ```

### Running the Demonstration

To run the self-learning agent benchmark:

```bash
python run_demo.py
```

### Running the Web Server & UI

Start the backend API server from the project root:

```bash
python -m backend.app
```

Open the local address shown in the terminal, typically `http://127.0.0.1:8000/`, to access the application.

## Improvements and Testing

This version includes targeted fixes and regression testing:

- Corrected the dashboard's ML accuracy display so an untrained model is not shown with a fabricated default accuracy.
- Fixed repeated bandit reward accumulation during model retraining by rebuilding statistics from stored episodes.
- Updated strategy score labels to display selection scores rather than presenting unnormalized values as probabilities.
- Added a regression test verifying that repeated retraining does not double-count stored bandit rewards.

**Latest local test result:** 5 tests passed.

## Screenshots

The dashboard screenshots can be added below. If you still have the original screenshot image links, preserve them here.

## License

MIT License. Ensure the license and attribution comply with the original project's permissions before distributing modified versions.
