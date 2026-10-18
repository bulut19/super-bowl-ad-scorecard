# Liked but Forgotten: Scoring 2025 Super Bowl Ads from YouTube Comments

USA Today's Ad Meter only asks whether viewers liked an ad. This project scores 2025 Super Bowl ads on three pillars using 10,547 cleaned YouTube comments: **likability**, **brand recall**, and **message fit**.

## Key Findings

- Comment-based likability tracks Ad Meter closely (Spearman **+0.78**).
- Liking and brand recall are unrelated (**-0.17**). Lay's, Stella Artois, Instacart and WeatherTech ranked high on Ad Meter but were rarely named in comments.
- Disney+ and T-Mobile had the highest recall, mostly from viewers criticizing the brand.
- Joy predicted Ad Meter scores. Humor tended to lower recall. Celebrities predicted neither.

## Methods

- **Likability:** RoBERTa and VADER sentiment, plus a 7-emotion model, validated on 50 hand-labeled comments (RoBERTa 64% vs. VADER 44%)
- **Brand recall:** regex brand dictionaries
- **Message fit:** sentence embeddings vs. bag-of-words similarity
- **Analysis:** bot-spam removal, LDA topics, k-means ad types, OLS regression, benchmarks against Ad Meter and the Kellogg Super Bowl Advertising Review

**Tools:** Python, pandas, scikit-learn, Hugging Face Transformers, sentence-transformers, statsmodels, Google Colab

## Team

Jonathan Choi, Shehryar Syed, Samantha Feinberg, Melisa Bulut, Yash Shrivastava
