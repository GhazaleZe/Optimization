# Grand Prix Automobile: A Transportation Problem

## The problem

The Grand Prix Automobile Company makes cars in three plants and sells them in four regions. Each plant can supply only a limited number of cars, and each region needs a set number of cars. The cost of shipping one car depends on which plant it leaves and which region it goes to.

**Unit shipping cost ($ per car), plant capacities and regional demands**

| From \ To | Region 1 | Region 2 | Region 3 | Region 4 | Capacity |
|---|---:|---:|---:|---:|---:|
| Plant 1 | 131 | 218 | 266 | 120 | 450 |
| Plant 2 | 250 | 116 | 263 | 278 | 600 |
| Plant 3 | 178 | 132 | 122 | 180 | 500 |
| **Demand** | **450** | **200** | **300** | **300** | |

Any plant can ship to any region. Shipments cannot be negative.

**Questions**

1. Represent the problem as a network. How many decision variables and constraints does it have?
2. Formulate it as a linear program.
3. Solve it. What is the cheapest shipping plan, and what does it cost? Which plants run at full capacity?
4. Write the same model in a more general way, as a list of arcs (origin, destination, unit cost), where the supply and demand totals are found by adding up the flow on the arcs that leave or enter each node. Confirm that it gives the same answer.
5. What is one more car of capacity worth at each plant? What does one more car of demand cost in each region?
6. Suppose every region's demand changes by the same percentage, from −20% to +30% in steps of 5%. How does the minimum cost change? What is the largest increase the plants can meet?


