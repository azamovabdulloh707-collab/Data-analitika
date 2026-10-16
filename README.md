# Titanic Survival Analysis Dashboard

An interactive data analytics dashboard exploring how passenger class and age group were associated with survival outcomes on the Titanic.

The dashboard presents passenger counts, survival rates by passenger class, and survival rates across age categories. Interactive filters let users explore the data by age group, passenger class, and sex.

## Dashboard Preview

> Add a screenshot of your dashboard to this repository and update the image path below.

![Titanic Survival Analysis Dashboard](images/titanic-dashboard.png)

## Project Overview

This project uses Titanic passenger data to examine survival patterns across selected demographic and ticket-class categories. The dashboard is designed to make the results easy to explore through summary metrics, charts, and filters.

### Key Features

- **Interactive filters** for age category, passenger class, and sex
- **KPI cards** showing the number of passengers in the current selection, survivors, survival rate, and selected age group
- **Passenger counts by class**, split into survivors and non-survivors
- **Survival rate by passenger class**
- **Survival rate by age category**, including children, youth and adults, and seniors
- **Responsive, clean dashboard layout** for convenient exploration

## Key Findings

The figures below reflect the dashboard view shown in the project screenshots, with all filters set to **All**:

| Metric | Value |
|---|---:|
| Passengers included in the dashboard view | 891 |
| Survivors | 342 |
| Overall survival rate | 38.4% |
| Age values filled with the mean | 29.699 |

### Survival by Passenger Class

The dashboard shows these survival rates by class:

| Passenger class | Survival rate |
|---|---:|
| 1st class | 63.0% |
| 2nd class | 47.3% |
| 3rd class | 24.2% |

In this dashboard view, first-class passengers had the highest survival rate, while third-class passengers had the lowest.

### Survival by Age Category

The chart reports the following survival rates:

| Age category | Survival rate |
|---|---:|
| Children (14 and under) | 57.7% |
| Youth and adults (15–64) | 36.9% |
| Seniors (65 and over) | 9.1% |

Children had the highest displayed survival rate among these age categories, while seniors had the lowest.

> **Interpretation note:** These are descriptive results from historical passenger data. They show associations, not proof that passenger class or age alone caused a particular outcome. The dashboard note also indicates that missing age values were filled with the mean, which may affect age-group comparisons.

## Tools and Technologies

- **HTML** — dashboard structure
- **CSS** — styling and layout
- **JavaScript** — interactivity and data presentation
- **Charts** — visual comparison of passenger counts and survival rates

Update this list if your implementation uses additional libraries (for example, Pandas, NumPy, or a JavaScript charting library).

## Getting Started

This dashboard is an HTML file and can be opened in a web browser.

1. Clone or download this repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   ```
2. Open the project folder.
3. Open `Titanic_dashboard.html` in your browser.

If the file uses external data or JavaScript libraries, make sure the required files and dependencies are available as expected.

## Suggested Repository Structure

```text
.
├── Titanic_dashboard.html
├── README.md
├── images/
│   └── titanic-dashboard.png
└── data/
    └── titanic.csv
```

This is a suggested structure. Keep only the folders and files that actually exist in your repository.

## Future Improvements

- Add a comparison of survival rates by sex.
- Display the number of passengers in each age category.
- Add tooltips and clearer chart-axis labels.
- Include a data-cleaning and exploratory data analysis notebook.
- Improve accessibility and mobile responsiveness.
- Document the dataset source and data-cleaning steps.

## Author

**Abdulloh Azamov**

Aspiring Data Analyst interested in data analysis, visualization, and extracting insights from real-world datasets.

## Disclaimer

This project is intended for educational and portfolio purposes. Results depend on the dataset, data-cleaning decisions, and selected filters.
