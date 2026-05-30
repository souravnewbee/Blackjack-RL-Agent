# Blackjack RL Agent 🃏

A Q-Learning agent trained to play Blackjack using the `Blackjack-v1` environment from OpenAI Gymnasium, following Sutton & Barto rules.

---

## 🎮 Live Demo

👉 [Play the Interactive Demo](https://souravnewbee.github.io/Blackjack-RL-Agent/blackjack_rl_demo.html)

> Watch the trained agent make real-time decisions — card dealing animations, step-by-step reasoning, and a full learned policy grid included.

---

## 📓 Notebook

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/17RwRlfpSJNY-RdS4LnaAUqiEKywuY9oo?hl=en)

---
> *Note: If the notebook doesn't render on GitHub, open it directly in Colab using the badge above.*

## 📌 Overview

The agent learns an optimal Blackjack strategy through trial and error across 100,000 episodes using:

- **Algorithm:** Q-Learning (model-free, off-policy TD control)
- **Exploration:** ε-greedy (ε decays from 1.0 → 0.1)
- **Environment:** Gymnasium `Blackjack-v1`
- **State space:** (player sum, dealer face-up card, usable ace)
- **Action space:** Hit or Stand

---

## 📁 Repository Structure

| File | Description |
|------|-------------|
| `RL_with_Gymnasium_BlackJack.ipynb` | Training notebook with policy visualizations |
| `blackjack_rl_demo.html` | Standalone interactive browser demo |
| `README.md` | Project documentation |

---

## ⚙️ Hyperparameters

| Parameter | Value |
|-----------|-------|
| Learning rate | `0.01` |
| Episodes | `100,000` |
| Initial epsilon | `1.0` |
| Final epsilon | `0.1` |
| Discount factor | `0.95` |

---

## 🚀 Run Locally

```bash
git clone https://github.com/souravnewbee/Blackjack-RL-Agent.git
cd Blackjack-RL-Agent
pip install gymnasium==0.27.0 matplotlib numpy seaborn tqdm
jupyter notebook RL_with_Gymnasium_BlackJack.ipynb
```

---

## 🧠 How It Works

The agent maintains a Q-table mapping every observed state to estimated action values. Early in training it explores randomly. Over time epsilon decays and the agent increasingly exploits its learned knowledge. By 100,000 episodes the policy converges — standing on 17+, hitting soft hands, and adjusting strategy based on the dealer's visible card.

---

## 📚 References

- Sutton & Barto — *Reinforcement Learning: An Introduction*
- [Gymnasium Blackjack-v1 Documentation](https://gymnasium.farama.org/environments/toy_text/blackjack/)

---

## 📄 License

MIT
