# NDN Topology Configuration and Simulation

## Introduction

This project aims to simulate a Named Data Networking (NDN) environment using ns-3, a discrete-event network simulator. The simulation involves configuring a network topology with a specified number of nodes, links, consumers, and producers, and then running the simulation to observe the behavior of NDN communication within this topology.

## Getting Started

### Prerequisites
Before running the simulation, ensure that you have the following prerequisites installed:

- ns-3 network simulator
- ndnSIM module for ns-3

### Installation
1. Clone this repository to your local machine:
    ```bash
    git clone https://github.com/Richard-YH/NDNNetSimulator.git
    ```
2. Compile the ns-3 simulation environment with ndnSIM module.
3. Ensure that all necessary libraries and dependencies are installed.

### Usage
1. Compile the simulation script:
    ```bash
    make
    ```
2. Run the simulation with a specified topology configuration file:
    ```bash
    ./ndn_simulation
    ```
3. Follow the prompts to input the topology configuration file path and observe the simulation output.

## Topology Configuration

The topology of the network is defined in a configuration file. The file should specify the following parameters:

- Number of nodes in the network.
- Number of links connecting the nodes.
- Number of consumers in the network.
- Number of producers in the network.

An example configuration file format is as follows:
```bash
5
6
3
2
0 1
1 2
2 3
3 4
4 0
0 2
Consumer1 10 20 /prefix1
Consumer2 5 30 /prefix2
Consumer3 8 25 /prefix3
Producer1 /prefix1
Producer2 /prefix2
```

## Simulation

Once the topology is configured, the simulation script will:

- Create nodes based on the specified topology.
- Connect nodes using point-to-point links.
- Install the NDN stack on all nodes.
- Implement forwarding strategy (to be specified).
- Configure consumers and producers (to be implemented).
- Run the simulation for a specified duration.
- Output simulation results.

## Contributing

Contributions to this project are welcome. Feel free to submit issues, feature requests, or pull requests.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---
Feel free to modify and expand this README according to your project's specific requirements and details.
