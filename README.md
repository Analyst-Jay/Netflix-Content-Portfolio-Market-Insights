# Netflix Content Portfolio & Market Insights Dashboard

## Project Overview

The Netflix Content Portfolio & Market Insights Dashboard is a data analytics project developed using Microsoft Power BI as part of the Auspify Business Analytics Internship.

The project explores Netflix's content catalogue to understand its composition, global distribution, content categories, audience ratings, and content growth trends.

Using the Netflix dataset, the analysis examines the distribution of Movies and TV Shows, countries represented in the catalogue, popular content genres, rating classifications, release patterns, and the timeline of content additions.

The goal is to transform raw catalogue data into an interactive dashboard that communicates meaningful insights about Netflix's content portfolio.

## Project Objectives

- Analyse the overall composition of Netflix's content catalogue.
- Compare the distribution of Movies and TV Shows.
- Explore Netflix's geographical content distribution.
- Identify countries with the highest content representation.
- Examine the distribution of content across genres.
- Analyse audience rating classifications.
- Explore content release patterns and catalogue growth over time.
- Build an interactive dashboard to communicate findings and recommendations.

## Dataset Overview

The project uses `Dataset.csv`, containing **8,790 unique titles and 10 columns**.

The dataset includes the following fields:

| Column | Description |
|---|---|
| `show_id` | Unique identifier for each title |
| `type` | Content type: Movie or TV Show |
| `title` | Name of the content |
| `director` | Director associated with the title |
| `country` | Country or countries associated with the content |
| `date_added` | Date the title was added to Netflix |
| `release_year` | Original release year |
| `rating` | Content rating classification |
| `duration` | Movie duration or number of TV show seasons |
| `listed_in` | Genre or category associated with the title |

## Tools and Technologies

- **Microsoft Power BI:** Dashboard development and data visualisation.
- **Power Query:** Data cleaning, transformation, and preparation.
- **DAX:** Measures, calculated metrics, and analytical calculations.
- **Data Modelling:** Relationships between the main title table, bridge tables, and date dimension.
- **Microsoft Excel:** Optional dataset inspection and preliminary review.

## Data Preparation and Modelling

The dataset required preparation before meaningful analysis could be performed.

### Data Cleaning and Transformation

The following operations were carried out:

- Reviewed the dataset structure and checked column data types.
- Prepared the `date_added` field for date-based analysis.
- Separated the `duration` field into numerical value and unit components.
- Examined multi-value fields such as `country` and `listed_in`.
- Split multiple country values into individual records in a separate Country Bridge table.
- Split multiple genre values into individual records in a separate Genre Bridge table.
- Preserved the unique `show_id` as the identifier for Netflix titles.
- Created a date dimension to support time-based analysis.

### Data Model

The model was structured around four main tables:

| Table | Purpose |
|---|---|
| Netflix Titles | Main table containing one record per title |
| Country Bridge | Connects individual titles to their associated countries |
| Genre Bridge | Connects individual titles to their associated genres |
| DimDate | Supports date-based analysis using `date_added` |

The bridge tables were introduced to handle titles associated with multiple countries and genres without duplicating the main title records.

DAX techniques such as `TREATAS` were used where necessary to apply filter selections from the bridge tables to the main Netflix Titles table.

## Dashboard Structure

The dashboard consists of five analytical pages.

### 1. Executive Overview

Provides a high-level summary of Netflix's content catalogue.

Key areas include:

- Total number of titles.
- Movie and TV Show distribution.
- Percentage contribution of each content type.
- Overall catalogue composition.
- High-level content distribution and summary metrics.

**Purpose:** To give users a quick understanding of the size and composition of Netflix's catalogue.

### 2. Global Market Analysis

Explores the geographical distribution of Netflix content.

Key areas include:

- Content distribution by country.
- Top countries by number of titles.
- Country-level comparisons.
- Geographical representation of the catalogue.
- Global content distribution patterns.

**Purpose:** To understand the countries contributing most to Netflix's content catalogue and examine its geographical representation.

### 3. Content Category Analysis

Focuses on the distribution of Netflix content across genres and categories.

Key areas include:

- Genre distribution.
- Top content genres.
- Comparison of genres across Movies and TV Shows.
- Content category contribution.
- Genre-level catalogue patterns.

**Purpose:** To identify the major content categories represented in the Netflix catalogue and understand how Movies and TV Shows are distributed across genres.

### 4. Audience & Rating Analysis

Examines the rating classifications assigned to Netflix titles.

Key areas include:

- Content rating distribution.
- Comparison of ratings across Movies and TV Shows.
- Major rating categories.
- Rating patterns within the catalogue.

**Purpose:** To understand the composition of Netflix's catalogue by rating classification and examine how ratings vary across content types.

### 5. Content Growth & Trends

Explores the historical distribution of Netflix titles based on release year and the date they were added to the platform.

Key areas include:

- Content distribution by release year.
- Titles added over time.
- Yearly content additions.
- Monthly content addition patterns.
- Cumulative catalogue additions.
- Year-over-year comparisons.

**Purpose:** To examine how the catalogue developed over time and distinguish between the original release dates of titles and the dates they were added to Netflix.

## Key Findings

The analysis produced the following observations:

### 1. Movies Represent the Majority of the Catalogue

Out of 8,790 titles:

- Movies: 6,126 (69.69%)
- TV Shows: 2,664 (30.31%)

This indicates that Movies account for a larger share of the titles in the analysed catalogue.

### 2. The United States Leads in Country Representation

The leading countries by title count included:

| Country | Number of Titles |
|---|---:|
| United States | 3,240 |
| India | 1,057 |
| United Kingdom | 638 |

The United States had the highest content representation among the countries analysed.

### 3. Mature and Teen Rating Categories Have Strong Representation

TV-MA and TV-14 were among the most represented rating classifications in the dataset.

- TV-MA: 3,205 titles.
- TV-14: One of the other leading rating categories.

This highlights the significant representation of mature and teen-rated content in the catalogue.

### 4. International Movies and Dramas Are Leading Genres

International Movies and Dramas appeared among the leading content categories.

This demonstrates the importance of examining genre distribution separately from content type.

### 5. Release-Year Concentration

A considerable concentration of titles was observed around the 2017–2019 release period.

This provides an opportunity to examine how the release-year distribution differs from the dates titles were added to Netflix.

## DAX and Analytical Techniques

The project involved developing measures and calculations for:

- Total Titles.
- Total Movies.
- Total TV Shows.
- Movie Percentage.
- TV Show Percentage.
- Titles by Country.
- Titles by Genre.
- Rating Distribution.
- Titles by Release Year.
- Titles Added Over Time.
- Cumulative Content Additions.

Additional techniques included:

- `DISTINCTCOUNT` for counting unique titles.
- `CALCULATE` for modifying filter context.
- `TREATAS` for applying filters through bridge tables.
- Date intelligence calculations for time-based comparisons.

## Business Insights and Recommendations

Based on the patterns observed in the dataset, the following areas deserve further attention:

1. **Global Content Representation:** Netflix can use country-level catalogue analysis to identify geographical areas with strong and limited content representation.

2. **Content Category Balance:** Genre analysis can help stakeholders understand the composition of the catalogue and identify categories with relatively lower representation.

3. **Rating Distribution:** The distribution of rating classifications provides a useful overview of the catalogue's content classification mix.

4. **Content Acquisition and Release Trends:** Comparing release years with dates added to the platform helps distinguish older content from more recently acquired titles.

5. **Data-Driven Catalogue Planning:** The dashboard provides a descriptive foundation for exploring content distribution and historical catalogue changes.

These recommendations are based on catalogue composition and historical records, not evidence of actual audience demand or content performance.

## Project Limitations

The dataset describes Netflix's content catalogue but does not include:

- Number of views or streams.
- Subscriber information.
- Revenue generated by individual titles.
- Viewer engagement.
- Audience preferences.
- Watch time or completion rates.

Therefore, the analysis measures content representation and catalogue patterns, not the popularity, profitability, or actual performance of individual titles.

Additionally, the dataset's latest recorded `date_added` value is September 25, 2021. Content additions around 2021 may be incomplete, so the final period should be interpreted cautiously.

## Conclusion

The Netflix Content Portfolio & Market Insights Dashboard demonstrates how Power BI can be used to transform a raw content catalogue into a structured analytical solution.

Through data cleaning, Power Query transformations, bridge-table modelling, DAX calculations, and interactive visualisations, the project explores Netflix's global content distribution, genre composition, rating classifications, and historical catalogue trends.

It also demonstrates practical skills in data preparation, relational modelling, analytical thinking, dashboard development, and business insight communication.

---

**Project:** Netflix Content Portfolio & Market Insights Dashboard  
**Organisation:** Auspify Business Analytics Internship  
**Project Category:** Data Analytics  
**Primary Tool:** Microsoft Power BI  
**Data Preparation:** Power Query  
**Analytical Language:** DAX  
**Dataset:** Netflix `Dataset.csv`  
**Records:** 8,790 unique titles  
**Dashboard Pages:** 5
