# Global Power Plants Data Exploration
## by Ayman Azzi


## Dataset

The Global Power Plant Database is an open-source open-access dataset of grid-scale (1 MW and greater) electricity generating facilities operating across the world. This documnet explores a dataset containing power plants data within the period from 2013 to 2019.
This data and other details about it can be found [here](https://datasets.wri.org/dataset/globalpowerplantdatabase).

In the wrangling step, I changed the datatype of both the years columns to string, then I dropped all rows with negative values at generation_gwh_xxxx columns. After that I took only about 99% of the data that have values of capacity less than 2000 mw, since it has massive outliers. 

The wrangled data contained 34145 power plants over the years 2013 until 2019. There are 36 features in this dataset:
- `country` 
- `country_long` 
- `capacity_mw` (MegaWatt) 
- `primary_fuel` 
- `other_fuel1`
- `other_fuel2`
- `other_fuel3`
- `commissioning_year` 
- `year_of_capacity_data` 
- `generation_gwh_2013` 
- `generation_gwh_2014` 
- `generation_gwh_2015` 
- `generation_gwh_2016`
- `generation_gwh_2017` 
- `generation_gwh_2018` 
- `generation_gwh_2019` 

## Summary of Findings

- Before using a logarithmic scale, the distribution of capacity values looked to be mostly limited between $0 and 500 MW$. But after scaling, it is a right skewed histogram clearly but with rough shape, and it became obvious that there are many outliers with huge values more than 2000 mw.

- Using the logarithmic scale, generations of power distributions have almost the same shape with values limitd between $0-20k GWH$, and they're getting more skewed to right with higher values every year.

- Most used primary fuels for power plants are: Solar, Hydro, Wind, Gas, Oil and Coal. Biomass seems to be another interesting choice for energy.

- The USA headed all countries with having the biggest number of power plants: around 10000. In addition to that, China (~4k) and the UK (~3k). There are some countries with only 1 or two plants in this dataset, like Luxembourg or Palestine. Brazil, France, India, Germany, Canada, Spain and Russia own most of the power plants in the world ($77.6$% of the world power plants).

- Number of plants is increasing amoung year on average, if we just exclude the year 2019 for not being complete, and 2020 for being wrongly included.

- Capacity average is increasing amoung years, it might be due to diversity of fuel types with higher capacities.

- Nuclear, Coal, Gas and Petcoke have the highest capacities amoung all kinds of energy sources for plants (starting from $200$ until $1200 MW$), and Solar.

- The most countries using solar energy are USA, China and UK. China has a high number of Wind, Hydro and Coal plants. The UK utilizes more Wind plants, and Oil plants is being employed widely by USA and Brazil.

- There isn't many Nuclear plants in the world regarding it's high capacity, like in France where it has only 2 plants but with the biggest capacity (around $1800 mw$). This applies also on Coal, where in the UK having only 6 plants but with capacity over $1300 mw$. Contrary to Solar and Hydro fuels, their capacity is low comparing to other fuels.

- The growth of capacity for each country must be related somehow with kind of fuel used for plants operations of that country that have even high or low capacity.

- Capacity of fuel is stable on average for most fuel kinds. Except for Gas, Coal, Hydro and Wind, there is a lot of changes over time, where Gas and Hydro are kind of slightly decreasing on general. Wind is increasing, and nothing to say about coal because of it's rough shape.

## Key Insights for Presentation

For the presentation, I'm focusing on the relation between fuel kinds as a primary choice and the capacity of these fuels, in addition to th years of commissioning. I start by introducing the distrubtion of capacity values with logarithmic scale, then the distribution of Primary fuel categories. 
Next, I discovered the relation between capacity vs. commissioning year, then vs. primary fuel.
In the end, I'm showing the growth of capacity amoung time for only specific fuel kinds.