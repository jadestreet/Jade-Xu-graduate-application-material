## What is the **graph** in burning graph?
In the realm of Burning Graph, our canvas is a finite, simple, and undirected graph, denoted as *G*. This graph, devoid of multiple edges between any two vertices and with no self-looping edges, sets the stage for our exploration.

## What is the Burning Process & Burning Number?
The Burning Process involves equipping each node in the graph *G* with an attribute called '**burned**.' In discrete-time rounds, vertices may either be burned or remain unburned. Once a node is burned, it retains this status unless reset.

### Details of The Burning Process
Starting with an unburned graph *G*, the process unfolds in two key steps: \
1. Burn Neighbors: Burned vertices propagate the burned status to their one-hop neighbors.
2. Pick and Burn A Source: A node is chosen as the ignition source and set burned if unburned. Typically, we select unburned nodes for ignition.

### The Burning Number
This quantifies the number of rounds or sources required to burn the entire graph.

## What is the *Burning Number Conjecture*?
The *Burning Number Conjecture* seeking to establish an upper limit for the burning number in a given graph.
"For a connected graph G with n nodes, the burning number is less than or equal to the ceiling of the square root of n."
