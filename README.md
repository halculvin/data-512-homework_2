# Human Centered Data Science - A2: Considering Bias in Data

This repository contains the code and resulting data which tries to explore the concept of bias in data using Wikipedia articles. It was originally completed for the second assignment of the University of Washington's Human Centered Data Science (DATA 512) course in Autumn 2022.
The goal of this assignment is to explore the concept of bias in data using Wikipedia articles. This assignment will consider articles on political figures from different countries. For this assignment, I combined datasets of Wikipedia articles with a dataset of country populations, and used a machine learning service called ORES to estimate the quality of each article.
I then performed an analysis of how the coverage of politicians on Wikipedia and the quality of articles about politicians varies among countries. 
My analysis consists of a series of tables that show:
The countries with the greatest and least coverage of politicians on Wikipedia compared to their population.
The countries with the highest and lowest proportion of high quality articles about politicians.
A ranking of geographic regions by articles-per-person and proportion of high quality articles.
Finally I wrote short reflection on the project that focuses on how both findings from this analysis and the process I went through to reach those findings helps me understand the causes and consequences of biased data in large, complex data science projects.


## API Documentation

I have used the Page View API, at monthly granularity to collect data for this assignment: [Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews#Monthly_counts)

## Directory Structure

```

.
├── raw_files
│   ├── dino_monthly_desktop_start201501-end202209.json
│   ├── dino_monthly_mobile-app_start201501-end202209.json
│   ├── dino_monthly_mobile-web_start201501-end202209.json
│   ├── dinosaur_genera_cleaned.csv
├── json_output
│   ├── dino_monthly_cumulative_start201501-end202209.json
│   ├── dino_monthly_desktop_start201501-end202209.json
│   └── dino_monthly_mobile_start201501-end202209.json
├── graphs
│   ├── Fewest_Months_of_Data.png
│   ├── Maximum_Average_and_Minimum_Average.png
│   └── Top_10_Peak_Page_Views.png
├── src
│   └── hcds-a1-data-curation.ipynb
├── README.md
└── LICENSE
```

## Data Description

| Column                    | Description                                                        |
| ------------------------- | ------------------------------------------------------------------ |
| `year`                    | The year of the data point                                         |
| `month`                   | The month of the data point.    |
| `date`                   | The year-month pair serve as a key    |
| `log_views`   | The natural log of the views column       |
| `access`  | Data contains three different access: desktop, mobile-app, mobile-web     |
| `article`      | This is the name of the articles we are pulling on Wikipedia      |


## Data Tables

![Maximum Average and Minimum Average](graphs/Maximum_Average_and_Minimum_Average.png)

![Top 10 Peak Page Views](graphs/Top_10_Peak_Page_Views.png)

![Fewest Months of Data](graphs/Fewest_Months_of_Data.png)

## License

This code is available under the [MIT License](LICENSE)

Wikimedia [Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en)
