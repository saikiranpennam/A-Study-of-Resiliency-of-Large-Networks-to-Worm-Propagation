# A-Study-of-Resiliency-of-Large-Networks-to-Worm-Propagation
The purpose of this program is to study the propagation of worm on the three different types of networks through simulation when no cure (that is, worm defense) is applied. In other words, the worm will continue to spread until no uninfected node remains.

This project simulates the propagation of a worm through various network types and evaluates the effectiveness of defense mechanisms in mitigating the spread. The simulation covers two main programs:
1. **Worm Propagation**: Models the spread of a worm in a network without any defense mechanisms.
2. **Worm Propagation with Defense**: Extends the first program by incorporating defense mechanisms that either inoculate uninfected nodes or cure infected nodes.

## Features

- Simulation of worm spread in networks based on the Erdös-Rényi, Barabási-Albert, and Watts-Strogatz models.
- Implementation of defense mechanisms to combat worm propagation.
- Analysis of the spread dynamics through cumulative and per-time-step visualizations.
- Comparison of the impact of different network topologies on the spread and defense effectiveness.

## Setup

Ensure you have Python installed on your system along with the necessary libraries: `networkx` for network manipulation and `matplotlib` for plotting.

Install the required packages using pip:

```bash
pip install networkx matplotlib
```
## Usage
### Prepare Network Files: 
Generate or obtain CSV files representing the network graphs. Each file should list the edges in the network, with one edge per line, formatted as node1,node2.

### Running Simulations:

For basic worm propagation, use the simulate_infection function.
For simulations with defense mechanisms, use the simultaneous_infection_with_defense function.

### Input Parameters:

Enter the filename of the network graph CSV.
Specify the probability of worm infection.
List initial infected nodes.
(For defense simulations) Specify the probability of node inoculation or curing and the initial cured node.

### Visualizing Results: 
The .ipynb file plots the cumulative number of infections over time, the number of new infections per time step, and, for defense simulations, the cumulative number of cures.

## Example
```python
# Example of running a basic simulation
filename = '{name_of_the_file}_{num_nodes}.csv'
p_infect = 0.1
initial_infected = 23,45,78,90 # comma seperated, no spaces when prompted
simulate_infection(graph, p_infect, initial_infected)

# Example of running a simulation with defense
p_defense = 0.05
initial_cured = 45,67,89,1
simultaneous_infection_with_defense(graph, p_infect, p_defense, initial_infected, initial_cured)
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)