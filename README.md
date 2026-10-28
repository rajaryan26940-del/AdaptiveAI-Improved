# AdaptiveAI — Self-Learning Autonomous Agent Framework

AdaptiveAI is a Python-based autonomous agent framework that executes tasks, evaluates execution results, stores episodic memories, and adapts its strategy selection using machine learning and contextual multi-armed bandit techniques.

The project includes a web dashboard for task execution, learning analytics, episodic memory, semantic knowledge lookup, and ML model retraining.

## Features

- **Autonomous Task Execution:** Supports Python code execution, mathematical calculations, web search, and data-processing tasks.
- **Episodic Memory:** Stores task execution experiences and associated performance metrics.
- **Reward-Based Evaluation:** Evaluates task outcomes using composite reward scores.
- **Adaptive Strategy Selection:** Combines ML-based strategy prediction with contextual multi-armed bandit selection.
- **Interactive Dashboard:** Provides task execution, learning analytics, episodic memory, and semantic knowledge views.
- **ML Model Retraining:** Supports retraining the strategy prediction model using stored experiences.
- **Automated Tests:** Includes unit and integration tests for core functionality and regression prevention.

## Tech Stack

- **Backend:** Python, FastAPI
- **Frontend:** HTML, CSS, JavaScript
- **Machine Learning:** scikit-learn, NumPy, joblib
- **Data Storage:** SQLite
- **Testing:** pytest

## Project Structure

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

### 1. Clone the repository

```bash
git clone https://github.com/rajaryan26940-del/AdaptiveAI-Improved.git
cd AdaptiveAI-Improved
```

### 2. Create and activate a virtual environment

**Windows PowerShell:**

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS/Linux:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
python -m pip install pytest
```

### 4. Run the application

Start the backend server from the project root:

```bash
python -m backend.app
```

Open the local address shown in the terminal, typically `http://127.0.0.1:8000/`, to access the application.

### 5. Run the demonstration

```bash
python run_demo.py
```

### 6. Run the tests

```bash
python -m pytest tests/test_adaptive_agent.py -v
```

The current test suite contains **5 passing tests** in the tested local environment.

## Improvements and Testing

This version includes targeted fixes and regression testing:

- Corrected the dashboard's ML accuracy display so an untrained model is not shown with a fabricated default accuracy.
- Fixed repeated bandit reward accumulation during model retraining by rebuilding the statistics from stored episodes.
- Updated strategy score labels to display selection scores rather than presenting unnormalized values as probabilities.
- Added a regression test to verify that repeated retraining does not double-count stored bandit rewards.

These changes were tested using pytest; all five tests passed in the local development environment.

## Screenshots

The dashboard provides views for task execution, learning analytics, episodic memory, and semantic knowledge. Screenshots are included below.

<!-- Keep your existing four GitHub screenshot image links here. -->

## Future Improvements

- Expand automated test coverage.
- Improve evaluation across a wider variety of tasks.
- Add more detailed learning and strategy-selection analytics.
- Improve documentation for configuration and deployment.

## License

This project currently declares the MIT License. Ensure the license and attribution are consistent with the permissions and licensing terms of the original project before distributing modified versions.
