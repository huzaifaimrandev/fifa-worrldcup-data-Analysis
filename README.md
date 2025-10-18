# FIFA World Cup Data Cleaning Project

A comprehensive data cleaning and preprocessing pipeline for historical FIFA World Cup match data from 1930 to 2022.

## 📊 Project Overview

This project focuses on cleaning and preparing FIFA World Cup match data for analysis. It handles missing values, creates new derived features, and transforms raw match data into an analysis-ready format.

## 🎯 Features

### Data Cleaning
- Handles missing penalty shootout data (fills with 0)
- Processes card information (yellow cards, red cards)
- Converts data types for consistency
- Manages missing values in categorical columns

### New Features Created
- **Total Goals**: Sum of home and away team scores
- **Penalty Shootout Scores**: Cleaned penalty shootout data
- **Card Statistics**: 
  - Yellow card counts per match
  - Red card counts (including direct reds and two-yellow reds)
- Match outcome indicators

## 📁 Dataset Information

### Source Files
1. **`world_cup (1).csv`** - World Cup tournament summary data
   - Year, Host country, Champion, Runner-Up
   - Top scorers, Attendance statistics
   - Number of teams and matches

2. **`matches_1930_2022 (1).csv`** - Detailed match-by-match data
   - Team names and scores
   - Penalty shootout results
   - Card information (yellow, red, yellow-red)
   - Match rounds and years

### Output
- **`cleaned_world_cup_matches.csv`** - Processed and enhanced dataset

## 🛠️ Technical Implementation

### Libraries Used
- `pandas` - Data manipulation and analysis
- `numpy` - Numerical operations
- `google.colab` - File upload (for Colab environment)

### Key Functions
- `count_entries()` - Counts comma-separated entries in card columns
- Data type conversion for penalty columns
- Missing value imputation strategies

## 🚀 Usage

### Running in Google Colab
1. Upload the dataset files when prompted
2. Execute the cleaning pipeline
3. Download the cleaned dataset (`cleaned_world_cup_matches.csv`)

### Data Processing Steps
1. **Load Data**: Read CSV files into pandas DataFrames
2. **Clean Missing Values**: 
   - Penalty data → fill with 0
   - Card data → fill with empty strings
3. **Create New Columns**:
   - Total goals calculation
   - Card counting functions
   - Penalty score columns
4. **Export Results**: Save cleaned data to new CSV

## 📈 Potential Analysis Applications

- **Team Performance**: Historical performance analysis
- **Match Statistics**: Goal patterns, card frequencies
- **Tournament Trends**: Evolution of World Cup football
- **Predictive Modeling**: Match outcome prediction
- **Visualization**: Historical trends and patterns

## 🔧 Code Structure

```python
# Main cleaning pipeline
1. Load datasets
2. Handle missing penalty data
3. Process card information
4. Create derived features:
   - total_goals
   - penalty_scores
   - yellow_card_counts
   - red_card_counts
5. Export cleaned data
