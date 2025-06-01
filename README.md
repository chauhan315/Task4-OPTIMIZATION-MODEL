# Optimization Model

*COMPANY*: CODETECH IT SOLUTIONS

*NAME*: ANKUR SINGH CHAUHAN

*INTERN ID*: CT12WV42

*DOMAIN*: DATA SCIENCE

*DURATION*: 12 WEEKS

*MENTOR*: NEELA SANTOSH

*OUTPUT*: ![Image](https://github.com/user-attachments/assets/e944a6b8-ffb9-4e7c-9452-4fc9022439f5)


# Supply Chain Optimization using Linear Programming (PuLP)

## Project Title

**Optimizing Warehouse-to-Store Shipments Using Linear Programming in Python**

---

## Project Overview

This project addresses a real-world logistics optimization challenge using Linear Programming (LP) and Python's PuLP library. The goal is to minimize the total cost of shipping goods from a set of warehouses to multiple stores, while considering both per-unit shipping costs and fixed activation costs for using a warehouse.

The problem is modeled and solved programmatically to provide cost-effective and practical shipping strategies for a retail distribution network.

---

## Tools and Libraries Used

- Python 3.x
- PuLP: A linear programming library for Python
- Pandas: For tabular data manipulation
- NumPy: For generating and working with arrays
- Matplotlib/Seaborn (Optional): For visualizing the cost matrix

---

## Problem Description

A retail company operates 12 warehouses and needs to supply goods to 16 stores. Each warehouse has a limited inventory (supply), and each store has a specific demand to be fulfilled. The cost of shipping varies depending on the warehouse-store pair, and each warehouse also has an associated activation cost — a fixed cost incurred if it is used for shipping.

The objective is to find the most cost-effective shipment plan that:

- Meets all store demands
- Respects warehouse supply limits
- Minimizes both shipping and activation costs

---

## Optimization Model

### Objective:

Minimize the total cost, which includes:
- Variable shipping costs (based on warehouse-store pairs)
- Fixed warehouse activation costs

### Decision Variables:

- `x[w,s]`: Number of units shipped from warehouse `w` to store `s`
- `y[w]`: Binary variable; 1 if warehouse `w` is used, 0 otherwise

### Constraints:

1. **Demand Fulfillment**: Each store's demand must be met exactly.
2. **Supply Limitation**: A warehouse cannot ship more than its available inventory.
3. **Warehouse Activation Logic**: If a warehouse is used to ship even one unit, its activation cost is incurred (`x[w,s] <= M * y[w]`).
4. **Non-negativity**: All shipment values must be ≥ 0.

---

## Dataset Details

Synthetic data was generated to simulate realistic logistics:

- 12 Warehouses: W1 to W12
- 16 Stores: S1 to S16
- Shipping Costs: Random integers from 10 to 100
- Supplies: Random integers from 1000 to 2000
- Demands: Random integers from 500 to 1500
- Activation Costs: Random integers from 500 to 1000 per warehouse

The cost matrix is a 12x16 table representing unit shipping costs between each warehouse-store pair.

---

## Key Steps in the Project

### Step 1: Define Problem Entities

- Define lists of warehouses and stores
- Generate random cost, supply, demand, and activation data

### Step 2: Visualize Shipping Cost Matrix

- Display cost matrix using a pandas DataFrame for better understanding

### Step 3: Formulate the Linear Programming Model

- Define decision variables
- Set up constraints for demand and supply

### Step 4: Add Warehouse Activation Logic

- Introduce binary variables and constraints
- Modify the objective to include activation costs

### Step 5: Solve the Model

- Use PuLP to define and solve the LP problem
- Extract the optimal solution: shipment matrix and total cost

### Step 6: Present Results and Draw Insights

- Show activated warehouses
- Display full shipment matrix
- Calculate and display total cost (shipping + activation)

---

## Insights

- All store demands were met exactly.
- All warehouses were used, which implies distributed store locations and the model's effort to minimize transportation distance and costs.
- Some warehouses handled more volume than others, suggesting potential hubs in a decentralized network.
- Activation costs helped distribute load and prevent over-reliance on a few warehouses.

---

## Possible Improvements

This base model can be extended with:

- Warehouse capacity and handling constraints
- Transport mode differentiation (e.g., truck, rail, air)
- Dynamic multi-period planning
- Multi-product optimization
- Route constraints or delivery windows

---

## File Structure

├── README.md
├── supply_chain_optimization.ipynb

yaml
Copy
Edit

---

## How to Run

1. Clone this repository or download the notebook.
2. Install necessary libraries: `pulp`, `pandas`, `numpy`.
3. Run the notebook in Jupyter, Google Colab, or any Python IDE.
4. Analyze results and adjust parameters (costs, demands, supplies) as needed.

---

## Internship Submission Info

- Company: CODTECH
- Task: Business case solving using optimization
- Language: Python
- Library: PuLP (COIN-OR)
- Deliverable: Executable notebook with markdown explanation and optimization logic

---

## Conclusion

This project demonstrates how linear programming can solve critical logistics challenges by reducing shipping costs and optimizing resource use. With activation cost modeling and real-world constraints, the solution closely mirrors actual supply chain decision-making.

Such optimization frameworks can greatly benefit inventory planners, logistics managers, and retail strategists by improving operational efficiency and cost transparency.



