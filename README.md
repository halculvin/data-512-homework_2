# Human Centered Data Science - A2: Considering Bias in Data

This repository contains the code and resulting data for a brief analysis of English Wikipedia articles on dinosaurs from July 2015 through to September 2022. It was originally completed for the first assignment of the University of Washington's Human Centered Data Science (DATA 512) course in Autumn 2022. The goal of this assignment was to complete an exercise in data curation, including all major steps in the pipeline, namely data acquisition, processing, and analysis. Another goal was to complete this exercise with reproducibility in mind, ensuring that the documentation for the repository and code are detailed such that somebody else could easily complete the same work.

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
