# Tesla_Cybertruck_Distribution

## Project Overview

This project explores the challenges Tesla faces in distributing its limited production of Cybertrucks to dealerships across the United States. Using an optimization model, we aim to determine the best distribution strategy that maximizes profits while minimizing costs related to production, transportation, and holding. 

The project focuses on allocating Cybertrucks produced at two Tesla factories—one in Kansas City (local) and the other in Taiwan (international)—to 10 key sales locations in the U.S.

## Problem Statement

Tesla operates two factories:
- **Local Factory (Kansas City)**: Production capacity of 15,000 trucks, with a production cost of $55,000 per truck.
![download](https://github.com/user-attachments/assets/fb6c56c2-af1a-48a0-a225-02828916526b)

- **International Factory (Taiwan)**: Production capacity of 50,000 trucks, with a production cost of $50,000 per truck.
![download](https://github.com/user-attachments/assets/c7fcc254-5c72-446b-bb38-e6d3d284a964)


The dealerships across the U.S. must meet the demand in the following locations:

- **Los Angeles**: 20,000 trucks
- **San Francisco**: 15,000 trucks
- **Miami**: 6,200 trucks
- **Houston**: 3,000 trucks
- **Austin**: 2,200 trucks
- **Seattle**: 4,300 trucks
- **New York**: 3,300 trucks
- **Phoenix**: 2,700 trucks
- **Denver**: 2,400 trucks
- **Chicago**: 2,400 trucks

Other factors include:
- **Holding Cost**: $37 per day per truck, with a minimum holding period of 30 days and a maximum of 45 days.
- **Transportation Cost**: $1.15 per mile.
- **Sales Price**: $60,000 per truck.

### Objective

The goal is to maximize the profit by optimizing the allocation of trucks from the two factories to various sales locations, considering:
- Production costs at each factory.
- Transportation costs.
- Holding costs.
- Meeting the demand at each location.

## Mathematical Model

### Problem Parameters
- **Local Factory Capacity**: 15,000 trucks, $55,000 per truck.
- **International Factory Capacity**: 50,000 trucks, $50,000 per truck.
- **Transportation Cost**: $1.15 per mile.
- **Holding Cost**: $37 per day (for 30-45 days).
- **Sales Price**: $60,000 per truck.

### Decision Variables
- Number of trucks to be shipped from the local factory to each sales location.
- Number of trucks to be shipped from the international factory to each sales location.
- Total number of trucks held at each location.

### Objective Function
Maximize profit, which is calculated as:
\[
\text{Profit} = \text{Total Revenue} - (\text{Production Cost} + \text{Transportation Cost} + \text{Holding Cost})
\]

### Constraints
- Factory capacity constraints: Each factory has a maximum production capacity.
- Demand satisfaction: Each location must receive enough trucks to meet its demand.
- Holding period: Trucks must be held for at least 30 days but no more than 45 days.
- Non-negativity: All decision variables must be non-negative.

### Assumptions
- The distance from Taiwan to Los Angeles is assumed to be 0 to avoid skewing the transportation cost in favor of the local factory.
- Simplified holding costs are used by averaging the holding days (30-45 days).
- The problem is solved for a single quarter and assumes constant demand throughout the quarter.

## Results

- **Optimal Objective Value**: $519,005,820
- **Total Profit**: $519,005,820.00
- **Total Revenue**: $3,690,000,000.00
- **Total Production Cost**: $3,132,500,000.00
- **Total Transportation Cost**: $38,494,180.00
- **Average Holding Cost**: $0.00 (due to simplifications)

### Optimal Truck Allocations:
#### Local Factory (Kansas City):
- To Chicago: 2,400 trucks
- To Austin: 100 trucks
- To NYC: 3,300 trucks
- To Miami: 6,200 trucks
- To Houston: 3,000 trucks

#### International Factory (Taiwan via LA):
- To LA: 20,000 trucks
- To San Francisco: 15,000 trucks
- To Phoenix: 2,700 trucks
- To Seattle: 4,300 trucks
- To Denver: 2,400 trucks
- To Austin: 2,100 trucks

## Major Assumptions and Limitations
1. **Zero International Transportation Cost**: To simplify the comparison between local and international factories, we assumed the transportation cost from Taiwan to LA is zero.
2. **Holding Costs**: We averaged the holding days to simplify calculations.
3. **Constant Demand**: The model assumes a fixed demand for each location and does not account for demand fluctuations.
4. **Single Quarter**: The model is designed for a single quarter and does not extend to multiple time periods.
   
While the model provides a good starting point, future iterations could include dynamic demand, international transportation costs, and fluctuating production costs.

## Conclusion

This optimization model offers valuable insights into how Tesla can efficiently distribute its limited production of Cybertrucks across the U.S. It balances the trade-offs between production costs, transportation costs, and holding costs to maximize overall profitability. Future enhancements could explore more detailed logistical constraints and incorporate real-world data for more accurate predictions.

## References
- Munro: What the Tesla Cyber Truck Will Really Cost to Build
- MotorTrend: Tesla Cybertruck Cost to Build
- LLCTLCC: Cost to Manufacture a Car
- World Population Review: Tesla Sales by State

