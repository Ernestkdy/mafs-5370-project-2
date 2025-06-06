# mafs-5370-project-2

---
# Super Tic-Tac-Toe Reinforcement Learning Agent

This repository contains the implementation of a Deep Q-Network (DQN) agent trained to play **Super Tic-Tac-Toe**, a variant of tic-tac-toe with a stochastic move mechanism on a cross-shaped 12x12 board.

---

## Project Overview

Super Tic-Tac-Toe is played on five 4x4 squares arranged in a cross shape within a 12x12 grid. The goal is to get four in a row or column, or five diagonally. Moves have a 50% chance of being accepted; otherwise, the move is randomly assigned to an adjacent square or forfeited.

This project implements:

- A custom Gym environment modeling the game rules and stochastic move logic.
- A DQN agent using PyTorch with experience replay and target network.
- Training loop with epsilon-greedy exploration and periodic target network updates.
- Evaluation of the trained agent against a random baseline.

---

## Repository Structure

- `proj2.ipynb` — Implementation of the Super Tic-Tac-Toe Gym Step by Step. 
- `README.md` — This file.

---

## Requirements

- Python 3.7+
- PyTorch
- NumPy
- Gym
- tqdm

Install dependencies with:

```bash
pip install torch numpy gym tqdm
```

---

## Usage

### Train the Agent

Run the training block in proj2.ipynb:

Training runs for 2000 episodes by default. The model checkpoints and training logs will be saved.

```bash
        O . O .        
        . . . .        
        . . . .        
        . O . X        
O . . . X . . . . . . .
O . . . . . X X X X . .
. X X . . O . . . . . .
. . X X O O . X . . . .
        . . . O        
        . . . O        
        . X . O        
        O . . .        
Episode 0, Total Reward: 1
```

### Evaluate the Agent

After training, evaluate the agent against a random player:

This will simulate 10000 games and print out the win/draw statistics.

```bash
🎉 结果汇总:
🏆 DQN Wins: 862 (86.20%)
🎲 Random Wins: 138 (13.80%)
🤝 Draws: 0 (0.00%)
```

---

## Key Features

- Custom environment with stochastic move acceptance.
- State normalization to current player's perspective.
- Experience replay buffer and target network for stable learning.
- Epsilon-greedy policy with decay for exploration-exploitation balance.

---

## Unique Trick
- Using the restart strategy to improve the computation efficiency and generalization.

---

## Citation

Gagliolo, M., & Schmidhuber, J. (2007). Learning Restart Strategies. In Proceedings of the 20th International Joint Conference on Artificial Intelligence (IJCAI'07), pp. 792–797.

---
## License

This project is released under the MIT License.

---

## Acknowledgements

Inspired by the assignment requirements for Reinforcement Learning coursework on advanced tic-tac-toe variants.

---

Feel free to open issues or submit pull requests for improvements or bug fixes!
  
