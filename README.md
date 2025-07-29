# 🎬 TMDB Movie Ranking Analysis

This project analyzes the TMDB 5000 Movie Dataset to identify top-rated and most popular movies using various statistical techniques including weighted average rating and min-max normalization. The result is a hybrid scoring system combining popularity and user ratings.


## 📊 Objective

- Merge credits and movie metadata
- Compute weighted average scores using vote count and vote average
- Normalize popularity and ratings
- Create a hybrid scoring mechanism using both metrics
- Visualize:
  - Top 10 movies by weighted average
  - Top 10 movies by popularity
  - Top 10 movies by combined (hybrid) score

## 🛠️ Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `sklearn.preprocessing.MinMaxScaler`

## 📈 Visual Outputs

- `best_movies.png` — Top 10 by weighted average rating
- `best_popular_movies.png` — Top 10 by popularity
- `scored_movies.png` — Top 10 by hybrid score

## 💡 How It Works

### Weighted Average Formula:
 - Weighted Average = (v / (v + m) * R) + (m / (v + m) * C)
 Where:
- `v` = vote count of the movie
- `R` = average rating of the movie
- `m` = minimum votes required (70th percentile of vote count)
- `C` = mean vote across all movies

### Hybrid Score:
- Score = 0.5 * Normalized Weighted Average + 0.5 * Normalized Popularity

  
## 📸 Sample Output (Top 5 Hybrid Scored Movies)

| Movie Title           | Weighted Avg | Popularity | Score |
|-----------------------|--------------|------------|-------|
| The Dark Knight       | 0.92         | 0.86       | 0.89  |
| Inception             | 0.89         | 0.91       | 0.90  |
| Interstellar          | 0.88         | 0.88       | 0.88  |
| Fight Club            | 0.86         | 0.83       | 0.845 |
| The Lord of the Rings | 0.85         | 0.80       | 0.825 |

## 🧪 Run the Code

```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# Run the script
python tmdb_movie_score_analysis.py

