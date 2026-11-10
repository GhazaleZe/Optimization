# Grand Prix Automobile: Solve a Transportation Problem with Python

## Question

The Grand Prix Automobile Company makes cars in **3 plants** and ships them to **4 regions**. Each plant can supply a limited number of cars, and each region needs a fixed number of cars. The cost of shipping one car depends on the route.

| From \ To | Region 1 | Region 2 | Region 3 | Region 4 | Capacity |
|---|---:|---:|---:|---:|---:|
| Plant 1 | $131 | $218 | $266 | $120 | 450 |
| Plant 2 | $250 | $116 | $263 | $278 | 600 |
| Plant 3 | $178 | $132 | $122 | $180 | 500 |
| **Demand** | **450** | **200** | **300** | **300** | |

The company wants to meet every region's demand at the **lowest total shipping cost**.

### Formulation

**Decision variables**

`xij` = number of cars shipped from Plant *i* to Region *j*, for *i* = 1, 2, 3 and *j* = 1, 2, 3, 4 (12 variables).

**Objective: minimize the total shipping cost**

```
Min Z = 131 x11 + 218 x12 + 266 x13 + 120 x14
      + 250 x21 + 116 x22 + 263 x23 + 278 x24
      + 178 x31 + 132 x32 + 122 x33 + 180 x34
```

**Constraints**

```
Capacity (each plant cannot ship more than it has)
    x11 + x12 + x13 + x14 <= 450      (Plant 1)
    x21 + x22 + x23 + x24 <= 600      (Plant 2)
    x31 + x32 + x33 + x34 <= 500      (Plant 3)

Demand (each region must get at least what it needs)
    x11 + x21 + x31 >= 450            (Region 1)
    x12 + x22 + x32 >= 200            (Region 2)
    x13 + x23 + x33 >= 300            (Region 3)
    x14 + x24 + x34 >= 300            (Region 4)

Non-negativity
    all xij >= 0
```

### Task

Solve this linear program with Python and answer:

1. What is the minimum total shipping cost?
2. How many cars should be shipped on each route?
3. Which plants use all of their capacity?
