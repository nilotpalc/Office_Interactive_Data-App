# Description: 
After cleaning and preparing some office equipment data, it is finally time to put it to use. The management team now wants a dashboard to explore product options, compare prices, and uncover insights from customer reviews — all in one place.
Your task is to build a full product intelligence and review analytics data app in KNIME. Starting from two clean and preprocessed Excel sheets (products and reviews), create an interactive experience where users can browse categories, find similar products by price and rating, visualize review trends over time, extract key phrases from customer feedback, and even map review activity by country. The goal is to deliver a data app that blends data wrangling, similarity search, text mining, geospatial enrichment, and reporting: the perfect showcase of full-stack analytics in KNIME.

## Beginner-friendly objective(s): 
1) Import and refine the Products and Product Reviews Excel sheets, ensuring headers and data types are correctly read, and replacing empty strings with missing values.
2) Add a category selection control and filter the product table by the chosen category; next, present the filtered result in an interactive table.
3) Create a simple title text driven by the selected category for display in the data app.

## Intermediate-friendly objective(s):
1) Standardize price and average rating, compute pairwise numeric distances, find the two nearest neighbors per product, and combine the selected item with its similar products.
2) Join selected/similar products to their reviews, compute monthly average review scores per product (pivoted by Product ID), handle missing values and rounding, and visualize ratings over time.
3) Add an autocomplete Product ID input to drive a single-product analysis branch.

## Advanced objective(s):
1) Convert reviews to documents, clean punctuation and stopwords, remove very short tokens, build bigrams, and render a tag cloud of key phrases.
2) Aggregate reviews by country, enrich with country boundary geometries from OSM, and display a choropleth map colored by number of reviews with informative popups.
3) Package the analytics into an interactive Component with a refresh button and generate a shareable PDF report.

![JKI LINK](https://www.knime.com/just-knime-it)

# Solution-Space
[ ✔️] 1) Import and refine the Products Excel sheet, to extract the ASIN product number from the product details sheet to form a key to connect to product reviews sheet.
[✔️ ] 2) Extract the product names using a GenAI-LLM setup to tag every product and brand basis the 'Title' description column