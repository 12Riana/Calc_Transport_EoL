# Solar EoL Transportation Cost Estimator

## Background and Motivation
- The Growing Waste Problem: Australia is one of the top users of solar panels in the world. As the panels installed years ago start reaching the end of their 20 to 25-year lifespans, we are going to face a massive amount of solar waste.
- The Shipping Problem: Most solar farms are located far away from big cities. Moving old solar panels from these distant locations to central recycling centers is very expensive. Because shipping costs so much, it is currently cheaper to just dump the panels in a landfill, which is bad for the environment.
- Finding the Best Solution: We need to figure out the cheapest and smartest way to handle this waste. Is it better to pack up the panels and ship them to one large central factory (Conventional recycling) or is it better to bring a smaller recycling setup directly to the solar farm (Mobile recycling)?
- Making Recycling Profitable: Old solar panels contain valuable materials like silicon, silver, and copper. This tool helps people figure out exactly how many panels need to be recycled in a single trip to cover the high shipping costs and actually make a profit.

## Project Goals
- Create an Easy-to-Use Tool: Provide a clear and accessible estimator (calculator) that policymakers, recycling companies, and solar farm owners can easily use to estimate logistic costs and make financial decisions.
- Estimate Shipping Costs: Calculate the total cost of moving end-of-life (EoL) solar panels from solar farms to the nearest recycling hub, and eventually transported to buyers for each recovered material.
- Compare Recycling Methods: Show the difference in transportation costs between Conventional recycling (shipping panels to a recycling hub) and Mobile recycling (bringing the recycling equipment directly to the solar farm).
- Calculate the total value of the materials recovered from the panels. This helps determine exactly how many panels need to be recycled in a single trip to cover the shipping costs and start making a profit.

## Methodology
### Data Collections
1. Power Stations: 
2. Recycling Hub:
3. Suppliers: 
    
### Assumptions
In order to simplify the calculation, this project decided to apply several assumptions.
1. "Photovoltaic solar panels consist of 95% recyclable materials" (Clean Energy Council, 2025). This means almost 100% of PV components can be recycled and sold. Hence, our assumption is 100% of PV materials can be recycled and would be available to be sold to supplier.
2. The composition of material in each PV module: 
3. The capacity of each solar EoL module is 300 W.
4. The dimension of each solar EoL module is 1.0m x 1.7m x 0.035m.
5. Truck capacity for transporting EoL modules: 7,000 kg. 
6. Truck dimension: 2.2 m x 6.2 m x 2.4 m.
7. Transport cost is based on fuel only.
8. For estimating monetary value and converting different units, we use the following estimation. \
    30kg/panel \
    0.6kW/panel \
    50kg/kW \
    10$/kw = worth of panel power \
    10$/50kg = 0.2$/kg = worth of panel waste

### Calculation

## Output
One Jupyter Notebook file containing code for estimating transportation costs of Conventional and Mobile Recycling of Solar EoL modules to suppliers of each recoverable material in Australia.

## Usage
In order to use this calculator, user needs to follow the following steps.
1. User must have Jupyter Notebook installed on their device.
2. Use git clone to access and download all files provided in this GitHub repository.
3. Run the `code.ipynb` file.
4. Input necessary data to process the calculation.

## Future Work
1. User may add more power stations, recycling hub, or suppliers that have not listed in this project in order to provide more options of places and make this project more reliable for real life scenario.
2. This project still apply many assumptions in order to simplify the cost calculation. User can improve the work in this project by removing some assumptions if they have valid data to substitute the number provided in the assumptions.
3. User can add other aspects that can be considered in transportation costs other than what is used in this project, e.g., truck maintenance costs.

