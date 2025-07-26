# S2G

## 🥇 Gold Layer: Genre-Based Movie Insights

This phase focuses on transforming enriched Silver Layer data into meaningful, aggregated insights at the genre level. The key objective is to evaluate user engagement and average ratings for each genre using PySpark.

### 🎯 Goals

- ✅ Standardized column names across DataFrames for consistency:
  - Renamed `movie_id` to `movieId` in `ratings_transformed.csv`
  - Renamed `year` to `releaseyear` in `movies_exploded.csv`
  - Renamed `date` to `date_rated`

- 🔗 Performed a `left` join between:
  - `movies_explodedB2S` (Silver layer - genre exploded movie data)
  - `RatingsB2S` (Silver layer - cleaned ratings data)

- 📊 Aggregated data using:
  - `avg(rating)` → Rounded to 2 decimal places
  - `count(user_id)` → Total number of user ratings per genre

- 📈 Sorted the results in descending order by:
  - Average rating
  - Number of user ratings

- 💾 Produced a final DataFrame showing:
  - Genre
  - Average Rating (rounded)
  - Number of Users who rated that genre

### 📌 Example Output

| Genre     | Average Rating | Number of Users |
|-----------|----------------|------------------|
| Film-Noir | 3.92           | 318,917          |
| War       | 3.80           | 1,697,649        |

This aggregated table can serve as the foundation for advanced visualizations, reporting, or feeding into recommendation systems in upcoming phases.
