# Solar EoL Transportation Cost Estimator

## Background and Motivation
- Australia is one of the top users of solar panels in the world. As the panels installed years ago start reaching the end of their 20 to 25-year lifespans, we are going to face a massive amount of solar waste.
- Most solar farms are located far away from big cities. Moving old solar panels from these distant locations to central recycling centers is very expensive. Because shipping costs so much, it is currently cheaper to just dump the panels in a landfill, which is bad for the environment.
- We need to figure out the cheapest and smartest way to handle this waste. Is it better to pack up the panels and ship them to one large central factory (Conventional recycling) or is it better to bring a smaller recycling setup directly to the solar farm (Mobile recycling)?
- Old solar panels contain valuable materials like silicon, silver, and copper. This project helps people figure out exactly how many panels need to be recycled in a single trip to cover the high shipping costs and actually make a profit.

## Project Goals
- The primary objective of this project is to provide a clear and accessible estimator (calculator) that policymakers, recycling companies, and solar farm owners can easily use to estimate the total transportation cost of moving end-of-life (EoL) solar panels from solar farms to the nearest recycling hub, and eventually transported to suppliers for each recovered material.
- This project also estimate the total value of the materials recovered from the panels. This helps determine exactly how many panels need to be recycled in a single trip to cover the shipping costs and start making a profit.
- Furthermore, this project also shows the difference in transportation costs between Conventional recycling (shipping panels to a recycling hub) and Mobile recycling (bringing the recycling equipment directly to the solar farm).

## Methodology

### Assumptions
In order to simplify the calculation, this project decided to apply several assumptions.
1. "Photovoltaic solar panels consist of 95% recyclable materials."[^1] This means almost 100% of PV components can be recycled and sold. Hence, our assumption is 100% of PV materials can be recycled and would be available to be sold to supplier.
2. We use one composition panel mentioned in 'Recycling c-Si PV Modules: A Review, a Proposed Energy Model and a Manufacturing Comparison.' The composition of material in each PV module is
72% glass, 15% of Al (frame), 7% EVA and Tedlar (encapsulant and back sheet), 2.5% Si, 0.8% Cu, 0.03% Ag, 0.1% Sn and 0.1% Pb.[^2]
3. The capacity of each solar EoL module is 300 W.
4. The dimension of each solar EoL module is 1.0m x 1.7m x 0.035m.
5. Truck capacity for transporting EoL modules: 7,000 kg. 
6. Truck dimension: 2.2 m x 6.2 m x 2.4 m.
7. Transport cost is currently based on fuel only. The price of diesel fuel in Australia is AUD 2.25 per liter based on the latest update from 18 May 2026.[^3] Truck diesel efficiency is 17L/100km.[^4]
8. For estimating monetary value and converting different units, we use the following estimation. \
    18kg/panel \
    0.3kW/panel \
    60kg/kW \
    10$/kw = worth of panel power \
    10$/50kg = 0.2$/kg = worth of panel waste

### Data Collection
#### Power Stations
This project focuses on Large-Scale PV Systems. The data about these PV systems is sourced from the Clean Energy Regulator and is up to date as of 31 December 2025.[^5]
#### Recycling Sites
This project uses 9 different recycling sites that are collected from individual research. The list is provided in `recycling_sites.csv`.
#### Suppliers


Note: this project allows user to add more power stations, recycling sites, and/or suppliers places, so the list from data collection step are not fixed.

### Calculation
For conventional recycling, the calculator works as the following.
1. Calculate the maximum capacity (number of panels) that one truck can carry in one go.
2. Calculate the number of trucks needed to carry EoL based on how many kW/kg/number of panels inputted by user.
3. Calculate the fuel cost of driving on path recycling site -> power stations -> recycling site.
4. Calculate the approximate worth of panel waste in AU$.

For mobile recycling, the calculator works as the following.

## Output
One Jupyter Notebook file named `code.ipynb` containing code for estimating transportation costs of Conventional and Mobile Recycling of Solar EoL modules to suppliers of each recoverable material in Australia. This file serves as the calculator, where user can input information while running the code, and eventually will receive the calculation result.

## Usage
To get the calculator up and running on their local machine, user needs to follow the following steps.
1. User must have Jupyter Notebook installed on their device.
2. Download the project files by running the following command in terminal.
```bash
   git clone https://github.com/12Riana/Calc_Transport_EoL.git
```
3. Launch Jupyter Notebook and open the `code.ipynb` file.
4. Run the notebook cells sequentially. When prompted, input the required parameters to process the calculations.

## Future Work
1. User may add more power stations, recycling hub, or suppliers that have not listed in this project in order to provide more options of places and make this project more reliable for real life scenario.
2. This project still apply many assumptions in order to simplify the cost calculation. User can improve the work in this project by removing some assumptions if they have valid data to substitute the number provided in the assumptions.
3. User can add other aspects that can be considered in transportation costs other than what is used in this project, e.g., truck maintenance costs.
4. Note that not all suppliers would willing to buy extracted materials from recycle solar panel. Hence, user can filter out and adjust suppliers list to make sure that the list only includes suppliers that are willing to buy the recoverable materials from solar PV waste.
5. The calculator is provided in Jupyter Notebook file with less interactive UI/UX and the raw code is still visible to user. This can be improved by creating another user interface for the calculator so user can use the calculator without looking at the raw code.

## References
[^1]: Clean Energy Council. (2025). [Recycling Wind Turbines, Solar Panels and Batteries: Fact Sheet](https://cleanenergycouncil.org.au/for-consumers/fact-sheets/recycling-get-the-facts/recyling-wind-turbines-solar-panels-batteries).
[^2]: Mulazzani, A., Eleftheriadis, P., Leva, S (2022). [Recycling c-Si PV Modules: A Review, a Proposed Energy Model and a Manufacturing Comparison](https://doi.org/10.3390/en15228419).
[^3]: GlobalPetrolPrices. (2026, May 18). [Australia Diesel prices](https://www.globalpetrolprices.com/Australia/diesel_prices/).
[^4]: Truck1. [Isuzu NQR75 Tech Specs](https://www.truck1.eu/blog/isuzu-nqr75-nqr75r-tech-specs-t31726).
[^5]: Australian Photovoltaic Institute (APVI). [Australian PV Map - Power Stations](https://pv-map.apvi.org.au/power-stations).