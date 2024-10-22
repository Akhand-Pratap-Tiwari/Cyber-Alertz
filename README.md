### Setting Up:
The readme for each project is included within the respective project. Set up and run them accordingly. First, run the scraper, then run the frontend for display.

### [Demo Video Here](https://drive.google.com/file/d/1VVe_GXD8vQG4VpPpSYwgdjOqOH2Mlt1g/view?usp=sharing)

### About Cyber Alertz:
This project scrapes multiple cybersecurity resources and aggregates them in one place, allowing users to search through them and skim or scan article content using GenAI.

### How it works:
- Scraping is initially done using bs4.
- The extracted content is in raw form and purified using the Gemini API.
- This purification results in neatly formatted JSON data.
- Next, embeddings are generated for the data using Google's text embedding model. These embeddings are used for semantic search purposes.
- The final JSON blocks are posted to MongoDB via Cosmocloud.
- On the website, you can view the articles.
- If you want to search for articles, we use semantic search rather than pattern matching, providing you with more relevant results. This is implemented through Atlas Vector Search using Cosmocloud's API.
- If you want to run queries on specific articles or understand complex concepts mentioned in the articles, it is also possible, as we use the Gemini API along with the article context to answer such queries.