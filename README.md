# Netflix-EDA-and-Recommendation
This project conducts a comprehensive Exploratory Data Analysis (EDA) on a Netflix dataset, followed by the development of a basic content-based recommendation system. The goal is to uncover patterns in Netflix's content library — such as distribution by type (Movies vs. TV Shows), production countries, genre preferences across top-producing nations, and cultural specializations — and then use these insights to build a simple personalized recommendation engine.

## Key Components & Analyses Performed

1. **Data Preparation & Cleaning**  
   - Handled multi-value fields (countries and genres) using exploding techniques to enable accurate per-country and per-genre counting.  
   - Removed empty/invalid entries and standardized text formatting.

2. **Core EDA Insights**  
   - **Content Type Distribution**: Netflix's catalog contains significantly more Movies (~6,200) than TV Shows (~2,700).  
   - **Top Producing Countries**: The United States dominates with over 3,500 titles, followed by India, United Kingdom, Canada, France, and Japan.  
   - **Top Genres**: International Movies, Dramas, and Comedies are the most prevalent categories overall.  
   - **Country-Specific Genre Preferences** (visualized with exploded donut charts):  
     - India shows strong focus on International Movies (31%) and Dramas (24%).  
     - France emphasizes International Movies (23%) and Independent content.  
     - Japan stands out with Anime Series (~20%) and International TV Shows.  
     - The US, UK, and Canada exhibit more balanced distributions with large "Others" portions.  
     - Dramas consistently appear among top genres in most major producing countries.

3. **Content-Based Recommendation System**  
   - Combined textual features: description + weighted genres (to reduce noise from generic words).  
   - Used TF-IDF vectorization to convert content into numerical vectors.  
   - Computed pairwise cosine similarity between all items.  
   - Built a function that, given any title (e.g. "Stranger Things" or "Emily in Paris"), returns the most similar titles based on thematic and genre overlap.  
   - Results show meaningful matches (e.g. mystery/thriller series for Stranger Things, romantic comedies for Emily in Paris).

## Main Findings
- Netflix pursues a dual strategy: broad, diversified production in English-speaking markets (US, UK, Canada) and targeted investment in culturally specific or internationally appealing content in non-English markets (India → International Movies & Dramas, Japan → Anime & International TV).  
- Dramas and International-labeled content are among the most consistent and cross-culturally important genres.

## Technical Stack 
- Python, Pandas (data manipulation & exploding), Matplotlib + Seaborn (visualizations), Scikit-learn (TF-IDF + cosine similarity)  
- Jupyter Notebook workflow with clear markdown explanations and visual outputs

## Limitations & Future Directions 
- Current recommendation is purely content-based (no user ratings or viewing history).  
- Long descriptions can introduce noise → potential improvement with sentence embeddings (e.g. Sentence-BERT).  
- Could be extended with collaborative filtering, temporal trends (content added over years), or user segmentation.

This project demonstrates end-to-end data analysis skills — from cleaning messy real-world data, through insightful visualization and interpretation, to implementing a functional recommendation algorithm — and provides actionable observations about Netflix's global content strategy.
