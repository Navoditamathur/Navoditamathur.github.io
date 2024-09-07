---
title: "Pitt Digital Scholarship"
excerpt: "A web application to search for people, units, areas, methods, tools, and resources required for scholarships with special privileges given depending on the permission level. My role was to query and construct the graph database using Neo4j, build APIs for CRUD operations on the SQL database, and deploy the website using Google Compute Engine. <br/> [![Title](https://navoditamathur.github.io/files/PittDSDb_title.png)](https://navoditamathur.github.io/portfolio/portfolio-PittDSDb/)"
tags: 
  - Web Development
  - Database
collection: portfolio
---
Objective:
------
To create a robust web application that enables users at the University of Pittsburgh to efficiently search for and connect with digital scholarship (DS) practitioners, resources, and tools. The application was designed to provide varying levels of access and privileges based on user permissions.

Purpose and Benefits:
------
Digital Scholarship (DS) is a multidisciplinary field requiring diverse expertise and resources, often scattered across different departments. This application aims to break down silos by facilitating the aggregation and discovery of DS experts, methods, tools, and resources at Pitt. By centralizing this information, the app helps scholars easily identify potential collaborators, access necessary resources, and ultimately advance their digital projects.

Target Audience:
------
The primary users of this application are scholars and researchers at the University of Pittsburgh who are involved in or support digital projects. This includes faculty, students, and staff who require access to specialized tools, methods, and collaborators to successfully complete DS projects.

Methodology:
------
Requirement Analysis:
We began by collaborating with stakeholders to gather and analyze the project requirements. This involved identifying the core features that the target audience—scholars at the University of Pittsburgh—would need, such as relationship model development, advanced search capabilities, and robust database management.

Database Design:
To effectively store and manage the complex relationships between entities like people, groups, methods, tools, and resources, I designed a dual-database architecture:

* Neo4j Graph Database: Used to model the intricate relationships, allowing users to search and visualize connections between various digital scholarship elements.
* MySQL Relational Database: Implemented to manage structured data, ensuring the integrity and efficient querying of records.

![pitt DS Db](https://navoditamathur.github.io/files/PittDSDb_DBDesign.png)

API Development:
Developed RESTful APIs to facilitate CRUD (Create, Read, Update, Delete) operations across both databases. These APIs enabled seamless interaction between the front-end interface and the back-end databases, ensuring users could efficiently manage records.

![pitt DS Db](https://navoditamathur.github.io/files/pittdsdb_documentation.png)

Flask Website Development:
Designed and developed a fully functional Flask website to serve as the application’s front-end. The website provided users with a simple, intuitive interface to search, view, and manage records, ensuring a smooth user experience.

![pitt DS Db](https://navoditamathur.github.io/files/PittDSDb_Search.png)

![pitt DS Db](https://navoditamathur.github.io/files/pittdsdb_add.png)

User Authentication:
A secure user authentication system was implemented to restrict access to the application. Only users with Pitt domain emails could create accounts and make changes to the database. This feature also logged user transactions, ensuring accountability and data security.


Testing and Deployment:
Rigorous testing was conducted to validate the functionality, performance, and security of the application. Once testing was completed, the Flask web application was deployed on Google Compute Engine. This ensured the app was scalable, reliable, and accessible to users at the University of Pittsburgh.
[![Deployed Website](https://navoditamathur.github.io/files/PITTDSDB.png)](https://pittdsdb.pythonanywhere.com/)

Contribution
-------
Database Design: Constructed a graph database using Neo4j to model the complex relationships between people, groups, methods, tools, and resources.
API Development: Developed APIs for CRUD (Create, Read, Update, Delete) operations on the SQL database to manage user interactions with the DS records.
User Authentication: Implemented a secure user authentication system ensuring only authorized users with Pitt domain emails can access and modify the database.
Deployment: Deployed the web application on Google Compute Engine, ensuring scalability and reliability.

Technologies Used:
------
Graph Database: Neo4j for modeling relationships.
API Development: Python, SQL for CRUD operations.
Deployment: Google Compute Engine for hosting the application.
Frontend: (If applicable) HTML, CSS, JavaScript for user interface.

Deliverables:
------
GitHub Repository: Pitt Digital Scholarship Database
A fully functional web application with user authentication and database management features.
Documentation and deployment scripts for future maintenance and updates.

Code:
-------
GitHub repository: https://github.com/tyt3/Pitt-Digital-Scholarship-DB
