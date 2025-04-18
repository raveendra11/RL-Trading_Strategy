# 📈 Reinforcement Learning-Based Stock Trading Strategy

This project implements a **Deep Q-Learning (DQN)** based trading agent that learns to make stock trading decisions (Buy, Sell, Hold) using **historical stock price data (OHLCV)**.

## 🧠 Project Overview

The RL agent interacts with the stock market environment in episodes and learns to take optimal actions based on a defined reward function. The main components include:

- **Agent**: Learns from market states to take actions.
- **Actions**: Buy, Sell, Hold.
- **State**: A window of past normalized OHLCV differences.
- **Reward**: Profit or loss from transactions.
- **Model**: Trained using Deep Q-Network (DQN) from Keras.

## 📂 File Structure

```
├── RL_Trading_Strategy_OHLCV.ipynb     # Main Jupyter notebook
├── sample_stock_data_full.csv          # Stock dataset (OHLCV format)
├── models/                             # Saved trained models (if any)
└── README.md                           # Project documentation (this file)
```

## 📊 Dataset

- **File**: `sample_stock_data_full.csv`
- **Format**: Open, High, Low, Close, Volume, Date
- **Purpose**: Used for training and evaluation of the RL agent.

## 🔁 Workflow

1. **Load stock data** from CSV
2. **Preprocess** OHLCV data into a suitable state representation
3. **Initialize** the DQN agent with a replay memory
4. **Train** over episodes where:
   - The agent observes a state
   - Takes an action (Buy/Sell/Hold)
   - Receives a reward
   - Updates its policy
5. **Evaluate** on test data and **visualize** trades and cumulative profit

## 📉 Output

- Visual plots showing:
  - Buy/Sell signals over time
  - Cumulative profits
- Saved model under `models/` directory
- Console logs for actions, rewards, and profits

## ⚙️ Dependencies

```bash
pip install numpy pandas matplotlib scikit-learn keras tensorflow
```

## ▶️ Run Instructions

Open the notebook and run cells step-by-step:

```bash
jupyter notebook RL_Trading_Strategy_OHLCV.ipynb
```

Make sure `sample_stock_data_full.csv` is in the same directory.

## ✅ Features

- State generation from OHLCV history
- Q-learning-based decision making
- Model training with replay memory
- Visualization of trading strategy performance

## 📌 To-Do

- [ ] Add support for multi-stock training
- [ ] Implement advanced reward functions
- [ ] Hyperparameter tuning and experiment logging

---

📫 For questions or contributions, reach out via [GitHub](https://github.com/raveendra11)
