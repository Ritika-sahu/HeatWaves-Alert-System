# Heatwave Alert Systems 

## Introduction

Heatwaves are extreme weather events with significant impacts on public health and economies globally. With the intensification of these events due to climate change, establishing efficient heatwave warning systems in a timely manner has become a priority.

## Project Objective

The overarching objective of this project is not just to provide a snapshot of the current state of Heatwave Warning Systems (HWS) globally but to establish a robust foundation for future research and improvements. By establishing a systematic approach to data extraction, cleaning, and predictive modeling, we aim to create a blueprint that WMO and other stakeholders can leverage. The methodologies and insights presented here can guide efforts to enhance data collection, refine predictive models, and ultimately, improve heatwave preparedness worldwide. This project underscores the potential of data-driven strategies in addressing global challenges and paves the way for more informed decision-making in the realm of climate preparedness.

## Technical Details

### Data Sources

- **[WMO's Heatwave Warning Systems Inventory](https://community.wmo.int/en/members/profiles)**: Primary source for understanding the HWS global distribution.
- **[Google Scholar and Google Search](https://scholar.google.com/)**: Used to cross-verify and supplement the information from WMO's database.

### Libraries and Tools Used

- **Python**: The primary programming language used for data analysis and processing.
- **Pandas**: For data manipulation and analysis.
- **Selenium**: For web scraping to gather data from online research journals.

## Data Engineering Journey

Our data engineering process can be visualized as a journey through several main steps:

### 1. Data Collection
- **WMO Data Extraction**: Data was sourced from the embedded Power BI dashboard on the WMO website, a task that presented unique challenges due to its dynamic nature. 
- **PubMed Data Retrieval**: Leveraged the PubMed API to fetch relevant data, transforming the XML response into a structured DataFrame.
- **Google Scholar and Google Search**: Scanned Google and Google Scholar using specific keywords to collect research journals and papers.

### 2. Data Cleaning & Validation
#### WMO Data:
- Harmonized data extracted from the WMO website with the provided WMO template, ensuring that country names were spelled correctly and matched the template.
- Checked for and handled duplicate entries to maintain data integrity.
- Randomly selected countries and validated their data to ensure accurate extraction from the WMO website.

#### API and Web Data:
- Cleaned and harmonized data extracted from APIs and other web sources.
- Checked for and handled duplicate entries to ensure data consistency and accuracy.
- Validated random samples to ensure the accuracy of data extraction from these sources.

### 3. Predictive Modeling & Analysis
- **PubMed Predictions**: Adopted advanced tokenization techniques using Hugging Face's RobertaTokenizer and utilized a pretrained RoBERTa model to predict the presence of heatwave systems based on abstracts from the PubMed results.
- **Google Scholar and Google Search Predictions**: Used a Random Forest model to make predictions based on the extracted data.
- The prediction approach has potential for future improvements with more training data and model fine-tuning.

### 4. Data Integration & Final Database Creation
- Unified various datasets, including predictions from PubMed, Google Search, and Google Scholar, to create a comprehensive database.

### 5. Results & Insights
- Formulated rules for overall prediction, emphasizing the significance of even a single positive prediction.
- Generated comprehensive summaries capturing research papers per country and detailed nested information.

For a detailed overview of our data engineering process, including the data flow, see [Data Flow Details](./project_documents/data_engineering/dataModeldetails.md).


## Power BI Dashboard

We've developed a comprehensive Power BI dashboard to visualize our findings and provide stakeholders with an interactive platform to explore the data. 
