
# ⚖️ Network Load Balancer

Welcome to the **Network Load Balancer** project! This Python-based application utilizes Q-learning to efficiently distribute jobs across network nodes, ensuring optimal performance and minimal job migration. The GUI is built with Tkinter, providing an interactive and user-friendly experience.

## ✨ Features

- 🌐 **Dynamic Network Configuration**: Easily add nodes and edges to simulate different network topologies.
- 🤖 **Reinforcement Learning**: Q-learning algorithm for intelligent job scheduling and migration.
- 📊 **Visualization**: Graphical representation of the network and job distribution using Matplotlib.
- 🔄 **Job Migration Tracking**: Keep track of job migrations and analyze performance.

## 🚀 Getting Started

### 📋 Prerequisites

Ensure you have the following installed:

- [Python 3.6+](https://www.python.org/downloads/)
- Required Python libraries: `tkinter`, `ttkthemes`, `networkx`, `matplotlib`

Install the required libraries using pip:
```bash
pip install tk ttkthemes networkx matplotlib
```

### ▶️ Running the Application

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/network-load-balancer.git
   cd network-load-balancer
   ```

2. **Run the Application**:
   ```bash
   python main.py
   ```

## 🖥️ User Interface Overview

### 🎛️ Main Interface

- **Add Nodes**: Define the number of nodes and their capacities.
- **Add Edges**: Create connections between nodes to simulate the network topology.
- **Run Scheduler**: Submit jobs to the network and observe the job distribution and migrations.
- **Visualize Graph**: Display a graphical representation of the network and job allocations.

### 📜 Instructions

1. **Add Nodes**:
   - Click 'Add Nodes' and specify the number of nodes and their respective capacities.
2. **Add Edges**:
   - Click 'Add Edges' and define the connections between nodes.
3. **Run Scheduler**:
   - Click 'Run Scheduler' to submit jobs and see the scheduling results, including any job migrations.
4. **Visualize Graph**:
   - Click 'Visualize Graph' to view the network graph with job allocations.

## 🧩 Code Overview

The main components of the project include:

- **QLearningAgent**: Implements the Q-learning algorithm for job scheduling.
- **Node**: Represents a network node with capacity and job handling.
- **Graph**: Manages the network topology, job submissions, and migrations.
- **JobSchedulerGUI**: The Tkinter-based GUI for user interaction.

### Key Classes and Methods

```python
class QLearningAgent:
    def __init__(self, nodes, alpha=0.1, gamma=0.9, epsilon=0.1):
        # Initialization code...

    def get_q_value(self, state, action):
        # Method to get Q-value...

    def choose_action(self, state, available_actions):
        # Method to choose action...

    def update_q_value(self, state, action, reward, next_state):
        # Method to update Q-value...

class Node:
    def __init__(self, capacity):
        # Initialization code...

    def add_job(self, job, execution_time):
        # Method to add job...

    def remaining_capacity(self):
        # Method to get remaining capacity...

class Graph:
    def __init__(self):
        # Initialization code...

    def add_node(self, node, capacity):
        # Method to add node...

    def add_edge(self, node1, node2):
        # Method to add edge...

    def submit_job(self, job):
        # Method to submit job...

    def migrate_job_with_rl(self, job, assigned_node):
        # Method to migrate job with RL...

    def visualize_graph(self):
        # Method to visualize graph...

class JobSchedulerGUI:
    def __init__(self, master):
        # Initialization code...

    def add_nodes(self):
        # Method to add nodes...

    def add_edges(self):
        # Method to add edges...

    def run_scheduler(self):
        # Method to run scheduler...

    def visualize_graph(self):
        # Method to visualize graph...

if __name__ == "__main__":
    root = Tk()
    app = JobSchedulerGUI(root)
    root.mainloop()
```

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for improvements and bug fixes.
