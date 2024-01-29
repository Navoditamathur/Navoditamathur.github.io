---
title: "Recipe Search Engine"
excerpt: "The project’s goal was to design a search engine to search for recipes through the dataset using title and ingredients. The website was made using Django. Indexing was done using Python using  ntlk libraries for tokenization and removal of stop words."
collection: portfolio
---
Description:
-------
The goal for this project was to design a search engine for a large variety of recipes. Incorporated with the search engine is a user-friendly interface that allows users to execute their query and have recipes returned that can then be accessed. 

The end users envisioned for this project are the aspiring home chefs looking for their next challenge in the kitchen, busy parents looking for fresh and quick meals to put on the table, and people that have made the switch from going out to staying in due to social climate. 

A recipe search engine is useful to a large and varied group of people, especially considering that the number of recipes that can exist is almost unlimited for as long as people have the access to explore new recipes and perhaps some inspiration. Without a search engine, looking for new recipes would be a time-consuming task that could possibly deter people from trying to cook at home!

Approach:
* The initial input for the search engine was sourced from Kaggle, it is a dataset containing over 2 million recipes gathered from multiple different sites across the web
* Pre-processing: Returns the title, ingredients, directions, and url of each recipe as string, tokenized, normalized and stop words removed.
* Prepare the index
* Read the index
* extract query
* Prepare results

Deliverables:
-------
A fully functional website to retrieve the recipes based on title and ingredients through a search bar ranked according to the relevence.