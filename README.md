# Restaurant Ratings Analysis

This project explores the factors contributing to high restaurant ratings and provides insights for restaurant owners to improve their reviews. By analyzing restaurant data, this project identifies trends, patterns, and actionable recommendations to enhance customer satisfaction.

## Project Overview

The project uses restaurant data stored in MongoDB (data is originally the yelp dataset of user reviews and restaurant ratings) to extract insights about:

- Most reviewed categories and cities
- Factors influencing high or low ratings
- Relationship between review counts and star ratings
- Top-rated and highly reviewed restaurants

## Workflow

The workflow consists of the following steps:

### 1. Data Extraction and Filtering

- **MongoDB Connector & Reader**: Connects to the database and reads restaurant data.
- **Row Filter**: Filters restaurants with at least 50 reviews to ensure statistical significance.
- **Column Filter**: Focuses on key columns like Restaurant Name, Review Count, Stars, and Category.

### 2. Analysis and Insights Generation

#### Analysis 1: Most Reviewed Categories
- **GroupBy & Sorter**: Groups data by category and sorts by descending review count.
- **Bar Chart**: Visualizes the top categories with the highest number of reviews.

#### Analysis 2: Low-Rated Restaurants by City
- **Row Filter**: Isolates poorly rated restaurants (<2.5 stars).
- **GroupBy**: Aggregates data to identify cities with the most low-rated restaurants.
- **Pie Chart**: Visualizes cities with the lowest-rated restaurants.

#### Analysis 3: Relationship Between Reviews and Ratings
- **Scatter Plot**: Analyzes the correlation between the number of reviews and star ratings.

#### Analysis 4: Disparity in Reviews by City
- **GroupBy & Bar Chart**: Visualizes review disparities across cities.

#### Analysis 5: Top Restaurants Analysis
- **Row Filter**: Isolates top restaurants (>4.6 stars).
- **GroupBy & Bar Chart**: Identifies the top 10 highly rated restaurants.
- **Pie Chart**: Highlights cities hosting top-rated restaurants.

### 3. Visualization

All insights are visualized using bar charts, scatter plots, and pie charts to convey actionable findings clearly.

## Key Insights

1. **Most Reviewed Categories**:
   - Top categories include Bars, Wine, Nightlife, and Spanish/Mexican restaurants.

2. **Low-Rated Restaurants**:
   - Cities like Boston dominate the low-rating category.

3. **Review and Rating Correlation**:
   - Restaurants with many reviews often have a broader range of ratings.

4. **Review Disparity**:
   - Boston leads with the highest disparity in review counts.

5. **Top Restaurants**:
   - Orlando dominates the list of cities with highly rated restaurants.

## Technologies Used

- **MongoDB**: For data storage and extraction.
- **Data Processing**: Filtering and grouping using Python.
- **Visualization**: Insights visualized through bar charts, scatter plots, and pie charts.

## How to Use

1. Clone the repository.
2. Set up MongoDB and import the dataset.
3. Run the analysis workflow using knime.
4. View generated visualizations for insights.
