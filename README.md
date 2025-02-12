# Aviation Risk Analysis

## Project Overview

The aviation industry is evolving rapidly—with modern technology, stricter safety regulations, and enhanced pilot training leading to significant improvements in operational safety. However, as companies look to diversify into new areas like commercial and private aviation, understanding the historical risks associated with aircraft becomes critical. 

This project analyzes aviation accident data spanning from 1962 to 2023 to determine which aircraft are the lowest risk for a new aviation business venture. By leveraging data cleaning, exploratory analysis, statistical evaluation, and data visualization (via Jupyter Notebook and Tableau), we extract meaningful insights on accident trends, weather-related impacts, and aircraft make and model performance.

## Objectives

The primary objectives of this project are to:

- **Assess Historical Accident Trends:**  
  Analyze aviation accident data from 1962 to 2023 to identify long-term trends and key turning points in aviation safety. This includes understanding periods of steady decline, fluctuations, and recent changes due to factors such as COVID-19.

- **Evaluate Aircraft Risk by Make and Model:**  
  Compare accident rates across various aircraft manufacturers and specific models to determine which aircraft pose higher or lower risk. Special attention is given to popular general aviation models (e.g., Cessna, Piper) versus commercial models (e.g., Boeing) and helicopter operations (e.g., Bell, Robinson).

- **Examine Weather Impact on Accidents:**  
  Investigate the influence of different weather conditions on accident frequency and severity. Determine how conditions like Visual Meteorological Conditions (VMC) and Instrument Meteorological Conditions (IMC) correlate with accident outcomes.

- **Generate Actionable Business Insights:**  
  Provide data-driven recommendations to support strategic decision-making in aircraft acquisition, pilot training, and maintenance. The aim is to help the head of the aviation division minimize risk while optimizing operational efficiency.

- **Enable Data-Driven Decision Making:**  
  Leverage advanced analytics and visualization (via Jupyter Notebook and Tableau) to transform complex data into clear, actionable insights for business stakeholders.

By achieving these objectives, the project will deliver a comprehensive risk analysis that informs the selection of the safest and most reliable aircraft for new business ventures in the aviation industry.

## Methodology

This project follows a systematic, multi-step approach to transform raw aviation accident data into actionable business insights. The methodology is broken down into the following phases:

1. **Data Collection & Cleaning**
   - **Data Ingestion:**  
     The raw dataset, which includes aviation accident records from 1962 to 2023, was imported into a Jupyter Notebook using Python and Pandas.
   - **Data Cleaning:**  
     - Missing values were handled using domain-specific logic. For example, rows with missing `Location` values (only 0.06% missing) were dropped, while other columns were imputed or standardized.
     - Unnecessary columns such as `Latitude`, `Longitude`, `Schedule`, `Air.carrier`, `FAR.Description`, and `Aircraft.Category` were removed to reduce noise and redundancy.
     - Columns that described the injury severity i.e Total.Fatal.Injuries, Total.Serious.Injuries, Total.Minor.Injuries, Total.Uninjured missing values were filled with 0, assuming that NaN or no value meant 0
     - Text fields (e.g., `Make` and `Model`) were standardized (e.g., converting all entries to title case) to ensure consistency across the dataset.

2. **Exploratory Data Analysis (EDA)**
   - **Trend Analysis:**  
     The dataset was grouped by time (year extracted from `Event.Date`) to analyze trends in accident frequency over the years. This provided insights into periods of steady decline, fluctuations, and the impact of external events like the COVID-19 lockdown.
   - **Geographical Analysis:**  
     Accident counts were aggregated by `Country` and `Location` to identify high-risk regions. This step helped in understanding the spatial distribution of accidents.
   - **Severity & Weather Analysis:**  
     The data was segmented by accident severity and weather conditions (e.g., Visual Meteorological Conditions vs. Instrument Meteorological Conditions) to determine how different factors impact accident outcomes.

3. **Data Visualization**
   1. **Jupyter Notebook Visualizations:**  
     Using libraries such as Matplotlib and Seaborn, multiple charts (line charts, bar charts, pie charts) were created to illustrate:
     - Accidents over time.
     - Accident distribution by country.
     - Severity analysis and trends.
     - Impact of weather conditions on accident frequency.


   2.  **Interactive Dashboard (Tableau):**
      An interactive dashboard is available on Tableau Public that visualizes key aspects of the aviation accident data, including accident trends, geographic distributions, and severity breakdowns.  
    You can view the dashboard here: [https://public.tableau.com/views/AviationRiskAnalysis_17392996968900/AviationRiskAnalysisDashboard?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link]
    The cleaned data was exported (e.g., as CSV) and imported into Tableau Public to create an interactive dashboard. This dashboard enables stakeholders to explore: 
    - **Accidents Over Time:** Temporal trends in aviation accidents from 1985 to the present.
    - **Accident Distribution by Country:** Geographic breakdown of incidents. Geospatial distributions of accidents.
    - **Severity Analysis:** Distribution of accident severities (Fatal, Serious, Minor, etc.).
    - **Aircraft Make & Model Analysis:** Identification of high-risk models & detailed breakdowns by aircraft make and model.
    - **Weather Conditions Analysis:** Impact of different weather conditions on accident rates.

**Dashboard Name:** *Aviation Risk Insights*


4. **Final Deliverables**
   - A comprehensive **Jupyter Notebook** documenting the entire analysis process.
   - An interactive **Tableau Dashboard** that visualizes key insights.
   - A **GitHub Repository** containing all code, cleaned data, and documentation.

This multi-phase methodology ensures that the final analysis is robust, reproducible, and directly applicable to making data-driven decisions in the aviation industry.

## Business Recommendations

Based on our comprehensive analysis of aviation accident data, we propose the following key recommendations to support a safer and more efficient aviation business:

- **Invest in Modern, Reliable Aircraft:**  
  Prioritize acquiring or leasing newer aircraft that feature advanced safety technologies and have proven lower accident rates. This is especially critical for commercial operations, where safety and efficiency are paramount.

- **Enhance Pilot Training and Maintenance Programs:**  
  Given that widely used general aviation models (e.g., Cessna and Piper) show higher accident rates, it is essential to implement rigorous pilot training and strict maintenance protocols to minimize human and mechanical errors.

- **Leverage Data-Driven Risk Management:**  
  Utilize predictive analytics and real-time monitoring systems to detect potential operational issues early and optimize maintenance schedules, reducing the overall risk of accidents.

- **Adapt to Market Trends and Operational Conditions:**  
  With trends showing a post-2020 rebound in air travel, continually reassess and update safety measures to match evolving operational demands and external conditions.

- **Strengthen Operational Procedures:**  
  Since most accidents occur under clear weather (VMC), focus on refining operational protocols and safety practices rather than solely on weather mitigation. This includes enhancing pre-flight checks and reinforcing a culture of safety.

These recommendations aim to guide strategic decision-making in aircraft selection, pilot training, and risk management to build a safer, more resilient aviation operation.



