# Sustainability Evaluation of Alva Energies


## Objective

The core focus of this project is to evaluate and promote sustainability within electric vehicle (EV) charging operations. The sustainability module tracks key metrics, including renewable energy usage, carbon emissions saved, fuel displacement, and overall environmental impact. These indicators help assess the greenness and climate resilience of current operations, while also identifying areas for improvement in energy sourcing and carbon offsetting. In addition to sustainability, financial and operational modules were implemented to provide context, tracking revenue trends and infrastructure efficiency, ensuring that eco-conscious decisions also align with economic viability and service reliability.

## Technologies and Tools Used

### Microsoft Excel
- Data Collection and Exploration
- File Format: *csv*

### Hadoop (MapReduce - Java)
- Processing the very huge amount of sustainability data that was collected from the systems and manually entered
- The Data was cleaned, and new sustainability metrics were derived from the existing data that will help us get better insights into the sustainability of the business

**Mapper Role:**
- Removes duplicates
- Parses each line and extracts values
- Calculates:
  - Revenue per kWh = Revenue / Energy Delivered
  - Energy Efficiency = Energy Delivered / Average Charging Time
  - CO₂ Saved per Session = CO₂ Saved / Charges per Day
  - Sustainability Score = Weighted sum of renewable %, utilization, CO₂ saved per session

**Reducer Role:**
- Since duplicates are already removed in Mapper, Reducer just passes data along

**Output:**
- A new cleaned dataset with 4 extra columns:
  - *Revenue per kWh*
  - *Energy Efficiency*
  - *CO₂ Saved per Session*
  - *Sustainability Score (0-100)*

### Microsoft Power BI
- The cleaned and newly derived sustainability metrics were loaded into Power BI for the creation of dashboards that will assist us with insights
- The dashboards focused on Energy Sustainability, Financial Insights, and Operational Insights

## Screenshots or Outputs

### Metrics derived using Big Data

| ![Derived Columns](<Big Data/Images/new generated columns.png>) |
|:----------------------------------------:|
| *Fig. 1: Derived Columns*  |

- **Revenue per kWh** = Revenue / Energy Delivered
- **Energy Efficiency** = Energy Delivered / Average Charging Time
- **CO₂ Saved per Session** = CO₂ Saved / Charges per Day
- **Sustainability Score** = Weighted sum of renewable %, utilization, CO₂ saved per session

### Power BI Dashboards

BI Dashboards were made to get insights about Sustainability, Finance, and Operations

**Sustainability Dashboard 1**

| ![Sustainability Dashboard 1](<Business Intelligence/Sustainability Dashboard 1.png>) |
|:----------------------------------------:|
| *Fig. 2: Sustainability Dashboard 1*  |

**Sustainability Dashboard 2**

| ![Sustainability Dashboard 2](<Business Intelligence/Sustainability Dashboard 2.png>) |
|:----------------------------------------:|
| *Fig. 3: Sustainability Dashboard 2*  |

**Financial Dashboard**

| ![Financial Dashboard](<Business Intelligence/Financial Dashboard.png>) |
|:----------------------------------------:|
| *Fig. 4: Financial Dashboard*  |

**Operational Dashboard**

| ![Operational Dashboard](Business Intelligence/Operations Dashboard.png>) |
|:----------------------------------------:|
| *Fig. 5: Operational Dashboard*  |