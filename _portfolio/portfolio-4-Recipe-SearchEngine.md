---
title: "Recipe Search Engine"
excerpt: "This project develops an NLP-powered recipe search engine that efficiently retrieves recipes based on titles and ingredients. Using natural language processing (NLP) techniques, such as tokenization, normalization, and stop word removal (NLTK), the system processes over 2 million recipes from a Kaggle dataset. The search engine leverages indexing and ranking algorithms to enhance retrieval accuracy and relevance. Built with Django, the platform provides a seamless user experience for discovering new recipes. Read more.... <br/><br/><br/> [![cover](https://navoditamathur.github.io/files/5..png)](https://navoditamathur.github.io/portfolio/portfolio-Recipe-SearchEngine)"
collection: portfolio
tags: 
  - NLP
  - Information Retrieval
  - Search Engine
---
Objective:
------
To develop a search engine that efficiently retrieves recipes from a large dataset based on user queries involving recipe titles and ingredients. The goal is to enhance the cooking experience for users by providing a streamlined method for discovering new recipes.

Methodology:
------
- Dataset Acquisition: Sourced a [comprehensive dataset from Kaggle](https://www.kaggle.com/datasets/wilmerarltstrmberg/recipe-dataset-over-2m/data), encompassing over 2 million recipes collected from various websites.
- Pre-processing: Processed the data to extract titles, ingredients, directions, and URLs. Applied tokenization, normalization, and stop word removal using NLTK to prepare the data for indexing.
- Indexing: Built an index to facilitate fast and accurate search operations.
- Query Processing: Developed functions to handle user queries, including extraction and preparation of search terms.
- Result Retrieval: Implemented a ranking algorithm to sort search results by relevance, ensuring users receive the most pertinent recipes.
- Website Design: Created a user-friendly web interface using Django, integrating the search engine with an intuitive design to enhance user experience.
![Web Interaface](https://navoditamathur.github.io/files/RecipeSearch.png)
- Read More [here](https://navoditamathur.github.io/files/INFSCI2140TermProjectFinalPresentation.pdf)

Contribution:
------
- Development: Designed and implemented the search engine using Django, ensuring a user-friendly interface and efficient search capabilities.
- Data Handling: Enhanced the dataset through meticulous pre-processing to improve search accuracy and relevance.
- Search Optimization: Developed a robust indexing and query handling system to deliver relevant search results swiftly.

Deliverables:
------
A fully functional Django-based website for recipe search, featuring:
- A search bar for querying recipes by title and ingredients.
- Results displayed with recipe titles, ingredients, directions, and URLs based on a ranking system to present results based on relevance to user queries.

Code
------
Github Repository: [Recipe Search Engine](https://github.com/Navoditamathur/Recipe-SearchEngine)
